---
title: Behandling av skift og kassaskuff
description: Dette emnet beskriver hvordan du definerer og bruker skift på salgssteder i Commerce.
author: jblucher
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d9d36bcb05cf466d34d921d8cd5266b6c12a63d7
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028257"
---
# <a name="shift-and-cash-drawer-management"></a>Behandling av skift og kassaskuff

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer og bruker skift på salgssteder i Commerce.

I Dynamics 365 Commerce beskriver *skift* samlingen av transaksjonsdata og aktiviteter mellom to punkter i tid for salgsstedet. For hvert skift sammenlignes forventet beløp sammenlignet med beløpet som ble talt og deklarert.

Skift åpnes vanligvis i begynnelsen av arbeidsdagen. På dette tidspunktet deklarerer brukeren startbeløpet som kassaskuffen inneholder. Salgstransaksjoner blir deretter utført i løpet av dagen. På slutten av dagen telles kassaskuffen, og sluttbeløpet deklareres. Skiftet lukkes, og det genereres en Z-rapport. Z-rapporten angir om det er for mye eller for lite.

## <a name="typical-shift-scenarios"></a>Vanlige skiftet scenarier

Commerce gir flere konfigurasjonsalternativer og salgsstedsoperasjoner for å støtte et bredt spekter av forretningsprosesser på slutten av dagen for salgsstedet. Denne delen beskriver noen vanlige skiftscenarier.

### <a name="fixed-till"></a>Fast kasse

Dette er vanligvis brukt oftest. Det brukes forsatt mye. I et "fast kasse"-skift tilknyttes skiftet og kassen med en bestemt kasse. De flyttes fra én kasse til en annen. Et "fast kasse"-skift kan brukes av én bruker eller deles mellom flere brukere. "Fast kasse"-skift krever ikke noen spesiell konfigurasjon.

### <a name="floating-till"></a>Flytende kasse

I et "flytende kasse"-skift kan skiftet og kassen flyttes fra én kasse til en annen. Selv om en kasse bare kan ha ett aktivt skift per kasse, kan skift stoppes og startes opp igjen senere eller på en annen kasse.

En butikk har for eksempel to kasser. Hver kasse åpnes ved starten av dagen når kassereren åpner et nytt skift og angir startbeløpet. Når én kasserer er klar til å ta en pause, stopper kassereren skiftet sitt og fjerner kassen fra kassaskuffen. Denne kassen blir da tilgjengelig for andre kasserere. En annen kasserer kan logge på og åpne sitt eget skift på kassen. Etter at pausen til den første kassereren er avsluttet, kan denne kassereren gjenoppta skiftet sitt når en av de andre kassene blir tilgjengelig. "Flytense kasse"-skift krever ikke noen spesiell konfigurasjon eller tillatelse.

### <a name="single-user"></a>Enkeltbruker

Mange forhandlere foretrekker å tillate bare én bruker pers skift for å garantere det høyeste nivået av ansvar for kontanter i kassaskuffen. Hvis bare én bruker har tilgang til å bruke kassen som er knyttet til et skift, vil denne brukeren ene og alene holdes ansvarlig for eventuelle avvik. Hvis flere brukere bruker et skift, er det vanskelig å avgjøre hvem som har gjort en feil eller som kanskje prøver å stjele fra kassen.

### <a name="multiple-users"></a>Flere brukere

Noen forhandlerne er villige til å ofre ansvarsnivået son enkeltbrukerskift gir, og tillate flere brukere per skift. Dette er vanlig når det er flere brukere enn tilgjengelige kasser, og behovet for fleksibilitet og hastighet oppveier muligheten for tap. Det er også vanlig når butikksjefer ikke har sine egne skift, men etter behov kan bruke et skift for en av kassererne. For å logge på og bruke et skift som ble åpnet av en annen bruker, må en bruker ha salgsstedstillatelsen **Tillat pålogging av flere skift**.

### <a name="shared-shift"></a>Delte skift

En "delt skift"-konfigurasjon lar forhandlere ha ett enkelt skift på tvers av flere kasser, pengeskuffer og brukere. Et delt skift har ett enkelt startbeløp og ett enkelt sluttbeløp som summeres på tvers av alle kassaskuffer. Delte skift er vanligst når mobilenheter brukes. I så fall er ikke en kassaskuff reservert for hver kasse. I stedet kan alle kasser dele én kassaskuff.

