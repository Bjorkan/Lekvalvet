# Föreslagna förbättringsaktiviteter

## Stavfel
- **Plats:** `docs/Lära känna/tacos.md`, rad 6.
- **Problem:** Texten använder uttrycket "För enkelheten skull" som är felstavat/grammatiskt fel. Det korrekta uttrycket är "För enkelhetens skull".
- **Föreslagen aktivitet:** Uppdatera formuleringen så att instruktionen använder det korrekta uttrycket "För enkelhetens skull".

## Bugg
- **Plats:** `docs/Lära känna/tacos.md`, raderna 10–14.
- **Problem:** Steglistan upprepar siffran 3 två gånger vilket gör att stegordningen blir fel vid rendering.
- **Föreslagen aktivitet:** Justera nummerlistan så att varje steg får en unik och stigande numrering (t.ex. 1–4).

## Dokumentationsavvikelse
- **Plats:** `README.md`, rad 6.
- **Problem:** Meningen "Sidan växer hela tiden med nya övningar och ska förhoppningsvis kunna hjälpa folk som leder grupper at Drivs med Material for MkDocs" innehåller grammatiska fel och saknar tydlig punktuation.
- **Föreslagen aktivitet:** Omformulera meningen till korrekt svenska, exempelvis genom att ersätta "at" med "att" och dela upp texten i två separata meningar.

## Testförbättring
- **Plats:** Projektet saknar automatiska kontroller som säkerställer att dokumentationen bygger korrekt.
- **Problem:** Utan automatisk testning kan ett trasigt MkDocs-bygg flyga under radarn tills sidan ska publiceras.
- **Föreslagen aktivitet:** Lägg till ett CI-steg (t.ex. GitHub Actions) som kör `mkdocs build` vid pull requests för att fånga strukturella fel i dokumentationen tidigt.
