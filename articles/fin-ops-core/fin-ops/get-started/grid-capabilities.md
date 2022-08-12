---
title: Rutenettfunksjoner
description: Denne artikkelen beskriver flere kraftfulle funksjoner i rutenettkontrollen. Du må aktivere den nye rutenettfunksjonen for å kunne få tilgang til disse funksjonene.
author: jasongre
ms.date: 04/25/2022
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
ms.openlocfilehash: 07791afb2de670a5b9b910e441395c2949460394
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124718"
---
# <a name="grid-capabilities"></a>Rutenettfunksjoner

[!include [banner](../includes/banner.md)]

Den nye rutenettkontrollen byr på flere nyttige og kraftfulle funksjoner du kan bruke til å forbedre brukerproduktivitet, konstruere mer interessante visninger av dataene og få meningsfull innsikt i dataene. Denne artikkelen dekker følgende funksjoner: 

- Beregner totaler
- Skriving i forkant av systemet
- Evaluering av matematiske uttrykk 
- Grupperetabelldata (aktivert separat ved hjelp av funksjonen **Gruppering i rutenett**)
- Fryse kolonner (aktiveres separat ved hjelp av funksjonen **Frys kolonnene i rutenett**)
- Beste tilpassing av kolonnebredde
- Kolonnene som kan strekkes

## <a name="calculating-totals"></a>Beregner totaler
I økonomi- og driftsapper har brukere muligheten til å se totalverdier nederst i numeriske kolonner i rutenett. Disse totalverdiene vises i en bunntekstinndeling nederst i rutenettet. 

### <a name="showing-the-grid-footer"></a>Vise rutenettbunnteksten
Det er et bunntekstområde nederst i alle tabellrutenett i økonomi- og driftsapper. Bunnteksten kan vise nyttig informasjon som er knyttet til dataene som vises i rutenettet. Her er noen eksempler på denne informasjonen:

- Antallet valgte rader i tabellen (når du velger flere oppføringer)
- Hovedsummer nederst i konfigurerte numeriske kolonner
- Antallet rader i datasettet 

Denne bunnteksten er skjult som standard, men du kan aktivere den. Hvis du vil vise bunnteksten for et rutenett, velger du **Alternativer for rutenett**-knappen i rutenettoverskriften og velger deretter **Vis bunntekst**-alternativet. Etter at du har aktivert bunnteksten for et bestemt rutenett, gjelder denne innstillingen til brukeren velger å skjule bunnteksten. Hvis du vil skjule bunnteksten, velger du **Skjul bunntekst** på menyen **Rutenettalternativer**.

### <a name="specifying-columns-with-totals"></a>Angi kolonner med totalverdier
For øyeblikket viser ingen kolonner totaler som standard. I stedet betraktes dette som en engangsoppsettsaktivitet, som tilsvarer justering av bredden på kolonnene i rutenett. Når du har angitt at du vil se totalverdier for en kolonne, vil denne innstillingen bli husket neste gang du besøker siden.

Det finnes to måter for å konfigurere en kolonne til å vise en totalverdi: 

- Høyreklikk i kolonnen du vil se en totalverdi for, og velg deretter **Summer denne kolonnen**. Denne handlingen fører til at tre hendelser skjer:

    1. Bunnteksten blir synlig. 
    2. Preferansene dine for å se totalverdien for denne kolonnen lagres. 
    3. En beregning av totalverdier startes for denne kolonnen og alle andre kolonner du tidligere konfigurerte til å se totalverdier for. Hvor lang tid det tar å vise en totalverdi, avhenger av størrelsen på datasettet du skal summere.

- Når bunnteksten er synlig, velger du **Vis totalverdi** i bunntekstområdet nederst i kolonnen som du vil vise en totalverdi for. Hvis det ikke finnes konfigurerte kolonner, vil **Vis totalverdi**-knappen være tilgjengelig for alle numeriske kolonner. 

    Når minst én kolonne er konfigurert for totalverdier, vil **Vis totalverdi**-knappene bare være tilgjengelige ved peking eller fokus. Handlingen ved å velge **Vis totalverdi** bare lagrer innstillingen for å vise en totalverdi i denne kolonnen, slik at innstillingen brukes ved fremtidige besøk på siden. I bunnteksten angis denne statusen av en bindestrek som vises i kolonnen. (Hvis datasettet er lite nok, vises også en totalverdi umiddelbart.)

