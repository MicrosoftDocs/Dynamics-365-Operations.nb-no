---
title: Fleksibel retningslinje for dimensjonsreservasjon på lagernivå
description: Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar virksomheter som selger partisporede produkter og kjører logistikken som WMS-aktiverte operasjoner, reservere spesifikke partier for kundesalgsordrer, selv om reservasjonshierarkiet som er assosiert med produktene, ikke tillater reservasjon av spesifikke partier.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b9bd4e67ed64218f9c4ac87bd143f73680af9ac4
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017650"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Fleksibel retningslinje for dimensjonsreservasjon på lagernivå

[!include [banner](../includes/banner.md)]

Når et hierarki for beholdningsreservasjon av "Parti under\[plassering\]"-typen er assosiert med produkter, kan bedrifter som selger partisporede produkter og kjører logistikken som operasjoner som er aktivert for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere spesifikke partier av disse produktene for kundesalgsordrer.

På lignende måte kan ikke bestemte lisensplater reserveres for produkter i salgsordrer når disse produktene er knyttet til standard reservasjonshierarki.

Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar disse virksomhetene reservere spesifikke partier eller lisensalter, selv når produktene er assosiert med et "Parti under\[plassering\]"-reservasjonshierarki.

## <a name="inventory-reservation-hierarchy"></a>Beholdningsreservasjonshierarki

Dette avsnittet oppsummerer det eksisterende beholdningsreservasjonshierarkiet.

Beholdningsreservasjonshierarkiet dikterer følgende: For lagringsdimensjoner angir etterspørselsordren de obligatoriske dimensjonene for sted, lager og beholdningsstatus, mens lagerlogikken har ansvar for å tilordne et sted til de forespurte kvantitetene og for å reservere stedet. Med andre ord gjelder følgende: I samhandlingene mellom etterspørselsordren og lagervirksomheten, forventes etterspørselsordren å indikere hvor ordren må sendes fra (det vil si hvilket sted og lager). Lageret er deretter avhengig av logikken for å finne påkrevd kvantitet i lagerlokalene.

For å gjenspeile virksomhetens driftsmodell er sporingsdimensjoner (parti- og serienumre) imidlertid gjenstand for mer fleksibilitet. Et beholdningsreservasjonshierarki kan omfatte scenarioer der følgende betingelser gjelder:

- Virksomheten avhenger av lagervirksomheten når det gjelder administrering av plukking av kvantiteter som har parti- eller serienumre, etter at kvantitetene er funnet i lagerlokalene. Denne modellen henvises ofte til som *Parti under\[plassering\]*. Den brukes vanligvis når et produkts parti- eller serienummeridentifikasjon ikke er viktig for kundene som legger inn etterspørselen hos det selgende selskapet.
- Hvis parti- eller serienumre er en del av en kundes ordrespesifikasjon, og de registreres i etterspørselsordren, blir lageroperasjonene som finner kvantitetene på lageret, begrenset av de spesifikke forespurte numrene og har ikke lov til å endre dem. Denne modellen henvises til som *Parti over\[plassering\]*.

I disse scenarioene er utfordringen at bare ett beholdningsreservasjonshierarki kan tilordnes til hvert utgitte produkt. For at WMS skal kunne håndtere sporede elementer gjelder derfor følgende: Etter at hierarkitildelingen bestemmer når parti- eller serienummeret skal reserveres (enten når etterspørselsordren tas imot eller under lagerplukkearbeidet), kan denne timingen ikke endres på et ad hoc-grunnlag.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Fleksibel reservasjon for partisporede varer

### <a name="business-scenario"></a>Forretningsscenario

I dette scenarioet bruker et selskap en beholdningsstrategi der fullførte varer spores etter partinumre. Dette selskapet bruker også WMS-arbeidsbelastning. Fordi denne arbeidsbelastningen har velutstyrt logikk for planlegging og drift av lagerplukkings- og forsendelsesoperasjoner for partiaktiverte varer, er de fleste av de fullførte varene tilknyttet et "Parti under\[plassering\]"-beholdningsreservasjonshierarki. Fordelen med denne typen driftsoppsett er at beslutninger (som faktisk er reservasjonsbeslutninger) om hvilke partier du skal plukkes, og hvor de skal settes på lageret, utsettes til lagerplukkingsoperasjonene starter. De utføres ikke når kundens ordre legges inn.

Selv om "Parti under\[plassering\]"-reservasjonshierarkiet tjener selskapets forretningsmessige mål godt, krever mange av selskapets etablerte kunder det samme partiet som de kjøpte tidligere, når de bestiller produkter på nytt. Derfor leter selskapet etter fleksibilitet i måten partireservasjonsreglene håndteres på, slik at det – avhengig av kundenes etterspørsel etter samme vare – oppstår følgende atferd:

- Et partinummer kan registreres og reserveres når ordren tas imot av salgsprosessoren, og det kan ikke endres under lageroperasjoner og/eller tas imot av andre krav. Denne atferden er med på å garantere at partinummeret som ble bestilt, sendes til kunden.
- Hvis partinummeret ikke er viktig for kunden, kan lageroperasjonen bestemme et partinummer under plukkearbeid, etter at salgsordreregistrering og reservasjon er utført.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Tillate reservering av et bestemt parti i salgsordren

For å imøtekomme ønsket fleksibilitet i partireservasjonsatferden for varer som er assosiert med et "Parti under\[plassering\]"-beholdningsreservasjonshierarki, må beholdningsledere merke av i **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen for **Partinummer** -nivået på **Beholdningsreservasjonshierarkier** -siden.

![Gjøre beholdningsreservasjonshierarkiet fleksibelt](media/Flexible-inventory-reservation-hierarchy.png)

Når **Partinummer** -nivået i hierarkiet er valgt, vil alle dimensjoner over det nivået og opp gjennom **Plassering** -nivået valgt automatisk. (Som standard er alle dimensjoner over **Plassering** -nivået forhåndsvalgt.) Denne atferden gjenspeiler logikken der alle dimensjoner i området mellom partinummeret og plasseringen også reserveres automatisk etter at du har reservert et spesifikt partinummer på ordrelinjen.

