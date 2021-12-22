---
title: Inntektsføringsoppsett
description: Dette emnet beskriver alternativene for inntektsføringsoppsett og deres betydning.
author: kweekley
ms.date: 11/24/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e8e29ec1ca5a02db67bb4baf522da96ec23c740f
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867226"
---
# <a name="revenue-recognition-setup"></a>Inntektsføringsoppsett
[!include [banner](../includes/banner.md)]

Den nye modulen **Inntektsføring** har blitt lagt til, og den omfatter menyelementer for alle nødvendige oppsett. Dette emnet beskriver alternativene for oppsett og deres betydning.

> [!NOTE]
> Funksjonen Inntektsføring er nå aktivert som standard via Funksjonsbehandling. Hvis organisasjonen ikke bruker denne funksjonen, kan du deaktivere den i arbeidsområdet **Funksjonsbehandling**.
>
> Inntektsføring, inkludert buntfunksjonalitet, innhold som ikke støttes i Commerce-kanaler (e-handel, salgssted og telefonsenter). Varer som konfigureres for inntektsføring, bør ikke legges til i ordrer eller transaksjoner som er opprettet i Commerce-kanaler.

Modulen **Inntektsføring** har følgende alternativer for oppsett:

- Inntektsføringsjournaler
- Parametere for inntektsføring
- Inntektsplaner 
- Lageroppsett

    - Varegrupper og frigitte produkter
    - Definere inntektsplan
    - Definere inntektspris
    - Lageroppsett

        - Definere inntektsplan
        - Definere inntektspris

    - Posteringsprofiler
    - Bunter

        - Buntkomponenter
        - Buntvare

- Prosjektoppsett

## <a name="revenue-recognition-journals"></a>Inntektsføringsjournaler

En ny journaltype er innført for inntektsføring. Journalen er obligatorisk, og den brukes i to scenarier.

Det første scenariet skjer etter at alle de kontraktsforpliktelsene er oppfylt, når den utsatte inntekten føres ved å opprette en journal for inntektsføring som er basert på detaljene i inntektsplanen. Journalen inneholder en regnskapsoppføring som flytter saldoen fra den utsatte inntektsfinanskontoen til inntektsfinanskontoen.

Det andre scenariet forekommer når en journal opprettes etter ny tildeling. Ny tildeling skjer når en salgsordrelinje legges til en salgsordre som allerede er fakturert, eller når det opprettes en ny salgsordre som inkluderer en linje som er en del av den opprinnelige kontrakten. Hvis en faktura ble postert før den nye salgsordrelinjen er lagt til, må det opprettes en korreksjonsregnskapsoppføring for den posterte kundefakturaen.

Journalen defineres på siden **Journalnavn** (**Inntektsføring \> Oppsett \> Journalnavn**). Journaltypen må settes til **Inntektsføring**. 

## <a name="parameters-for-revenue-recognition"></a>Parametere for inntektsføring

Innstillinger for inntektsføring blir konfigurert i fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**). Følgende innstillinger er tilgjengelige:

