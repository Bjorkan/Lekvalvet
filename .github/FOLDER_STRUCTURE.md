# Mappstruktur

Detta dokument beskriver hur filerna i Lekvalvet är organiserade.

## Översikt

```
Lekvalvet/
├── .github/                    # GitHub-specifika filer
│   └── GAME_TEMPLATE.md       # Mall för att skapa nya lekar
├── docs/                      # Alla lekar och dokumentation
│   ├── Lära känna/           # Lekar för att lära känna varandra
│   ├── Gruppövningar/        # Övningar för gruppdynamik och samarbete
│   ├── Övrigt/               # Andra typer av lekar
│   └── index.md              # Startsida för webbplatsen
├── CONTRIBUTING.md           # Guide för hur man bidrar
├── LICENSE                   # CC0 1.0 Universiell licens
├── README.md                 # Projektbeskrivning
└── mkdocs.yml               # Konfiguration för MkDocs
```

## Detaljerad beskrivning

### `.github/`

Innehåller GitHub-specifika filer:
- **GAME_TEMPLATE.md** - Mall för att skapa nya lekbeskrivningar

### `docs/`

Huvudmappen för alla lekar och webbplatsinnehåll.

#### `docs/Lära känna/`

Lekar vars huvudsakliga syfte är att hjälpa deltagare att lära känna varandra.

**Exempel:**
- Fruktsallad
- Tacos
- Namnlekar

#### `docs/Gruppövningar/`

Övningar som fokuserar på att bygga gruppdynamik, samarbete och teamwork.

**Exempel:**
- Fyra man i soffan
- Samarbetslekar
- Förtroendeövningar

#### `docs/Övrigt/`

Lekar som inte passar tydligt in i de andra kategorierna eller har andra syften.

**Exempel:**
- Amöba
- Reaktionslekar
- Energizers

#### `docs/index.md`

Webbplatsens startsida som visas på https://bjorkan.github.io/Lekvalvet/

### Projektfiler i roten

- **CONTRIBUTING.md** - Omfattande guide för hur man bidrar till projektet
- **LICENSE** - Fullständig licenstext för CC0 1.0 Universiell
- **README.md** - Projektöversikt och snabb introduktion
- **mkdocs.yml** - Konfigurationsfil för Material for MkDocs

## Namngivningskonventioner

### Filnamn

- Använd gemener (små bokstäver)
- Använd bindestreck (`-`) istället för mellanslag
- Använd `.md` filändelse för Markdown-filer
- Använd svenska tecken (å, ä, ö) i filnamn om det behövs

**Bra exempel:**
- `fruktsallad.md`
- `lära-känna-bollen.md`
- `amöba.md`

**Dåliga exempel:**
- `FruktSallad.md` (stora bokstäver)
- `fruktsallad.txt` (fel filändelse)
- `lara_kanna_bollen.md` (understreck istället för bindestreck)

### Mappnamn

- Använd beskrivande namn på svenska
- Använd versaler/stora bokstäver i början av varje ord
- Använd mellanslag mellan ord
- Använd svenska tecken (å, ä, ö)

**Exempel:**
- `Lära känna/`
- `Gruppövningar/`
- `Övrigt/`

## Hur man lägger till en ny kategori

Om du vill lägga till en ny kategori av lekar:

1. Skapa en ny mapp under `docs/` med ett beskrivande namn
2. Lägg till en `.meta.yml` fil i mappen med följande innehåll:
   ```yaml
   tags:
     - Kategorinamn
   ```
3. Uppdatera `mkdocs.yml` om det behövs
4. Uppdatera denna fil (`FOLDER_STRUCTURE.md`) med beskrivning av den nya kategorin

## Frågor?

Om du är osäker på var din lek ska placeras, fråga i ett issue eller i din Pull Request så hjälper vi dig!
