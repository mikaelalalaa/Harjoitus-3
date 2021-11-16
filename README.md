# Harjoitus-3

Tehtävät löytyvät opettajamme [Tero Karvisen sivulta](https://terokarvinen.com/2021/configuration-management-systems-palvelinten-hallinta-ict4tn022-2021-autumn/#h3-versionhallinta)

## Tiivistelmä

[Markdown reference](https://commonmark.org/help/)



## a) MarkDown



## b) Pull first

Harjoitusta varen tein kolme uutta tiedostoa komennolla `nano` :

  * iloweu.txt
  * bunny.txt
  * foo.txt
 
Sitten tallensin luodut teidostot git-varastooni komennolla 
```
git add iloweu.txt bunny.txt foo.txt
```
![image](https://user-images.githubusercontent.com/93308960/142022361-dddcb200-444e-47e4-8c6c-6b826af4e483.png)


Tallennuksen jälkeen tein commit message jossa oli viestinä "Add top level menu to Foobar synchronizer"
Komento oli:
```
 git commit -m "Add top level menu to Foobar synchronizer"
```
Lopputlos oli tämän näköinen 

![image](https://user-images.githubusercontent.com/93308960/142022300-3f5fb920-c210-4a85-b0b1-388d886626d0.png)


## b) Kaikki karjataan

Harjoituksessa aja komennot `git log, git diff ja git blame ` ja lopuksi selitän tulokset

#### git log
Alhaalta kuvassa näkyy kaikki muutokset joita ollaa tehty kyseisessä git-varastossa.

* Ihan ensimmäisessä kohdassa 'commit' on id numero.
* 'Author' kohdassa näkyy tekijän nimi ja s-posti osoite
* 'Date' kohdassa näkyy aika ja päivämäärä milloin muutokset ovat tehty
* viimeisessä kohdassa näkyy viesti, joka on jätetty kun `commit` komento on tehty.

![image](https://user-images.githubusercontent.com/93308960/142026022-34e2f798-cc34-4e72-8d61-088c258cdc5d.png)


#### git diff

Olin aikaisemmin tehny jo kaksi tiedostoa.

Testi koomentona oli:

```
git diff --cached boo.txt file.txt
```

Alhaalla olevassa kuvassa näkyy mitä muutoksia tuli voimaan. Tiedoston nimi ja mitä tiedosto sisältää


![image](https://user-images.githubusercontent.com/93308960/142029831-dfff20eb-de36-46c8-9085-0088ddeed3ee.png)



#### git blame

Git blame komennolla näkyy yksittäisen tiedoston  muutokset mitä sille ollaa tehty.

* Ensimmäisessä kohdassa näkyy id numero.
* Toisessa kohdassa näkyy tekijän nimi.
* Kolmannessa kohdassa näkyy päivämäärä ja sen jälkeen tulee aika.
* Ihan viimeisenä sulkuje sisällä on rivinumero.
* Sulkujen ulkopuolella lopussa näkyy mitä tiedosto sisältää.

![image](https://user-images.githubusercontent.com/93308960/142024976-fd3d5151-afa6-42b8-89ec-34c9f304efa0.png)



## c) Huppis

Aluksi tein kaksi tiedostoa `file1.txt ja file2.txt`. Sitten katsoin statuksen `git status` komennolla.

Kuten huomaa kaksi tiedostoa pitää tallentaa git-varastooni

![image](https://user-images.githubusercontent.com/93308960/142031755-3efadc04-706e-44d3-9b7f-ab4d9cc487e2.png)

Tallensin tiedostot varastooni komennolla `git add -A`. Katsoin taas statuksen ja tila oli vaihtunut siihen että tiedostot pitää ajaa `commit` komennolla.

![image](https://user-images.githubusercontent.com/93308960/142031821-0ad83502-7e83-4fb0-87e0-a5ef7c39f1ee.png)

En tehnyt commit kohtaan ja ajoin komennon

```
git reset --hard
```

Tämän jälkeen katsoin taas statuksen ja huomasin että tiedostot olivat poistunut.

![image](https://user-images.githubusercontent.com/93308960/142031902-bfe50743-5d82-44d2-b4a7-bbf9a30c93db.png)
cd



## d) Formula
