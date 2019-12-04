---
title: Integrert original for leverandør
description: Dette emnet beskriver integreringen av leverandørdata mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770997"
---
# <a name="integrated-vendor-master"></a>Integrert original for leverandør

[!include [banner](../includes/banner.md)]

Begrepet *leverandør* refererer til en leverandørorganisasjon eller en enkelt innehaver som er en del av forsyningskjedeprosessen, og som leverer varer til virksomheten. Selv om *leverandør* er et etablert begrep i Finance and Operations-apper, finnes det ikke noe leverandørbegrep i andre Dynamics 365-apper. I stedet overbelaster noen firmaer kontoenheten for å lagre både kundeinformasjon og leverandørinformasjon. Andre bedrifter bruker et egendefinert leverandørbegrep. Common Data Service-integrering støtter begge disse utforminger. Du kan derfor aktivere en av utformingene, avhengig av forretningsscenarioet.

Integrering av leverandørdata mellom Finance and Operations-apper og andre Dynamics 365-apper gjør at du kan bruke dataene i flere maler. Uansett hvor leverandørdataene kommer fra, er de integrert bak kulissene på tvers av applikasjonsgrenser og infrastrukturforskjeller. 

### <a name="vendor-data-flow"></a>Flyt for leverandørdata

Hvis du vil bruke andre Dynamics 365-apper for leverandørkontroll, og du vil isolere leverandørinformasjon fra kundeinformasjon, kan du bruke den nye leverandørutformingen.

![Flyt for leverandørdata](media/dual-write-vendor-data-flow.png)

Hvis du vil bruke andre Dynamics 365-apper for leverandørkontroll, og du vil fortsatt bruke kontoenheten til å lagre leverandørinformasjon, kan du bruke den nye utvidede leverandørutformingen. I denne utformingen lagres utvidet leverandørinformasjon, for eksempel leverandørgruppen og leverandørposteringsprofilen, i leverandørdetaljene.

![Utvidet flyt for leverandørdata](media/dual-write-vendor-detail.jpg)

Leverandørkontaktinformasjon ligner på kundekontaktinformasjon. I kulissene lagres kontaktpersonens informasjon og hentes fra de samme enhetene.

## <a name="templates"></a>Maler

Leverandørdata inkluderer all informasjon om leverandøren, for eksempel leverandørgruppe, adresser, kontaktinformasjon, betalingsprofil og fakturaprofil. En samling enhetstilordninger fungerer sammen under leverandørdatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Andre Dynamics 365-apper         | Beskrivelse
----------------------------|---------------------------------|------------
Vendor V2               | Konto | Firmaer som bruker kontoenheten til å lagre leverandørinformasjon, kan fortsette å bruke den på samme måte. De kan også dra fordel av den eksplisitte leverandørfunksjonaliteten som kommer på grunn av Finance and Operations-appintegrasjonen.
Vendor V2               | Msdyn\_vendors | Bedrifter som bruker en egendefinert løsning for leverandører, kan benytte seg av leverandørkonseptet som blir introdusert i Common Data Service, på grunn av Finance and Operations-appintegrasjonen. 
Leverandørgrupper | msdyn_vendorgroups | Denne malen synkroniserer leverandørgruppeinformasjon.
Betalingsmåte for leverandør | msdyn_vendorpaymentmethods | Denne malen synkroniserer informasjon om leverandørbetalingsmåte.
CDS-kontakter V2             | kontakter                        | Malen [kontakter](dual-write-customer.md#cds-contacts-v2-to-contacts) synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
Linjer i betalingsplan      | msdyn_paymentschedulelines      | Malen [betalingstidsplanlinjer](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsplan            | msdyn_paymentschedules          | Malen [betalingsplaner](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsdagslinjer, CDS V2    | msdyn_paymentdaylines           | Malen [betalingsdagslinjer](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synkroniserer referansedata om betalingsdagslinjer for kunder og leverandører.
Betalingsdager, CDS            | msdyn_paymentdays               | Malen [betalingsdager](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
Betalingsbetingelser            | msdyn_paymentterms              | Malen [betalingsbetingelser](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.
Navnevedlegg                | msdyn_nameaffixes               | Malen [navnevedlegg](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
