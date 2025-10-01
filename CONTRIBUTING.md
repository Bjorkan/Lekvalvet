# Bidragsguide till Lekvalvet 🪁

Tack för att du vill bidra till Lekvalvet! Vi välkomnar alla bidrag, oavsett om det är nya lekar, förbättringar av befintliga beskrivningar, rättningar av stavfel eller förbättringar av dokumentationen.

## Innan du bidrar - viktigt om licensen

**Lekvalvet är licenserat under CC0 1.0 Universiell**, vilket innebär att allt innehåll är fritt tillgängligt för vem som helst att använda, ändra och distribuera - även kommersiellt.

### Vad innebär detta för dig som bidragare?

När du bidrar till Lekvalvet godkänner du att:

- Ditt bidrag släpps under CC0 1.0 Universiell licens
- Du avstår från alla upphovsrätter till ditt bidrag
- Ditt bidrag blir en del av allmän egendom (public domain)
- Vem som helst kan använda, ändra och distribuera ditt bidrag utan begränsningar
- Du kommer inte ha någon kontroll över hur ditt bidrag används i framtiden

**Om du inte är bekväm med detta, bidra inte till projektet.**

## Hur du bidrar

### 1. Skapa eller välj ett issue

- Titta först om det redan finns ett issue för det du vill göra
- Om inte, skapa ett nytt issue där du beskriver vad du vill bidra med
- Vänta på feedback innan du börjar arbeta (så att du inte gör onödigt arbete)

### 2. Forka och klona projektet

```bash
# Forka projektet via GitHub's webbgränssnitt
# Klona sedan din fork
git clone https://github.com/DITT-ANVÄNDARNAMN/Lekvalvet.git
cd Lekvalvet
```

### 3. Skapa en ny branch

```bash
git checkout -b min-nya-lek
```

### 4. Lägg till ditt bidrag

#### Om du lägger till en ny lek:

1. Bestäm vilken kategori leken passar i:
   - `docs/Lära känna/` - Lekar för att lära känna varandra
   - `docs/Gruppövningar/` - Övningar för att bygga gruppdynamik
   - `docs/Övrigt/` - Andra typer av lekar

2. Använd vår [lekmall](.github/GAME_TEMPLATE.md) som utgångspunkt

3. Skapa en ny fil med ett beskrivande namn (använd gemener och bindestreck):
   ```
   docs/Lära känna/min-nya-lek.md
   ```

4. Fyll i mallen med information om din lek

#### Om du förbättrar befintligt innehåll:

- Rätta stavfel
- Förtydliga instruktioner
- Lägg till anpassningar eller varianter
- Förbättra strukturen

### 5. Testa ditt bidrag lokalt (valfritt)

Om du vill se hur din lek ser ut på webbplatsen:

```bash
# Installera MkDocs och Material theme
pip install mkdocs-material

# Starta lokal server
mkdocs serve

# Öppna http://127.0.0.1:8000 i din webbläsare
```

### 6. Commit och push

```bash
git add .
git commit -m "Lägg till lek: [Leknamn]"
git push origin min-nya-lek
```

### 7. Öppna en Pull Request

1. Gå till din fork på GitHub
2. Klicka på "Pull Request"
3. Fyll i en tydlig beskrivning av vad du har gjort
4. Vänta på feedback och var beredd att göra ändringar om det behövs

## Riktlinjer för lekar

### Vad gör en bra lekbeskrivning?

- **Tydlig titel** - Namnet på leken
- **Kort beskrivning** - Vad är leken och vad är målet?
- **Tydliga instruktioner** - Steg-för-steg hur man genomför leken
- **Anpassningar** (valfritt) - Hur kan leken göras enklare/svårare eller anpassas för olika grupper?
- **Material** (om relevant) - Vad behövs för att genomföra leken?
- **Gruppdynamik** (valfritt) - Vad tränar leken? (samarbete, kommunikation, etc.)

### Språk och ton

- Skriv på svenska
- Använd du-tilltal eller infinitiv
- Var tydlig och koncis
- Undvik komplicerade ord när det finns enklare alternativ
- Inkluderande språk - tänk på att beskriva leken så att alla kan vara med

### Struktur

Följ strukturen i [lekmallen](.github/GAME_TEMPLATE.md):

```markdown
# Leknamn

En kort beskrivning av leken och dess syfte.

## Instruktioner

1. Första steget
2. Andra steget
3. ...

## Anpassningar (valfritt)

Olika sätt att anpassa leken.

## Material (om relevant)

- Sak 1
- Sak 2
```

## Kodstil och formatering

- Använd Markdown för all dokumentation
- Använd meningsfulla filnamn (gemener, bindestreck istället för mellanslag)
- Följ befintlig struktur och formatering i projektet

## Frågor?

Om du har några frågor, tveka inte att:
- Öppna ett issue på GitHub
- Kommentera i ett befintligt issue
- Nå ut till projektägaren

Tack för ditt bidrag! 🎉