For delte skift som skal brukes i en butikk må kassaskuffen konfigureres som en "kassakuff for delt skift" på **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler \> Skuff**. Brukerne må i tillegg ha ett eller begge av de delte skifttillatelsene (Tillat administrasjon av delte skift og Tillat bruk av delt skift).

> [!NOTE]
> Bare ett delt skift kan være åpent om gangen i hver butikk. Delte skift og frittstående skift kan brukes i den samme butikken.

## <a name="shift-and-drawer-operations"></a>Skift og skuffoperasjoner

Forskjellige operasjoner kan utføres for å endre statusen for et skift, eller for å øke eller redusere pengebeløpet i kassaskuffen. Dette avsnittet beskriver disse skiftoperasjonene for Modern POS og Cloud POS.

### <a name="open-shift"></a>Åpne skift

Salgsstedet krever at brukere har et aktivt, åpent skift for å utføre handlinger som vil resultere i en finanstransaksjon, for eksempel salg, retur eller kundeordre.

Når en bruker logger på salgsstedet, vil systemet først kontrollerer om et aktivt skift er tilgjengelig for denne brukeren på den aktuelle kassen. Hvis et aktivt skift ikke er tilgjengelig, kan brukeren åpne et nytt skift, gjenoppta et eksisterende skift eller fortsette å logge på i "ikke-skuff"-modus, avhengig av systemkonfigurasjonen og brukerens tillatelser.

### <a name="declare-start-amount"></a>Rapporter startbeløp

Denne operasjonen er ofte den første operasjonen som utføres et nylig åpnet skift. For denne operasjonen angir brukere startbeløpet i kassaskuffen for skiftet. Denne operasjonen er viktig på grunn av beregningen av for mye/lite som utføres når et skift som lukkes vurderer startbeløpet.

### <a name="float-entry"></a>Flytoppføring

*Flytoppføringer* er ikke-salgstransaksjoner som utføres i et aktivt skift for å øke pengebeløpet i kassaskuffen. Et vanlig eksempel på en flytoppføring er å legge til flere vekslepenger i skuffen når det er lite.

### <a name="tender-removal"></a>Fjerning av betalingsmidler

*Fjerning av betalingsmidler* er ikke-salgstransaksjoner som utføres i et aktivt skift for å redusere pengebeløpet i kassaskuffen. Denne operasjonen brukes vanligvis sammen med en flytoppføringsoperasjon i et annet skift. Kasse 1 har for eksempel lite vekslepenger, så brukeren på kasse 2 utfører en fjerning av betalingsmidler for å redusere beløpet i kassaskuffen. Brukeren i kasse 1 gjør deretter en flytoppføring for å øke beløpet i kassaskuffen sin.

### <a name="suspend-shift"></a>Avbryt skift

Brukere kan deaktivere sine aktive skift for å frigjøre gjeldende kasse for en annen bruker, eller flytte skiftet til en annen kasse (dette er kalles skiftet ofte et "flytende kasse"-skift).

Suspendering av skiftet forhindrer eventuelle nye transaksjoner eller endringer til skiftet før det gjenopptas.

### <a name="resume-shift"></a>Gjenoppta skift

Denne operasjonen lar bruker gjenoppta et tidligere suspendert skift i en kasse som ikke allerede har et aktivt skift.

### <a name="tender-declaration"></a>Kasseoppgjør

Denne operasjonen utføres for å angi det totale beløpet som er i kassaskuffen. Brukere utføre oftest operasjonen før de lukker et skift. Det angitte beløpet sammenlignes med det forventede skiftbeløpet for å beregne over-/underbeløpet.

### <a name="safe-drop"></a>Deponer til safe

Deponeringer til safe kan når som helst utføres på et aktivt skift. Denne operasjonen fjerner penger fra kassaskuffen, slik at de kan overføres til en sikrere plassering, så som en safe på bakrommet. Det totale beløpet som er registrert for deponeringer til safe, er fremdeles inkludert i skifttotalene, men trenger ikke regnes som en del av kasseoppgjøret.

### <a name="bank-drop"></a>Deponer til bank

I likhet med deponeringer til safe utføres også deponeringer til bank på aktive skift. Denne operasjonen fjerner penger fra skiftet for å klargjøre for bankinnskuddet.

