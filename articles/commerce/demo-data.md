---
title: Skjermoppsett for demonstrasjonsdata i Moderne salgssted (MPOS) og Skysalgssted
description: Denne artikkelen inneholder informasjon om skjermoppsett som er inkludert i settet med demonstrasjonsdata for salgsstedsopplevelser i Dynamics 365 Commerce.
author: josaw1
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: eb7a288b61e8b467dd8ad6a8f7dc42b7fca0d943
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897231"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Skjermoppsett for demonstrasjonsdata i Moderne salgssted (MPOS) og Skysalgssted

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder informasjon om skjermoppsett som er inkludert i settet med demonstrasjonsdata for salgsstedsopplevelser i Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Eksempelskjermoppsett som er inkludert i Handel-demonstrasjonsdata har innhold som er optimalisert for forskjellige segmenter for detaljhandel, butikkarbeiderroller og enheter. Ett enkelt oppsett kan inneholde flere oppsettstørrelser og kombinasjoner av knappegrupper for å sikre dekning når butikkarbeidere flytter mellom enheter og stasjoner. Denne artikkelen fremhever forskjellene mellom disse oppsettene, operasjonene som de gir og de helhetlige opplevelsene som de leverer.

![Oppsett for demonstrasjonsdata på tvers av enheter.](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Innholdet i en skjermoppsett-ID

Hvis du vil finne skjermoppsett, går du til **Detaljhandel og handel** \> **Kanaloppsett** \> **Oppsett av salgssted** \> **Salgssted** \> **Skjermoppsett**.

![Skjermoppsett-side.](../commerce/media/demo-screen-layouts-fig-2-1.png)

Skjermoppsett-ID-er kan inneholde opptil ti tegn. ID-en er en streng som består av tre typer informasjon i denne rekkefølgen:

1. Firma
2. Oppsettversjon
3. Egenskap

### <a name="company"></a>Firma

| Brev | Firma         |
|--------|-----------------|
| A      | Adventure Works |
| Ø      | Fabrikam        |
| K      | Contoso         |

### <a name="layout-version"></a>Oppsettversjon

| Versjonsnummer | beskrivelse                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Den grunnleggende versjonen som støtter flere skjermstørrelser for forskjellige enheter og sideforhold |
| 3.1            | Den grunnleggende versjonen som har ekstra støtte for panelet **Anbefalte produkter**        |
| 4              | Den utvidede versjonen for det oppdaterte oppsettet for utvidet Fabrikam                                  |

### <a name="persona"></a>Egenskap

| Forkortelse | Egenskap       | Innhold |
|--------------|---------------|----------|
| CSH          | Kasserer       | Kassereroppsett inkluderer alle transaksjonsrelaterte operasjoner, for eksempel kundeordrer, returer, rabatter, annulleringer og gavekort. Disse oppsettene inkluderer også daglige oppgaver for lagerstyring, for eksempel priskontroller, lageroppslag og lagertellinger. Det finnes også grunnleggende skiftadministrasjon for startbeløp, suspendering av skift og tidsklokke. |
| MGR          | Butikksjef | Butikksjefoppsett inkluderer alle transaksjonsrelaterte operasjoner som finnes i et kassereroppsett, men det inneholder også mva-overstyringer. Disse oppsettene inkluderer også daglige oppgaver for lagerstyring, for eksempel priskontroller, lageroppslag og lagertellinger. Skiftadministrasjon finnes for start, suspendering og avslutning av skift. I tillegg inkluderer oppsettene skuffoperasjoner for oppføring, fjerning, kasseoppgjør og safe- og banklevering. Til slutt inkluderer disse oppsettene tilgangen til prestasjonsrapporter og tillater utskrift av X- og Z-rapporter. |
| STK          | Lagermedarbeider   | Lagermedarbeideroppsett er optimalisert for lagerstyring. De inkluderer tilgang til daglige oppgaver for priskontroller, lageroppslag, plukk og mottak, lagertelling og settdemontering. Disse oppsettene gir også grunnleggende skiftoperasjoner for tidsklokke og suspendering av skift. Selv om disse oppsettene først og fremst er beregnet for back office-oppgaver, har lagermedarbeidere de samme operasjonene som kasserere for transaksjonsskjermer. |

### <a name="example-layout"></a>Eksempel-oppsett

Her er et eksempel på en skjermoppsett-ID for firmaet Fabrikam, oppsettversjon 4 og Butikksjef:

F4MGR

Illustrasjonen nedenfor viser et eksempel på velkomstskjermen for Fabrikam-butikksjef.

![Velkomstskjermen for Fabrikam-butikksjefen.](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Oppsettstørrelser

### <a name="full-vs-compact-layouts"></a>Fullstendige kontra kompakte oppsett

Et skjermoppsett kan ha konfigurasjoner for både fullstendige og kompakte enheter. Derfor kan en bruker tilordnes til ett enkelt skjermoppsettet som fungerer på tvers av ulike størrelser og formfaktorer i butikken.

- **Modern POS - Fullstendig** – Fullstendige oppsett brukes vanligvis helst for større skjermer, for eksempel PC-skjermer eller nettbrett. Brukere kan velge elementene i brukergrensesnittet som oppsettet inneholder, angi størrelsen og plasseringen til elementene og konfigurere de detaljerte egenskapene. Fullstendig oppsett støtter både liggende og stående konfigurasjoner.
- **Moderne POS - Kompakt** – Kompakt oppsett brukes vanligvis helst for telefoner eller små nettbrett. Utformingsmulighetene er begrenset for kompakte enheter. Brukere kan konfigurere kolonner og felt for rutene for kvittering og totaler.

### <a name="screen-resolutions-that-are-provided"></a>Skjermoppløsninger som tilbys

Tabellen nedenfor viser oppsettstørrelsene som finnes for vanlige skjermoppløsninger.

| Oppsettype | Oppløsning | Størrelsesforhold | Målskjerm          |
|-------------|------------|--------------|-------------------------|
| Komprimer\*   | 480 × 853  | 16:9         | Telefoner                  |
| Full        | 1024 × 768 | 4:3          | Nettbrett                 |
| Full\*      | 1280 × 720 | 16:9         | Nettbrett                 |
| Full        | 1366 × 768 | 16:9         | Nettbrett, store skjermer |
| Full        | 1440 × 960 | 3:2          | Nettbrett, store skjermer |
| Full\*      | 1536 × 864 | 16:9         | Nettbrett, store skjermer |

\* Disse ekstra oppsettstørrelsene er bare tilgjengelige i oppsett for Adventure Works og Fabrikam.

> [!TIP]
> POS velger automatisk oppsettstørrelser basert på den nærmeste størrelsen som er tilgjengelig for skjermoppløsningen for gjeldende appvindu. Hvis du vil finne skjermoppsett-ID og oppsettoppløsning som brukes for øyeblikket i Moderne salgssted (MPOS) eller Detaljhandel-skysalgssted (CPOS), kan du åpne siden **Innstillinger** og se i delen **Øktinformasjon**. Du kan også se den faktiske vindusoppløsningen for gjeldende appe eller nettleserramme. Når du har denne informasjonen, kan du finne kilden til oppsettinnholdet ved å gå til **Kanaloppsett** \> **Salgsstedsoppsett** \> **Salgssted** \> **Skjermoppsett**.

![Skjermoppsett og oppsettoppløsninger/-størrelser i Handel og Salgssted.](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Firmaer og merker

Hvert fiktive firma er rettet mot ulike detaljhandelsegmentet og inkluderer produktkataloger som er beregnet for firmaets marked. Hvert firma har et unikt visuell merke som følger med produktene. Varemerkeelementene omfatter uthevingsfargen, mørkt eller lyst tema og tilhørende bilder med realistiske opplevelser.

### <a name="company-segment-and-visual-characteristics"></a>Firmasegmentet og visuelle egenskaper

| Firma         | Sted | Segment        | Utheving | Tema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sportsartikler | Blå   | Mørk  |
| Fabrikam        | San Francisco  | Mote        | Grønn  | Lys |
| Contoso         | Boston   | Elektronikk    | Rød    | Mørk  |

> [!NOTE]
> Adventure Works og Fabrikam er de to ledende merkene. Contoso er tilgjengelig, men ikke alle oppsettene følger med.

Illustrasjonene nedenfor viser eksempler på velkomstsiden og transaksjonssiden for de tre fiktive firmaene.

### <a name="adventure-works"></a>Adventure Works

![Velkomstside for Adventure Works med demonstrasjonsdata.](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Transaksjonsside for Adventure Works med demonstrasjonsdata.](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Velkomstside for Fabrikam med demonstrasjonsdata.](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Transaksjonsside for Fabrikam med demonstrasjonsdata.](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Oppsett for demonstrasjonsdata for Contoso.](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Matrise for brukerpålogging

Brukere er angitt for de forskjellige skjermoppsettene. Ved å bruke tabellen nedenfor, får du tilgang til alle skjermene. Logg ganske enkelt på ved hjelp av en riktig operator-ID.

| Firma         | Skjermoppsett-ID | Egenskap       | Operatør-ID-er           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Butikksjef | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kasserer       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Lagermedarbeider   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | Butikksjef | 000160, 000713         |
| Fabrikam        | F3CSH            | Kasserer       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Lagermedarbeider   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Butikksjef | 000100, 000111         |
| Contoso         | C3CSH            | Kasserer       | 000110, 000120         |
| Contoso         | Gjelder ikke her   | Lagermedarbeider   | Gjelder ikke her         |

> [!TIP]
> Aktivere en kasse på den tilsvarende butikklokasjonen for best mulig resultat, og angi firmaet til personen som du vil bruke når du logger på. På denne måten kan bidra til å garantere at den visuelle profilen og merkebildene er justert på tvers av opplevelsen. Hvis du for eksempel er interessert i å vise et Fabrikam-oppsett for en kasserer, kan du aktivere en kasse i Houston-butikken.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce.](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]