> [!NOTE]
> **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen gjelder bare for reservasjonshierarkinivåer som er under dimensjonen til lagerplasseringen.
>
> **Partinummer** og **Nummerskilt** er de eneste nivåene i hierarkiet som er åpne for den fleksible reservasjonsretningslinjen. Med andre ord kan du ikke merke av for **Tillat reservasjon på etterspørselsordre** for nivået **Plassering** eller **Serienummer**.
>
> Hvis reservasjonshierarkiet inkluderer serienummerdimensjonen (som alltid må være under **Partinummer** -nivået), og hvis du har aktivert partispesifikk reservasjon for partinummeret, vil systemet fortsette å håndtere serienummerreservasjon og plukkeoperasjoner, basert på reglene som gjelder for "Serienr. under\[plassering\]"-reservasjonsretningslinjen.

Du kan når som helst tillate partispesifikk reservasjon for et eksisterende "Parti under\[plassering\]"-reservasjonshierarki i distribusjonen. Denne endringen påvirker ikke reservasjoner og åpent lagerarbeid som ble opprettet før endringen fant sted. **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen kan imidlertid ikke tømmes hvis det finnes beholdningstransaksjoner med utstedelsestypen **Reservert bestilt** , **Reservert fysisk** eller **Bestilt** for én eller flere varer som er tilknyttet til dette reservasjonshierarkiet.

> [!NOTE]
> Hvis eksisterende reservasjonshierarki for en vare ikke tillater partispesifikasjon på ordren, kan du tilordne den på nytt til et reservasjonshierarki som tillater partispesifikasjon, forutsatt at hierarkinivåstrukturen er lik i begge hierarkier. Bruk **Endre reservasjonshierarki for varer** -funksjonen til å gjennomføre omtilordningen. Denne endringen kan være relevant når du vil forhindre fleksibel partireservering for et delsett av partisporede elementer, men tillate den for resten av produktporteføljen.

Uavhengig av om du har merket av i **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen, gjelder følgende: Hvis du ikke vil reservere et spesifikt partinummer for varen på en ordrelinje, vil standard lagerstyringslogikk som er gyldig for et "Parti under\[plassering\]"-reservasjonshierarki, fremdeles gjelde.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Reservere et bestemt partinummer for en kundeordre

Etter at "Parti under\[plassering\]"-beholdningsreservasjonshierarki for en partisporet vare er satt opp for å tillate reservasjon av spesifikke partinumre på salgsordrer, kan salgsordreprosessorer ta imot kundeordrer for samme vare på en av følgende måter, avhengig av kundens forespørsel:

- **Angi ordredetaljer uten å angi et partinummer** – Denne fremgangsmåten skal brukes når produktets partispesifikasjon ikke er viktig for kunden. Alle eksisterende prosesser som er knyttet til håndtering av en ordre av denne typen i systemet, forblir uendret. Ingen ekstra hensyn kreves fra brukerne.
- **Angi ordredetaljer og reserver et bestemt partinummer** – Denne fremgangsmåten skal brukes når kunden ber om et bestemt parti. Vanligvis vil kunder be om et bestemt parti når de ombestiller et produkt som de har kjøpt tidligere. Denne typen partispesifikk reservasjon omtales som *Ordreigangsatt reservasjon*.

Følgende sett med regler er gyldig når kvantiteter behandles, og et partinummer er bundet til en bestemt ordre:

- For å tillate reservasjon av et spesifikt partinummer for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen. Dette området inkluderer vanligvis nummerskiltdimensjonen.
- Plasseringsdirektiver brukes ikke når det opprettes plukkarbeid for en salgslinje som bruker ordrebundet partireservering.
- Under lagerbehandling av arbeid for ordrebundne partier har verken brukeren eller systemet lov til å endre partinummeret. (Denne behandlingen omfatter unntakshåndtering.)

Det følgende eksempelet viser ende-til-ende-flyten.

## <a name="example-scenario-batch-number-allocation"></a>Eksempelscenario: Tildeling av partinummer

For dette eksempelet må demonstrasjonsdata være installert, og du må bruke **USMF** -demonstrasjonsdataselskapet.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Sette opp et beholdningsreservasjonshierarki for å tillate partispesifikk reservasjon

1. Gå til **Lagerstyring** \> **Oppsett** \> **Beholdning \> Reservasjonshierarki**.
2. Velg **Ny**.
3. I **Navn** -feltet skriver du inn et navn (for eksempel **BatchFlex** ).
4. I **Beskrivelse** -feltet skriver du inn en beskrivelse (for eksempel **Parti under fleksibelt** ).
5. I **Valgt** -feltet velger du **Serienummer** og **Eier** , og velg deretter venstre pilknapp for å flytte dem til **Tilgjengelig** -feltet.
6. Velg **OK**.
7. I raden for **Partinummer** -dimensjonsnivået merker du av i **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen. **Nummerskilt** - og **Plassering** -nivåene velges automatisk, og du kan ikke fjerne avmerkingen i avmerkingsboksene for dem.
8. Velg **Lagre**.

### <a name="create-a-new-released-product"></a>Opprette et nytt frigitt produkt

1. Angi de tre hoveddataparameterne for produktet ved å bruke disse verdiene:

    - I **Lagringsdimensjonsgruppe** -feltet velger du **Lager**.
    - I **Sporingsdimensjonsgruppe** -feltet velger du **Parti-fys**.
    - I **Reservasjonshierarki** -feltet velger du **BatchFlex**.

2. Opprett to partinumre, for eksempel **B11** og **B22**.
3. Legg til varekvantiteter i beholdningen på lager ved hjelp av følgende verdier:

    | Lager | Partinummer | Lokasjon | Nummerskilt | Antall |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Ingen          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Angi salgsordredetaljer

