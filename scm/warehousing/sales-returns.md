---
title: Salgsreturer
description: "Dette emnet inneholder informasjon om prosessen for returordrer. Den inneholder informasjon om kunden returnerer og deres innvirkning på lagerantall for etterkalkulering og lagerbeholdning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Salgsreturer

Dette emnet inneholder informasjon om prosessen for returordrer. Den inneholder informasjon om kunden returnerer og deres innvirkning på lagerantall for etterkalkulering og lagerbeholdning.

Kunder kan returnere varer av ulike årsaker. For eksempel en vare kan være ødelagt, eller den oppfyller ikke kundens forventninger. Prosessen starter når en kunde sender en forespørsel om å returnere en vare. Når kundens forespørsel mottas, opprettes en returordre i Microsoft Dynamics 365 for operasjoner.

## <a name="return-order-process"></a>Returordren prosess
Illustrasjonen nedenfor gir en oversikt over prosessen for returordren.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Det finnes to typer Returordreprosessen: fysisk gå tilbake og kreditere bare.

-   **Fysisk retur** – returordren autoriserer fysisk retur av produkter.
-   **Kreditere bare** – returordren autoriserer kundekreditt, men ikke krever at kunden returnere varene fysisk.

### <a name="physical-return-order-process"></a>Fysisk Returordreprosessen

1.  **Opprette en returordre.** Formelt dokument godkjenning for kunden til å returnere et defekt eller uønskede produkter. Returordren krever ikke at selskapet godta de returnerte produktene eller gi en kreditnota for kunden. Hvis avkastning er godtatt, kan du godkjenne en erstatningsvare som skal sendes før defekt vare er returnert.
2.  **Ankomme lageret for inspeksjon.** Fullføre en første inspeksjon og validering mot returordren dokumentet. Returordren støtter også karantene av de returnerte varene for ekstra inspeksjon og kvalitetskontroll.
3.  **Bestemme fjerning.** Fullføre inspeksjon prosessen, og bestemme hva som skal gjøres med de returnerte produktene. Som en del av dette trinnet, kan du bestemme om du vil kreditere kunden, avvise produktretur, eller godta produktet gå tilbake, svinn produktet og deretter sende et erstatningsprodukt til kunden.
4.  **Generere en følgeseddel.** Generere en følgeseddel, og Utfør fjerning beslutningen om du gjorde i trinn 3. Fullfør logistikk-prosesser.
5.  **Generere en faktura.** Lukk returordren.

### <a name="credit-only-process"></a>Bare behandle kreditt

1.  **Opprette en returordre.** Formelt dokument godkjenning for kunden som skal motta en kreditt uten å returnere de defekte eller uønskede produktene. Den **kreditt bare** disposisjonskode autoriserer beslutningen om å kreditere kunden uten fysisk retur.
2.  **Generere en faktura.** Generer kreditnotaen, og deretter lukker returordren.

## <a name="return-material-authorization"></a>Return material authorization
Return Material Authorization (RMA) behandling bygger på funksjonalitet for ordren. En ARM er registrert som en returordre som er opprettet som en salgsordre, og kan ha en annen salgsordren som er knyttet til den, kalles en erstatningsordre. Både salgsordrer, koble til det opprinnelige ARM-nummeret.

-   **Ordreretur** – til å registrere en ARM du opprette en ordreretur, som er en ordre som er tilordnet typen, **returnerte ordren.** Eventuelle endringer du gjør i ARM-informasjonen oppdateres automatisk i ordren. Til returordren har statusen **åpne**, vises ikke i listen over salgsordrer. Du bruker ARM til å håndtere ankomst og mottak av returnerte varer, i tillegg til å godkjenne en eneste disposisjonshandlingen kredit (se avsnitt **disposisjonskoder og handlingene du har utført**). Alle andre oppfølgingsaktiviteten prosesser må håndteres i ordren.
-   **Erstatningsordre** – når en erstatningsordre må leveres til kunden, RMA kan inkludere en andre tilknyttede salgsordre. Du kan manuelt opprette erstatningsordren for ARM støtte for umiddelbar levering. Du kan eventuelt kan erstatningsordren bli opprettet automatisk etter ankomst, inspeksjon og mottak er fullført for varen på ARM som har en disposisjonskode som angir erstatning. Erstatningsordren har samme funksjonalitet som er knyttet til en salgsordre. Du kan for eksempel bruke den til å konfigurere et tilpasset produkt som erstatningsvaren, opprette en produksjonsordre for å reparere en returnert vare, oppretter en bestilling for direkte levering å sende erstatning fra en leverandør, eller støtte for andre formål.