- **Journalnavn for inntektsføring** – velg journalen som ble opprettet for inntektsføring. Journalen er nødvendig når inntekt føres fra inntektsplanen, eller når du tildeler en salgsordre på nytt som allerede er fakturert.
- **Aktiver rabattildelingsmetode** – sett dette alternativet **Ja** for å bestemme inntektsprisen gjennom tildeling av den rimelige markedsverdien som er definert i inntektsprisen for hvert frigitt produkt. Denne tildelingen omfatter tildeling av alle linjerabatter på tvers av varene. Hvis dette alternativet er satt til **Nei**, bruker systemet medianprisen som er definert i inntektsprisen for hvert frigitt produkt. Hvis dette alternativet er satt til **Nei**, men ingen medianpris er angitt for de frigitte produktene, oppstår det ikke tildeling av inntektsprisen.
- **Inkluder hoderabatter** – sett dette alternativet til **Ja** for å bestemme inntektsprisen ved å tildele hode rabatter på tvers av produkter. Hvis dette alternativet er satt til **Nei**, blir ikke hoderabatten tatt med i inntektspristildelingen.
- **Deaktiver kontraktsbetingelser** – sett dette alternativet til **Ja** hvis produkter som har en inntektstypen **Støtte etter kontrakt**, kan frigis selv om kontraktens start- og sluttdatoer ikke er definert for dem. Vanligvis kreves det start- og sluttdatoer for kontrakter for varer med inntektstypen **Støtte etter kontrakt**. Når start- og sluttdatoene for kontrakten ikke er definert, beregnes detaljene i inntektsplanen for posteringen ved hjelp av antall forekomster og fakturadatoen.
- **Poster fakturakorrigeringer til Kunder ved ny tildeling** – når du tildeler på nytt for fakturaer som allerede er postert, må regnskapsoppføringen for den posterte fakturaen korrigeres. Bruk dette alternativet til å angi hvordan korrigeringen skal utføres.

    - Sett dette alternativet til **Nei** for å begrense postering av den korrigeringstransaksjonen til økonomimodulen. Når dette alternativet er satt til **Nei**, opprettes det ingen flere dokumenter i Kunder for korrigeringen av det interne regnskapet. Når fakturaen betales, bruker utligningsprosessen den gamle regnskapsposten til å postere eventuelle kontantrabatter, eller realisert fortjeneste eller tap.
    - Sett dette alternativet til **Ja** for automatisk å opprette et tilbakeføringsdokument og ny faktura for den korrigeringstransaksjonen i Kunder. Ettersom denne korrigeringen er en intern regnskapskorrigering, blir ikke de nye dokumentene sendt eller formidlet til kunden. Tilbakeføringsdokumentet utlignes mot den opprinnelige fakturaen, og den nye, korrigerte fakturaen betales av kunden. Vær oppmerksom på at alle tre dokumentene vises i rapporter, for eksempel kundeutdraget.

