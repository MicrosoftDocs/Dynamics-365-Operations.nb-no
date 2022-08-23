---
title: Rutenettfunksjoner
description: Denne artikkelen beskriver flere kraftfulle funksjoner i rutenettkontrollen. Du må aktivere den nye rutenettfunksjonen for å kunne få tilgang til disse funksjonene.
author: jasongre
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a8968a1263dfafd67b07b4beb78c51493e95756e
ms.sourcegitcommit: 47534a943f87a9931066e28f5d59323776e6ac65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9258955"
---
# <a name="grid-capabilities"></a>Rutenettfunksjoner

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Den nye rutenettkontrollen byr på flere nyttige og kraftfulle funksjoner du kan bruke til å forbedre brukerproduktivitet, konstruere mer interessante visninger av dataene og få meningsfull innsikt i dataene. Denne artikkelen dekker følgende funksjoner: 

- Vis beregnede verdier 
- Skriving i forkant av systemet
- Evaluering av matematiske uttrykk 
- Grupperetabelldata (aktivert separat ved hjelp av funksjonen **Gruppering i rutenett**)
- Fryse kolonner (aktiveres separat ved hjelp av funksjonen **Frys kolonnene i rutenett**)
- Beste tilpassing av kolonnebredde
- Kolonnene som kan strekkes

## <a name="showing-calculated-values"></a>Vis beregnede verdier
I økonomi- og driftsapper kan brukere vise en beregnet verdi for hver numerisk kolonne i et rutenett. Disse beregnede verdiene vises i en bunntekstinndeling nederst i rutenettet.