### <a name="blind-close-shift"></a>Lukk skift usporet

*Lukkede usporede skift* er ikke lenger er aktive, men er ikke fullstendig lukket. I motsetning til skift kan ikke lukkede usporede skift gjenopptas. Operasjoner, for eksempel Rapporter startbeløp og Kasseoppgjør, kan imidlertid utføres på dem senere eller fra en annen kasse.

Lukkede usporede skift brukes ofte til å frigjøre et register for en ny bruker eller skift, uten først å telle, avstemme og lukke dette skiftet fullstendig.

### <a name="close-shift"></a>Lukk skift

Denne operasjonen beregner totaler for skift og over-/underbeløp, og fullfører deretter et aktivt eller lukket usporet skift. Avhengig av brukerens tillatelser skrives også en Z-rapport for skiftet. Lukkede skift kan ikke gjenopptas eller endres.

### <a name="print-x"></a>Skriv ut X

Denne operasjonen genererer og skriver ut en X-rapport for gjeldende aktive skift.

### <a name="reprint-z"></a>Skriv ut Z på nytt

Denne operasjonen skriver ut den siste Z-rapporten på nytt som blir generert da et skift ble lukket.

### <a name="manage-shifts"></a>Behandle skift

Denne operasjonen lar brukerne vise alle aktive, suspenderte og lukkede usporede skift for butikken. Avhengig av tillatelsene kan brukere utføre sine endelige lukkingsprosedyrer, for eksempel Kasseoppgjør og Lukk skift for lukkede usporede skift. Denne operasjonen lar også brukere vise og slette ugyldige skift hvis et skift står i en ugyldig tilstand etter å ha byttet mellom frakoblet og tilkoblet modus. Disse ugyldige skiftene inneholder ingen økonomisk informasjon eller transaksjonsdata som trengs for avstemming.

## <a name="shift-and-drawer-permissions"></a>Skift og skufftillatelser

Følgende salgsstedstillatelser påvirker hva en bruker kan og ikke kan gjøre i ulike scenarier:

- **Tillat usporet lukking**
- **Tillat utskrift av X-rapport**
- **Tillat utskrift av Z-rapport**
- **Tillat kasseoppgjør**
- **Tillat flytende rapportering**
- **Åpne skuff uten salg**
- **Tillat pålogging av flere skift** – Denne tillatelsen lar brukere logge på og bruke et skift som en annen bruker åpnet. Brukere som ikke har denne tillatelsen kan bare logge på og bruke skift som vedkommende har åpnet.
- **Tillat administrasjon av delte skift** – Brukere må ha denne tillatelse for å åpne eller lukke et delt skift.
- **Tillat bruk av delte skift** – Brukere må ha denne tillatelse for å logge på og bruke et delt skift.

## <a name="back-office-end-of-day-considerations"></a>Hensyn å ta ved Back Office-dagsoppgjør

Måten skift og kontantskuffavstemming brukes på salgsstedet er forskjellig fra måten at transaksjonsdata summers under utdragsberegning. Det er viktig at du forstår denne forskjellen. Avhengig av konfigurasjon og forretningsprosesser kan skiftdataene på salgsstedet (Z-rapporten) og et beregnede utdrag i Back Office gi deg forskjellige resultater. Denne forskjellen betyr ikke nødvendigvis at skiftdataene eller det beregnede utdraget er feil, eller at det er et problem med dataene. Det betyr at bare at de angitte parameterne kan inneholde tilleggstransaksjoner eller færre transaksjoner, eller at transaksjonene har blitt summert på forskjellige måter.

Selv om alle forhandleren har ulike forretningsbehov, anbefaler vi at du stiller inn systemet på følgende måte for å unngå situasjoner der forskjeller av denne typen oppstår:

Gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker \> Utdrag/avslutning**, og for hver butikk setter du feltet **Utdragsmetode** og **Avslutningsmetode** til **Skift**.

Dette oppsettet bidrar til at Back Office-utdrag inneholder de samme transaksjonene som skift på salgsstedet, og at dataene blir summert etter dette skiftet.

Hvis du vil ha mer informasjon om utdrag og avslutingsmetoder, kan du se [Butikkonfigurasjoner for detaljhandelsutdrag](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]