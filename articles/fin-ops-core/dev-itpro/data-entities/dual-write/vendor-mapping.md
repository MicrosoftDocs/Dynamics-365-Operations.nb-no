---
title: Integrert original for leverandør
description: Dette emnet beskriver integrering av leverandørdata mellom Finance and Operations-apper og Dataverse .
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f57a20ed56a761894b2cedf8835310dac098b098
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750624"
---
# <a name="integrated-vendor-master"></a>Integrert original for leverandør

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Begrepet *leverandør* refererer til en leverandørorganisasjon, eller en enkelt innehaver som leverer varer eller tjenester til en virksomhet. Selv om *leverandør* er et etablert begrep i Microsoft Dynamics 365 Supply Chain Management-, finnes det ikke noe leverandørbegrep i modelldrevne apper i Dynamics 365. Du kan imidlertid overbelaste tabellen **Konto/kontakt** for å lagre leverandørinformasjon. Den integrerte leverandørstandarden innfører et eksplisitt leverandørbegrep i modelldrevne apper i Dynamics 365. Du kan enten bruke den nye leverandørutformingen eller butikkleverandørdataene i tabellen **Konto/kontakt**. Dobbel skriving støtter begge metoder.

I begge fremgangsmåtene er leverandørdataene integrert i Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service og Power Apps-portaler. I Supply Chain Management er dataene tilgjengelige for arbeidsflyter som innkjøpsrekvisisjoner og bestillinger.

## <a name="vendor-data-flow"></a>Flyt for leverandørdata

Hvis du ikke vil lagre leverandørdata i tabellen **Konto/kontakt** i Dataverse, kan du bruke den nye leverandørutformingen.

![Flyt for leverandørdata](media/dual-write-vendor-data-flow.png)

Hvis du ikke vil fortsette å lagre leverandørdata i tabellen **Konto/kontakt**, kan du bruke den utvidede leverandørutformingen. Hvis du vil bruke den utvidede leverandørutformingen, må du konfigurere leverandørarbeidsflytene i løsningspakken med dobbel skriving. Hvis du vil ha mer informasjon, se [Bytte mellom leverandørutforminger](vendor-switch.md).

![Utvidet flyt for leverandørdata](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Hvis du bruker Power Apps-portaler for selvbetjeningsleverandører, kan leverandørinformasjonen flyte direkte til Finance and Operations-apper.

## <a name="templates"></a>Maler

Leverandørdata inkluderer all informasjon om leverandøren, for eksempel leverandørgruppe, adresser, kontaktinformasjon, betalingsprofil og fakturaprofil. En samling tabelltilordninger fungerer sammen under leverandørdatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Andre Dynamics 365-apper     | beskrivelse
----------------------------|-----------------------------|------------
Vendor V2                   | Konto                     | Firmaer som bruker kontotabellen til å lagre leverandørinformasjon, kan fortsette å bruke den på samme måte. De kan også dra fordel av den eksplisitte leverandørfunksjonaliteten som kommer på grunn av Finance and Operations-appintegrasjonen.
Vendor V2                   | Msdyn\_vendors              | Bedrifter som bruker en egendefinert løsning for leverandører, kan benytte seg av leverandørkonseptet som blir introdusert i Dataverse, på grunn av Finance and Operations-appintegrasjonen. 
Leverandørgrupper               | msdyn\_vendorgroups         | Denne malen synkroniserer leverandørgruppeinformasjon.
Betalingsmåte for leverandør       | msdyn\_vendorpaymentmethods | Denne malen synkroniserer informasjon om leverandørbetalingsmåte.
CDS-kontakter V2             | kontakter                    | Malen [kontakter](customer-mapping.md#cds-contacts-v2-to-contacts) synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
Linjer i betalingsplan      | msdyn\_paymentschedulelines | Malen [betalingstidsplanlinjer](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsplan            | msdyn\_paymentschedules     | Malen [betalingsplaner](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsdagslinjer, CDS V2    | msdyn\_paymentdaylines      | Malen [betalingsdagslinjer](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synkroniserer referansedata om betalingsdagslinjer for kunder og leverandører.
Betalingsdager, CDS            | msdyn\_paymentdays          | Malen [betalingsdager](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
Betalingsbetingelser            | msdyn\_paymentterms         | Malen [betalingsbetingelser](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.
Navnevedlegg                | msdyn\_nameaffixes          | Malen [navnevedlegg](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]