[![Oppsettsinformasjon.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Inntektsplaner

En inntektsplan må opprettes for hver forekomst som inntekt kan utsettes for. Hvis organisasjonen for eksempel har støtte over seks måneder, 12-måneders, 18 måneder og 24-måneders perioder, må du opprette en inntektsplan for hver periode. Oppsettet av inntektsplanen bestemmer hvordan inntektsprisen skal tildeles over det antallet perioder du velger. Den bestemmer også standarddatoene som angis for inntektsplanen som opprettes når fakturaen posteres.

Hvis du fører inntekt etter milepæl, anbefaler det at du oppretter en inntektsføringsplan for antallet milepæler, uavhengig av føringsdatoene. Når du har opprettet tidsplanene, kan du redigere dem slik at de gjenspeiler de forventede milepældatoene. Disse postene kan settes på vent til du får melding om at milepælen er oppfylt og at inntekten kan føres.

Inntektsplaner opprettes på siden **Inntektsplaner** (**Inntektsføring \> Oppsett \> Inntektsplaner**).

[![Inntektsplaner.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Angi beskrivende verdier i feltene **Inntektsplan** og **Beskrivelse**. Følgende tilleggsinnstillinger brukes til å opprette inntektsplanen når fakturaen er postert.

- **Forekomster** – angi antall måneder eller forekomster for inntektshenvisningen.
- **Automatisk sperring** – merk av i denne avmerkingsboksen hvis alle linjene i inntektsplanen skal plasseres på vent når fakturaen posteres. Sperringen må fjernes manuelt fra hver linje i tidsplanen før linjens utsatte inntekt kan føres.
- **Automatiske kontraktsbetingelser** – merk av i denne avmerkingsboksen hvis start- og slutt datoene for kontrakten skal angis automatisk. Disse datoene angis automatisk for frigitte produkter av inntektstypen **Støtte etter kontrakt**. Start datoen for kontrakten settes automatisk til salgsordrelinjens ønskede forsendelsesdato, og kontraktens sluttdato settes automatisk til startdatoen pluss antall måneder eller forekomster som er definert i oppsettet til inntektsplanen. Produktet på salgsordrelinjen er for eksempel for en garanti i ett år. Standard inntektsplan er **12M** (12 måneder), og det er merket av for **Automatiske kontraktsbetingelser** for denne inntektsplanen. Hvis salgsordrelinjen har en ønsket forsendelsesdato på 16. desember 2019, er startdatoen for standardkontrakten 16. desember 2019, og standardkontraktens sluttdato er 15. desember 2020.
- **Føringsgrunnlag** – føringsgrunnlaget bestemmer hvordan inntektsprisen skal tildeles på tvers av forekomstene.

    - **Månedlig etter dager** – beløpet blir tildelt basert på de faktiske dagene i hver kalendermåned.
    - **Månedlig** – beløpet fordeles likt på tvers av antallet måneder som er definert i forekomstene.
    - **Forekomster** – beløpet tildeles likt på tvers av forekomstene, men kan inkludere en ekstra periode hvis du velger **Faktisk startdato** som føringens konvensjon.
    - **Regnskapsperiode etter dager** – beløpet blir tildelt basert på de faktiske dagene i hver regnskapsperiode. 

    Resultatene i **Månedlig etter dager** og **Regnskapsperiode etter dager** vil være de samme når regnskapsperiodene følger kalendermåneder. Det eneste unntaket er når føringskonvensjonen er satt til **Slutten av måned/periode**, og feltene **Kontraktens startdato** og **Sluttdato** er tomme på en salgsordrelinje.

- **Føringskonvensjon** – føringskonvensjonen bestemmer datoene som angis i inntektsplanen for fakturaen.

    - **Faktisk startdato** – planen blir opprettet ved hjelp av startdatoen for kontrakten (for \[PCS\]-varer som har støtte etter kontrakten) eller fakturadatoen (for viktige og uviktige varer).
    - **1. dag i måned/periode** – datoen på den første tidsplanlinjen er kontraktens startdato (eller fakturadato). Alle etterfølgende tidsplanlinjer opprettes imidlertid for den første i måneden eller regnskapsperioden.
    - **Delt midt i måneden** – datoen på den første planleggingslinjen er avhengig av fakturadatoen. Hvis fakturaen er postert mellom den 1. og 15. i måneden, opprettes inntektsplanen ved hjelp av den første dagen i måneden. Hvis fakturaen er postert den 16. eller senere, opprettes inntektsplanen ved hjelp av den første dagen i neste måned.

        **Delt midt i måneden** kan ikke velges hvis føringsgrunnlaget er satt til **Regnskapsperiode etter dager**.

    - **1. dag i neste måned/periode** – datoen som tidsplanen starter på er den første dagen i neste måned eller regnskapsperiode.
    - **Slutten av måned/periode** – datoen på den første tidsplanlinjen er kontraktens startdato (eller fakturadato). Alle etterfølgende tidsplanlinjer opprettes imidlertid for den siste dagen i måneden eller regnskapsperioden. 

Velg knappen **Detaljer for inntektsplan** for å vise de generelle periodene og prosentandelene som føres i hver periode. Som standard er verdien for **Føringsprosent** likt tildelt på tvers av antall perioder. Hvis føringsgrunnlaget er satt til **Månedlig**, kan føringsprosenten endres. Når du endrer føringsprosenten, får du melding om at totalen ikke er lik 100 prosent. Hvis du mottar denne meldingen, kan du fortsette å redigere linjer. Den totale prosenten må imidlertid være lik 100 før du lukker siden.

[![Detaljer for inntektsplan.](./media/revenue-schedule-details-2nd-scrn.png)](./media/revenue-schedule-details-2nd-scrn.png)

## <a name="inventory-setup"></a>Lageroppsett

Du kan føre inntekt for frigitte produkter på salgsordrer, men ikke med salgskategorier i salgsordrene eller med fritekstfakturaer hvis ingen varer er inkludert i dokumentet. Valgene du gjør når du definerer frigitte produkter, bestemmer hvordan varens inntekt føres. Valgene bestemmer for eksempel om inntektsprisen skal tildeles og om inntekten utsettes ved hjelp av en inntektsplan.

Oppsett kan starte i hurtigfanen **Inntektsføring** på siden **Varegruppe** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Varegruppe**). Denne siden inneholder flere oppsettsfelt. Disse feltene brukes til å angi standardverdier bare for nye frigitte produkter som er opprettet i systemet. Etter hvert som nye produkter opprettes, angis verdiene du angir her, som standard for varegruppen. Du kan overstyre standardverdiene for frigitte produkter på siden **Frigitte produkter** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Frigitte produkter**). Standardverdiene som er angitt for de frigitte produktene, blir deretter overført til salgsordren.

## <a name="item-groups-and-released-products"></a>Varegrupper og frigitte produkter

### <a name="define-the-revenue-schedule"></a>Definere inntektsplanen

Inntekt på salgsordrelinjen blir utsatt hvis en inntektsplan er definert for det frigitte produktet og brukes som standard i salgsordrelinjen. Hvis innstillingen skal brukes som standard for produktet, kan du definere inntektsplanen i hurtigfanen **Inntektsføring** på siden **Varegruppe** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Varegruppe**). Du kan også definere innstillingen for det frigitte produktet i hurtigfanen **Innføring** på siden **Frigitte produkter** (**Inntektsføring \> Oppsett \> Lageroppsett \> Frigitte produkter**).

Velg inntektsplanen som representerer perioden inntekten skal utsettes til, i feltet **Inntektsplan**. Inntektsplanen registreres automatisk på salgsordrelinjen, og detaljene for tidsplanen opprettes når salgsordrefakturaen posteres.

### <a name="define-the-revenue-price"></a>Definere inntektsprisen

Varegrupper og frigitte produkter kan defineres ved hjelp av medianprismetoden eller rabattildelingsmetoden. Begge metodene krever ulike innstillinger på siden **Frigitte produkter**:

- **Er inntektstildeling aktiv** – sett dette alternativet til **Ja** for å inkludere det frigitte produktet i beregningen av inntektstildeling. Hvis dette alternativet er satt til **Nei**, bruker det frigitte produktet medianprismetoden hvis medianprisen er definert. Hvis medianprisen ikke er definert, brukes enhetsprisen på salgsordrelinjen til å postere inntekt eller utsatt inntekt.
- **Inntektstype** – velg inntektstypen som definerer det frigitte produktet:

    - **Viktig** – varen er en hovedkilde for en organisasjons inntekt. Denne verdien er standardinnstillingen.
    - **Uviktig** – varen er ikke en hovedkilde for en organisasjons inntekt. Når innstillingene for medianpris brukes, blir prisen "stipulert" til medianprisen og deretter tildelt. En viktig vare har for eksempel en fast pris som må føres for inntekten. Hvis det er en rabatt, kan rabatten være stipulert for den viktige vareinntekten, **men** bare til det faste prisbeløpet. Resten av rabatten trekkes ut av inntekten for uviktige varer. Ellers kan det hende at rabatten ikke er stipulert for den grunnleggende vareinntekten.
    - **Støtte etter kontrakt** – varen har støtte for andre elementer som er inkludert i salget til kunden. Inntektsprisen distribueres på tvers av de viktige og uviktige produktene som er inkludert i salget. Avhengig av konfigurasjonen kan det hende at PCS-varer ikke krever at start- og sluttdatoen for kontrakten defineres på salgsordrelinjen.

- **Utelat fra stipulering** – sett dette alternativet til **Ja** for å angi at varens medianpris ikke kan justeres under minimumsprosenten som er definert eller over maksimumsprosenten. Alle inntektspriser vil bli avledet fra inntektsprisen til et annet frigitt produkt som er inkludert på salgsordren. Hvis dette alternativet er satt til **Nei**, kan varens medianpris justeres eller stipuleres. Vær oppmerksom på at hvis du selger mer enn én vare som er definert som medianpris, må minst ett frigitt produkt defineres, der verdien for alternativet **Utelat fra stipulering** er satt til **Nei**. På denne måten finnes det minst én vare som det kan tildeles forskjeller til i inntektsprisen.
- **Medianpris** – sett dette alternativet til **Ja** for å angi at varens inntektspris skal justeres slik at den tilsvarer medianprisen hvis den er under minimumstoleransen som du angir, eller over maksimaltoleransen, og at stipuleringsbeløpet må fordeles på linjer som har produkter der verdien for alternativet **Utelat fra stipulering** er satt til **Nei**.

    - **Maksimumstoleranse** – angi prosentandelen over medianprisen som er tillatt.
    - **Minimumstoleranse** – angi prosentandelen under medianprisen som er tillatt.

Når du er ferdig med å konfigurere innstillingene for det frigitte produktet, må du definere inntektsprisen manuelt ved å registrere gjennomsnittsprisen eller medianprisen (hvis du bruker medianprismetoden) på siden **Inntektspriser** (gå til **Inntektsføring \> Oppsett \> Lageroppsett \> Frigitte produkter**, og velg deretter **Inntektspriser** i gruppen **Inntektsføring** i fanen **Selg** i handlingsruten).

[![Inntektspriser.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Inntektsprisen som er definert manuelt på denne siden, brukes til å bestemme inntektspristildelingen for hver salgsordre, basert på kriteriene som er definert. Hvert kriterium samsvarer med salgsordrelinjen for å bestemme inntektsprisen som skal brukes i tildelingsprosessen.

- **Varekode** og **Varerelasjon** – en inntektspris kan defineres for ett produkt eller en gruppe med produkter. Hvis du velger **Tabell** i feltet **Varekode**, velger du det frigitte produktet i feltet **Varerelasjon**. Hvis du velger **Gruppe** i feltet **Varekode**, velger du varegruppen i feltet **Varerelasjon**.
- **Kontokode** og **Konto-/gruppenummer** – en inntektspris kan defineres for alle kunder, en individuell kunde eller en gruppe av kunder. Hvis du velger **Alle** i feltet **Kontokode**, brukes prisen for alle kunder. Hvis du velger **Tabell** i feltet **Kontokode**, velger du kunden i feltet **Konto-/gruppenummer**. Hvis du velger **Gruppe** i feltet **Kontokode**, velger du kundegruppen i feltet **Konto-/gruppenummer**.
- **Valuta** – du må angi en egen inntektspris for hver valuta du angir en salgsordre i. Hvis du for eksempel selger i amerikanske dollar, kanadiske dollar og euro, må du definere en inntektspris i alle de tre valutaene. Inntektsprisen er ikke oversatt fra én valuta, for eksempel regnskapsvalutaen, til andre transaksjonsvalutaer du bruker.
- **Beløp eller prosent av liste** – angi om inntektsprisen er definert som et beløp eller som en prosent av listeprisen. Hvis du velger **Prosent av liste**, kan brukere angi medianprisen som en prosent av listeprisen i stedet for et beløp. Verdien for **Prosent av liste** brukes bare for frigitte produkter som er definert som PCS-varer.
- **Pris for inntektstildeling** – avhengig av verdien du valgte i feltet **Beløp eller prosent av liste**, angir du et beløp eller en prosent som skal representere inntektsprisen som brukes til å fordele inntekten på tvers av varene på salgsordren.
- **Fra-dato** og **Til-dato** – angi datointervallet som inntektsprisen er aktiv for. Disse feltene er valgfrie.

Hvis alternativet **Aktiver rabattildelingsmetode** på siden **Parametere for økonomimodul** er satt til **Ja**, og hvis feltet **Inntektstype** for det frigitte produktet er satt til **Støtte etter kontrakt**, må du også angi varene som støttes av det frigitte produktet. Dette oppsettet gjøres på siden **Oppsettsgrunnlag** (gå til **Inntektsføring \> Oppsett \> Lageroppsett \> Frigitte produkter**, og velg deretter **Oppsettsgrunnlag** i gruppen **Inntektsføring** i fanen **Selge** i handlingsruten).

På siden **Oppsettsgrunnlag** legger du til en post for hver vare gruppe som varen støtter. Når inntektstildelingen skjer, fordeles inntektsprisen på tvers av de grunnleggende og uviktige delene av PCS-varen.

### <a name="posting-profiles"></a>Posteringsprofiler

Tre ekstra posteringstyper støtter muligheten til å utsette inntekten. Disse posteringstypene defineres i fanen **Salgsordre** på siden **Postering** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Postering**).

- **Utsatt inntekt** – angi hovedkontoen for inntektsprisen som posterer til utsatt inntekt (i stedet for inntekt). Inntektsprisen utsettes hvis salgsordrelinjen har en inntektsplan.
- **Utsatt kost for solgte varer** – angi hovedkontoen for kostnadene for solgte varers beløp som posterer til utsatt kost for solgte varer hvis inntekten også utsettes.
- **Delvis avregning av fakturainntekt** – angi hovedkontoen for avregningskontoen som brukes når salgsordren er delvis fakturert eller når ny tildeling skjer. Saldoen i denne kontoen blir returnert til 0 (null) når salgsordrene er fullstendig fakturert.

### <a name="bundles"></a>Bunter

Buntvarer er unike frigitte produkter som er definert slik at de omfatter komponenter. Dette oppsettet utføres ved hjelp av stykklistefunksjonaliteten. Når en buntvare angis i en salgsordre, brukes enkelt komponentene til å bestemme inntektsprisene og inntektsplanene. Utskriftsdokumenter for kunden, for eksempel salgsordren og fakturaen, gjenspeiler imidlertid buntvaren.

#### <a name="bundle-components"></a>Buntkomponenter

Komponentene som er inkludert i bunten, må defineres på siden **Frigitte produkter** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Frigitte produkter**). Disse komponentene er frigitte produkter, og de må defineres på samme måte som produkter som er inkludert i en stykkliste. Et frigitt produkt kan for eksempel være en vare av typen **Vare** eller typen **Tjeneste**, men den må tilordnes en varemodellgruppe der alternativet **Lagerført produkt** er satt til **Ja**. Hvis du vil ha mer informasjon, kan du se dokumentasjonen for oppsett av stykklistevarer.

Komponentene må også være definert for inntektsføring, på samme måte som om de er produkter som kan selges enkeltvis i en salgsordre. Du kan for eksempel kontrollere at riktig inntektspris er definert for hver komponent, og at prisgrunnlaget skal defineres for PCS-varer.

#### <a name="bundle-items"></a>Buntvarer

Når du definerer en buntvare, må du angi en verdi i to felt på siden **Frigitte produkter** (**Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Frigitte produkter**):

- I hurtigfanen **Utvikle** i feltet **Produksjonstype** må du definere varen som en stykklistevare.
- I hurtigfanen **Generelt** i feltet **Bunt** må du merke av for vare som en buntvare.

Komponentene må deretter tilordnes til den overordnede varen for bunt/stykkliste på siden **Stykklisteversjoner** (gå til **Inntektsføring \> Oppsett \> Lager- og produktoppsett \> Frigitte produkter**, og klikk deretter **Stykklisteversjoner** i gruppen **Stykkliste** i fanen **Utvikle** i handlingsruten). Hvis du vil ha mer informasjon, kan du se dokumentasjonen for oppsett av stykklister.

[![Frigitte produkter, tidsplaner for stykkliste.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Hvis den overordnede vare- og pakke komponenten for bunt er satt til tildeling, blir inntektsprisen for bunten distribuert til komponentene, basert på prosentene for inntektsbidrag.

## <a name="project-setup"></a>Prosjektoppsett

Inntektsføring kan også brukes for salgsordrer som opprettes via et Etter regning-prosjekt. For salgsordrer som stammer fra prosjekter, må du bare definere hovedkontoene i prosjektposteringsprofilene som brukes til å postere prosjektfakturaer. Hovedkontoene er definert på siden **Finansposteringsoppsett** (**Inntektsføring \> Oppsett \> Prosjektoppsett \> Finansposteringsoppsett**).

- **Utsatt fakturainntekt** (under **Inntektskontoer**) – angi hovedkontoen for inntektsprisen som posterer til utsatt inntekt (i stedet for inntekt). Inntektsprisen utsettes hvis salgsordrelinjen har en inntektsplan.
- **Utsatt kostnad** (under **Kostnadskontoer**) – angi hovedkontoen for kostnadene for solgte varers beløp som posterer til utsatt kost for solgte varer hvis inntekten også utsettes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
