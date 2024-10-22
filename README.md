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

<image src="./git-overview.png">

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

### Git kommandon

<details>
<summary>Lista på kommandon</summary>

- [git clone](#git-clone)
- [git add]()
- [git commit]()
- [git pull]()
- [git push]()
- [git status]()
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

[Tillbaks till toppen](#intro-grundläggande-programmering)

---

#### `git status`

Status-kommndot är ett bra kommando för att se statusen på de olika filerna som du har arbeta med. Den kan visa vilka filerna du har ändrat i, vilka du har skapat samt vilka du har raderat. Den visar också vilken status de olika filerna har, har de status "untracked", "changes" eller "staged changes". Olika status betyder olika saker.

[Tillbaks till toppen](#intro-grundläggande-programmering)

---
