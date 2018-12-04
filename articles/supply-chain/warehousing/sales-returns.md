---
title: Salgsreturer
description: "Dette emnet inneholder informasjon om prosessen for returordrer. Det inneholder informasjon om kundereturer og deres innvirkning på lagerantall for etterkalkulering og lagerbeholdning."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d4da2ed8d61ffae3a4a4dc24793d82de22e86e59
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="sales-returns"></a>Salgsreturer

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om prosessen for returordrer. Det inneholder informasjon om kundereturer og deres innvirkning på lagerantall for etterkalkulering og lagerbeholdning.

Kunder kan returnere varer av ulike årsaker. En vare kan for eksempel være ødelagt, eller den oppfyller kanskje ikke kundens forventninger. Returprosessen starter når en kunde sender en forespørsel om å returnere en vare. Når kundens forespørsel mottas, opprettes en returordre i Microsoft Dynamics 365 for Finance and Operations.

## <a name="return-order-process"></a>Ordrereturprosessen
Illustrasjonen nedenfor gir en oversikt over returordreprosessen.  

[![Ordrereturprosessen](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Det finnes to typer ordrereturprosesser: fysisk retur og bare kreditering.

-   **Fysisk retur** – Returordren autoriserer fysisk retur av produkter.
-   **Bare kreditering** – Returordren autoriserer en kundekreditt, men krever ikke at kunden returnere varene fysisk.

### <a name="physical-return-order-process"></a>Returordrerprosess for fysisk retur

1.  **Opprett en returordre.** Dokumenter formelt autorisasjonen for at kunden kan returnere defekte eller uønskede produkter. Returordren krever ikke at selskapet godtar de returnerte produktene eller krediterer kunden. Hvis returen godtas, kan du autorisere at en erstatningsvare skal sendes før den defekt varen er returnert.
2.  **Ankomme lageret for inspeksjon.** Fullføre en første inspeksjon og validering mot returordredokumentet. Returordren støtter også karantene av de returnerte varene for ekstra inspeksjon og kvalitetskontroll.
3.  **Bestemme disposisjon.** Fullfør inspeksjonsprosessen, og bestemme hva som skal gjøres med de returnerte produktene. Som en del av dette trinnet, kan du bestemme om du vil kreditere kunden, avvise eller godta produktreturen, kassere produktet og deretter sende et erstatningsprodukt til kunden.
4.  **Generer en følgeseddel.** Generer en følgeseddel, og utfør disposisjonsbeslutningen om du gjorde i trinn 3. Fullfør logistikkprosessene.
5.  **Generer en faktura.** Lukk returordren.

### <a name="credit-only-process"></a>Prosess for bare kreditering

1.  **Opprett en returordre.** Dokumenter formelt autorisasjonen for at kunden kan motta en kreditering uten å returnere defekte eller uønskede produkter. Disposisjonskoden **Bare kreditering** autoriserer beslutningen om å kreditere kunden uten fysisk retur.
2.  **Generer en faktura.** Generer kreditnotaen, og lukk deretter returordren.

## <a name="return-material-authorization"></a>Autorisasjon for returmaterialer
Behandling av autorisasjonsreturnummeret bygger på funksjonalitet for salgsordren. En ARM registreres som en returordre, som opprettes som en salgsordre, og den kan ha en annen salgsordre tilknyttet kalt en erstatningsordre. Begge salgsordrene er koble til det opprinnelige ARM-nummeret.

-   **Returordre** – Hvis du vil registrere en ARM, oppretter du en returordre, som er en ordre som er tilordnet typen, **Returordre**. Eventuelle endringer du gjør i ARM-informasjonen oppdateres automatisk i salgsordren. Returordren vises ikke i listen over salgsordrer før den har statusen **Åpen**. Du bruker ARM til å håndtere ankomst og mottak av returnerte varer, i tillegg til å autorisere en Bare kreditering-disposisjonshandling (se avsnitt **Disposisjonskoder og -handlinger**). Alle andre oppfølgingsprosesser må håndteres i salgsordren.
-   **Erstatningsordre** – Når en erstatningsordre må leveres til kunden, kan ARM-en inneholde en andre tilknyttet salgsordre. Du kan manuelt opprette erstatningsordren, slik at ARM-en støtter umiddelbar levering. Erstatningsordren kan eventuelt opprettes automatisk etter at ankomst, inspeksjon og mottak er fullført for ARM-linjevaren som har en disposisjonskode som angir erstatning. Erstatningsordren har samme funksjonalitet som er knyttet til en salgsordre. Du kan for eksempel bruke den til å konfigurere et tilpasset produkt som erstatningsvaren, opprette en produksjonsordre for å reparere en returnert vare, opprette en bestilling for direktelevering for å sende erstatning fra en leverandør, eller støtte for andre formål.

## <a name="create-a-return-order"></a>Opprette en returordre
Returordreprosessen starter når en kunde kontakter organisasjonen for å returnere et defekt eller uønsket produkt og/eller for å krediteres. Når organisasjonen har godtatt returen, dokumenteres returen av en returordre. Denne returordren blir fokuspunktet i den interne behandlingen av det returnerte produktet. Illustrasjonen nedenfor viser fremgangsmåten for å opprette en returordre.  

[![Fremgangsmåte for å opprette en returordre](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Opprette et nytt returordrehode

Når du oppretter en returordre, må informasjonen i tabellen nedenfor inkluderes.

| Felt              | beskrivelse                                              | Kommentarer                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kundekonto   | En referanse til Kunder-tabellen                       | Du må angi en eksisterende kundekonto.                                                                                                                                                                                                                                                                                                  |
| Leveringsadresse   | Adressen som varen returneres til                 | Organisasjonens adressen brukes som standard. Hvis et bestemt lager er valgt i hodet, endres leveringsadressen til leveringsadressen til lageret. Du kan endre denne adressen på siden **Returordredetaljer**.                                                                                                  |
| Område/lager     | Stedet eller lageret som mottar det returnerte produktet | Leveringsadressen for returordren bestemmes basert på leveringsadressen til stedet eller lageret.                                                                                                                                                                                                                                 |
| Autorisasjonsreturnr.         | ID-en som er knyttet til returordren              | ARM-nummeret brukes som en alternativ nøkkel gjennom hele returordreprosessen. ARM-nummeret som tilordnes, er basert på ARM-nummerserien som er definert på siden **Kundeparametere**.                                                                                                                              |
| Frist           | Den siste datoen som en vare kan returneres               | Standardverdien beregnes som gjeldende dato pluss gyldighetsperioden. Hvis en retur for eksempel er gyldig i bare 90 dager fra datoen da returordren opprettes, og returordren ble opprettet i 1. mai, er verdien i feltet **30. juli**. Gyldighetsperioden er satt på siden **Kundeparametere**. |
| Kode for returårsak | Årsaken til at kunden returnerer produktet.          | Årsakskoden velges i listen over brukerdefinerte årsakskoder. Du kan oppdatere dette feltet når som helst.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Opprette returordrelinjer

Når du har fullført returhodet, kan du opprette returlinjer ved hjelp av én av følgende metoder:

-   Angi manuelt varedetaljer, antall og annen informasjon for hver returlinje.
-   Opprett en returlinje ved hjelp av funksjonen **Søk etter salgsordre**. Vi anbefaler at du bruker denne funksjonen når du oppretter en returordre. Funksjonen **Søk etter salgsordre** oppretter en referanse fra returlinjen tilbake til den fakturerte salgsordrelinjen, og henter linjedetaljer som varenummer, antall, pris, rabatt og kostnadsverdier fra salgslinjen. Referansen bidrar til å garantere at når produktet returneres til selskapet, blir det verdisatt til samme enhetskostnad som den ble solgt for. Referansen validerer også at returordrer ikke opprettes for et antall som er større enn antallet som ble solgt på fakturaen.

>Obs! Returlinjer som har en referanse til en salgsordre behandles som korrigeringer eller tilbakeføringer av salget. Hvis du vil ha mer informasjon, kan du se "Postere til finans" senere i dette emnet.

### <a name="charges"></a>Tillegg

Gebyrer og avgifter kan legges til ordrereturen ved hjelp av én eller flere av følgende metoder:

-   Du kan manuelt legge til tillegg i returordrehodet, returordrelinjen eller begge.
-   Tillegg kan legges automatisk til returordrehodet som en funksjon av returårsakskoden.
-   Tillegg kan legges automatisk til returordrelinjen basert på disposisjonskoden for linjen.

Tillegg legges automatisk til etter at en returårsakskoden eller disposisjonskoden er tilordnet linjen. Hvis årsakskoden endres senere, fjernes ikke det eksisterende tillegget, men et nytt tillegg kan legges til basert på den nye årsakskoden. Når du legger til tillegg i returordrelinjer, blir tillegg som beregnes som en prosent av linje- eller ordreverdien negativ når linjen eller linjeordren er negativ, med mindre prosentandelen også et et negativt tall. Et tillegg som har en negativ verdi representerer en kreditnota til kunden.

### <a name="return-reason-codes"></a>Koder for returårsaker

Ved å bruke årsakskoder for returer, kan du bidra til å gjøre det enklere å analysere returmønstre. Årsakskoder gir informasjon om hvorfor en kunde vil returnere varer. Noen organisasjoner har mange årsakskoder. Disse organisasjon kan gruppere årsakskodene i årsakskodegrupper for å få en bedre oversikt og akkumulert rapportering.

### <a name="disposition-codes-and-disposition-actions"></a>Disposisjonskoder og -handlinger

Et viktig trinn i returordreprosessen er å tilordne en disposisjonskode til returordrelinjen som en del av ankomstregistrering. Disposisjonskoden bestemmer følgende informasjon:

-   **Økonomiske konsekvenser** – Skal kunden krediteres for de returnerte varene, og skal tillegg legges til i returordrelinjen?
-   **Disposisjonen av den returnerte varen** – Skal varen legges tilbake i beholdningen, skal den kasseres eller skal den returneres til kunden?
-   **Logistikken for den returnerte varen** – Skal det utstedes en erstatningsvare til kunden?

I tillegg til å bestemme hvordan de returnerte skal disponeres, kan disposisjonskoder føre til at det brukes tillegg i returlinjen. De kan også brukes til å gruppere returer for statistisk analyse. Disposisjonskoder defineres som en del av oppsettet av returordrer. Hver disposisjonskode må imidlertid referere til én av de innebygde disposisjonshandlingene. Tabellen nedenfor viser de innebygde disposisjonskodene og handlingene deres. **Viktig!** Hvis en vare ikke skal returneres, men kunden fortsatt skal krediteres, tilordnes disposisjonskode **Bare kreditering** til returlinjen.

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
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassering av varen posteres til finans.</li>
</ul></td>
<td>Varen skal ikke returneres. Denne disposisjonshandlingen brukes i følgende tilfeller:
<ul>
<li>Det er tilstrekkelig tillit mellom partene.</li>
<li>Kostnaden for retur av defekt vare er hindre deg.</li>
<li>Varene kan ikke tilbakeføres til beholdningen. Det kreves ingen fysisk retur på grunn av andre forhold.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditt</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Lagerverdien økes med kostnaden for den returnerte varen.</li>
</ul></td>
<td>Varen returneres og legges tilbake i beholdningen.</td>
</tr>
<tr class="odd">
<td>Erstatt og krediter</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Lagerverdien økes med kostnaden for den returnerte varen.</li>
<li>En separat salgsordre for en erstatning opprettes og håndteres separat.</li>
</ul></td>
<td>Varen returneres og legges tilbake i beholdningen.</td>
</tr>
<tr class="even">
<td>Erstatt og kasser</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassering av varen posteres til finans.</li>
<li>En separat salgsordre for en erstatning opprettes og håndteres separat.</li>
</ul></td>
<td>Varen returneres og kasseres.</td>
</tr>
<tr class="odd">
<td>Returner til kunde</td>
<td>Ingen, unntatt gebyrer eller avgifter.</td>
<td>Vare returneres, men sendes tilbake til kunden etter inspeksjon. Denne disposisjonshandlingen kan brukes hvis varen er skadet med hensikt, eller hvis garantien er ugyldig.</td>
</tr>
<tr class="even">
<td>Svinn</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller avgifter.</li>
<li>Tap fra kassering av varen posteres til finans.</li>
</ul></td>
<td>Varen returneres eller kasseres.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Ankomst på lageret for inspeksjon
Før du kan motta returnerte varer fysisk til lager ved å bokføre en følgeseddel, må varene gå gjennom ankomstregistreringen og en valgfri inspeksjon. Illustrasjonen nedenfor gir en oversikt over ankomstprosessen. Avsnittene nedenfor beskriver hvert enkelt trinn som er vist i illustrasjonen.  

[![Ankomstprosessen](./media/salesreturn03.png)](./media/salesreturn03.png)  

Prosessen har flere andre variasjoner som ikke omtales i dette emnet. Her er noen av disse variasjonene:

-   Ikke bruk listen **Ankomstoversikt** til å opprette en ankomstjournal. Opprett i stedet ankomstjournalen manuelt. Returordrer vil ha **Salgsordre** som referanse.
-   Hvis du bruker lagerstyring, genererer du palltransporter. Returlinjen vil ha statusen **Ankommet** under palltransporten.
-   Registrer mottaket av den returnerte varen direkte fra returordrelinje, ved hjelp av **Registrering**-funksjonen.

Under ankomstprosessen integreres returer med den generelle prosessen for lagerankomst. Ankomstprosessen støtter også oppretting av karanteneordrer for returnerte varer som må gjennomgå en egen undersøkelse.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identifisere produkter i listen for ankomstoversikt

Siden **Ankomstoversikt** viser en liste over alle planlagte innkommende ankomster. 
>Obs! Ankomster fra returordrer må behandles separat fra andre typer ankomsttransaksjoner. Når du har identifisert en innkommende pakke på siden **Ankomstoversikt** (for eksempel ved hjelp av det medfølgende ARM-dokumentet), går du til handlingsruten og klikker på **Start ankomst** for å opprette og starte en ankomstjournal som samsvarer med ankomsten.

### <a name="edit-the-arrival-journal"></a>Redigere ankomstjournalen

Ved å sette alternativet **Karantenestyring** til **Ja**, kan du opprette en karanteneordre for returlinjen. Hvis en linje er sendt til karantene for inspeksjon, kan du ikke angi en disposisjonskode. 
 
Hvis du setter alternativet **Karantenestyring** til **Ja** i varens lagermodellgruppe, vil alternativet **Karantenestyring** på siden **Journallinjer** bli merket for ankomstjournallinjer og kan ikke endres. Hvis linjen sendes til karantene, må du angi riktig karantenelager. 

Hvis ankomstlinjen ikke sendes til inspeksjon, må lagerankomstassistenten angi disposisjonskoden direkte på ankomstjournallinjen og deretter postere ankomstjournalen. Hvis den samme disposisjonskoden ikke skal tilordnes hele antallet i returlinjen, eller hvis hele antallet i linjen ikke er mottatt, må du dele linjen. Når du deler en ankomstjournallinje, deler du også returlinjen (**SalesLine**) og oppretter en ny parti-ID. Du kan dele linjen ved å redusere antallet i ankomstjournallinjen. Når journalen posteres, opprettes en ny returlinje som har statusen **Forventet** for restantallet. Du kan også dele linjen ved å klikke på **Funksjoner** &gt; **Del**.

### <a name="process-the-quarantine-order"></a>Behandle karanteneordren

Hvis de returnerte produktene sendes til inspeksjon i karantenelageret, fullføres eventuell tilleggsbehandling i en karanteneordre. Det opprettes én karanteneordre for hver ankomstlinje som sendes til karantene. Disposisjonskoden angir resultatet av inspeksjonsprosessen. 

Du kan dele en karanteneordre på samme måte som du kan dele ankomstjournalen. Hvis du deler karanteneordren, fører det til en tilsvarende deling av returlinjen. Når disposisjonskoden er angitt, må du fullføre karanteneordren ved hjelp av funksjonen **Slutt** eller **Ferdigmeld**. Hvis du velger **Ferdigmeld**, opprettes en ny ankomst i den angitte lageret. Du kan deretter behandle denne ankomsten ved hjelp av siden **Ankomstoversikt**. 

Hvis ankomsten stammer fra en karanteneordre, kan du ikke endre disposisjonskoden som tilordnes under inspeksjon. Hvis du fullfører karanteneordren ved hjelp av **Slutt**-funksjonen, registreres partiet automatisk. Noen ganger kan en vare sendes tilbake fra karantene til forsendelses- og mottaksavdelingen. Karantenekontrolløren vet for eksempel ikke hvor du vil lagre varen på lageret. I slike tilfeller må den tilsvarende følgeseddelen oppdateres for riktig å registrere og gjøre noe med disposisjonskoden som er angitt på grunn av karantenen. 

Bekreftelse av mottak kan sendes til kunden når returlinjen er registrert. Rapporten **Returbekreftelse** ligner på returordredokumentet. Rapporten **Returbekreftelse** blir ikke journalført eller registrert i systemet, og det er ikke et obligatorisk trinn i returordreprosessen.

## <a name="replace-a-product"></a>Erstatte et produkt
Det finnes to metoder for håndtering av produkterstatning:

-   **Forskuddserstatning** – Erstatte et produkt før det returnerte produktet er mottatt fra kunden.
-   **Erstatning etter disposisjonskode** – Opprett automatisk en ny ordrelinje for erstatning.

### <a name="up-front-replacement"></a>Forskuddserstatning

Ved forskuddserstatning kan erstatningsvaren leveres til kunden før varen er returnert. Denne metoden er nyttig hvis for eksempel varen er en maskindel som ikke kan fjernes med mindre en reservedel kan brukes i stedet, eller hvis du bare vil at kunden skal ha erstatningsproduktet så snart som mulig. Forskuddserstatningsordren er en uavhengig salgsordre. Informasjonen i hodet er initialisert fra kunden, og linjeinformasjonen er initialisert fra returordren. Du kan redigere, behandle og slette erstatningsordren uavhengig av returordren. Når du sletter en erstatningsordre, får du en melding om at ordren ble opprettet som en erstatningsordre. Illustrasjonen nedenfor viser prosessen for forskuddserstatning.  

![Forskuddserstatningsprosess](./media/SalesReturn04.png)

Returorden inneholder en referanse til erstatningsordren. Hvis en forskuddserstatning opprettes for en returordre før den defekt vare returneres, kan du ikke velge disposisjonskoder for erstatning etter at den defekte vare er returnert.

### <a name="replacement-by-disposition-code"></a>Erstatning etter disposisjonskode

Hvis du leverer en erstatningsvare til kunden og du bruker disposisjonshandlingen **Erstatt og kasser** eller **Erstatt og krediter** i returordren, bruker du prosessen som vises i illustrasjonen nedenfor.  

![Erstatningsprosess når en disposisjonskode brukes](./media/SalesReturn05.png)

Erstatningsvaren sendes ved hjelp av en uavhengig salgsordre, erstatningsordren. Denne salgsordren blir opprettet når følgeseddelen for returordren genereres. Ordrehodet bruker informasjon fra kunden som det refereres til i returordrehodet. Linjeinformasjonen som samles inn fra informasjonen som er angitt på siden **Erstatningsvare**. Siden **Erstatningsvare** må fylles ut for linjer som har disposisjonhandlinger som begynner med ordet "erstatt". Verken antallet eller identiteten til erstatningsvaren er imidlertid validert eller begrenset. Denne virkemåten tillater tilfeller der kunden ønsker den samme varen, men i en annen konfigurasjon eller størrelse, og også tilfeller der kundene vil ha et helt annen vare. Som standard angis en identisk vare på siden **Erstatningsvare**. Du kan imidlertid velge en annen vare, forutsatt at funksjonen er definert. 

>Obs! Du kan redigere og slette erstatningssalgsordren etter at den er opprettet.

## <a name="generate-a-packing-slip"></a>Generere en følgeseddel
Før returnerte varer kan mottas til lager, må du oppdatere følgeseddelen for ordren som varene tilhører. På samme måte som fakturaoppdateringsprosessen er en oppdatering av finanstransaksjonen, er oppdateringsprosessen for følgeseddelen den fysiske oppdateringen av lagerposten. Denne prosessen utfører med andre ord endringene i beholdningen. Når det gjelder returer, implementeres trinnene som er tilordnet til disposisjonshandlingen, når følgeseddelen oppdateres Når du genererer følgeseddelen, oppstår følgende hendelser:

-   I lageret brukes standardprosessen til å utføre et fysisk mottak. Finansposteringer genereres hvis lagermodellgruppen (**Poster aktuell beholdning**) og kundeparameterne (**Poster følgeseddel i finans**) er angitt riktig.
-   Varer som er merket med en disposisjonshandling som inneholder ordet "svinn", kasseres, og lagertap posteres til finans.
-   Varer som er merket med disposisjonshandlingen **Returner til kunde** er mottatt og levert til kunden. Disse varene har ingen nettoinnvirkning på beholdningen.
-   Det opprettes en erstatningssalgsordre. Denne salgsordren er basert på informasjon på siden **Erstatningsvare**.

Du kan generere følgeseddelen bare for linjer som har returstatusen **Registrert**, og bare for hele antallet i returlinjen. Hvis flere linjer på returordren har statusen **Registrert**, kan du generere følgeseddelen for et delsett av linjene ved å slette de andre linjene fra siden **Poster følgeseddel**. 

Delvise returer defineres som returordrelinjer, ikke som returordreforsendelser. Det vil si at hvis du mottar hele antallet som er angitt på én returordrelinje, men ikke mottar noe fra de andre linjene i returordren, er leveringen ikke en delvis levering. Hvis en returordrelinje krever at ti enheter av en vare returneres, men du bare mottar fire enheter, er dette imidlertid en delvis levering. Hvis ikke alle forventede returnerte varer har ankommet, kan du sette forsendelsen til side og vente til resten av det returnerte antallet ankommer. Du kan også registrere og postere det delvise antallet. Som en del av prosessen for postering av følgeseddelen kan du tilordne følgeseddelens referansenummer fra kundens forsendelsesdokumenter, til ordrelinjene. Denne tilknytningen er valgfri og er bare til referanseformål. Det opprettes ikke transaksjonsoppdateringer. 

Du kan som regel hoppe over følgeseddelprosessen og gå direkte til fakturering. I slike tilfeller vil trinnene som du ville ha utført under generering av følgeseddelen, bli fullført under fakturering.

## <a name="generate-an-invoice"></a>Generer en faktura
Selv om siden **Returordre** inneholder informasjonen og handlingene som kreves for å håndtere de spesielle logistikkdelene av returordren, må du bruke siden **Salgsordre** for å fullføre faktureringsprosessen. Organisasjonen kan deretter fakturere returordrer og salgsordrer samtidig, og den samme personen kan fullføre faktureringsprosessen etter behov. Hvis du vil vise returordren fra siden **Salgsordre**, klikker du på koblingen for salgsordrenummeret for å åpne den tilknyttede salgsordren. Du kan også finne returordren på siden **Alle salgsordrer**. Returordrer er salgsordrer som har ordretypen **Returordre**.

### <a name="credit-correction"></a>Kreditrettelse

Som en del av faktureringsprosessen, kan du kontrollere at eventuelle tilleggsgebyrer er riktige. Hvis du vil at finansposteringer skal bli korrigeringer (Storno), bør du vurdere å bruke alternativet **Kreditrettelse** i kategorien **Annet** på siden **Postering av faktura**, når du bokfører fakturaen eller kreditnotaen. 
>Obs! Som standard er alternativet **Kreditrettelse** aktivert hvis alternativet **Kreditnota som rettelse** på siden **Kundeparametere** har blitt aktivert. Vi anbefaler imidlertid at du ikke posterer returer med Storno.

## <a name="create-intercompany-return-orders"></a>Opprette konserninterne returordrer
Returordrer kan fullføres mellom to selskaper i organisasjonen. Følgende scenarier støttes:

-   Enkle konserninterne returer mellom to selskaper som deltar i en konsernintern relasjon
-   En konsernintern kjede som opprettes når en kundereturordre opprettes i det selgende selskapet
-   En konsernintern kjede som opprettes når en leverandørreturordre opprettes i det kjøpende selskapet
-   Leveringsreturer for direktelevering mellom en ekstern kunde og to selskaper som deltar i en konsernintern relasjon

### <a name="setup"></a>Konfigurer

Illustrasjonen nedenfor er minimumsoppsettet som kreves for to selskaper for å delta i en konserninterne forhold og dra nytte av konsernintern handel.  

![Minimumsoppsett](./media/SalesReturn06.png)

I scenariet nedenfor er CompBuy det kjøpende selskapet, og CompSell er det selgende selskapet. Vanligvis leverer det selgende selskapet varer til det kjøpende selskapet, eller i scenarier med direktelevering, direkte til sluttkunden. I CompBuy er leverandøren IC\_CompSell definert som et konserninternt sluttpunkt som er knyttet til selskapet CompSell. I CompSell er kunden IC\_CompBuy samtidig definert som et konserninternt sluttpunkt som er knyttet til selskapet CompBuy. Riktige detaljer for handlingpolicy og verditilordninger må defineres i begge selskapene. I scenarier med direktelevering blir en konsernintern returordre, som også er en konsernintern salgsordre, opprettet i det selgende selskapet. Autorisasjonsreturnummeret for den konserninterne returordren kan hentes fra ARM-nummersekvensen i CompSell, eller det kan kopieres fra ARM-nummeret som er tilordnet til den opprinnelige returordren i CompBuy. ARM-nummerinnstillingene i handlingspolicyen **PurchaseRequisition** i CompBuy bestemmer disse handlingene. Hvis autorisasjonsreturnummeret synkroniseres, bør du planlegge å redusere risikoen for antall konflikter hvis de to selskapene bruker den samme nummerserien.

### <a name="simple-intercompany-returns"></a>Enkle konserninterne returordrer

Dette scenariet omfatter to selskaper i samme organisasjon, som vist i illustrasjonen nedenfor.  

![Enkel konsernintern retur](./media/SalesReturn07.png)

Ordrekjeden kan opprettes når det opprettes en bestillingsretur for leverandøren i det kjøpende selskapet eller en ordreretur fra kunden som er opprettet i det selgende selskapet. Finance and Operations oppretter den tilsvarende ordren i det andre selskapet, og sørger for at hode- og linjeinformasjon på leverandørreturordren gjenspeiler innstillingene på kundereturordren. Returordren som er opprettet, kan inkludere eller utelukke referansen (**Søk etter salgsordre**) til en eksisterende kundefaktura. Følgesedler og fakturaer for de to bestillingene kan behandles enkeltvis. Du behøver for eksempel ikke generere en følgeseddel for leverandørreturordren før du genererer følgeseddelen for kundereturordren.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Leveringsreturer for direktelevering mellom tre parter

Dette scenariet kan opprettes hvis et tidligere salg av typen **Direktelevering** er fullført, og hvis en faktura mot kunden finnes i selskapet som samhandler med kunden. I illustrasjonen nedenfor har selskapet CompBuy tidligere solgt og fakturert produkter til kunden Extern. Produktene er levert direkte fra selskapet CompSell til kunden via en konsernintern ordrekjede.  

![Leveringsreturer for direkte levering mellom tre parter](./media/SalesReturn08.png)

Hvis kunden Ekstern vil returnere produktene, opprettes en returordre (RMA02) for kunden i selskapet CompBuy. Hvis du vil opprette den konserninterne kjeden, må returordren merkes for direktelevering. Når du bruker funksjonen **Søk etter salgsordre** til å velge kundefakturaen skal returneres, opprettes en konsernintern ordrekjede som består av følgende dokumenter:

-   **Opprinnelig returordre**: RMA02 (selskapet CompBuy)
-   **Bestilling**: PO02 (selskapet CompBuy)
-   **Konsernintern returordre**: ARM\_00032 (selskapet CompSell)

Når den konserninterne kjeden for direktelevering er opprettet, må all fysiske håndtering og behandling av returnerer være i konteksten for den konserninterne returordren, ARM\_00032 i selskapet CompSell. Produktene kan ikke mottas i selskapet CompBuy. Når en disposisjonskode knyttes til den konserninterne returordren, synkroniseres den med den opprinnelige returordren for å tillate riktig fakturering av den opprinnelige ordren.

## <a name="post-to-the-ledger"></a>Postere til finans
Finansposteringer som genereres når returordren faktureres, påvirkes av noen viktige innstillinger og parametere:

-   **Returkostpris** – For andre lagermodeller enn **Standardkost** bestemmer **Returkostpris**-parameteren kostnadene for varen når den godtas tilbake til beholdningen eller kasseres. Hvis du vil beregne en riktig verdisetting av beholdningen, er det viktig at du angir **Returkostpris**-parameter på riktig måte. Hvis du bruker funksjonen **Søk etter salgsordre** til å opprette en returordrelinje som har en referanse til en kundefaktura, er **Returkostpris**-verdien lik kostprisen for varen som selges. Hvis ikke, kommer kostprisverdien fra vareoppsettet eller kan angis manuelt.
-   **Kreditrettelse/Storno** – Parameteren **Kreditrettelse** på siden **Postering av faktura**, bestemmer om posteringer skal registreres som positive (debet/kredit) posteringer, eller som korrigerende, negative poster.

I eksemplene nedenfor representeres returkostprisen som **Lagerkostpris**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Eksempel 1: Returordren refererer ikke til en kundefaktura

Returordren refererer ikke til en kundefaktura. Den returnerte varen krediteres. Parameteren **Kreditrettelse** velges ikke når returordre, faktura eller kreditnota genereres.  

![Returordre refererer ikke til en kundefaktura](./media/SalesReturn09.png)  

>Obs! Hovedprisen for varen brukes som standardverdi for **Returkostpris**-parameteren. Standardprisen er forskjellig fra kostprisen ved lageravgang. Derfor er implikasjonen at et tap på 3 er påløpt. I tillegg inneholder ikke returordren rabatten som ble gitt til kunden i salgsordren. Derfor oppstår det en overskytende kreditering.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Eksempel 2: Kreditrettelse velges for returordren

Eksempel 2 er den samme som eksempel 1, men **Kreditrettelse**-parameteren velges når returordrefakturaen genereres.  

![Returordre der krediteringskorrigering er valg  ](./media/SalesReturn10.png)  

>Obs! Finansposteringer angis som negative korrigeringer.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Eksempel 3: Returordrelinjen opprettes ved hjelp av funksjonen Søk etter salgsordre.

I dette eksemplet opprettes returordrelinjen ved hjelp av funksjonen **Søk etter salgsordre**. **Kreditrettelse**-parameteren velges ikke når fakturaen opprettes.  

![Returordrelinje som opprettes ved hjelp av funksjonen Søk etter salgsordre  ](./media/SalesReturn11.png)  

>Obs! **Rabatt** og **Returkostpris** er riktig angitt. Derfor oppstår derfor en nøyaktig tilbakeføring av kundefakturaen.