Hvis du gjør en feil og ikke lenger ønsker å se en totalverdi i en bestemt kolonne, høyreklikker du på kolonnen og velger **Skjul totalverdi** eller velger **Skjul totalverdi**-knappen i bunnteksten i denne kolonnen. Denne innstillingen vil også bli lagret for fremtidige besøk på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side der bunnteksten er synlig og kolonnene allerede er konfigurert for totalverdier, kan det hende at totalverdiene ikke vises i bunnteksten. Atferden avhenger av størrelsen på datasettet på siden. Hvis datasettet er tilstrekkelig lite, vises totalverdiene automatisk sammen med antallet rader i datasettet. Hvis det finnes streker i bunnteksten under kolonnene du har konfigurert for totalverdier, er datasettet for stort til at systemet kan vise totalverdier umiddelbart, og en eksplisitt handling er nødvendig for å beregne totalverdiene. Hvis du vil gjøre dette, klikker du på **Beregn**-knappen i bunnteksten, eller høyreklikker på en kolonne du vil ha totalverdi for, og velger **Summer denne kolonnen**.

Hvis det tar lang tid å fullføre beregningen, kan du avbryte operasjonen ved å velge **Avbryt**-knappen. Noen ganger er datasettet for stort til at totalverdier (en grense som pålegges av organisasjonen) kan beregnes, og du får i stedet et varsel om at dataene må filtreres mer. 

> [!NOTE]
> Systemansvarlige kan endre grensen for antall poster som er tilgjengelige for beregning av totaler, ved å justere parameteren **Maksimalt antall lokale poster for hvert rutenett** på siden **Alternativer for klientytelse**. Standardverdien er 25 000 poster. Systemansvarlige må være forsiktige når de justerer denne verdien, fordi en verdi som er for stor, kan bruke opp det tilgjengelige minnet på maskinen til brukeren. Vi anbefaler at 50 000 poster ikke overskrides.   

Totalverdier oppdateres automatisk når du oppdaterer, sletter eller oppretter rader i datasettet.

## <a name="typing-ahead-of-the-system"></a>Skriving i forkant av systemet
I mange forretningsscenarier er muligheten til raskt å legge inn data i systemet svært viktig. Før den nye rutenetrkontrollen ble innført, kunne brukere bare endre data i den gjeldende raden. Før de kunne opprette en ny rad eller bytte til en annen rad, ble de tvunget til å vente på at systemet skal validere eventuelle endringer. I et forsøk på å redusere tiden som brukere venter på at disse valideringene skal fullføres, og for å forbedre brukerproduktiviteten, justerer det nye rutenettet disse valideringene slik at de er asynkrone. Derfor kan brukeren flytte til andre rader for å gjøre endringer mens tidligere radvalideringer venter. 

For å støtte denne nye virkemåten, er det lagt til en ny kolonne for radstatusen til høyre for radvelgerkolonnen når rutenettet er i redigeringsmodus. Denne kolonnen angir én av følgende statuser:

- **Tom** – ingen statusbilde angir at raden er lagret i systemet.
- **Behandling venter** – denne statusen angir at endringene i raden ikke er lagret på serveren ennå, men er i en kø av endringer som må behandles. Før du utfører handlinger utenfor rutenettet, må du vente på at alle ventende endringer skal behandles. I tillegg er teksten i disse radene i kursiv for å angi den ulagrede statusen for radene. 
- **Ugyldig tilstand** – denne statusen angir at en advarsel eller melding ble utløst under behandlingen av raden, og den kan ha forhindret systemet fra å lagre endringene i den raden. I det gamle rutenettet måtte du gå tilbake til raden for å løse problemet umiddelbart dersom lagringsoperasjonen mislyktes. I det nye rutenettet blir du imidlertid varslet om at det ble funnet et valideringsproblem, men du kan bestemme når du vil rette opp eventuelle problemer i raden. Når du er klar til å løse et problem, kan du flytte fokus tilbake til raden manuelt. Du kan også velge handlingen **Løs dette problemet**. Denne handlingen flytter umiddelbart fokus tilbake til raden som har problemet, og gjør det mulig å redigere i eller utenfor rutenettet. Legg merke til at behandlingen av påfølgende ventende rader blir stoppet til denne valideringsadvarselen blir løst. 
- **Midlertidig stanset** – denne statusen angir at behandlingen av serveren er stoppet midlertidig fordi valideringen av raden utløste en popup-dialogboks som krever inndata fra brukeren. Fordi brukeren kan registrere data i en annen rad, blir hurtigdialogboksen ikke umiddelbart presentert for denne brukeren. Den vil i stedet presenteres når brukeren velger å gjenoppta behandlingen. Denne statusen følges av et varsel som informerer brukeren om situasjonen. Varslingen inneholder en **Gjenoppta behandling**-handling som vil utløse hurtigdialogboksen.

