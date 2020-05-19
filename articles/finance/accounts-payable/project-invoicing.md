---
title: Prosjektfakturering
description: Denne artikkelen inneholder en oversikt over prosjektfakturering for etter regning-prosjekter og reparert og fastprisprosjekter. Den inneholder informasjon om fakturaforslag (foreløpig fakturaer), fakturakontroll, a konto-fakturering, leverandørfakturering og kreditnotaer.
author: ShylaThompson
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81a3d64d04ceb20fec2f5ca4bb005e7ecb3c1929
ms.sourcegitcommit: d2b111bf7a5fbf62ff2874d6c57c5ef8412df82e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331378"
---
# <a name="project-invoicing"></a>Prosjektfakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder en oversikt over prosjektfakturering for etter regning-prosjekter og reparert og fastprisprosjekter. Den inneholder informasjon om fakturaforslag (foreløpig fakturaer), fakturakontroll, a konto-fakturering, leverandørfakturering og kreditnotaer.

Prosjekttypen avgjør hvilken faktureringsprosess som skal brukes. Det er bare de to eksterne prosjekttyper, Etter regning og Fastpris, som kan faktureres. Etter regning-prosjekter og fastprisprosjekter er alltid knyttet til prosjektkontrakt.

-   **Fastprisprosjekter** – Kundefakturabeløpet er basert på fakturabetalingsplaner. Fakturering utføres ved et a konto-oppsett, også kalt faktureringstidsplan. Fastprisprosjekter kan faktureres per prosjekt eller per prosjektkontrakt.
-   **Etter regning-prosjekter** – Kundefakturabeløpet er basert på transaksjonslinjer som er angitt for prosjekter. Transaksjoner kan faktureres per prosjekt eller per prosjektkontrakt.

Det er tre måter å knytte Etter regning-prosjekter og fastprisprosjekter til fakturaprosjektene:

-   **A konto-fakturering** – Etter regning-prosjekter og fastprisprosjekter kan faktureres a konto. To typer a konto-oppsett kreves, ett for hver prosjekttype.
-   **Fakturering i den periodiske delen** – Transaksjoner kan faktureres på tvers av prosjekter gjennom de periodiske funksjonene. De periodiske funksjonene gir en oversikt over transaksjoner som må faktureres.
-   **Bruke kreditnotaer i faktureringen** – En kreditnota kan opprettes for både Etter regning-prosjekter og fastprisprosjekter.

## <a name="invoice-proposals"></a>Fakturaforslag
Før du oppretter en kundefaktura for et prosjekt, kan du opprette en foreløpig faktura, eller et fakturaforslag. Du kan velge prosjekttransaksjoner som skal tas med i en prosjektfaktura, i et fakturaforslag. Deretter kan du se gjennom fakturadetaljene før du posterer prosjektfakturaen og sende den til kunden eller en annen finansieringskilde.

### <a name="creating-invoice-proposals"></a>Opprette fakturaforslag

Du kan opprette fakturaforslag ved manuelt å velge fra en liste over transaksjoner for et bestemt prosjekt. Du kan også definere faktureringsregler som angir når det skal opprettes et fakturaforslag automatisk. Du kan for eksempel opprette en faktureringsregel for å opprette et fakturaforslag når arbeidet på et prosjekt er 25 prosent, 50 prosent, 75 prosent og 100 prosent fullført. 

Du kan opprette fakturaforslag for følgende transaksjoner:

-   Timer, utgifter og andre prosjekttransaksjoner
-   Beløp som holdes tilbake av kunder på tidligere prosjektfakturaer
-   Kreditnotaer
-   Beløp som en kunde har betalt til deg, før et prosjekt starter

