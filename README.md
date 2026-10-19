# Dag 9 · Git-grunderna

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du går från att köra Git som ett recept till att förstå det: `status`, `add`, `commit`, `log`, `diff` och `restore`. Du gör minst sex commits med begripliga meddelanden och pushar dem.

## Bakgrund

Git är ett system som sparar historik över dina filer. Varje *commit* är ett sparat läge med ett meddelande. Du kan alltid gå tillbaka, och alla som tittar på din kod kan se hur arbetet växte fram. Du har kört `add`, `commit` och `push` som ett recept sedan dag 1. Idag förstår du vad de gör. Dag 10 publicerar du på riktigt med GitHub Pages.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Kontrollera Git

Öppna terminalen i VS Code. Skriv `git --version`. Du ska få ett versionsnummer. Skriv sedan `git config user.name` och `git config user.email`. Saknas något: `git config --global user.name "Ditt Namn"` och motsvarande för e-post.

### Steg 2. Titta på läget

I mappen du klonade: `git status`. Läs vad det står, ord för ord. Du ska se "nothing to commit, working tree clean".

### Steg 3. Din första ändring och commit

Ändra titeln i `index.html` till något eget. Kör `git status` (filen är röd), `git add index.html` (grön), `git commit -m "Ändra sidans titel"`. Kör `git log --oneline` och se din commit.

### Steg 4. Gör fem commits till

Gör fem ytterligare små ändringar, en i taget, och gör en commit för varje:
   1. ändra en rubriktext
   2. lägg till en fjärde maträtt i menyn
   3. ändra färgen `--color-primary`
   4. lägg till en rad i `README.md` om dig själv
   5. ändra öppettiderna i Om oss

Kör alltid `git status` före `git add` och `git log --oneline` efter.

### Steg 5. Skriv bra commit-meddelanden

Ett bra meddelande säger *vad* och *varför*, i presens eller imperativ: "Lägg till fjärde maträtt i menyn". Undvik "ändrat", "fix", "asdf".

### Steg 6. Se skillnaden

Ändra något utan att committa. Kör `git diff` och läs vad Git ser. Ångra sedan med `git restore <filnamn>`.

### Steg 7. Skicka upp

Kör `git push` och kontrollera på GitHub att alla dina nya commits syns under *Commits*.

### Steg 8. Ditt projekt

Öppna `mitt-projekt` och kör `git log --oneline`: det är din historik från dag 1–8. Gör minst tre nya commits där på dagens steg, med bra meddelanden, och pusha. Se `PROJEKTSTEG.md`.

## AI-spåret (nivå 3: Styr och ansvara)

**Git-handledare som du styr** (cirka 25 minuter, efter att du gjort din egen lösning)

Fri användning, full loggning. Du bär ansvaret för allt du lämnar in. AI är en bra förklarare av felmeddelanden, men en dålig bedömare av vad som är säkert i just ditt repo.

Regler: egen lösning först, du ska kunna förklara varje rad, och du loggar i `docs/ai-logg.md` i `mitt-projekt`. Reglerna finns i `AI-REGLER.md` i `mitt-projekt`.

1. Ge AI din git diff och be om ett förslag på commit-meddelande. Jämför med ditt eget.
2. Slå upp ett Git-felmeddelande (eller skapa ett) och be AI förklara det med prompten nedan.
3. Regel: kör aldrig ett kommando du inte kan förklara, särskilt inte reset --hard eller push --force.
4. Kontrollera med git status före och efter.
5. Logga: vad var bra, vad var farligt?

Prompt att utgå från:

```
Förklara detta Git-felmeddelande på enkel
svenska. Beskriv varje alternativ och
säg om det riskerar att radera mitt
arbete.

[klistra in felmeddelandet här]
```

**Kontrollera med:**

- git status före och efter.
- Kan du förklara kommandot för en kollega?

**I ditt projekt:** Använd AI för commit-meddelanden i ditt projekt. Skriv om de som är oklara.

## Kontrollista: så vet du att du är klar

- [ ] `git log --oneline` visar minst sex commits med begripliga meddelanden i övningsrepot.
- [ ] Du kan förklara vad `status`, `add`, `commit` och `log` gör.
- [ ] Du har använt `git diff` och `git restore` minst en gång.
- [ ] Du har gjort minst tre nya commits i `mitt-projekt` och pushat dem.
- [ ] Du har klistrat in din `git log --oneline` i Forms.
- [ ] Du har gjort AI-uppgiften och skrivit en post i `docs/ai-logg.md`.

## Tips om du fastnar

- `git: command not found`? Starta om VS Code. Fungerar det fortfarande: be om hjälp i handledningen.
- "Please tell me who you are"? Du har inte ställt in namn och e-post, se steg 1.
- Fastnat i en konstig skärm med `:`? Tryck `q`.
- Läs alltid vad Git säger. Det är oftast ett ganska tydligt meddelande.

## Ditt projekt: Dagens steg i `mitt-projekt`

Efter övningen här jobbar du vidare i ditt eget projekt (din design från modul 3). Dagens steg står i `PROJEKTSTEG.md` i ditt repo `mitt-projekt`, under **Dag 9**. Det är där ditt riktiga arbete växer. Övningen här är träningsbanan.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Länk till ditt `mitt-projekt`.
3. Reflektion: Klistra in utskriften från `git log --oneline` och skriv vilket av dina commit-meddelanden du är mest nöjd med och varför.

## Vill du mer? (frivilligt)

- Läs om `git commit --amend` och ändra ett meddelande.
- Skapa en `.gitignore` med `.DS_Store`.