Når brukere angir data før serveren behandles, kan de forvente seg noen reduksjoner i dataregistreringsopplevelsen, for eksempel mangel på oppslag, validering på kontrollnivå og oppføring av standardverdier. Brukere som trenger en rullegardinliste for å finne en verdi, oppfordres til å vente til serveren blir oppdatert til gjeldende rad. Kontrollnivå-validering og registrering av standardverdier vil også forekomme når serveren behandler denne raden.

### <a name="pasting-from-excel"></a>Lime inn fra Excel
Brukere har alltid hatt muligheten til å eksportere data fra rutenett i økonomi- og driftsapper til Microsoft Excel ved hjelp av funksjonen **Eksporter til Excel**. Muligheten til å angi data før systemet gjør imidlertid at det nye rutenettet kan støtte kopiering av tabeller fra Excel og lime dem direkte inn i rutenett i økonomi- og driftsapper. Rutenettcellen som innlimingen startes fra, bestemmer hvor den kopierte tabellen begynner å limes inn. Innholdet i rutenettet overskrives av innholdet i den kopierte tabellen, med unntak av to tilfeller:

- Hvis antallet kolonner i den kopierte tabellen overskrider antall kolonner som beholdes i rutenettet, med start fra innlimingen, varsles brukeren om at de ekstra kolonnene er ignorert. 
- Hvis antall rader i den kopierte tabellen overskrider antall rader i rutenettet, med start fra innlimingen, blir de eksisterende cellene overskrevet av det innlimte innholdet, og eventuelle ekstra rader fra den kopierte tabellen blir satt inn som nye rader nederst i rutenettet. 

## <a name="evaluating-math-expressions"></a>Evaluering av matematiske uttrykk
Som en produktivitetsforsterkning kan brukeren legge inn matematiske formler i numeriske celler i et rutenett. De trenger ikke å utføre beregningen i en app utenfor systemet. Hvis du for eksempel angir **=15\*4** og deretter trykker på **Tab**-tasten for å gå ut av feltet, evaluerer systemet uttrykket og lagrer verdien **60** for feltet.