> [!NOTE]
> Funksjonen **Aktiver sortering etter ressurs under oppretting av prosjektfakturaforslag** gjør at prosjektregnskapsføreren kan sortere prosjekttransaksjonene som er tilgjengelige for fakturering etter ressursen ved oppretting av et nytt prosjektfakturaforslag. Rutenettet som viser de tilgjengelige prosjekttransaksjonene, har et separat felt for ressurs-ID og ressurs, slik at brukeren kan filtrere og sortere på ressursnavnet. Denne funksjonen er som standard deaktivert og kan aktiveres i **Arbeidsområder > Funksjonsbehandling**. Ta kontakt med systemansvarlig for å få hjelp til å aktivere denne funksjonen.

Du kan opprette gebyrtransaksjoner i et fakturaforslag. Du kan også endre salgsprisen i time-, utgifts-, vare- og gebyrtransaksjoner. Når du posterer et fakturaforslag, legges de oppdaterte prisene og transaksjonene til i prosjektrapporter og transaksjonshistorikken. 

Hvis du vil opprette flere kundefakturaer for et prosjekt, må du opprette et fakturaforslag for hver faktura. Du kan for eksempel opprette fakturaer basert på transaksjonstypen. Hvis du vil angi timer på én kundefaktura og varer på en annen, må du opprette separate fakturaforslag for timetransaksjoner og gebyrtransaksjoner. 

Hvis et prosjekt har mer enn én finansieringskilde, kan du opprette et separat fakturaforslag for hver finansieringskilde. På **Finansieringsregeltildelinger**-siden kan du definere prosenten av transaksjonsbeløpet som skal fordeles til hver finansieringskilde, og kilden avrundingsforskjeller skal posteres til.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Opprette kundefakturaer fra fakturaforslag

Når du har opprettet og postert et fakturaforslag, opprettes det automatisk en kundefaktura for transaksjonene som skal tas med i fakturaforslaget. 

Før du postere et fakturaforslag kan du legge til transaksjoner i forslaget eller slette transaksjoner fra det. Du kan for eksempel fjerne utgiftstransaksjoner som er postert til et prosjekt, men som ikke kan belastes til kunden. 

Hvis organisasjonen krever at fakturaforslag gås gjennom før de posteres, må kanskje fakturaforslaget godkjennes via arbeidsflyten "Gå gjennom fakturaforslag for prosjekt" før det posteres.

## <a name="on-account-invoicing"></a>A konto-fakturering
Beløpet du angir på en a konto-faktura for et prosjekt, er basert på tidsmåling, fullførelsesprosent og andre faktureringsbetingelser som er angitt i den tilknyttede prosjektkontrakten. Beløpet beregnes ikke basert på timer, varer, utgifter eller gebyrer som posteres til prosjektet. 

Du må opprette en a konto-transaksjon for et Etter regning-prosjekt eller et Fastprisprosjekt før du kan legge til a konto-transaksjonen i en prosjektfaktura. I a konto-transaksjonen angir du beløpet som skal faktureres en kunde. Hvis du vil opprette en prosjektfaktura for beløpet, oppretter du en foreløpig faktura (fakturaforslag). Velg a konto-transaksjonen i fakturaforslaget. Du kan gå gjennom a konto-informasjonen i fakturaforslaget før du oppretter en prosjektfaktura for den.

### <a name="fixed-price-projects"></a>Fastprisprosjekter

For fastprisprosjekter er a konto-transaksjoner basert på en avtalt milepæl, leveringsenhet eller fremdriftsfakturering som er angitt i en prosjektkontrakt. Det opprettes én linje for hver betaling som må mottas fra prosjektkunden. Ingen fradrag er nødvendig.

### <a name="time-and-material-projects"></a>Etter regning-prosjekter

For Etter regning-prosjekter kan du fakturere en kunde eller en annen finansieringskilde et forskuddsbeløp ved hjelp av et a konto-fakturaforslag. Angi a konto-transaksjoner som én linje. Du kan også angi flere linjer som fradrag for å motregne eventuelle forskuddsbetalinger som kunden allerede har foretatt. Hvis du vil opprette linjer for fradrag, setter du et minustegn foran beløpet.