[![Vis beregnede verdier i rutenett.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

I versjoner før 10.0.29 er totalen den eneste beregnede verdien som støttes. Brukere kan imidlertid velge blant følgende fire beregnede verdier etter at de har aktivert funksjonen **Utvidede rutenettaggregeringsfunksjoner** fra og med 10.0.29:

- Minimum
- Maksimum
- Totalsum
- Gjennomsnitt

En enkelt kolonne kan bare vise én type beregnet verdi. Hver kolonne i rutenettet kan imidlertid konfigureres til å vise en annen type beregnet verdi.

### <a name="showing-the-grid-footer"></a>Vise rutenettbunnteksten
Det er et bunntekstområde nederst i alle tabellrutenett i økonomi- og driftsapper. Bunnteksten kan vise nyttig informasjon som er knyttet til dataene som vises i rutenettet. Her er noen eksempler på denne informasjonen:

- Antallet valgte rader i tabellen (når du velger flere oppføringer)
- Beregnede verdier nederst i konfigurerte numeriske kolonner (f.eks. totalsummer)
- Antallet rader i datasettet 

Denne bunnteksten er skjult som standard, men du kan aktivere den. Hvis du vil vise bunnteksten for et rutenett, velger du **Alternativer for rutenett**-knappen i rutenettoverskriften og velger deretter **Vis bunntekst**-alternativet. Etter at du har aktivert bunnteksten for et bestemt rutenett, gjelder denne innstillingen til brukeren velger å skjule bunnteksten. Hvis du vil skjule bunnteksten, velger du **Skjul bunntekst** på menyen **Rutenettalternativer**.

### <a name="specifying-columns-with-calculated-values"></a>Angi kolonner med beregnede verdier
For øyeblikket viser ingen kolonner beregnede verdier som standard. I stedet betraktes oppsettet som en engangsaktivitet, som tilsvarer justering av bredden på kolonnene i rutenett. Når du har angitt at du vil se en beregnet verdi for en kolonne, vil denne innstillingen bli husket neste gang du besøker siden.

Det finnes to måter for å konfigurere en kolonne til å vise en beregnet verdi:

- Velg og hold (eller høyreklikk) i kolonnen du vil vise en beregnet verdi for. Hvis funksjonen **Utvidede rutenettaggregeringsfunksjoner** er aktivert, velger du **Vis kolonnetotaler**, og deretter velger du ønsket beregnet verdi. Hvis funksjonen ikke er aktivert, velger du **Summer denne kolonnen**. Denne handlingen fører til at tre hendelser skjer:

    1. Rutenettbunnteksten blir synlig. 
    2. Ønsket om å vise en beregnet verdi for kolonnen lagres. 
    3. Den ønskede beregningen startes for kolonnen og alle andre kolonner du tidligere konfigurerte til å vise en beregnet verdi. Hvor lang tid det tar å vise de beregnede verdiene, avhenger av størrelsen på datasettet du skal summere.

- Når bunnteksten er synlig, velger du **Vis total** (eller **Velg beregnet verdi** hvis funksjonen **Utvidede rutenettaggregeringsfunksjoner** er aktivert) i bunntekstområdet nederst i kolonnen som du vil vise en beregnet verdi for. Hvis det ikke finnes konfigurerte kolonner, er knappen tilgjengelig i bunnteksten i alle numeriske kolonner.

    Når minst én kolonne er konfigurert til å vise en beregnet verdi, vil knappen **Vis total** (eller **Velg beregnet verdi**) bare være tilgjengelig på hold over eller fokus. Handlingen ved å velge knappen bare lagrer innstillingen for å vise en beregnet verdi i kolonnen, slik at innstillingen brukes ved fremtidige besøk på siden. I bunnteksten angis denne statusen av en bindestrek som vises i kolonnen. (Legg merke til at den beregnede verdien vises umiddelbart hvis datasettet er lite nok.)

Hvis du gjør en feil og ikke vil vise en beregnet verdi i en bestemt kolonne, velger du og holder (eller høyreklikker) i kolonnen, og velger deretter **Skjul totalsummer** (eller **Vis kolonnetotaler \> Ingen** hvis funksjonen **Utvidede rutenettaggregeringsfunksjoner** er aktivert). Du kan også velge **Skjul totalsummen** (eller **Skjul beregnet verdi**) i bunnteksten i denne kolonnen. Denne innstillingen vil også bli lagret for fremtidige besøk på siden. 

### <a name="calculating-aggregate-values"></a>Beregn samleverdier
Når du går til en side der bunnteksten er synlig og kolonnene allerede er konfigurert til å vise beregnede verdier, kan det hende at disse verdiene ikke vises i bunnteksten. Atferden avhenger av størrelsen på datasettet på siden. Hvis datasettet er tilstrekkelig lite, vises beregnede verdier automatisk sammen med antallet rader i datasettet. Hvis det finnes streker i bunnteksten under kolonnene du har konfigurert, er datasettet for stort til at systemet kan vise beregnede verdier umiddelbart. I dette tilfellet kreves det en eksplisitt handling for å beregne verdiene. Hvis du vil beregne verdiene, velger du **Beregn**-knappen i bunnteksten. Du kan også velge og holde (eller høyreklikker) i en kolonne som du vil vise totalen for, og deretter velger du **Summer denne kolonnen** (eller **Vis kolonnetotaler** og ønsket beregnet verdi hvis funksjonen **Utvidede rutenettaggregeringsfunksjoner** er aktivert).

Hvis det tar lang tid å fullføre beregningen, kan du avbryte operasjonen ved å velge **Avbryt**-knappen når som helst. Noen ganger er datasettet for stort til å beregne mengdeverdier (en grense som finnes i organisasjonen). I så fall blir du varslet om dette for å filtrere dataene mer.

> [!NOTE]
> Systemadministratorer kan endre grensen for antall poster som er tilgjengelige for beregning av samlinger, ved å justere parameteren **Maksimalt antall lokale poster for hvert rutenett** på siden **Alternativer for klientytelse**. Standardverdien er 25 000 poster. Systemansvarlige må være forsiktige når de justerer denne verdien, fordi en verdi som er for stor, kan bruke opp det tilgjengelige minnet på maskinen til brukeren. Vi anbefaler at verdien ikke overskrider 50 000 poster.

Beregnede verdier oppdateres automatisk når du oppdaterer, sletter eller oppretter rader i datasettet.

## <a name="typing-ahead-of-the-system"></a>Skriving i forkant av systemet
I mange forretningsscenarier er muligheten til raskt å legge inn data i systemet svært viktig. Før innføringen av den nye rutenetrkontrollen, kunne brukere bare endre data i den gjeldende raden. Etter at de gjorde endringer i en rad, kunne brukerne derfor ikke bytte til en annen rad eller opprette en ny rad før systemet validerte endringene i den nåværende raden, og (i tilfelle radoppretting) kjørte all logikken som er knyttet til opprettingen av en ny rad. For å bidra til å redusere tiden som brukere bruker på vente på disse operasjonene skal fullføres, og for å bidra til å forbedre brukerproduktiviteten, justerer det nye handlingene slik at de er asynkrone. Brukere kan opprette nye rader eller flytte til andre rader for å gjøre endringer mens tidligere radvalideringer og radopprettingslogikk venter. 

[![Skriving i forkant av systemet.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

For å støtte denne nye virkemåten, er det lagt til en ny kolonne for radstatusen til høyre for radvelgerkolonnen når rutenettet er i redigeringsmodus. Denne kolonnen angir én av følgende statuser:

- **Tom** – ingen statusbilde angir at raden er lagret i systemet.
- **Behandling venter** – denne statusen angir at endringene i raden ikke er lagret på serveren ennå, men er i en kø av endringer som må behandles. Før du utfører handlinger utenfor rutenettet, må du vente på at alle ventende endringer skal behandles. I tillegg er teksten i disse radene i kursiv for å angi den ulagrede statusen for radene. 
- **Ugyldig tilstand** – denne statusen angir at en advarsel eller melding ble utløst under behandlingen av raden, og den kan ha forhindret systemet fra å lagre endringene i den raden. I det gamle rutenettet måtte du gå tilbake til raden for å løse problemet umiddelbart dersom lagringsoperasjonen mislyktes. I det nye rutenettet blir du imidlertid varslet om at det ble funnet et valideringsproblem, men du kan bestemme når du vil rette opp eventuelle problemer i raden. Når du er klar til å løse et problem, kan du flytte fokus tilbake til raden manuelt. Du kan også velge handlingen **Løs dette problemet**. Denne handlingen flytter umiddelbart fokus tilbake til raden som har problemet, og gjør det mulig å redigere i eller utenfor rutenettet. Legg merke til at behandlingen av påfølgende ventende rader blir stoppet til denne valideringsadvarselen blir løst. 
- **Midlertidig stanset** – denne statusen angir at behandlingen av serveren er stoppet midlertidig fordi valideringen av raden utløste en popup-dialogboks som krever inndata fra brukeren. Fordi brukeren kan registrere data i en annen rad, blir hurtigdialogboksen ikke umiddelbart presentert for denne brukeren. Den vil i stedet presenteres når brukeren velger å gjenoppta behandlingen. Denne statusen følges av et varsel som informerer brukeren om situasjonen. Varslingen inneholder en **Gjenoppta behandling**-handling som vil utløse hurtigdialogboksen.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Forskjeller når data registreres før systemet
Når du angir data før stedet der systemet behandler, kan du forvente noen endringer i dataoppføringserfaringen:

- Du vil se at det ikke finnes noen oppslagsrullegardinlistene, feltverdier som ikke er validert etter at du har flyttet til en annen kolonne i samme rad, og kolonnene viser ikke standardverdier i utgangspunktet. Dette skjer når du oppretter eller oppdaterer før systemet. Etter at systemet har tatt seg opp til det stedet du redigerer for øyeblikket, vil imidlertid standarderfaringen fortsette. Hvis du gjorde endringer i et felt som vanligvis mottar en standardverdi, overstyrer endringene den standard feltverdien når serveren begynner å behandle raden.
- Hvis du oppretter en ny rad ved å bruke **Pil ned**, vises alle kolonnene i rutenettet som redigerbare. Som standard blir fokuset plassert i første kolonne i den nye raden. Denne kolonnen er kanskje ikke den samme kolonnen som mottok første fokus i den eldre rutenettet, eller den samme kolonnen som får fokus etter at du velger en **Ny**-knapp. Organisasjonen kan tilpasse systemet og endre kolonnen som får det innledende fokuset når tasten **Pil ned** velges. Hvis du vil ha mer informasjon , kan du se [Angi kolonnen som skal motta det innledende fokuset når nye rader opprettes, ved å bruke pil ned](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key)-delen. Uansett kan du bruke tilpasningen til å optimalisere hvert rutenett for dataregistrering. Mer bestemt kan du endre rekkefølgen på feltene slik at den første kolonnen er den kolonnen du vil begynne å angi data i. Det kan også være at du ønsker å endre rekkefølge på felter for dataregistrering for å redusere kategoristopper og skjule felter som ikke er nødvendige for dataregistrering i denne bestemte visningen.

### <a name="pasting-from-excel"></a>Lime inn fra Excel
Brukere har alltid hatt muligheten til å eksportere data fra rutenett i økonomi- og driftsapper til Microsoft Excel ved hjelp av funksjonen **Eksporter til Excel**. Muligheten til å angi data før systemet gjør imidlertid at det nye rutenettet kan støtte kopiering av tabeller fra Excel og lime dem direkte inn i rutenett i økonomi- og driftsapper. Rutenettcellen som innlimingen startes fra, bestemmer hvor den kopierte tabellen begynner å limes inn. Innholdet i rutenettet overskrives av innholdet i den kopierte tabellen, med unntak av to tilfeller:

- Hvis antallet kolonner i den kopierte tabellen overskrider antall kolonner som beholdes i rutenettet, med start fra innlimingen, varsles brukeren om at de ekstra kolonnene er ignorert. 
- Hvis antall rader i den kopierte tabellen overskrider antall rader i rutenettet, med start fra innlimingen, blir de eksisterende cellene overskrevet av det innlimte innholdet, og eventuelle ekstra rader fra den kopierte tabellen blir satt inn som nye rader nederst i rutenettet. 

## <a name="evaluating-math-expressions"></a>Evaluering av matematiske uttrykk
Som en produktivitetsforsterkning kan brukeren legge inn matematiske formler i numeriske celler i et rutenett. De trenger ikke å utføre beregningen i en app utenfor systemet. Hvis du for eksempel angir **=15\*4** og deretter trykker på **Tab**-tasten for å gå ut av feltet, evaluerer systemet uttrykket og lagrer verdien **60** for feltet.

[![Evaluering av matematiske uttrykk.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Hvis du vil at systemet skal gjenkjenne en verdi som et uttrykk, starter du verdien med et likhetstegn (**=**). Hvis du vil ha mer informasjon om de støttede operatorene og syntaksen, kan du se [Støttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Per versjon 10.0.29 er muligheten til å evaluere flere uttrykk i numeriske kontroller utvidet, og er nå tilgjengelig utenfor rutenettet også.

## <a name="grouping-tabular-data"></a>Gruppere tabelldata
Bedriftsbrukere må ofte utføre ad hoc-analyse av data. Selv om denne analysen kan utføres ved å eksportere data til Microsoft Excel og bruke pivottabeller, gjør funksjonen **Gruppering i rutenett**, som er avhengig av den nye rutenettkontrollfunksjonen, det mulig for brukere å organisere sine tabelldata på interessante måter i økonomi- og driftsapper. Ettersom denne funksjonen utvider **Beregnede verdier**-funksjonen, gjør **Gruppering** det mulig å få meningsfulle innsikter i dataene ved å gi beregnede verdier (f.eks. subtotalverdier) på gruppenivå.

[![Gruppere data i et rutenett.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Hvis du vil bruke denne funksjonen, høyreklikker du kolonnen du vil gruppere etter, og velger **Grupper etter denne kolonnen**. Denne handlingen sorterer dataene etter den valgte kolonnen, legger til en ny **Grupper etter**-kolonne i begynnelsen av rutenettet og setter inn "topptekstrader" i begynnelsen av hver gruppe. Disse topptekstradene inneholder følgende informasjon om hver gruppe:

- Dataverdi for gruppen 
- Kolonnenavn (denne informasjonen er spesielt nyttig når du har grupperinger på flere nivåer)
- Antallet datarader i denne gruppen
- Beregnede verdier for en hvilken som helst konfigurert kolonne (f.eks. delsummer hvis kolonnen er konfigurert til å vise en total)

Når [Lagrede visninger](saved-views.md) er aktivert, kan du lagre gruppering som en del av en visning på sider som gjør det mulig å lagre spørringer i visninger. For eksempel de med store visningsvelgere. Se delen [Bytt mellom visninger](saved-views.md#switching-between-views) for mer informasjon. 

### <a name="multiple-levels-of-grouping"></a>Flere nivåer med gruppering
Når du har gruppert data etter én enkelt kolonne, kan du gruppere dataene etter en annen kolonne ved å velge **Grupper etter denne kolonnen** på ønsket kolonne. Denne prosessen kan gjentas til du har 5 nestede nivåer av gruppering, som er den maksimale dybden som støttes. På dette stadiet vil du ikke lenger kunne gruppere etter flere kolonner.

Du kan når som helst fjerne grupperingen på en kolonne ved å høyreklikke denne kolonnen og velge **Del opp gruppe**. Du kan også fjerne grupperingen fra alle kolonnene ved å velge **Alternativer for rutenett** og deretter velge **Del opp alle grupper**.

### <a name="sorting-grouped-data"></a>Sortere grupperte data
Når du har gruppert data etter en eller flere kolonner, kan du endre sorteringsretningen for en hvilken som helst grupperingskolonne via den tilsvarende kolonneoverskriften. 

Hvis du sorterer i en kolonne som ikke er gruppert, forblir grupperingen intakt. Dataene sorteres i hver gruppe, basert på den valgte kolonnen.

### <a name="expanding-and-collapsing-groups"></a>Vise og skjule grupper
Den innledende grupperingen av data vil få alle grupper vist. Du kan opprette sammendragsvisninger av dataene ved å skjule enkeltstående grupper, eller du kan bruke gruppevisning og -skjuling for å hjelpe til med å navigere gjennom dataene. Hvis du vil vise eller skjule en gruppe, velger du knappen med vinkeltegnet (>) i den tilsvarende topptekstraden for gruppe. Legg merke til at vis/skjul-statusen til enkelt grupper **ikke** lagres i tilpassing.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Merke og oppheve merking av rader på gruppenivå
På samme måte som du kan merke (eller oppheve) alle radene i rutenettet ved å merke av øverst i den første kolonnen i rutenettet, kan du også raskt merke av for (eller oppheve merking) for alle radene i en gruppe ved å merke av i den tilsvarende topptekstraden for gruppe. Avmerkingsboksen i topptekstraden for gruppe vil alltid gjenspeile den gjeldende valgstatusen for rader i denne gruppen, uavhengig av om alle rader er merket, ingen rader er merket, eller bare enkelte rader er merket.

### <a name="hiding-column-names"></a>Skjule kolonnenavn
Når du grupperer data, er standard virkemåte å vise kolonnenavnet i topptekstraden for gruppe. Du kan velge å skjule kolonnenavnet i topptekstrader for gruppe ved å velge **Alternativer for rutenett** > **Skjul gruppekolonnenavn**.

### <a name="grouping-on-date-and-time-columns"></a>Gruppere etter dato- og klokkeslettkolonner
Når du grupperer på Dato- eller DateTime-felter har du alternativet om gruppere etter år, måned eller dag. Gruppens verdi i den tilsvarende overskriftsraden vil samsvare med formatet fra dette feltet. I tillegg kan du for DateTime- og Klokkeslett-feltene gruppere etter time, minutt eller sekund.

> [!IMPORTANT]
> Brukere kan ikke legge til en grupperingskolonne etter at de har gruppert på et segment av en dato- eller klokkeslettkolonne.

## <a name="freezing-columns"></a>Låse kolonner
Noen kolonner i et rutenett kan så viktige for konteksten at du ikke vil at de kan rulle ut av visningen. Du vil i stedet kanskje at verdiene i disse kolonnene alltid vises. Med funksjonen **Frys kolonnene i rutenett** får brukerne denne fleksibiliteten. 

[![Låsing av kolonner i et rutenett.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Du låser en kolonne ved å høyreklikke på kolonneoverskriften og deretter velge **Lås kolonne**. Første gang du fullfører dette trinnet, blir den valgte kolonnen den første kolonnen og ruller ikke lenger ut av visningen. Alle påfølgende kolonner du låser, blir lagt til til høyre for den sist låste kolonnen. Du kan bruke standardfunksjonen for flytting til å endre rekkefølgen på låste kolonner etter behov. Låste kolonner kan imidlertid ikke flyttes slik at de vises blant settet med ulåste kolonner. Ulåste kolonner kan likeledes ikke flyttes slik at de vises blant settet med låste kolonner.

Du låser opp en kolonne ved å høyreklikke på den låste kolonneoverskriften og deretter velge **Lås opp kolonne**. 

Merk at kolonnen for radvalg og radstatus i det nye rutenettet alltid låses som de to første kolonnene. Når disse kolonnene tas med i et rutenett, er de derfor alltid synlige for brukere, uavhengig av den vannrette rulleplasseringen i rutenettet. Du kan ikke endre rekkefølgen på disse to kolonnene.

## <a name="autofit-column-width"></a>Beste tilpassing av kolonnebredde
Som i Excel kan brukere tvinge en kolonne til å endre størrelse automatisk basert på innholdet som vises i den. Du kan bare dobbelttrykke (eller dobbeltklikke) størrelseshåndtakene i kolonnen. Du kan også plassere fokuset i kolonnehodet, og deretter velge **A**-tasten (for autotilpasning).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg den nye rutenettkontrollen i miljøet? 

Funksjonen **Ny rutenettkontroll** er tilgjengelig direkte i funksjonsbehandling i et hvilket som helst miljø. Når funksjonen er aktivert i Funksjonsstyring, vil alle etterfølgende brukerøkter bruke den nye rutenettkontrollen. 

Denne funksjonen begynte å bli aktivert som standard i versjon 10.0.21. Den har som mål å bli obligatorisk i oktober 2022.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Utvikler] Velge bort enkeltsider fra å bruke det nye rutenettet 
Hvis organisasjonen oppdager en side der det er noen problemer med å bruke det nye rut nettet, er det tilgjengelig et API for å tillate at et enkelt skjema bruker den gamle rutenettkontrollen samtidig som resten av systemet brukes til å utnytte den nye rutenettkontrollen. Hvis du vil velge bort en enkelt side fra det nye rutenettet, legger du til følgende oppkallspost `super()` i skjemaets `run()`-metode.

```this.forceLegacyGrid();```

Denne API-en vil til slutt bli avskrevet for å tillate fjerning av den eldre rutenettkontrollen. Den vil imidlertid fortsatt være tilgjengelig i minst 12 måneder etter at den har blitt nedskrevet. Hvis problemer gjør at denne APIen brukes, rapporterer du dem til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Tvinge en side til å bruke det nye rutenettet etter tidligere å ha valgt bort rutenettet
Hvis du har valgt bort en enkeltside fra å bruke det nye rutenettet, kan det hende at du senere vil aktivere det nye rutenettet på nytt etter at de underliggende problemene ble løst. For å gjøre dette må du ganske enkelt fjerne oppkallet til `forceLegacyGrid()`. Endringen trer ikke i kraft før et av følgende skjer:

- **Ny distribusjon av miljø**: Når et miljø oppdateres og distribueres på nytt, tømmes automatisk tabellen som lagrer sidene som har valgt det nye rutenettet (FormControlReactGridState).
- **Manuell fjerning av tabellen**: I utviklingsscenarier må du bruke SQL for å fjerne FormControlReactGridState-tabellen og deretter starte AOS på nytt. Denne kombinasjonen av handlinger tilbakestiller hurtigbufring av sider som ikke er valgt for det nye rutenettet.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Utvikler] Velge bort rutenett fra funksjonen Skriving i forkant av systemet
Det har oppstått enkelte scenarioer som ikke fungerer bra sammen med funksjonen *Skriving i forkant av systemet* i rutenettet. (Noen typer kode som for eksempel utløses når en rad valideres, fører til at en datakildeundersøkelse utløses, og undersøkelsen kan deretter ødelegge ikke-fordelte endringer på eksisterende rader.) Hvis organisasjonen oppdager et slikt scenario, er en API tilgjengelig som gjør det mulig for en utvikler å velge bort et individuelt rutenett fra asynkron radvalidering og gå tilbake til den eldre virkemåten.

Når asynkron radvalidering deaktiveres i et rutenett, kan brukere ikke opprette en ny rad eller flytte til en annen eksisterende rad i rutenettet mens det er valideringsproblemer i gjeldende rad. Som en sideeffekt av denne handlingen kan du ikke lime inn tabeller fra Excel i økonomi- og driftsrutenett.

Hvis du vil velge bort ett enkelt rutenett fra asynkron radvalidering, legger du til følgende oppkall etter `super()` i skjemaets `run()`-metode.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Dette kallet bør bare aktiveres i spesielle tilfeller, og skal ikke være normen for alle rutenett.
> - Vi anbefaler ikke at du veksler denne API-en ved kjøretid etter at skjemaet lastes.

## <a name="developer-size-to-available-width-columns"></a>[Utvikler] Skaler-til-tilgjengelig-bredde-kolonner
Hvis en utvikler setter egenskapen **WidthMode** til **SizeToAvailable** for kolonner i det nye rutenettet, har disse kolonnene i utgangspunktet samme bredde som de ville ha hvis egenskapen ble satt til **SizeToContent**. De kan imidlertid strekke seg for å bruke en eventuell ekstra tilgjengelig bredde i rutenettet. Hvis egenskapen er satt til **SizeToAvailable** for flere kolonner, deler alle disse kolonnene tilgjengelig ekstra bredde i rutenettet. Hvis en bruker imidlertid endrer størrelsen på en av disse kolonnene manuelt, blir kolonnen statisk. Den blir stående i denne bredden, og strekker seg ikke lenger til å bruke ekstra tilgjengelig rutenettbredde.

## <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Utvikler] Angi kolonnen som skal motta det innledende fokuset når nye rader opprettes, ved å bruke pil ned
Som det ble omtalt i [Forskjellene ved angivelse av data før system](#differences-when-entering-data-ahead-of-the-system)-delen, hvis funksjonen Skriv inn før systemet, og en bruker oppretter en ny rad ved hjelp av **Pil ned**, er standardvalget å sette fokuset i den første kolonnen i den nye raden. Denne opplevelsen kan være forskjellig fra erfaringen i den eldre rutenettet, eller når en **Ny**-knapp velges.

Brukere og organisasjoner kan opprette lagrede visninger som er optimert for dataregistrering. (Du kan for eksempel endre rekkefølge på kolonner slik at den første kolonnen er den du vil begynne å angi data i.) I tillegg kan organisasjoner justere dette problemet ved hjelp av den valgte **selectedControlOnCreate()**-metoden fra versjon 10.0.29. Med denne moten kan en utvikler angi kolonnen som skal motta det innledende fokuset når en ny rad opprettes, ved å bruke **Pil ned**-tasten. Som inndata tar denne API kontroll-ID-en som samsvarer med kolonnen som skal motta det innledende fokuset.

## <a name="known-issues"></a>Kjente problemer
Denne delen viser en liste over kjente problemer for den nye rutenettkontrollen.

### <a name="open-issues"></a>Åpne problemer
- Når du har aktivert funksjonen **Ny rutenettkontroll**, vil noen sider fortsette å bruke den eksisterende rutenettkontrollen. Dette vil skje i følgende situasjoner:
 
    - Det finnes en kortliste på siden som gjengis i flere kolonner.
    - Det finnes en gruppert kortliste på siden.
    - En rutenettkolonne med en ikke-reagerende utvidbar kontroll.

    Når en bruker først støter på én av disse situasjonene, vil det vises en melding om oppdatering av siden. Når denne meldingen vises, vil siden fortsette å bruke det eksisterende rutenettet for alle brukere til neste oppdatering av produktversjonen. Bedre behandling av disse scenariene, slik at det nye rutenettet kan brukes, vurderes for en fremtidig oppdatering.

- [KB 4582758] Poster er utydelige når du endrer zooming fra 100 til en annen prosent

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