Hvis du vil at systemet skal gjenkjenne en verdi som et uttrykk, starter du verdien med et likhetstegn (**=**). Hvis du vil ha mer informasjon om de støttede operatorene og syntaksen, kan du se [Støttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppere tabelldata
Bedriftsbrukere må ofte utføre ad hoc-analyse av data. Selv om dette kan utføres ved å eksportere data til Microsoft Excel og bruke pivottabeller, gjør funksjonen **Gruppering i rutenett**, som er avhengig av den nye rutenettkontrollfunksjonen, det mulig for brukere å organisere sine tabelldata på interessante måter i økonomi- og driftsapper. Ettersom denne funksjonen utvider **Totalverdier**-funksjonen, gjør **Gruppering** det mulig å få meningsfulle innsikter i dataene takket være oppgivelse av subtotalverdier på gruppenivå.

Hvis du vil bruke denne funksjonen, høyreklikker du kolonnen du vil gruppere etter, og velger **Grupper etter denne kolonnen**. Denne handlingen sorterer dataene etter den valgte kolonnen, legger til en ny **Grupper etter**-kolonne i begynnelsen av rutenettet og setter inn "topptekstrader" i begynnelsen av hver gruppe. Disse topptekstradene inneholder følgende informasjon om hver gruppe:

- Dataverdi for gruppen 
- Kolonnenavn (denne informasjonen er spesielt nyttig når du har grupperinger på flere nivåer)
- Antallet datarader i denne gruppen
- Subtotalverdier for enhver kolonne som er konfigurert for å vise totalverdier

Når [Lagrede visninger](saved-views.md) er aktivert, kan du lagre gruppering som en del av en visning på sider som gjør det mulig å lagre spørringer i visninger. For eksempel de med store visningsvelgere. Se delen [Bytt mellom visninger](saved-views.md#switching-between-views) for mer informasjon. 

### <a name="multiple-levels-of-grouping"></a>Flere nivåer med gruppering
Når du har gruppert data etter én enkelt kolonne, kan du gruppere dataene etter en annen kolonne ved å velge **Grupper etter denne kolonnen** på ønsket kolonne. Denne prosessen kan gjentas til du har 5 nestede nivåer av gruppering, som er den maksimale dybden som støttes. På dette stadiet vil du ikke lenger kunne gruppere etter flere kolonner.

Du kan når som helst fjerne grupperingen på en kolonne ved å høyreklikke denne kolonnen og velge **Del opp gruppe**. Du kan også fjerne grupperingen fra alle kolonnene ved å velge **Alternativer for rutenett** og deretter velge **Del opp alle grupper**.

### <a name="sorting-grouped-data"></a>Sortere grupperte data
Når du har gruppert data etter en eller flere kolonner, kan du endre sorteringsretningen for en hvilken som helst grupperingskolonne via den tilsvarende kolonneoverskriften. 

Virkemåten når du sorterer på kolonner som ikke er gruppert, er avhengig av produktversjonen:

- I versjon 10.0.24 og tidligere, hvis du sorterer i en kolonne som ikke er gruppert, fjernes grupperingen fra alle kolonner, og dataene sorteres i den valgte kolonnen. 
- I versjon 10.0.25 og senere, hvis du sorterer i en kolonne som ikke er gruppert, forblir grupperingen intakt, og dataene sorteres internt i hver gruppe, basert på den valgte kolonnen.

### <a name="expanding-and-collapsing-groups"></a>Vise og skjule grupper
Den innledende grupperingen av data vil få alle grupper vist. Du kan opprette sammendragsvisninger av dataene ved å skjule enkeltstående grupper, eller du kan bruke gruppevisning og -skjuling for å hjelpe til med å navigere gjennom dataene. Hvis du vil vise eller skjule en gruppe, velger du knappen med vinkeltegnet (>) i den tilsvarende topptekstraden for gruppe. Legg merke til at vis/skjul-statusen til enkelt grupper **ikke** lagres i tilpassing.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Merke og oppheve merking av rader på gruppenivå
På samme måte som du kan merke (eller oppheve) alle radene i rutenettet ved å merke av øverst i den første kolonnen i rutenettet, kan du også raskt merke av for (eller oppheve merking) for alle radene i en gruppe ved å merke av i den tilsvarende topptekstraden for gruppe. Avmerkingsboksen i topptekstraden for gruppe vil alltid gjenspeile den gjeldende valgstatusen for rader i denne gruppen, uavhengig av om alle rader er merket, ingen rader er merket, eller bare enkelte rader er merket.

### <a name="hiding-column-names"></a>Skjule kolonnenavn
Når du grupperer data, er standard virkemåte å vise kolonnenavnet i topptekstraden for gruppe. Du kan velge å skjule kolonnenavnet i topptekstrader for gruppe ved å velge **Alternativer for rutenett** > **Skjul gruppekolonnenavn**.

### <a name="grouping-on-date-and-time-columns"></a>Gruppere etter dato- og klokkeslettkolonner
Fra og med versjon 10.0.24, er det for Dato- eller DateTime-felt lagt til et alternativet for å gruppere etter år, måned eller dag. Gruppens verdi i den tilsvarende overskriftsraden vil samsvare med formatet fra dette feltet. I tillegg kan du for DateTime- og Klokkeslett-feltene gruppere etter time, minutt eller sekund. 

## <a name="freezing-columns"></a>Låse kolonner
Noen kolonner i et rutenett kan så viktige for konteksten at du ikke vil at de kan rulle ut av visningen. Du vil i stedet kanskje at verdiene i disse kolonnene alltid vises. Med funksjonen **Frys kolonnene i rutenett** får brukerne denne fleksibiliteten. 

Du låser en kolonne ved å høyreklikke på kolonneoverskriften og deretter velge **Lås kolonne**. Første gang du fullfører dette trinnet, blir den valgte kolonnen den første kolonnen og ruller ikke lenger ut av visningen. Alle påfølgende kolonner du låser, blir lagt til til høyre for den sist låste kolonnen. Du kan bruke standardfunksjonen for flytting til å endre rekkefølgen på låste kolonner etter behov. Låste kolonner kan imidlertid ikke flyttes slik at de vises blant settet med ulåste kolonner. Ulåste kolonner kan likeledes ikke flyttes slik at de vises blant settet med låste kolonner.

Du låser opp en kolonne ved å høyreklikke på den låste kolonneoverskriften og deretter velge **Lås opp kolonne**. 

Merk at kolonnen for radvalg og radstatus i det nye rutenettet alltid låses som de to første kolonnene. Når disse kolonnene tas med i et rutenett, er de derfor alltid synlige for brukere, uavhengig av den vannrette rulleplasseringen i rutenettet. Du kan ikke endre rekkefølgen på disse to kolonnene.

## <a name="autofit-column-width"></a>Beste tilpassing av kolonnebredde
I likhet med Excel kan brukere automatisk tvinge en kolonne til å endre størrelsen på basert på innholdet som vises i den kolonnen. Dobbeltklikk størrelseshåndtakene i kolonnen for å gjøre dette, eller ved å legge fokus i kolonneoverskriften og trykke **A** (for automatisk tilpassing). Denne funksjonen er tilgjengelig fra og med versjon 10.0.23.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg den nye rutenettkontrollen i miljøet? 

Funksjonen **Ny rutenettkontroll** er tilgjengelig direkte i funksjonsbehandling i et hvilket som helst miljø. Når funksjonen er aktivert i Funksjonsstyring, vil alle etterfølgende brukerøkter bruke den nye rutenettkontrollen. 

Denne funksjonen er aktivert som standard i versjon 10.0.21 og har som mål å bli obligatorisk i oktober 2022.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Utvikler] Velge bort enkeltsider fra å bruke det nye rutenettet 
Hvis organisasjonen oppdager en side der det er noen problemer med å bruke det nye rut nettet, er det tilgjengelig et API for å tillate at et enkelt skjema bruker den gamle rutenettkontrollen samtidig som resten av systemet brukes til å utnytte den nye rutenettkontrollen. Hvis du vil velge bort en enkelt side fra det nye rutenettet, legger du til følgende oppkallspost `super()` i skjemaets `run()`-metode.

```this.forceLegacyGrid();```

Dette API-et støttes til den nye rutenettkontrollen blir obligatorisk. Denne endringen er for øyeblikket planlagt for oktober 2022. Hvis problemer gjør at denne APIen brukes, rapporterer du dem til Microsoft.

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

## <a name="known-issues"></a>Kjente problemer
Denne delen viser en liste over kjente problemer for den nye rutenettkontrollen.

### <a name="open-issues"></a>Åpne problemer
- Når du har aktivert funksjonen **Ny rutenettkontroll**, vil noen sider fortsette å bruke den eksisterende rutenettkontrollen. Dette vil skje i følgende situasjoner:
 
    - Det finnes en kortliste på siden som gjengis i flere kolonner.
    - Det finnes en gruppert kortliste på siden.
    - En rutenettkolonne med en ikke-reagerende utvidbar kontroll.

    Når en bruker først støter på én av disse situasjonene, vil det vises en melding om oppdatering av siden. Når denne meldingen vises, vil siden fortsette å bruke det eksisterende rutenettet for alle brukere til neste oppdatering av produktversjonen. Bedre behandling av disse scenariene, slik at det nye rutenettet kan brukes, vurderes for en fremtidig oppdatering.

- [KB 4582758] Poster er utydelige når du endrer zooming fra 100 til en annen prosent
- [KB 4592012] Uventet klientfeil i IE11 når du limer inn flere linjer fra Excel

    Microsoft arbeider ikke med en løsning på dette problemet


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