## <a name="invoice-control"></a>Fakturakontroll
Du kan bruke fakturakontroll til å spore både fakturerte og ikke-fakturerte transaksjoner, og til å analysere disse transaksjonene mot tilbud for en komplett visning av prosjektene dine fra tilbudsfasen til fullførelse. Du kan se hvilke transaksjoner som er belastet et bestemt prosjekt, og hvilke linjer som har blitt fakturert. Du kan også vise de individuelle transaksjonene slik at du kan justere dem etter at de har blitt postert.

## <a name="invoicing-fixed-price-projects"></a>Fakturere fastprisprosjekter
Hvis du vil fakturere et fastprisprosjekt, må du definere en faktureringstidsplan og fullføre faktureringsprosedyren.

### <a name="billing-schedule"></a>Faktureringstidsplan

Du kan fakturere fastprisprosjekter på en faktureringstidsplan. Faktureringstidsplanen er definert i form av én eller flere milepæler for prosjektet. For hver milepæl kan du definere en bestemt dato, salgsvaluta, salgspris og aktivitet. 

Du kan for eksempel sette opp følgende faktureringstidsplan:

-   20 prosent når prosjektkontrakten er signert
-   30 prosent ved første levering
-   15 prosent ved andre levering
-   35 prosent ved sluttlevering

### <a name="invoicing-procedure"></a>Faktureringsprosess

Når delbetalingene er klare for fakturering, bruker du fremgangsmåten for fakturering av a konto-beløp.

## <a name="vendor-invoicing"></a>Leverandørfakturering
Når du bestiller en vare fra en leverandør og tilordner varen til et prosjekt, bestemmer linjeegenskapen som du velger for bestillingslinjen for varen, om den innkjøpte varen faktureres til en kunde. Hvis du setter opp standard linjeegenskaper, vises de for varen på bestillingslinjen (Linjedetaljer &gt; Prosjekt &gt; Linjeegenskap). Det finnes to metoder å endre linjeegenskapen på:

-   Fakturer prosjektets kunde for varen: Sett linjeegenskapen for varen til en belastbar verdi på bestillingen, og fakturer deretter kunden ved hjelp av riktig prosjektfaktureringsmåte.
-   Ikke fakturer prosjektets kunde for varen: Ikke velg linjeegenskapen **Belastbar** på bestillingslinjen for varen. Du kan deretter fakturere bestillingen, og mer er det ikke nødvendig å gjøre.

> [!NOTE] 
> Linjer for frigivelse av tilbakeholdelse er ikke-belastbare som standard. Dette betyr at muligheten til å opprette et fakturaforslag for den frigitte tilbakeholdelsen ikke er aktivert.

## <a name="credit-notes"></a>Kreditnotaer
Når et beløp på en kundefaktura har en negativ verdi, klassifiseres fakturaen som en kreditnota. Når dokumentet skrives ut, har det navnet "Kreditnota". 

Når du oppretter en kreditnota for å kreditere et beløp som tidligere er fakturert, må du først velge det fakturerte beløpet for kreditering. Du oppretter deretter en kreditnota ved å følge samme fremgangsmåte som for oppretting av en vanlig kundefaktura. Du må med andre ord velge transaksjonene som tidligere ble postert på en kundefaktura, og deretter opprette og postere et kreditnotaforslag. 

Det samme dokumentet kan inkludere transaksjoner som er valgt for kreditering, kredittransaksjoner og transaksjoner som er postert. Dokumentet klassifiseres som en faktura eller en kreditnota, avhengig av om totalbeløpet er positivt eller negativt. 

For å kreditere et fakturert beløp velger du først det fakturerte beløpet som skal krediteres, og deretter oppretter du en kreditnota. Du oppretter en kreditnota ved å følge samme fremgangsmåte som for generering av en kundefaktura. 

Du kan opprette en faktura som har et negativt beløp, som blir en faktura som klassifiseres som en kreditnota. For å opprette og skrive ut en kreditnota må du velge transaksjonene som tidligere er postert for en kundefaktura, og deretter redigere transaksjonene. Med mindre primæradressen til den juridiske enheten er i Tyskland, vil tittelen på fakturaen være "Korrigerende faktura".



