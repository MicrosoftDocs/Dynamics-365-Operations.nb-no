---
title: Rapport for fremoverrulling av anleggsmidler
description: Dette emnet forklarer hvordan du bruker rapporten Rull anleggsmidler forover.
author: saraschi2
manager: ''
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b91da4679a23ba0a70c18e2bcae1b7f757f661ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969159"
---
# <a name="fixed-assets-roll-forward-report"></a>Rapport for fremoverrulling av anleggsmidler

[!include [banner](../includes/banner.md)]

**Rull anleggsmidler forover**-rapporten inneholder, i et lesevennlig Microsoft Excel-format, de detaljerte anleggsmiddeldataene du trenger for periodeavslutning, regnskapsoppgjør og mva-rapportering. Rapporten inkluderer start- og sluttsaldoer for anleggsmidler, sammen med vurderingsbevegelser for perioden, og eventuelle nye anleggsmiddelanskaffelser og -salg som ble utført i løpet av perioden. Data rapporteres for individuelle anleggsmidler, og verdier summeres også for anleggsmiddelgrupper og den juridiske enheten.

**Rull anleggsmidler forover**-rapporten bruker rammeverket for elektronisk rapportering (ER). Før du kan kjøre rapporten, må anleggsmiddelmodell- og Rull anleggsmidler forover-konfigurasjonene importeres fra Microsoft Dynamics Lifecycle Services (LCS). hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Denne rapporten er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, eller som en hurtigreparasjon for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017). Tre hurtigreparasjoner må brukes i miljøer som har juli 2017-versjonen:

- **KB 4041754:** Konfigurasjonen for elektronisk rapportering (ER) kan ikke lastes ned fra LCS som ikke gjeldende for gjeldende versjon etter bruk av plattformoppdateringspakken
- **KB 4056107:** Elektronisk rapportering (GER) – kumulativ oppdatering 5
- **KB 4056353:** Utdrags- og merknadsrapporter for anleggsmidler oppfyller ikke kravene i GAAP og IFRS

Følgende tabell beskriver feltene som er tilgjengelige i rapporten.


|                    Felt                    |                                                                                                                                beskrivelse                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Saldoer: Åpning              |                                                                                           Anleggsmiddelets netto bokførte verdi per fra-datoen som er angitt i rapporten.                                                                                           |
|              Saldoer: Slutt              |                                                                                            Anleggsmiddelets netto bokførte verdi per til-datoen som er angitt i rapporten.                                                                                            |
|         Anskaffelser: Inngående verdi         |                                                 Summen av alle transaksjoner av typen <strong>Anskaffelse</strong> og <strong>Anskaffelsesjustering</strong> opptil fra-datoen som er angitt i rapporten.                                                  |
|      Anskaffelser: Periodeanskaffelser      |                                                 Summen av alle transaksjoner av typen <strong>Anskaffelse</strong> og <strong>Anskaffelsesjustering</strong> som ble postert i tidsperioden for rapporten.                                                  |
|       Anskaffelser: Periodeavhendinger        |                                                                        Summen av alle tilbakeføringer av anskaffelser som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten.                                                                        |
|         Anskaffelser: Lukkingsverdi         |                                                  Summen av alle transaksjoner av typen <strong>Anskaffelse</strong> og <strong>Anskaffelsesjustering</strong> opptil til-datoen som er angitt i rapporten.                                                   |
|        Avskrivninger: Åpningsverdi         | Summen av alle transaksjoner av typen <strong>Avskrivning</strong>, <strong>Avskrivningsjustering</strong>, <strong>Særskilte avskrivningsfradrag</strong> og <strong>Ekstraordinær avskrivning</strong> opptil fra-datoen som er angitt i rapporten. |
|     Avskrivninger: Periodiske avskrivninger     |                         Summen av alle transaksjoner av typen <strong>Avskrivning</strong>, <strong>Avskrivningsjustering</strong> og <strong>Ekstraordinær avskrivning</strong> som ble postert i tidsperioden for rapporten.                          |
| Avskrivninger: Periodiske spesielle avskrivninger |                                                              Summen av alle transaksjoner av typen <strong>Særskilte avskrivningsfradrag</strong> som ble postert i tidsperioden for rapporten.                                                               |
|       Avskrivninger: Periodeavhendinger       |                                                                       Summen av alle tilbakeføringer av avskrivninger som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten.                                                                        |
|        Avskrivninger Lukkingsverdi         |  Summen av alle transaksjoner av typen <strong>Avskrivning</strong>, <strong>Avskrivningsjustering</strong>, <strong>Særskilte avskrivningsfradrag</strong> og <strong>Ekstraordinær avskrivning</strong> opptil til-datoen som er angitt i rapporten.  |
|    Opp-/nedskrivinger: Åpningsverdi     |                              Summen av alle transaksjoner av typen <strong>Skriv opp justering</strong>, <strong>Skriv ned justering</strong> og <strong>Revaluering</strong> opptil fra-datoen som er angitt i rapporten.                               |
|   Opp-/nedskrivinger: Oppskrivninger for periode   |                                                                    Summen av alle transaksjoner av typen <strong>Skriv opp justering</strong> som ble postert i tidsperioden for rapporten.                                                                    |
|  Opp-/nedskrivinger: Nedskrivninger for periode  |                                                                   Summen av alle transaksjoner av typen <strong>Skriv ned justering</strong> som ble postert i tidsperioden for rapporten.                                                                   |
| Opp-/nedskrivinger: Revalueringer for periode  |                                                                        Summen av alle transaksjoner av typen <strong>Revaluering</strong> som ble postert i tidsperioden for rapporten.                                                                        |
|   Opp-/nedskrivinger: Periodeavhendinger   |                                                           Summen av alle tilbakeføringer av oppskrivninger, nedskrivninger og revalueringer som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten.                                                           |
|    Opp-/nedskrivinger: Lukkingsverdi     |                               Summen av alle transaksjoner av typen <strong>Skriv opp justering</strong>, <strong>Skriv ned justering</strong> og <strong>Revaluering</strong> opptil til-datoen som er angitt i rapporten.                                |
|          Avhendinger: Avhendingsdato           |                                                                                                                Avhendingsdatoen for anleggsmiddeltablået.                                                                                                                |
|    Avhendinger: Netto bokført verdi ved avhending    |                                                                                                    Netto bokført verdi for anleggsmiddelet ved avhendingstidspunktet.                                                                                                    |
|            Avhendinger: Salgsverdien            |                                                                                               Salgsverdien for anleggsmiddeltablået med en avhending – salgstransaksjon.                                                                                                |
|           Avhendinger: Skrapverdi            |                                                                                               Skrapverdien for anleggsmiddeltablået med en avhending – skraptransaksjon.                                                                                               |
|           Avhendinger: Resultat            |                                                                                 Resultatverdien som beregnes som en del av avhendingstransaksjonen for anleggsmiddeltablået.                                                                                 |

