---
title: Integrert original for leverandør
description: Dette emnet beskriver integreringen av leverandørdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7794f33aed7364b76a7d5ffd08a068342887e468
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063168"
---
# <a name="integrated-vendor-master"></a>Integrert original for leverandør

[!include [banner](../../includes/banner.md)]



Begrepet *leverandør* refererer til en leverandørorganisasjon, eller en enkelt innehaver som leverer varer eller tjenester til en virksomhet. Selv om *leverandør* er et etablert begrep i Microsoft Dynamics 365 Supply Chain Management-, finnes det ikke noe leverandørbegrep i kundeengasjementsapper i Dynamics 365. Du kan imidlertid overbelaste tabellen **Konto/kontakt** for å lagre leverandørinformasjon. Den integrerte leverandørstandarden innfører et eksplisitt leverandørbegrep i kundeengasjementsapper. Du kan enten bruke den nye leverandørutformingen eller butikkleverandørdataene i tabellen **Konto/kontakt**. Dobbel skriving støtter begge metoder.

I begge fremgangsmåtene er leverandørdataene integrert i Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service og Power Apps-portaler. I Supply Chain Management er dataene tilgjengelige for arbeidsflyter som innkjøpsrekvisisjoner og bestillinger.

## <a name="vendor-data-flow"></a>Flyt for leverandørdata

Hvis du ikke vil lagre leverandørdata i tabellen **Konto/kontakt** i Dataverse, kan du bruke den nye leverandørutformingen.

![Flyt for leverandørdata.](media/dual-write-vendor-data-flow.png)

Hvis du ikke vil fortsette å lagre leverandørdata i tabellen **Konto/kontakt**, kan du bruke den utvidede leverandørutformingen. Hvis du vil bruke den utvidede leverandørutformingen, må du konfigurere leverandørarbeidsflytene i løsningspakken med dobbel skriving. Hvis du vil ha mer informasjon, se [Bytte mellom leverandørutforminger](vendor-switch.md).

![Utvidet flyt for leverandørdata.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Hvis du bruker Power Apps-portaler for selvbetjeningsleverandører, kan leverandørinformasjonen flyte direkte til økonomi- og driftsapper.

## <a name="templates"></a>Maler

Leverandørdata inkluderer all informasjon om leverandøren, for eksempel leverandørgruppe, adresser, kontaktinformasjon, betalingsprofil og fakturaprofil. En samling tabelltilordninger fungerer sammen under leverandørdatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Kundeengasjementsapper     | beskrivelse
----------------------------|-----------------------------|------------
[CDS-kontakter V2](mapping-reference.md#115) | kontakter | Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
[Navnevedlegg](mapping-reference.md#155) | msdyn_nameaffixes | Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.
[Betalingsdagslinjer, CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.
[Betalingsdager, CDS](mapping-reference.md#158) | msdyn_paymentdays | Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
[Linjer i betalingsplan](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.
[Betalingsplan](mapping-reference.md#160) | msdyn_paymentschedules | Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
[Betalingsbetingelser](mapping-reference.md#161) | msdyn_paymentterms | Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.
[Leverandører V2](mapping-reference.md#202) | msdyn_vendors | Bedrifter som bruker en egendefinert løsning for leverandører, kan benytte seg av leverandørkonseptet som blir introdusert i Dataverse, på grunn av Finance and Operations-appintegrasjonen.
[Leverandørgrupper](mapping-reference.md#200) | msdyn_vendorgroups | Denne malen synkroniserer leverandørgruppeinformasjon.
[Betalingsmåte for leverandør](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Denne malen synkroniserer informasjon om leverandørbetalingsmåte.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
