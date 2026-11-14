# Välkommen till **Lekvalvet** 🪁

**Lekvalvet** är ett öppet och fritt tillgängligt arkiv av lekar.  
Projektets syfte är att samla, strukturera och tillgängliggöra lekbeskrivningar på ett sätt som gör det enkelt för alla att hitta, använda och vidareutveckla dem.

---

## Licens och rättigheter

Allt innehåll i Lekvalvet är publicerat under [**CC0 1.0 Universell (Public Domain Dedication)**](https://creativecommons.org/publicdomain/zero/1.0/deed.sv).

Det innebär följande:

- Du har **fullständig frihet** att kopiera, ändra, sprida och använda materialet – även i kommersiella sammanhang.  
- Du är **inte skyldig** att ange upphovsperson eller källa (även om hänvisning uppskattas).  
- Innehållet är **utan begränsningar** i hur det får användas, både digitalt och i tryckt form.

Kort sagt: allt material i Lekvalvet är **släppt till allmän egendom** (”public domain”) och kan användas fritt, utan tillstånd.

---

## Bidrag till projektet

Genom att bidra till Lekvalvet – till exempel genom att lägga till, redigera eller förbättra innehåll – godkänner du att ditt bidrag **publiceras under samma licens (CC0 1.0 Universell)**.  

Det innebär att:

- Du **avstår från dina upphovsrättsliga anspråk** till det material du bidrar med, i den utsträckning som lagen tillåter.  
- Ditt bidrag blir en del av det fria arkivet och kan användas av vem som helst, utan tillstånd eller erkännande.  
- Du bekräftar att du har **rätt att bidra** med det material du lämnar in, och att det inte inkräktar på någon annans upphovsrätt eller immateriella rättigheter.

Syftet med detta är att säkerställa att hela Lekvalvet förblir ett **helt fritt och öppet** resursarkiv för alla.

---

## Teknisk information

- **Ramverk:** Projektet byggs med [**Zensical**](https://zensical.org/) och använder konfigurationen i `mkdocs.yml`.
- **Hosting:** Webbplatsen publiceras via **GitHub Pages**, en tjänst som ägs och tillhandahålls av **Microsoft**.

### Utveckla och bygga lokalt

Installera [uv](https://docs.astral.sh/uv/getting-started/installation/). Projektets uv-version anges i `pyproject.toml` och Python-versionen i `.python-version`. uv hämtar Python automatiskt vid behov.

```sh
uv sync --locked
uv run --locked zensical serve
```

Kör samma kontroll som i CI innan du skickar in en ändring:

```sh
uv run --locked zensical build --clean --strict
```

`--strict` gör att bygget misslyckas vid valideringsvarningar, exempelvis trasiga interna länkar. Resultatet skrivs till `site/`.

Alla beroenden låses i `uv.lock`, som ska checkas in. Uppdatera dem med `uv lock --upgrade`, kör strict-bygget igen och checka in den uppdaterade låsfilen tillsammans med eventuella ändringar i `pyproject.toml`.

### CI och publicering

GitHub Actions kör kontrollen **Build (strict)** för pull requests till `master`, vid push till `master`, i merge-kön och vid manuell körning. `uv sync --locked` avbryter om låsfilen saknas eller inte stämmer med projektets beroenden.

Efter ett godkänt bygge på `master` publiceras samma byggartefakt till GitHub Pages i ett separat jobb. Bara publiceringsjobbet har skrivrättigheter för Pages och tillgång till en OIDC-token. Actions är låsta till fullständiga commit-hashar, och utcheckningen sparar inga GitHub-inloggningsuppgifter.

I repots GitHub-inställningar ska **Pages → Build and deployment → Source** vara **GitHub Actions**. För att förhindra att ändringar med underkända byggen slås ihop, konfigurera en branch rule/ruleset för `master` som kräver pull requests och statuskontrollen **Build (strict)** samt att grenen är uppdaterad eller använder merge-kön. Även undantag från regeln behöver begränsas. Dessa inställningar hanteras i GitHub och aktiveras inte av workflow-filen.

### Beroendeuppdateringar med Renovate

`renovate.json` konfigurerar Renovate för beroendeuppdateringar och behåller GitHub Actions låsta till commit-hashar. Renovate behöver vara aktiverat för repot.

Nya versioner måste ha varit publicerade i minst **14 dagar** innan Renovate föreslår dem. Versioner utan publiceringsdatum hålls tillbaka. Regeln gäller även säkerhetsuppdateringar. Det är versionens publiceringsdatum som räknas, inte hur länge en pull request har varit öppen.

**Lock file maintenance** är det enda undantaget från ålderskravet och körs på måndagar före 04:00 svensk tid. Även dessa pull requests måste klara **Build (strict)**.

GitHubs inbyggda automerge är aktiverat i Renovate. Pull requests hålls tillbaka tills ålderskontrollen är klar, även för säkerhetsuppdateringar. Aktivera **Settings → General → Allow auto-merge** i GitHub och gör **Build (strict)** till en obligatorisk statuskontroll för `master`, så att GitHub inväntar ett godkänt strict-bygge innan automatisk merge. Dessa repo-inställningar måste aktiveras separat.

Renovates ålderskontroll heter **renovate/stability-days**. En lokal Renovate-konfiguration kan inte ensam hindra manuella merges eller undantag från branch-regler. Kräv inte den kontrollen generellt för alla pull requests utan att även hantera vanliga bidrag, eftersom Renovate inte rapporterar status på dem.

---

## Ansvarsfriskrivning

Innehållet i Lekvalvet tillhandahålls **”i befintligt skick”** utan några som helst garantier, uttryckliga eller underförstådda.  
Projektets underhållare och bidragsgivare **ansvarar inte** för eventuella skador, förluster eller konsekvenser som kan uppstå genom användning av informationen eller materialet i arkivet.  

Det är alltid upp till användaren att bedöma säkerheten och lämpligheten i hur lekarna genomförs.