1. Gå til **Salg og markedsføring** \> **Salgsordrer** \> **Alle salgsordrer**.
2. Velg **Ny**.
3. På salgsordretoppteksten, i **Kundekonto** -feltet angir du **US-003**.
4. Legg til en linje for den nye varen, og angi **10** som kvantiteten. Sørg for at **Lager** -feltet er satt til **24**.
5. På **Salgsordrelinjer** -hurtigfanen velger du **Beholdning** , og går deretter til **Vedlikehold** -gruppen og velger **Partireservasjon**. **Partireservasjon** -siden viser en liste over partier som er tilgjengelige for reservasjon for ordrelinjen. For dette eksempelet viser den en kvantitet på **20** for partinummer **B11** og en kvantitet på **10** for partinummer **B22**. Vær oppmerksom på at **Partireservasjon** -siden ikke kan åpnes fra en linje hvis varen på denne linjen er assosiert med "Parti under\[plassering\]"-reservasjonshierarki med mindre den er satt opp for å tillate partispesifikk reservasjon.

    > [!NOTE]
    > Hvis du vil reservere et bestemt parti for en salgsordre, må du bruke **Partireservasjon** -siden.
    >
    > Hvis du oppgir partinummeret direkte på salgsordrelinjen, vil systemet fungere som om du skrev inn en spesifikk partiverdi for en vare som er underlagt "Parti under\[plassering\]"-reservasjonsretningslinjen. Når du lagrer linjen, får du en advarselmelding. Hvis du bekrefter at partinummeret skal angis direkte på ordrelinjen, vil ikke linjen bli håndtert av den vanlige lagerbehandlingslogikken.
    >
    > Hvis du reserverer kvantiteten fra **Reservasjon** -siden, vil ikke noe spesifikt parti bli reservert, og kjøringen av lageroperasjoner for linjen vil følge reglene som gjelder under "Parti under\[plassering\]"-reservasjonsretningslinjen.

    Generelt fungerer og samhandles denne siden med på samme måte som den fungerer og samhandles med for varer som har et tilknyttet reservasjonshierarki i "Parti over\[plassering\]"-typen. Følgende unntak gjelder imidlertid:

    - **Partinumre bundet til kildelinjen** -hurtigfanen viser partinumrene som er reservert for ordrelinjen. Partiverdiene i rutenettet vises gjennom oppfyllingssyklusen til ordrelinjen, inkludert lagerbehandlingsstadiene. På **Oversikt** -hurtigfanen vises vanlig bestillingslinjereservasjon (det vil si reservasjon som utføres for dimensjonene over **Plassering** -nivået) derimot i rutenettet opp til tidspunktet lagerarbeidet opprettes på. Deretter overtar arbeidsenheten linjereservasjonen, og linjereservasjonen vises ikke lenger på siden. **Partinumre bundet til kildelinjen** -hurtigfanen bidrar til å garantere at salgsordreprosessoren kan vise partinumrene som ble bundet til kundens ordre, når som helst i løpet av livssyklusen, opp gjennom faktureringen.
    - I tillegg til å reservere et bestemt parti kan en bruker manuelt velge den partispesifikke plasseringen og nummerskiltet i stedet for å la systemet velge dem automatisk. Denne funksjonen er knyttet til utformingen av den ordreigangsatte partireservasjonsmekanismen. Som nevnt tidligere, gjelder følgende: Når et partinummer er reservert for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen. Derfor vil lagerarbeid ha de samme lagringsdimensjonene som ble reservert av brukerne som jobbet med ordrene, og det kan hende at det ikke alltid representerer varelagerplasseringen som er praktisk, eller til og med mulig, for plukkeoperasjoner. Hvis ordreprosessorer er klare over lagerbegrensningene, kan det være lurt manuelt å velge de spesifikke plasseringene og nummerskiltene når de reserverer et parti. I slike tilfeller må brukeren bruke **Visningsdimensjoner** -funksjonaliteten på sidetoppteksten og legge til plasseringen og nummerskiltet i rutenettet på **Oversikt** -hurtigfanen.