## <a name="create-a-return-order"></a>Opprette en returordre
Returordreprosessen starter når en kunde kontakter organisasjonen til å returnere et defekt eller uønsket produkt og/eller som skal krediteres. Etter at organisasjonen godtar retur, dokumentert retur ved en returordre. Denne returordren blir Blikkfang i den interne behandlingen av det returnerte produktet. Følgende illustrasjon viser fremgangsmåten for å opprette en returordre.  

[![Fremgangsmåten for å opprette en returordre](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Opprette en returordrehodet

Når du oppretter en ordreretur, kan informasjonen i tabellen nedenfor, må inkluderes.

| Felt              | beskrivelse                                              | Kommentarer                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kundekonto   | En referanse til Kunder-tabellen                       | Du må angi en eksisterende kundekonto.                                                                                                                                                                                                                                                                                                  |
| Leveringsadresse   | Adressen som elementet returneres til                 | Organisasjonens adressen brukes som standard. Hvis et bestemt lager er valgt i hodet, endres adressen til adressen til lageret. Du kan endre denne adressen på den **Returordredetaljer** siden.                                                                                                  |
| /-Lager     | Området eller lageret som mottar det returnerte produktet | Leveringsadressen for returordren bestemmes basert på adressen til området eller lageret.                                                                                                                                                                                                                                 |
| Autorisasjonsreturnr.         | IDen som er tilordnet til returordren              | ARM-nummeret brukes som en alternativ nøkkel gjennom hele prosessen for returordren. ARM-nummer som tilordnes basert på ARM nummerserien som er satt opp på den **Kundeparametere** siden.                                                                                                                              |
| Frist           | Den siste datoen som et element som kan returneres               | Standardverdien er beregnet som gjeldende dato pluss gyldighetsperioden. For eksempel hvis en retur er gyldig for 90 dager fra datoen da returordren er opprettet, og returordren ble opprettet i mai 1, verdien i feltet er **30 juli**. Gyldighetsperioden er satt på den **Kundeparametere** siden. |
| Kode for returårsak | Kundens årsak til å returnere produktet          | Årsakskoden som er valgt i listen over brukerdefinerte årsakskoder. Du kan oppdatere dette feltet når som helst.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Opprett linjer for returordren

Når du har fullført retur hodet, kan du opprette returnerte linjer ved hjelp av én av følgende metoder:

-   Angi elementdetaljene, antall og annen informasjon for hver returledning manuelt.
-   Opprette en retur linje ved hjelp av den **finne salgsordren** funksjon. Vi anbefaler at du bruker denne funksjonen når du oppretter en returordre. Den **finne salgsordren** funksjonen etablerer en referanse fra linjen tilbake til fakturert salgsordre-linjen, og henter linje detaljer som varenummer, antall, pris, rabatt og kostnadsverdier fra salgslinjen. Referansen kan garantere at når produktet returneres til selskapet, det har enkeltverdier til samme enhetskost at den ble solgt på. Referansen validerer som returnerer bestillinger ikke opprettes for et antall som er større enn antallet som ble solgt på fakturaen.

**Merk:** returnerte linjer som har en referanse til en salgsordre, behandlet som korrigeringer eller tilbakeføringer av salget. Hvis du vil ha mer informasjon, kan du se delen "Post til finans" senere i dette emnet.

### <a name="charges"></a>Tillegg

Gebyrer og avgifter kan legges til ordrereturen gjennom ett eller flere av følgende metoder:

-   Du kan manuelt legge til tillegg i returordrehodet, returordrelinjen eller begge.
-   Tillegg kan legges automatisk til returordrehodet som en funksjon av returårsakskoden.
-   Tillegg kan legges automatisk til returordrelinje, basert på disposisjonskoden for linjen.

Tillegg legges automatisk etter en returårsakskoden eller disposisjonskoden som er tilordnet til linjen. Hvis årsakssporet endres senere, eksisterende belastning posten vil ikke bli fjernet, men kan legges til en ny oppføring for tillegget, basert på den nye årsakskoden. Når du legger til i tillegg til å returnere ordrelinjer, blir gebyrer som beregnes som en prosent av linje- eller verdien negativ når linjen eller linje ordre er negativ, med mindre prosentandelen er også et negativt tall. Et tillegg som har en negativ verdi representerer en kreditnota til kunden.

### <a name="return-reason-codes"></a>Koder for returårsaker

Ved å bruke årsakskoder returnerer, kan du bidra til å gjøre det enklere å analysere retur mønstre. Årsakskoder gir informasjon om hvorfor en kunde vil returnere varer. Noen organisasjoner har mange årsakskoder. Disse organisasjon kan gruppere årsakssporene i årsakskodegrupper for å få en bedre oversikt og akkumulert rapportering.

### <a name="disposition-codes-and-disposition-actions"></a>Disposisjonskoder og handlingene du har utført

Et viktig trinn i Returordreprosessen er å tilordne en disposisjonskode til returordrelinjen som en del av ankomstregistrering. Disposisjonskoden bestemmer følgende informasjon:

-   **Økonomiske konsekvenser** – skal kunden skal krediteres for de returnerte varene, og bør noen tillegg legges til i returordrelinjen?
-   **Fjerning av den returnerte varen** – skal varen kan være lagt til tilbake til lager, bør det kasseres, eller skal det returneres til kunden?
-   **Logistikk for den returnerte varen** – skal utstedes en erstatningsvare for kunden?

I tillegg til å bestemme hvordan de returnerte varene er solgt, disposisjonskoder kan føre til tilleggene som skal brukes til retur linje. De kan også brukes til å gruppere returer for statistisk analyse. Disposisjonskoder er definert som en del av oppsettet av returordrer. Imidlertid må hver disposisjonskode referere til en av de innebygde fjerning handlingene. Følgende tabell viser de innebygde disposisjonskoder og sine handlinger. **Viktig:** Hvis et element ikke bli returnert, men bør fortsatt kreditert til kunden, kan du tilordne den **kreditt bare** disposisjonskode for å returnere linjen.

<table>
<thead>
<tr class="header">
<th>Disposisjonskode</th>
<th>Økonomiske konsekvenser</th>
<th>Konsekvensene for logistikk</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bare kreditering</td>
<td><ul>
<li>Kunden er kreditert salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassere varen er postert til finansmodulen.</li>
</ul></td>
<td>Varen bør ikke bli returnert. Denne disposisjonshandlingen brukes i følgende tilfeller:
<ul>
<li>Det er tilstrekkelig klarering mellom partene.</li>
<li>Kostnaden for retur av defekt vare er hindre deg.</li>
<li>Være kan ikke tillatt varene tilbake til lager. Av andre grunner, en fysisk retur er ikke nødvendig.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditt</td>
<td><ul>
<li>Kunden er kreditert salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Lagerverdien økes med kostnaden for den returnerte varen.</li>
</ul></td>
<td>Elementet returneres og legges tilbake i lageret.</td>
</tr>
<tr class="odd">
<td>Erstatt og krediter</td>
<td><ul>
<li>Kunden er kreditert salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Lagerverdi økes med kostnaden for den returnerte varen.</li>
<li>En separat salgsordre for en erstatning opprettes og håndteres separat.</li>
</ul></td>
<td>Elementet returneres og legges tilbake i lageret.</td>
</tr>
<tr class="even">
<td>Erstatt og kasser</td>
<td><ul>
<li>Kunden er kreditert salgsprisen, minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassere varen er postert til finansmodulen.</li>
<li>En separat salgsordre for en erstatning opprettes og håndteres separat.</li>
</ul></td>
<td>Elementet returneres og kassert.</td>
</tr>
<tr class="odd">
<td>Returner til kunde</td>
<td>Ingen, unntatt gebyrer eller avgifter.</td>
<td>Elementet returneres, men sendes tilbake til kunden etter inspeksjon. Denne disposisjonshandlingen kan brukes hvis elementet er skadet med hensikt, eller hvis garantien er annullert.</td>
</tr>
<tr class="even">
<td>Svinn</td>
<td><ul>
<li>Kunden er kreditert salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassere varen er postert til finansmodulen.</li>
</ul></td>
<td>Elementet returneres eller kasseres.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Ankomst på lageret for inspeksjon
Før du kan motta returnerte varer fysisk til lager, ved å bokføre en følgeseddel, må varene gå gjennom ankomstregistreringen og en valgfri inspeksjon. Illustrasjonen nedenfor gir en oversikt over ankomstprosessen. Avsnittene nedenfor beskriver hvert trinn som er vist i illustrasjonen.  

[![Ankomstprosess](./media/salesreturn03.png)](./media/salesreturn03.png)  

Prosessen har flere andre variasjoner som ikke dekkes i dette emnet. Her er noen av disse variasjonene:

-   Ikke bruk det **Ankomstoversikt** listen til å opprette en ankomstjournal. I stedet opprette ankomstjournalen manuelt. Returnere ordrer skal ha **ordre** som referanse.
-   Hvis du bruker lagerstyring, kan du generere palltransporter. Returner linjen har statusen **mottatt** under palltransporten.
-   Registrere mottak av returnerte varer direkte fra returordrelinje, ved hjelp av den **registrering** funksjon.

Når du ankommer, er returnerer integrert med den generelle prosessen for lageret innganger. Ankomstprosessen støtter også oppretting av ordrer i karantene for returnerte varer som må gjennomgå en egen undersøkelse.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identifisere produktene i listen ankomst-oversikt

Den **Ankomstoversikt** siden viser en liste over alle planlagte innkommende ankomster. **Merk:** ankomster fra ordrereturer må behandles separat fra andre typer transaksjoner for ankomst. Når du har identifisert en innkommende pakke på den **Ankomstoversikt** side (for eksempel ved hjelp av det medfølgende ARM-dokumentet), i handlingsruten, klikker du **Start ankomst** til å opprette og starte en ankomstjournal som samsvarer med overgangen.

### <a name="edit-the-arrival-journal"></a>Rediger ankomstjournalen

Ved å angi den **karantene management** å **Ja**, kan du opprette en karanteneordre for returlinjen. Hvis en linje er sendt til karantene for inspeksjon, kan du ikke angi en disposisjonskode. **Merk:** Hvis du setter den **karantene management** å **Ja** i varens lagermodellgruppe, den **karantene management** alternativet på den **journallinjer** siden vil bli merket for kladdelinjen ankomst og kan ikke endres. Hvis linjen sendes til karantene, må du angi riktige karantenelageret. Hvis linjen ankomst ikke er sendt for inspeksjon, må ankomst Lagerarbeideren angi disposisjonskoden direkte på kladdelinjen ankomst og deretter bokføre ankomstjournalen. Hvis den samme disposisjonskoden ikke skal tilordnes hele antallet av returlinjen, eller hvis du ikke har mottatt hele antallet på linjen, må du dele linjen. Når du deler en kladdelinje for ankomst, du også dele returlinjen (**SalesLine**), og Opprett et nytt parti-ID. Du kan dele linjen ved å redusere antall ankomstjournallinjen. Når journalen posteres, opprettes en ny linje return som har statusen **forventet** for det gjenstående antallet. Du kan også dele linjen ved å klikke **funksjoner**&gt;**del**.

### <a name="process-the-quarantine-order"></a>Behandle karanteneordren

Hvis de returnerte produktene sendes for inspeksjon i karantenelageret, fullført Tilleggsbehandling i en karanteneordre. Opprettes en karanteneordre for hver ankomst-linjen som sendes til karantene. Disposisjonskoden, angir resultatet av inspeksjonen prosessen. Du kan dele en karanteneordre, på samme måte som du kan dele ankomstjournalen. Hvis du deler karanteneordren, forårsake en tilsvarende del av returlinjen. Etter at disposisjonskoden som er angitt, må du fullføre karanteneordren ved hjelp av den **slutten** funksjon eller **ferdigmelde** funksjon. Hvis du velger **ferdigmelde**, opprettes en ny ankomst i den angitte lageret. Du kan deretter behandle denne ankomst ved hjelp av den **Ankomstoversikt** siden. Hvis ankomsten stammer fra en karanteneordre, kan du ikke endre disposisjonskoden som er tilordnet under inspeksjon. Hvis du fullfører karanteneordren ved hjelp av den **slutten** funksjon, partiet registreres automatisk. Noen ganger kan en vare sendes tilbake fra karantene til levering og mottak avdeling. Karantene kontrolløren kan for eksempel ikke vet hvor du vil lagre varen på lager. I dette tilfellet må den tilsvarende følgeseddel oppdateres for å registrere og handle på disposisjonskoden som er angitt på grunn av karantenen på riktig måte. Bekreftelse av mottak kan sendes til kunden når returlinjen er registrert. Den **returbekreftelse** rapporten ligner dokumentet returordren. Den **returbekreftelse** rapporten ikke er journalført, eller hvis ikke registrert i systemet, og det er ikke et obligatorisk trinn i prosessen for returordren.

## <a name="replace-a-product"></a>Erstatte et produkt
Det finnes to metoder for håndtering av Produkterstatning:

-   **Den fremste erstatning** – erstatte et produkt før det returnerte produktet er mottatt fra kunden.
-   **Erstatning av disposisjonskoden** – automatisk opprette en ny ordrelinje for erstatning.

### <a name="up-front-replacement"></a>Forskuddserstatning

Erstatningsvaren kan leveres til kunden i den fremste erstatning før elementet returneres. Denne metoden er nyttig hvis du for eksempel varen inngår en maskin som ikke kan fjernes med mindre en reservedel kan ta stedet, eller hvis du bare vil at kunden skal ha erstatning produktet så snart som mulig. Den fremste erstatningsordren er en uavhengig salgsordre. Informasjonen i hodet er initialisert fra kunden, og informasjonen om er initialisert fra bestillingsreturen. Du kan redigere, behandle og slette erstatningsordren uavhengig av returordren. Når du sletter en erstatningsordre, får du en melding som at ordren ble opprettet som en erstatningsordre. Illustrasjonen nedenfor viser prosessen for den fremste erstatning.  

[![Den fremste erstatning-prosess](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Returordren inneholder en referanse til erstatningsordren. Hvis en gang erstatningsordre er opprettet for en returordre før defekt vare returneres, kan du ikke velge disposisjonskoder for erstatning etter defekt vare er returnert.

### <a name="replacement-by-disposition-code"></a>Erstatning av disposisjonskoden

Hvis du leverer en erstatningsvare for kunden, og du bruker den **Erstatt og kasser** eller **Erstatt og krediter** disposisjonshandlingen på bestillingsreturen, bruker du prosessen som er vist i illustrasjonen nedenfor.  

[![Erstatning prosessen når en disposisjonskode brukes](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Erstatningsvaren sendes ved hjelp av en uavhengig salgsordre, erstatningsordren. Denne salgsordren blir opprettet når følgeseddelen for returordren genereres. Ordrehodet bruker informasjon fra kunden som det refereres til i returordrehodet. Linjeinformasjon som samles inn fra informasjonen som er angitt på den **erstatningsvaren** siden. Den **erstatningsvaren** siden må fylles ut for linjer med handlingene du har utført som begynner med ordet "Erstatt". Verken antallet eller identiteten til erstatningsvaren er imidlertid validert eller begrenset. Dette gjør det mulig for tilfeller der kunden ønsker den samme varen, men i en annen konfigurasjon eller størrelse og også tilfeller der kundene vil ha et helt annet element. Som standard et identisk element som er lagt inn i den **erstatningsvaren** siden. Du kan imidlertid velge en annen vare, forutsatt at funksjonen er definert. **Merk:** du kan redigere og slette erstatningsordren opprettes.

## <a name="generate-a-packing-slip"></a>Generere en følgeseddel
Før returnerte varer kan mottas til lager, må du oppdatere følgeseddelen for ordren som varene tilhører. På samme måte som fakturaoppdateringsprosessen er en oppdatering av den økonomiske transaksjonen, for oppdatering av følgeseddel prosessen er en fysisk oppdatering av lagerposten. Med andre ord, gjør denne prosessen den endringene i lager. Når det gjelder returer, implementeres trinnene som er tilordnet til disposisjonshandlingen under følgeseddelantallet følgebrevoppdateringen. Når du genererer følgeseddelen, oppstår følgende hendelser:

-   I lageret brukes standard prosessen til å utføre en fysisk mottak. Finansposteringer genereres hvis lageret modell gruppe (**poster fysisk lager**) og parameterne for kundesamlekonto (**Poster følgeseddel i Finans**) er angitt riktig.
-   Elementer som er merket med en disposisjonshandling som inneholder ordet "Kladd" kasseres, og lagertap posteres til finansmodulen.
-   Elementer som er merket med den **Returner til kunde** disposisjonshandlingen er mottatt og leveres til kunden. Disse elementene har ingen netto effekt på lager.
-   En erstatningsordre opprettes. Denne salgsordren er basert på informasjon på den **erstatningsvaren** siden.

Du kan generere følgeseddelen bare for linjer som har statusen tilbake til **registrerte**, og bare for hele antallet på linjen tilbake. Hvis flere linjer på bestillingsreturen har den **registrerte** status, kan du generere følgeseddelen for et delsett av linjene ved å slette de andre linjene fra den **Poster følgeseddel** siden. Delvis returnerer defineres som returordrelinjer, ikke i returordreforsendelser. Hvis du mottar hele antallet som er angitt på én returordrelinje, men du får ikke noe fra de andre linjene i returordren, er leveringen en delvis levering. Hvis en returordrelinje krever at 10 enheter av en vare returneres, men du får bare fire enheter, er imidlertid en delvis levering i leveringen. Hvis ikke alle forventede returnerte varer er ankommet, kan du sette forsendelsen til side og vente til resten av det returnerte antallet ankommer. Du kan også registrere og postere den delvise leveringen. Som en del av prosessen med bokføring følgesedler, kan du knytte det følgeseddelens referansenummeret fra kundens leveringsdokumentene ordrelinjene. Denne tilknytningen er valgfri, og er bare til referanseformål. Den oppretter ikke noen transaksjonsoppdateringer. Generelt, kan du hoppe over følgeseddelantallet forsinket prosessen og gå direkte til fakturering. I dette tilfellet, trinnene som du ville ha utført når følgeseddelen slip generasjon fullføres under fakturering.

## <a name="generate-an-invoice"></a>Generer en faktura
Selv om den **ordreretur** siden inneholder informasjon og handlinger som kreves for å håndtere de spesielle Logistiske aspektene for returordren, må du bruke den **ordre** siden for å fullføre faktureringsprosessen. Organisasjonen kan deretter fakturere returordrer og salgsordrer samtidig, og den samme personen kan fullføre faktureringsprosessen, etter behov. Slik viser du returordren fra den **ordre** klikker du koblingen for salgsordre-nummeret for å åpne den tilknyttede salgsordren. Du kan også finne returordren på den **alle salgsordrer** siden. Gå tilbake til ordrer, er ordrer som har en ordretype av **returnerte ordre**.

### <a name="credit-correction"></a>Kreditrettelse

Som en del av faktureringsprosessen, kan du kontrollere at eventuelle tilleggsgebyrer er riktige. Hvis du vil føre til finansposteringer blir rettelser (Storno), bør du vurdere å bruke den **kreditere rettelse** alternativet på den **andre** -kategorien i den **postering av faktura** når du bokfører fakturaen eller kreditnotaen. **Merk:** som standard i **kreditering rettelse** alternativet er aktivert hvis den **kreditnota som rettelse** alternativet på den **Kundeparametere** siden har blitt aktivert. Vi anbefaler imidlertid at du ikke bokfører returnerer med Storno.

## <a name="create-intercompany-return-orders"></a>Opprette konserninterne returordrer
Returordrene kan fullføres mellom to firmaer i organisasjonen. Det er støtte for følgende scenarier:

-   Enkel konsernintern retur mellom to selskaper som deltar i en konsernintern relasjon
-   En konsernintern kjede som opprettes når en kunde returordre opprettes i det selgende firmaet
-   En konsernintern kjede som opprettes når det blir opprettet en bestillingsretur for leverandøren i det kjøpende selskapet
-   Direktelevering levering returnerer mellom en ekstern kunde og to firmaene som deltar i en konsernintern relasjon

### <a name="setup"></a>Konfigurer

Den følgende illustrasjonen minimum oppsettet som kreves for to selskaper til å delta i en konserninterne forhold, og dra nytte av konsernintern handel.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

I følgende scenario, CompBuy er det kjøpende selskapet, og CompSell er selgende firma. Vanligvis leverer det selgende firmaet varer til det kjøpende selskapet eller, i scenarier med direkte levering levering, direkte til sluttkunden. I CompBuy, leverandøren IC\_CompSell er definert som et konserninternt sluttpunkt som er knyttet til firmaet CompSell. Samtidig, i CompSell, kunden IC\_CompBuy er definert som et konserninternt sluttpunkt som er knyttet til firmaet CompBuy. Riktig handling policydetaljene og verditilordninger må defineres i begge firmaene. I en direkte levering forsendelsen situasjon opprettes en konsernintern returordre, som også er en konsernintern salgsordre, i det selgende firmaet. Autorisasjonsreturnummeret for konserninterne returordren kan plukkes fra ARM nummersekvensen i CompSell, eller den kan kopieres fra ARM-nummeret som er tilordnet til den opprinnelige returordren i CompBuy. ARM-nummer-innstillingene på den **PurchaseRequisition** handlingspolicyen i CompBuy finne ut disse handlingene. Hvis synkroniseres autorisasjonsreturnummeret, bør du planlegge å redusere risikoen for tallet konflikt hvis de to firmaene bruker den samme nummerserien.

### <a name="simple-intercompany-returns"></a>Enkel konserninterne returnerer

Dette scenariet omfatter to selskaper i samme organisasjon, som vist i illustrasjonen nedenfor.  

[![Enkel konsernintern retur](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Kan opprette ordrekjeden når det opprettes en bestillingsretur for leverandøren i det kjøpende selskapet eller en ordreretur for kunden som er opprettet i det selgende firmaet. Dynamics 365 for operasjoner oppretter den tilsvarende ordren i det andre firmaet, og sørger for at topp- og linjeinformasjon for leverandøren returnere gjenspeiler rekkefølgen innstillingene på kunden ordreretur. Returordren som er etablert kan inkludere eller ekskludere referansen (**finne salgsordren**) til en eksisterende kundefaktura. Følgesedler og fakturaer for to bestillinger kan behandles individuelt. Du har ikke generere en følgeseddel for returordren leverandør før du genererer følgeseddelen for kundereturordren.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Direktelevering levering returnerer mellom tre parter

Dette scenariet kan opprettes hvis en tidligere salg av den **direkte levering** type er fylt ut, og hvis en faktura mot kunden finnes i firmaet som fungerer sammen med kunden. I illustrasjonen nedenfor har firmaet CompBuy tidligere solgt og fakturert produkter til kunden Extern. Produktene er levert direkte fra selskapet CompSell til kunden via en konsernintern ordrekjede.  

[![Direktelevering levering returnerer mellom tre parter](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Hvis kunden Extern vil returnere produktene, opprettes en returordre (RMA02) for kunden i firmaet CompBuy. Hvis du vil opprette den konserninterne kjeden, må returordren merkes for direkte levering. Når du bruker den **finne salgsordren** -funksjonen til å velge kundefakturaen skal returneres, opprettes en konsernintern ordrekjede som består av følgende dokumenter:

-   **Opprinnelige returordren:** RMA02 (firma CompBuy)
-   **Bestilling:** PO02 (firma CompBuy)
-   **Konsernintern returordre:** ARM\_00032 (firma CompSell)

Etter at den konserninterne kjeden direkte levering opprettes, alle fysiske håndtering og behandling av returnerer må være i kontekst med konserninterne returordren, ARM\_00032 i firmaet CompSell. Produktene kan ikke mottas i firmaet CompBuy. Når en disposisjonskode er knyttet til konserninterne returordren, er det synkronisert med den opprinnelige returordren å tillate riktig fakturering av den opprinnelige ordren.

## <a name="post-to-the-ledger"></a>Posterer til finans
Finansposteringer som blir generert når returordren faktureres er påvirket av noen viktige innstillinger og parametere:

-   **Returkostpris** – For lager-modeller, annet enn **standardkost**, **Returkostpris** parameteren bestemmer kostnadene for varen når den har godtatt tilbake til lager eller kassert. Hvis du vil beregne en riktig vurdering av beholdning, er det viktig at du setter det **Returkostpris** parameter på riktig måte. Hvis du bruker den **finne salgsordren** -funksjonen til å opprette en returordrelinje som har en referanse til en kundefaktura, den **Returkostpris** er lik verdien i kostprisen for varen som selges. Hvis ikke, kostpris verdien kommer fra vareoppsettet eller kan angis manuelt.
-   **Kreditere rettelse/Storno** – den **kreditering rettelse** parameter i den **postering av faktura** siden bestemmer om bokføringer skal være registrert som positive (DR/CR) poster eller korrigere, negative poster.

I eksemplene nedenfor, representeres den returnerte kostprisen som **Avrund.presisjon, faktura(NOK) kostpris**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Eksempel 1: Returordren ikke refererer til en kundefaktura

Returordren referere ikke til en kundefaktura. Den returnerte varen er kreditert. Den **kreditering rettelse** parameteren ikke er valgt når returordre, faktura eller kreditnota, genereres.  

[![Returordren refererer ikke til et kunde-invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Merk:** master vareprisen brukes som standardverdi for den **Returkostpris** parameter. Standard prisen er forskjellig fra kostprisen ved lageravgang. Derfor er implisitt tap av 3 som er påløpt. I tillegg inneholder ikke returordren rabatten som er gitt til kunden i ordren. Derfor oppstår en stor kreditt.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Eksempel 2: Kredittrettelse er valgt for returordren

Eksempel 2 er den samme som eksempel 1, men den **kreditere rettelse** parameteren velges når returordren fakturaen genereres.  

[![Returordren der Kredittrettelse er valgt](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Merk:** finansposteringer angis som negative korrigeringer.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Eksempel 3: Returordrelinjen opprettes ved hjelp av funksjonen Søk etter salgsordren.

I dette eksemplet opprettes returordrelinjen ved hjelp av den **finne salgsordren** funksjon. Den **kreditering rettelse** parameteren ikke er valgt når fakturaen er opprettet.  

[![Returnere ordrelinje som er opprettet ved hjelp av Søk etter salgsordren.](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Merk:****rabatt** og **Returkostpris** er riktig innstilt. Derfor oppstår en nøyaktig reversering av kundefakturaen.


