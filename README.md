# Harjoitus-3

Tässä harjoituksessa tehdään MarkDown kirjoitusta, git ohjelman perus komentoja/toimintaa. Myös vielä vähän infrakoodia ja sisältää tiivistelmän.

Tehtävät löytyvät opettajamme [Tero Karvisen sivulta](https://terokarvinen.com/2021/configuration-management-systems-palvelinten-hallinta-ict4tn022-2021-autumn/#h3-versionhallinta)

## Tiivistelmä

[Markdown reference](https://commonmark.org/help/)

* Linkin saa toteutettua `[nimi](url)`
* otsikko 1 saa `# otsikko`
* otsikko 2 saa `## otsikko`
* Koodi kuution saa näillä ` `` `
* quote kuution saa `> suuruus merkillä`


## a) MarkDown

Tämä harjoitus on tehty markdown tyypillä.


## b) Pull first

Kloonasin harjoitukseni ssh avulla git-varastoon komennolla 

```
git clone git@github.com:mikaelalalaa/Harjoitus-3.git
```

Harjoitusta varen tein kaksi uutta tiedostoa komennolla `mkdir` :

  * testdirec
  * toinentesti

Luomisen jälkeen ajoin komennon 

```
sudo touch testdirec/.gitkeep
sudo touch toinentesti/.gitkeep
```

![image](https://user-images.githubusercontent.com/93308960/142051509-205c0f0d-16f3-4000-9409-fc5cc980a902.png)
 
Luomisien jälkeen tallensin vasta tehdyt tiedostot komennolla 
```
git add -A
```
Sitten katsoin statuksen komennolla `git status`, jossa näkyi että tiedostot pitää vielä committaa.

![image](https://user-images.githubusercontent.com/93308960/142051925-085ca9b4-2d07-46e3-814a-9917588bc8f6.png)


Tallennuksen jälkeen tein commit message jossa oli viestinä "created from git"
Komento oli:
```
 git commit -m "created from fit"
```

Tämän jälkeen vielä työn sin sen githubiin, komennolla `git push`

![image](https://user-images.githubusercontent.com/93308960/142052440-7c5323c5-6daf-435a-958d-9597ec8ce493.png)

Tulokset työnnettiin onnistuneestin sivulle

![image](https://user-images.githubusercontent.com/93308960/142053058-0092f85f-ccf7-4ff1-b0ca-0ccc27a71844.png)


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


## d) Formula

Loin tein uuden hakemiston komennolla

```
sudo mkdir -p /srv/salt/fromula
```

Loin sinne uuden tiedoston `nano init.sls`.

Laitoin sinne koodiski alla olevan tekstin
```
test:
  pkg.installed:
      - name: vim
  file.managed:
      - name: /srv/salt/fromula/testi_tt.txt
```
Ajoin komennon 
```
sudo salt '*' state.apply fromula
```

Kuvasta näkyy että tiedoston luominen onnistui ja että vim oli jo asennettu.

![image](https://user-images.githubusercontent.com/93308960/142057954-be8fe3f0-80d8-400a-8cea-b240204c78de.png)

`ls -la` komennolla näkyy että tiedosto luotiin

![image](https://user-images.githubusercontent.com/93308960/142058105-a136fb3c-5f49-4f4e-b357-4118de75e1a8.png)