6. På **Partireservasjon** -siden velger du linjen for parti **B11** , og velger deretter **Reserver linje**. Det er ikke angitt noen logikk for tilordning av plasseringen og nummerskilt under automatisk reservasjon. Du kan angi kvantiteten manuelt i **Reservasjon** -feltet. Vær oppmerksom på at **Partinumre bundet til kildelinjen** -hurtigfanen, parti **B11** vises som **Bind**.

    ![Binde et spesifikt partinummer til en salgsordrelinje på Partireservasjon-siden](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Reservasjon av kvantiteten på en salgsordrelinje kan utføres på tvers av flere partier. På samme måte kan reservasjon av samme parti utføres mot flere plasseringer og nummerskilt (hvis nummerskilt er aktivert for plasseringene).
    >
    > Reservasjon av et bestemt parti for kvantiteten på en salgsordrelinje kan også være delvis. Den totale kvantiteten på 100 enheter kan for eksempel reserveres slik at et spesifikt parti bindes til 20 enheter, mens 80 enheter reserveres på stedet og lagernivåer for ethvert tilgjengelig parti. I dette tilfellet vil WMS håndtere plukkoperasjoner ved hjelp av to separate arbeidslinjer.

7. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**. Velg varen, og velg deretter **Administrer beholdning** \> **Vis** \> **Transaksjoner**.

    ![Ordreigangsatt reservasjon som lagertransaksjonstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. Gjennomgå varens lagertransaksjoner som er knyttet til salgsordrelinjereservasjonen.

    - En transaksjon der **Referanse** -feltet er satt til **Salgsordre** og **Utsted** -feltet er satt til **Reservert fysisk** , representerer ordrelinjereservasjonen for beholdningsdimensjonene over **Plassering** -nivået. I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene sted, lager og beholdningsstatus.
    - En transaksjon der **Referanse** -feltet er satt til **Ordreigangsatt reservasjon** og **Utsted** -feltet er satt til **Reservert fysisk** , representerer ordrelinjereservasjonen for det spesifikke partiet og alle beholdningsdimensjonene over det. I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene partinummer og plassering. I dette eksempelet er plasseringen **Bulk-001**.

9. I salgsordretoppteksten velger du **Lager** \> **Handlinger** \> **Frigi til lager**. Ordrelinjen er nå bølgete, og det opprettes en belastning og et arbeid.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Gjennomgå og behandle lagerarbeid som har ordreigangsatte partinumre

1. I **Salgsordrer** -hurtigfanen velger du **Lager** \> **Arbeidsdetaljer**.

    Arbeidet som håndterer plukkoperasjonen for partikvantiteter som er bundet til salgsordrelinjen, har følgende egenskaper:

    - For opprettelse av arbeid bruker systemet arbeidsmaler, men ikke plasseringsdirektiver. Alle standardinnstillingene som er definert for arbeidsmaler, for eksempel et maksimalt antall plukklinjer eller en bestemt måleenhet, brukes for å bestemme når nytt arbeid skal opprettes. Reglene som er assosiert med plasseringsdirektiver for identifisering av plukkplasseringer blir ikke vurdert, fordi den ordreigangsatte reservasjonen allerede angir alle beholdningsdimensjonene. Disse beholdningsdimensjonene inkluderer dimensjonene på lageroppbevaringsnivået. Derfor arver arbeidet disse dimensjonene uten å måtte sjekke plasseringsdirektiver.
    - Partinummeret vises ikke på plukklinjen (noe som også er tilfelle for arbeidslinjen som opprettes for en vare som har et tilknyttet "Parti over\[plassering\]"-reservasjonshierarki). I stedet vises "fra"-partinummeret og alle andre lagringsdimensjoner på arbeidslinjens arbeidsbeholdningstransaksjon som det henvises til fra de tilhørende beholdningstransaksjonene.

        ![Lagerbeholdningstransaksjon for arbeid som stammer fra ordreigangsatt reservasjon](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Etter at arbeidet er opprettet, blir varens beholdningstransaksjon der **Referanse** -feltet er satt til **Ordreigangsatt reservasjon** , fjernet. Beholdningstransaksjonen der **Referanse** -feltet er satt til **Arbeid** , inneholder nå den fysiske reservasjonen for alle beholdningsdimensjoner for kvantiteten.

        Lageroperasjoner kan fortsette å håndtere utførelsen av arbeidet på vanlig måte. Instruksjonene på mobilenheten vil imidlertid instruere arbeideren om å velge et bestemt partinummer. I lagermiljøer der plasseringene er nummerskiltkontrollert, gjelder følgende: Etter at en arbeider har nådd en plassering som lagrer det samme partiet på flere nummerskilt, kan han eller hun velge fra et hvilket som helst nummerskilt som ikke allerede er reservert (for eksempel av en annen ordreigangsatt reservasjon eller arbeid som stammer fra en reservasjon av denne typen.)

        Hvis det viser seg at det blir upraktisk å velge fra plasseringen som er spesifisert på arbeidslinjen, kan lageroperatørene bruke en av følgende handlinger for å omdirigere plukking av det spesifikke partiet fra en mer praktisk plassering:

        - Standardhandlingen **Overstyr plassering** på en mobilenhet (forutsatt at lagerarbeiderens **Tillat overstyring av plukkplassering** -innstilling er aktivert)
        - **Endre plassering** -handlingen på **Arbeidslistedetaljer** -siden. 

2. Fullfør plukking og plassering av arbeidet på mobilenheten.

    Antallet **10** for partinummer **B11** er nå valgt for salgsordrelinjen og plassert i **Båsdør** -plasseringen. På dette tidspunktet er det klart til å lastes på lastebilen og sendes til kundens adresse.

## <a name="flexible-license-plate-reservation"></a>Fleksibel nummerskiltreservering

### <a name="business-scenario"></a>Forretningsscenario

I dette scenariet bruker et firma lagerstyring og arbeidsbehandling, og håndterer belastningsplanlegging på nivået for individuelle paller/beholdere utenfor Supply Chain Management før arbeidet opprettes. Disse beholderne representeres av nummerskilt i lager dimensjonene. Derfor må spesifikke nummerskilt være forhåndstilordnet til salgsordrelinjer før plukkearbeidet utføres, for denne fremgangsmåten. Firmaet ser etter fleksibilitet i måten regler for nummerskiltreservasjon behandles på, slik at følgende virkemåter skjer:

- Et nummerskilt kan registreres og reserveres når ordren tas imot av salgsprosessoren, og det kan ikke tas imot av andre krav. Denne atferden er med på å garantere at numerskiltet som var planlagt, sendes til kunden.
- Hvis nummerskiltet ikke allerede er tilordnet til en salgsordrelinje, kan lagerpersonell velge et nummerskilt under plukkingen, etter at salgsordreregistreringen og reservering er fullført.

### <a name="turn-on-flexible-license-plate-reservation"></a>Aktivere fleksibel nummerskiltreservering

Før du kan bruke fleksibel nummerskiltreservering, må to funksjoner aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonene og aktivere dem hvis nødvendig. Du må aktivere funksjonene i følgende rekkefølge:

1. **Funksjonsnavn:** *Fleksibel dimensjonsreservasjonspolicy for lagernivå*
1. **Funksjonsnavn:** *Fleksibel ordreigangsatt nummerskiltreservering*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Reservere et bestemt nummerskilt på salgsordren

Hvis du vil aktivere nummerskiltreservering for en ordre, må du merke av for **Tillat reservasjon på etterspørselsordre** for **Nummerskilt** -nivået på siden **Beholdningsreservasjonshierarkier** for hierarkiet som er knyttet til den aktuelle varen.

![Siden Beholdningsreservasjonshierarkier for et fleksibelt hierarki for nummerskiltreservasjon](media/Flexible-LP-reservation-hierarchy.png)

Du kan aktivere reservasjon av nummerskilt for ordren på et hvilket som helst sted i distribusjonen. Denne endringen påvirker ikke reservasjoner eller åpent lagerarbeid som ble opprettet før endringen fant sted. Du kan imidlertid ikke fjerne merket for **Tillat reservasjon på etterspørselsordre** hvis det finnes åpne utgående beholdningstransaksjoner med utstedelsesstatusen *På bestilling* , *Reservert bestilt* eller *Reservert fysisk* for én eller flere varer som er tilknyttet til dette reservasjonshierarkiet.

Selv om det er merket av for **Tillat reservasjon på etterspørselsordre** for **Nummerskilt** -nivået, er det fremdeles mulig *ikke* å reservere et bestemt nummerskilt i ordren. I dette tilfellet gjelder standard lageroperasjonslogikk som er gyldig for reservasjonshierarkiet.

Hvis du vil reservere et bestemt nummerskilt, må du bruke en prosess av typen [åpen dataprotokoll (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md). I appen kan du foreta denne reservasjonen direkte fra en salgsordre ved å bruke alternativet **Ordreigangsatte reservasjoner per nummerskilt** for kommandoen **Åpne i Excel**. I enhetsdataene som åpnes i Excel-tillegget, må du angi følgende data for reservasjon, og deretter velge **Publiser** for å sende dataene tilbake til Supply Chain Management:

- Referanse (bare *Salgsordre* -verdien støttes.)
- Ordrenummer (verdien kan avledes fra partiet).
- Parti-ID
- Nummerskilt
- Antall

Hvis du må reservere et bestemt nummerskilt for en partisporet vare, bruker du **Partireservasjon** -siden som beskrevet i dele [Angi salgsordredetaljer](#sales-order-details).

Når salgsordrelinjen som bruker en tildelt nummerskiltreservasjon, behandles av lageroperasjoner, brukes ikke lokasjonsdirektiver.

Hvis en lagerarbeidsvare består av linjer som er lik en fullstendig pall og har antall igangsatt av nummerskilt, kan du optimalisere plukkeprosessen ved å bruke menyelementet for en mobilenhet der alternativet **Behandle etter nummerskilt** er satt til *Ja*. En lagerarbeider kan deretter skanne et nummerskilt for å fullføre en plukking i stedet for å måtte skanne varene fra arbeidet én etter én.

![Menyelementet for mobilenhet der alternativet Behandle etter nummerskilt er satt til Ja](media/Handle-by-LP-menu-item.png)

Fordi funksjonen **Behandle etter nummerskilt** ikke støtter arbeid som dekker flere paller, er det bedre å ha et separat arbeidselement for forskjellige nummerskilt. Hvis du vil bruke denne fremgangsmåten, legger du til eltet **ID for ordreigangsatt nummerskilt** som et arbeidshodeskift på **Arbeidsmal** -siden.

> [!NOTE]
> For den ordreigangsatt arbeidsopprettelsesprosessen blir en verdi for "ordreigangsatt lagerdimensjon" tilordnet til plukkarbeidslinjene, og det er ikke mulig å vise nummerskiltverdien direkte. Bare den *Brukerstyrt* -prosessen støttes når du setter opp menyelement for en mobilenhet.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Eksempelscenario: Definere og behandle en ordreigangsatt nummerskiltreservering

Dette scenarioet viser hvordan du definerer og behandler en ordreigangsatt nummerskiltreservering.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Dette scenarioet refererer til verdier og poster som er inkludert i standard demodata som leveres for Supply Chain Management. Hvis du vil arbeide deg gjennom dette scenariet ved å bruke verdiene som presenteres her, må du arbeide i et miljø der standard demodata er installert. Du må også angi den juridiske enheten til **USMF** før du begynner.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Opprette et lagerreservasjonshierarki som tillater nummerskiltreservering

1. Gå til **Lagerstyring \> Oppsett \> Beholdning \> Reservasjonshierarki**.
1. Velg **Ny**.
1. I **Navn** -feltet angir du en verdi (for eksempel *FlexibleLP* ).
1. I **Beskrivelse** -feltet angir du en verdi (for eksempel *Fleksibel nummerskiltreservasjon* ).
1. I **Valgt** -listen velger du **Partinummer** , **Serienummer** og **Eier**.
1. Velg **Fjern** -knappen ![bakoverpil](media/backward-button.png) for å flytte de valgte oppføringene til listen **Tilgjengelig**.
1. Velg **OK**.
1. I raden for **Nummerskilt** -dimensjonsnivået merker du av i **Tillat reservasjon på etterspørselsordre** -avmerkingsboksen. **Plassering** -nivået velges automatisk, og du kan ikke fjerne avmerkingen i avmerkingsboksen for det.
1. Velg **Lagre**.

### <a name="create-two-released-products"></a>Opprette to frigitte produkter

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg **Ny** i handlingsruten.
1. Angi følgende verdier i dialogboksen **Nytt frigitt produkt** :

    - **Produktnummer:** *Vare 1*
    - **Varenummer:** *Vare 1*
    - **Varemodellgruppe:** *FIFO*
    - **Varegruppe:** *Lyd*
    - **Lagringsdimensjonsgruppe:** *Bølge*
    - **Sporingsdimensjonsgruppe:** *Ingen*
    - **Reservasjonshierarki:** *Fleksibelt nummerskilt*

1. Velg **OK** for å opprette produktet og lukke dialogboksen.
1. Det nye produktet åpnes. På **Lager** -hurtigfanen angir du *ea* i **Sekvensgruppe-ID for enhet** -feltet.
1. Gjenta de forrige trinnene for å opprette et nytt produkt som har de samme innstillingene, men sett feltene **Produktnumer** og **Varenummer** til *Vare 2*.
1. I handlingsruten i kategorien **Administrer lager** i gruppen **Visning** velger du **Lagerbeholdning**. Velg deretter **Antallsjustering**.
1. Juster lagerbeholdningen for de nye varene slik det er angitt i følgende tabell.

    | Artikkel  | Lager | Lokasjon | Nummerskilt | Antall |
    |-------|-----------|----------|---------------|----------|
    | Vare 1 | 24        | FL-010   | LP01          | 10       |
    | Vare 1 | 24        | FL-011   | LP02          | 10       |
    | Vare 2 | 24        | FL-010   | LP01          | 5        |
    | Vare 2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Du må opprette de to nummerskiltene og bruke lokasjoner som tillater blandede varer, for eksempel *FL-010* og *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Opprette en salgsordre og reservere et bestemt nummerskilt

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny**.
1. I **Opprett salgsordre** -dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *24*

1. Velg **OK** for lukke dialogboksen **Opprett salgsordre** og åpne den nye salgsorden.
1. På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:

    - **Varenummer:** *Vare 1*
    - **Antall:** *10*

1. Legg til en ny salgsordrelinje som har følgende innstillinger:

    - **Varenummer:** *Vare 2*
    - **Antall:** *5*

1. Velg **Lagre**.
1. På hurtigfanen **Linjedetaljer** på **Oppsett** -fanen noterer du ned verdien for **Parti-ID** for hver linje. Disse verdiene er nødvendige under reservering av bestemte nummerskilt.

    > [!NOTE]
    > Hvis du vil reservere et bestemt nummerskilt, må du bruke dataenheten **Ordreigangsatte reservasjoner per nummerskilt**. Hvis du vil reservere en partisporet vare på et bestemt nummerskilt, kan du også bruke **Partireservasjon** -siden som beskrevet i delen [Angi salgsordredetaljer](#sales-order-details).
    >
    > Hvis du angir nummerskiltet direkte på salgsordrelinjen og bekrefter det til systemet, brukes ikke prosessering av lagerstyring for linjen.

1. Velg **Åpne i Microsoft Office** , velg **Ordreigangsatte reservasjoner per nummerskilt** , og last ned filen.
1. Åpne den nedlastede filen i Excel, og velg **Aktiver redigering** for å aktivere kjøring av Excel-tillegget.
1. Hvis du kjører Excel-tillegget for første gang, velger du **Klarer tillegget**.
1. Hvis du blir bedt om å logge på, velger du **Logg på** , og deretter logger du på ved å bruke samme legitimasjon som du brukte til å logge på Supply Chain Management.
1. Hvis du vil reservere en vare på et bestemt nummerskilt i Excel-tillegget, velger du **Ny** for å legge til en reservasjonslinje, og angir deretter følgende verdier:

    - **Parti-ID:** Angi verdien for **Parti-ID** som du fant for salgsordrelinjen for *Vare 1*.
    - **Nummerskilt:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. Velg **Ny** for å legge til en ny reservasjonslinje, og angi deretter følgende verdier:

    - **Parti-ID:** Angi verdien for **Parti-ID** som du fant for salgsordrelinjen for *Vare 2*.
    - **Nummerskilt:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. I Excel-tillegget velger du **Publiser** for å sende dataene tilbake til Supply Chain Management.

    > [!NOTE]
    > Reservasjonslinjen vil bare vises i systemet hvis publiseringen er fullført uten feil.

1. Gå tilbake til Supply Chain Management. 
1. Hvis du vil gå gjennom varens reservasjon, går du til **Salgsordrelinje** -hurtigfanen på **Lager** -menyen og velger **Vedlikehold \> Reservasjon**. Legg merke til at for salgsordrelinjen for *Vare 1* , er en beholdning på *10* reservert, og for salgsordrelinjen for *Vare 2* er en beholdning på *5* reservert.
1. Hvis du vil se gjennom lagertransaksjoner som er knyttet til salgsordrelinjereservasjonen, går du til **Salgsordrelinjer** -hurtigfanen på **Lager** -menyen og velger **Vis \> Transaksjoner**. Legg merke til at det er to transaksjoner som er knyttet til reserveringen: én der **Referanse** -feltet er satt til *Salgsordre* , og én der **Referanse** -feltet er satt til *Ordreigangsatt reservasjon*.

    > [!NOTE]
    > En transaksjon der **Referanse** -feltet er satt til *Salgsordre* , representerer ordrelinjereservasjonen for beholdningsdimensjonene som er over **Plassering** -nivået (anlegg, lager og inventarstatus). En transaksjon der **Referanse** -feltet er angitt til *Ordreigangsatt reservasjon* , representerer ordrelinjereservasjonen for det bestemte nummerskiltet og lokasjonen.

1. Du kan frigi salgsordren ved å gå til handlingsruten og **Lager** -fanen i **Handlinger** -gruppen og velge **Frigi til lager**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Gå gjennom og behandle lagerarbeidet med ordreigangsatte nummerskilt tilordnet

1. På **Salgsordrelinjer** -fanen, på **Lager** -menyen, velger du **Arbeidsdetaljer**.

    Når reservasjon er utført for et bestemt parti, bruker ikke systemet lokasjonsdirektiver når det oppretter arbeidet for salgsordren som bruker nummerskiltreservering. Siden den ordreigangsatte reservasjonen angir alle lagerdimensjonene, inkludert lokasjonen, trenger ikke lokasjonsdirektiver å brukes, fordi disse lagerdimensjonene akkurat ble angitt i arbeidet. De vises i delen **Fra lagerdimensjoner** på siden **Arbeidslagertransaksjoner**.

    > [!NOTE]
    > Etter at arbeidet er opprettet, blir varens beholdningstransaksjon der **Referanse** -feltet er satt til *Ordreigangsatt reservasjon* , fjernet. Beholdningstransaksjonen der **Referanse** -feltet er satt til *Arbeid* , inneholder nå den fysiske reservasjonen for alle beholdningsdimensjoner for antallet.

1. Fullfør plukkingen på mobilenheten, og plasser arbeidet ved hjelp av et menyelement der det er merket av for **Behandle etter nummerskilt**.

    > [!NOTE]
    > Funksjonaliteten **Behandle etter nummerskilt** hjelper deg med å behandle hele nummerskiltet. Hvis du må behandle deler av nummerskiltet, kan du ikke bruke denne funksjonaliteten.
    >
    > Vi anbefaler at du har separat arbeid generert for hvert nummerskilt. Du oppnår dette resultatet ved å bruke funksjonen **Arbeidshodeskift** på **Arbeidsmal** -siden.

    Nummerskiltet *LP02* plukkes nå for salgsordrelinjer og plasseres på *Rampedør* -lokasjonen. På dette tidspunktet er det klart til å lastes og sendes til kunden.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Unntakshåndtering av lagerarbeid som har ordreigangsatte partinumre

Lagerarbeid for plukking av ordreigangsatte partinumre er underlagt samme standard lagerunntakshåndtering og -handlinger som vanlig arbeid. Generelt kan det åpne arbeidet eller arbeidslinjen avbrytes. De kan avbrytes fordi en brukerplassering er full, det kan mangle tilstrekkelig antall, og de kan oppdateres på grunn av en bevegelse. Tilsvarende kan den valgte kvantiteten arbeid som allerede er fullført, reduseres, eller arbeidet kan reverseres.

Følgende nøkkelregel brukes for alle disse unntakshåndteringshandlingene: Partinummeret som var reservert for kunden, kan aldri erstattes med et annet partinummer, men lagringsdimensjonene (plassering og nummerskilt) kan endres gjennom enten en manuell oppdatering utført av brukeren eller en automatisk oppdatering utført av systemet. Den automatiske oppdateringen er basert på den samme tilfeldige tilordningen av lagringsdimensjoner som gjaldt da et spesifikt parti ble reservert automatisk, men ingen lagringsdimensjoner ble spesifisert.

### <a name="example-scenario"></a>Eksempelscenario

Et eksempel på dette scenarioet er en situasjon der tidligere avsluttet arbeid plukkes fra hverandre ved å benytte **Reduser plukket kvantitet** -funksjonen. Dette eksemplet forutsetter at du allerede har fullført trinnene som er beskrevet i [Eksempelscenario: Tildeling av partinummer](#Example-batch-allocation). Den fortsetter fra dette eksemplet.

1. Gå til **Lagerstyring** \> **Belastninger** \> **Aktive belastninger**.
2. Velg belastningen som ble opprettet i forbindelse med forsendelsen av salgsordren.
3. Gå til **Last inn ordrelinjer** -hurtigfanen og velg **Reduser plukket kvantitet**.
4. Gå til **Reduser plukket kvantitet** -siden i **Flytt til plassering** -feltet og velg **FL-001**.
5. I **Flytt til nummerskilt** -feltet velger du **LP33**.
6. I rutenettet, i **Beholdningskvantitet som skal plukkes vekk** -feltet, angir du **10**.
7. Velg **OK**.

Her er resultatene av handlingen med vekkplukking:

- Statusen til det tidligere lukkede verket er satt til **Avbrutt**.
- Nytt arbeid av **Beholdningsbevegelse** -typen opprettes for det vekkplukkede antallet **10** for partinummer **B11**. Dette arbeidet representerer bevegelsen fra **Båsdør** -plasseringen til nummerskiltet **LP33** på plasseringen **FL-001**. Status er satt til **Lukket**.
- Systemet reserverer partinummeret som opprinnelig ble bestilt, på nytt og tilordner plasseringen og nummerskilt-ID-er. (Denne prosessen tilsvarer kjøring av **Reserver linje** -funksjonen for ordrelinjen for et gitt partinummer). Som et resultat vises parti **B11** som bundet på **Partinumre bundet til kildelinje** -hurtigfanen på **Partireservasjon** -siden, og **Reservasjon** -feltet inneholder antallet **10** for partinummer **B11**. I tillegg er **Plassering** -feltet satt til **FL-001** , og **Nummerskilt** -feltet er satt til **LP11**. (Du kan legge til disse feltene i rutenettet hvis de ikke er synlige.)

Følgende tabeller inneholder en oversikt som viser hvordan systemet håndterer ordreigangsatt partireservasjon for bestemte lagerhandlinger. Hvis du vil tolke innholdet i tabellene, må du anta at hver lagerhandling kjøres i konteksten av eksisterende lagerarbeid som stammer fra en ordreigangsatt partireservasjon, eller at utførelsen av hver lagerhandling påvirker arbeid av denne typen.

> [!NOTE]
> I disse tabellene angir "Partikvantitet er tilgjengelig"-kolonnen om en partikvantitet er tilgjengelig, i tillegg til kvantiteten som allerede er reservert for gjeldende ordreigangsatte reservasjoner, eller som allerede er reservert av lagerarbeidet som stammer fra reservasjoner av denne typen.

#### <a name="override-the-pick-location-on-the-open-work"></a>Overstyr plukkplasseringen for det åpne arbeidet

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Tillat overstyring av plukkplassering</strong>-alternativet er aktivert for arbeideren.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg <strong>Overstyr plassering</strong>-menyelementet på lagerappen når du begynner plukkarbeid.</li>
<li>Velg <strong>Foreslå</strong>.</li>
<li>Bekreft den nye plasseringen som foreslås, basert på tilgjengeligheten av partikvantitet.</li>
</ol>
</td>
<td>For gjeldende arbeid oppstår det følgende handlinger:
<ul>
<li>Plasseringen på plukklinjen oppdateres til den nye plasseringen. (Hvis plasseringen er navneskiltstyrt, tilordnes et tilfeldig nummerskilt til arbeidslagertransaksjonen, og arbeideren kan plukke et hvilket som helst nummerskilt som har tilgjengelig kvantitet.)</li>
<li>Hvis kvantiteten blir funnet for mer enn ett nummerskilt på den nye plasseringen, blir den opprinnelige plukklinjen delt opp i flere linjer for å matche hvert nummerskilt.</li>
</ul>
</td>
<td>Gjelder ikke</td>
</tr>
<tr>
<td>Nr.</td>
<td>
<ol>
<li>Velg <strong>Overstyr plassering</strong>-menyelementet på lagerappen når du begynner plukkarbeid.</li>
<li>Angi en plassering manuelt.</li>
</ol>
</td>
<td><strong>Overstyr plassering</strong>-handlingen er ikke mulig. Den mislykkes, og det oppstår en feil.</td>
<td>Gjelder ikke</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Full knapp – del opp en arbeidslinje på grunn av overflyt på brukerplasseringen

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Tillat oppdeling av arbeid</strong>-alternativet er aktivert på mobilenhetens menyelement.</td>
<td>Gjelder ikke</td>
<td>
<ol>
<li>Velg menyelementet <strong>Full</strong> på lagerappen når du behandler plukkarbeid.</li>
<li>I <strong>Plukkvantitet</strong>-feltet angir du en delvis kvantitet for den påkrevde plukkingen for å indikere hele kapasiteten.</li>
</ol>
</td>
<td>
<ul>
<li>I gjeldende arbeid oppdateres kvantiteten til den gjenværende kvantiteten som må plukkes.</li>
<li>Nytt arbeid for den plukkede kvantiteten opprettes og lukkes.</li>
</ul></td>
<td>Gjelder ikke</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Redusere den plukkede kvantiteten for fullført arbeid (fra en belastning)

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Gjelder ikke</td>
<td>Ja</td>
<td>
<ol>
<li>Åpne <strong>Reduser plukket kvantitet</strong>-siden fra belastningslinjen.</li>
<li>Angi den fullstendige kvantiteten som skal plukkes vekk.</li>
<li>Velg "Flytt til"-plassering/-nummerskilt.</li>
</ol>
</td>
<td>
<ul> 
<li>Arbeid som er knyttet til belastningslinjen, avbrytes.</li>
<li>Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</li>
</ul>
</td>
<td>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Se den forrige raden.</td>
<td>Kvantiteten reserveres på nytt for samme parti, samt for samme plassering og nummerskilt (hvis plasseringen er nummerskiltstyrt) som ble angitt under vekkplukking.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Flytte en vare i et lager

> [!NOTE]
> Denne lagerhandlingen gjelder bare for bevegelse av **Arbeidsopprettelsesprosess** -typen, ikke for bevegelse etter mal.

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Tillat bevegelse av beholdning med tilhørende arbeid</strong>-alternativet er aktivert for arbeideren.</td>
<td>Ja</td>
<td>
<ol>
<li>Start en flytting på lagerappen.</li>
<li>Angi "fra"- og "til"-plasseringene.</li>
</ol></td>
<td>
<ul>
<li>For alt eksisterende arbeid som påvirkes av flyttingen, oppdateres plukkplasseringen til den nye plasseringen.</li>
<li>Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</li>
</ul>
</td>
<td>Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Se den forrige raden.</td>
<td>Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres for samme parti, samt for den nye "til"- plasseringen og det nye "til"-nummerskiltet (hvis plasseringen er nummerskiltstyrt).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Reversere den plukkede kvantiteten for fullført arbeid (fra en belastning eller en bølge)

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Gjelder ikke</td>
<td>Ja</td>
<td>
<ol>
<li>Åpne <strong>Reverser arbeid</strong>-siden.</li>
<li>På forespørselssiden velger du <strong>Etterlat varer på gjeldende plassering</strong>-alternativet.</li>
</ol>
</td>
<td>Alt arbeid som er knyttet til belastningen, avbrytes.</td>
<td>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Se den forrige raden.</td>
<td>Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet der kvantiteten ble etterlatt ved reversering.</td>
</tr>
<tr>
<td>Ja</td>
<td>
<ol>
<li>Åpne <strong>Reverser arbeid</strong>-siden.</li>
<li>På forespørselssiden velger du <strong>Tilordne varer til denne plasseringen</strong>-alternativet.</li>
</ol>
</td>
<td>
<ul>
<li>Det gjeldende arbeidet avbrytes.</li>
<li>Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</li>
</ul>
</td>
<td>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Se den forrige raden.</td>
<td>Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet som kvantiteten ble tilordnet til ved reversering.</td>
</tr>
<tr>
<td>Ja/nei</td>
<td>
<ol>
<li>Åpne <strong>Reverser arbeid</strong>-siden.</li>
<li>På forespørselssiden velger du <strong>Flytt varer til denne plasseringen</strong>-alternativet.</li>
</ol>
</td>
<td>Reversering støttes ikke.</td>
<td>Gjelder ikke</td>
</tr>
<tr>
<td>Ja/nei</td>
<td>
<ol>
<li>Åpne <strong>Reverser arbeid</strong>-siden.</li>
<li>På forespørselssiden velger du <strong>Flytt varer basert på plasseringsdirektiver</strong>-alternativet.</li>
</ol>
</td>
<td>Reversering støttes ikke. </td>
<td>Gjelder ikke</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Plukk en kvantitet med mangler – Registrer kvantiteten som fysisk ikke funnet på plasseringen/nummerskiltet mens du utfører plukkarbeidet

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</li>
<li>Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</li>
</ul>
</td>
<td>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>
<ul>
<li>Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</li>
<li>Gjeldende arbeid forblir åpent.</li>
</ul>
</td>
<td>Gjelder ikke</td>
</tr>
<tr>
<td rowspan='2'>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</li>
<li>Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</li>
</ul>
</td>
<td>Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Se den forrige raden.</td>
<td>Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, fjernes.</td>
</tr>
<tr>
<td>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei/Ja</strong>. I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</li>
<li>Velg plasseringen/nummerskiltet i listen.</li>
</ol>
</td>
<td>
<ul>
<li>For gjeldende arbeid oppstår det følgende handlinger:
<ul>
<li>Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</li>
<li>Plasseringslinjen avbrytes.</li>
<li>Det opprettes en ny plukklinje. Den bruker plasseringen/nummerskiltet som brukeren valgte.</li>
<li>Det opprettes en ny plasseringslinje.</li>
</ul>
</li>
<li>Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</li>
</ul>
</td>
<td>Gjelder ikke</td>
</tr>
<tr>
<td>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>. I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</td>
<td>Nr.</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</li>
</ol>
</td>
<td>Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</td>
<td>Gjelder ikke</td>
</tr>
<tr>
<td>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>. I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</td>
<td>Nr.</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</li>
<li>Velg plasseringen/nummerskiltet i listen.</li>
</ol>
</td>
<td>
<ul>
<li>For gjeldende arbeid oppstår det følgende handlinger:
<ul>
<li>Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</li>
<li>Plasseringslinjen avbrytes.</li>
</ul>
</li>
<li>Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</li>
</ul>
</td>
<td>Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen/nummerskiltet for plukking med mangler, fjernes.</td>
</tr>
<tr>
<td>Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Automatisk</strong>, <strong>Juster beholdning</strong> = <strong>Ja/Nei</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja/Nei</strong>.</td>
<td>Gjelder ikke</td>
<td>
<ol>
<li>Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</li>
<li>I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</li>
<li>I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med automatisk omfordeling</strong>.</li>
</ol>
</td>
<td>Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</td>
<td>Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Endre beholdningsstatusen

> [!NOTE]
> Denne lagerhandlingen kan utføres fra flere inngangspunkter. I eksempelet som vises her, benyttes **Beholdningsstatusendring** -handlingen på **På lager etter plassering** -siden.

<table>
<thead>
<tr>
<th>Nøkkeloppsettsparameter</th>
<th>Partikvantitet er tilgjengelig</th>
<th>Nøkkelbrukertrinn</th>
<th>Lagerarbeid</th>
<th>Ordreigangsatt partireservasjon</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Reservasjoner</strong> eller <strong>Merkinger og reservasjoner</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg en spesifikk plassering.</li>
<li>Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</li>
<li>Velg <strong>Beholdningsstatusendring</strong>.</li>
<li>Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</li>
</ol>
</td>
<td>Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</td>
<td>
<ul>
<li>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</li>
<li>Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</li>
<li>En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</li>
</ul>
</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</td>
<td>
<ul>
<li>Reservasjonen fjernes.</li>
<li>Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</li>
<li>En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Ingen</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Velg en spesifikk plassering.</li>
<li>Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</li>
<li>Velg <strong>Beholdningsstatusendring</strong>.</li>
<li>Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</li>
</ol>
</td>
<td>Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</td>
<td>Kvantiteten reserveres på nytt for samme parti. Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</td>
</tr>
<tr>
<td>Nei</td>
<td>Se den forrige raden.</td>
<td>Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</td>
<td>Beholdningsstatusendringer er ikke tillatt.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Begrensninger

- Den fleksible funksjonaliteten for dimensjonsreservasjon på lagernivå støtter ikke følgende funksjoner:

    - Administrering av faktisk vekt
    - Fysisk negativt lager
    - Reservasjon mot bestilt forsyning
    - Plukking av overføringsordrer og råvarer

- Regelen for konsolidering av containere for pakking etter direktivenhet har begrensninger. For ordreigangsatte reservasjoner anbefaler vi at du ikke bruker maler for containerbygging i tilfeller der **Pakk etter direktivenhet** -feltet er aktivert. I gjeldende utforming brukes ikke plasseringsdirektiver når det opprettes lagerarbeid. Derfor brukes bare den laveste enheten i enhetssekvensgruppen (beholdningsenheten) under bølgetrinnet containerbruk.
