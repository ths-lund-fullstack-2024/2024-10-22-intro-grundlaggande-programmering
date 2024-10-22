# Intro Grundläggande Programmering

Intro till kursen och kursinnehållet.

<details>
<summary>Innehåll</summary>

- [Dagens agenda](#dagens-agenda)
  - [Skapa repo på github](#skapa-repo-på-github)
- [Git intro](#git-intro)
  - [Git overview]()
  - [Git kommandon](#git-kommandon)

</details>

## Dagens agenda

- Presentera mig själv
- Gå igenom kursplanen
- Prata om planeringen för kursen, vad vi gör under de kommande 10 veckorna.
- Övrigt
- Prata om tidigare JS-kunskaper och var vi ska ta avstamp ifrån.
- Intro till git, github, github-konto, organisation och hur vi kommer använda git under kursen.
- Börja kika på JS.

[Tillbaks till toppen](#intro-grundläggande-programmering)

### Skapa repo på github

Det första vi vill göra för att börja arbeta med git är att skapa ett repository _(repo)_ på github. Detta görs enkelt genom att logga in på sit github-konto, gå till sin repository-sida och sen klicka på den gröna knappen där det står "new". Då skickas man till nästa sida där man fyller i några uppgifter, bland annat, namn på det nya repot, vilken visninsstatus den ska ha samt om man vill lägga till en readme-fil eller inte. Mer än så behöver man inte göra. Efter det är det bara att trycka på "create". Då har du ditt nya repo.

Repot blir sen tillgängligt på din repository-sida där du kan klona ner det.

[Tillbaks till toppen](#intro-grundläggande-programmering)

## Git Intro

Git är ett versionshanteringssystem som hjälper utvecklare att hålla koll på förändringar i sin kod över tid. Det används för att spara olika versioner av ett projekt, vilket gör det lättare att samarbeta med andra och gå tillbaka till tidigare versioner om något går fel.

Grundprinciper:

- **Repository (repo)**: En mapp som innehåller ditt projekt och dess versionshistorik.
- **Commit**: En "ögonblicksbild" av dina förändringar som du sparar med ett meddelande om vad som ändrats.
- **Branch**: En separat "gren" där du kan jobba på en viss del av projektet utan att påverka huvudversionen.
- **Remote**: vårt repo som ligger i molnet, alltså det vi kan se på github. Detta repo är tillgänglit överallt oavsett vilken dator du sitter på. Det är detta remote repo vi hela tiden vill uppdatera så det har den senaste versionen.
- **Local**: vårt lokala repo, det vi får när vi klonar ner ett repo från remote. Alla ändringar som sker på vår local, sker endast på vår local. Vi måste först skicka upp det till remote för att det ska uppdateras där.

Git används oftast tillsammans med plattformar som GitHub för att enkelt dela och samarbeta med andra utvecklare.

För att använda git så måste vi installera det om det inte redan finns tillgänglig på din dator.

```
https://git-scm.com/downloads
```

För att dubbelkolla att det är installerat så kör detta kommando i en terminal.

`git --version`.

Då bör det skrivas ut en version i din terminal, och då vet vi att git funkar som det ska.

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

### Git overview

Bilden nedan visar på en illustration av hur git-flödet ser ut. De delarna som ni bör fokusera på i detta skede av kursen är följande:

- Worksspace
- Staging area
- Local Repository
- Remote repository
- git add, git commit, git pull och git push.

Övrig tillhör mer avancerad git och det återkommer vi till senare i utbildningen.

<image src="./git-overview.png">

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

### Git kommandon

<details>
<summary>Lista på kommandon</summary>

- [git clone](#git-clone)
- [git add](#git-add)
- [git commit](#git-commit)
- [git pull](#git-pull)
- [git push](#git-push)
- [git status](#git-status)
- [git log](#git-log)
- [Länk till fler git-kommandon](https://www.freecodecamp.org/news/git-cheat-sheet/)
- [Tillbaks till toppen](#intro-grundläggande-programmering)
</details>

---

#### `git clone`

Detta kommando är det första vi använder för att klona ner vårt repo från remote. Öppna en terminal och navigera till den mapp där du vill spara ner ditt repo. Antingen gör du det via en extern terminal eller visual studio codes _( VSC )_ inbyggda terminal. Fördelen med den inbyggda i VSC är att den öppnar terminalen direkt i den mapp du har öppen.

Kopiera ner url:en till ditt repo, något i stil med:

```
https://github.com/DerFahnrich/test.git
```

sen i terminalen du har öppnat _( i rätt mapp! )_ så skriver du:

```
git clone https://github.com/DerFahnrich/test.git
```

då har du lyckats klona ner ditt repo lokalt och kan nu börja jobba med det i VSC.

Det som händer bakom kulisserna är att git skapar en automatiskt koppling mellan ditt lokala repo och ditt remote repo. Vilket gör att alla ändringar du gör i denna mapp, och som du sen skickar upp med en [git push](#git-push) kommer automatiskt att hamna på rätt remote repo. I bakgrunden sker även en [git pull](#git-pull) som hämtar ner det senaste innehållet från ditt rempote repo.

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git add`

Detta kommando används för att lägga till ändringar i det som kallas för staging area. I staging area ligger alla ändring som vi vill ta med i nästa commit/version. Så förs nät vi gör en ändring så kommer git att lägga märke till det och met registrerar endast det som "changes". Add lägger till det i "staging area". Det är alltså förberedd för att committas.

Vi kan göra detta på två sätt egentligen. Antingen så "addar" vi alla ändringar, då skriver vi:

```
git add .
```

Vill man endast lägga till en del av de ändringarna man har gjort så använder man samma kommando, men man specificerar filnamnet hela tiden.

```
git add index.html
git add index.css
git add README.md
```

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git commit`

Detta kommando används för att skapa en ny version av din kod. Den kommer att plocka allt du har i din "staging area", paketera ihop det och skapa en commit av det. Alla commits sen kan du titta på genom att skriva "[git log](#git-log)". En commit är något som lever lokalt på din dator till en början. För att skicka upp den till ditt remote-repo så får du använda dig av "[git push](#git-push)".

När man gör en commit så är det jätteviktigt att man lägger till ett meddelande också som sammanfattar vad den skapade commiten har gjort för något. Det är sätt att dokumentera de olika versionerna man har. Så här ser följande kommando ut:

```
git commit -m "Ditt commit-meddelande"
```

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git pull`

git pull är kommando som drar ner de sensate ändringarna från remote-repot. Se det som en synk i riktningen "remote -> local". Detta används extremt mycket när man sitter flera personer i samma applikation. Har någon kollega gjort en ändring i er kodbas, och du vill dra ner den ändringen till ditt lokala repo så är det en git pull du gör. Ser ut som följande:

```
git pull
```

En git pull bör man alltid göra innan man börjar arbeta för att säkerhetsställa att man inte missar några uppdateringar som har skett på remote,

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

### `git push`

Git push är det kommando som pushar upp dina lokala commits till remote repot. Se det som en sync i riktningt "local -> remote". Alltså motsatt riktigt som en "[git pull](#git-pull)". En push behöver man inte göra efter varje commit, utan man kan göra det lite när som helst egentligen. Kanske i slutet av dagen när man stänger ner datorn. Så fort du gör en push så kommer din commit att läggas till remote och du skulle kunna gå in på en annan datorn och hämta hem de ändringar som du precis har gjort.

```
git push
```

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git status`

Status-kommndot är ett bra kommando för att se statusen på de olika filerna som du har arbeta med. Den kan visa vilka filerna du har ändrat i, vilka du har skapat samt vilka du har raderat. Den visar också vilken status de olika filerna har, har de status "untracked", "changes" eller "staged changes".

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git log`

Log är ett bra kommando för att lista de commitsen som finns registrerade. Kan ju en bra överblick vad som har skett det senaste tiden samt i vilken ordning ändringarna har skett i.

Skulle man behöva backa tillbaks i version är det i git log man hitter id på den commiten man vill backa tillbaks till.

Enkelt kommando:

```
git log
```

[Tillbaks till git kommandon](#git-kommandon)

[Tillbaks till toppen](#intro-grundläggande-programmering)

---
