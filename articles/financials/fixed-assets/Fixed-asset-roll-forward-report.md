---
title: Rapport for fremoverrulling av anleggsmidler
description: Dette emnet forklarer hvordan du bruker rapporten Rull anleggsmidler forover.
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 0a78df4ede8fd57afbc3e9a7e5a38b840f479cdf
ms.contentlocale: nb-no
ms.lasthandoff: 01/25/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Rapport for fremoverrulling av anleggsmidler

[!include[banner](../includes/banner.md)]

**Rull anleggsmidler forover**-rapporten inneholder, i et lesevennlig Microsoft Excel-format, de detaljerte anleggsmiddeldataene du trenger for periodeavslutning, regnskapsoppgjør og mva-rapportering. Rapporten inkluderer start- og sluttsaldoer for anleggsmidler, sammen med vurderingsbevegelser for perioden, og eventuelle nye anleggsmiddelanskaffelser og -salg som ble utført i løpet av perioden. Data rapporteres for individuelle anleggsmidler, og verdier summeres også for anleggsmiddelgrupper og den juridiske enheten.

**Rull anleggsmidler forover**-rapporten bruker rammeverket for elektronisk rapportering (ER). Før du kan kjøre rapporten, må anleggsmiddelmodell- og Rull anleggsmidler forover-konfigurasjonene importeres fra Microsoft Dynamics Lifecycle Services (LCS). hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Denne rapporten er tilgjengelig i Microsoft Dynamics 365 Finance and Operations, Enterprise edition 7.3 eller som en hurtigreparasjon for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017). Tre hurtigreparasjoner må brukes i miljøer som har juli 2017-versjonen:

- **KB 4041754:** Konfigurasjonen for elektronisk rapportering (ER) kan ikke lastes ned fra LCS som ikke gjeldende for gjeldende programversjon etter bruk av plattformoppdateringspakken
- **KB 4056107:** Elektronisk rapportering (GER) – kumulativ oppdatering 5
- **KB 4056353:** Utdrags- og merknadsrapporter for anleggsmidler oppfyller ikke kravene i GAAP og IFRS

Følgende tabell beskriver feltene som er tilgjengelige i rapporten.

| Felt                                       | beskrivelse |
|---------------------------------------------|-------------|
| Saldoer: Åpning                           | Anleggsmiddelets netto bokførte verdi per fra-datoen som er angitt i rapporten. |
| Saldoer: Slutt                           | Anleggsmiddelets netto bokførte verdi per til-datoen som er angitt i rapporten. |
| Anskaffelser: Inngående verdi                 | Summen av alle transaksjoner av typen **Anskaffelse** og **Anskaffelsesjustering** opptil fra-datoen som er angitt i rapporten. |
| Anskaffelser: Periodeanskaffelser           | Summen av alle transaksjoner av typen **Anskaffelse** og **Anskaffelsesjustering** som ble postert i tidsperioden for rapporten. |
| Anskaffelser: Periodeavhendinger              | Summen av alle tilbakeføringer av anskaffelser som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten. |
| Anskaffelser: Lukkingsverdi                 | Summen av alle transaksjoner av typen **Anskaffelse** og **Anskaffelsesjustering** opptil til-datoen som er angitt i rapporten. |
| Avskrivninger: Åpningsverdi                | Summen av alle transaksjoner av typen **Avskrivning**, **Avskrivningsjustering**, **Særskilte avskrivningsfradrag** og **Ekstraordinær avskrivning** opptil fra-datoen som er angitt i rapporten. |
| Avskrivninger: Periodiske avskrivninger         | Summen av alle transaksjoner av typen **Avskrivning**, **Avskrivningsjustering** og **Ekstraordinær avskrivning** som ble postert i tidsperioden for rapporten. |
| Avskrivninger: Periodiske spesielle avskrivninger | Summen av alle transaksjoner av typen **Særskilte avskrivningsfradrag** som ble postert i tidsperioden for rapporten. |
| Avskrivninger: Periodeavhendinger             | Summen av alle tilbakeføringer av avskrivninger som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten. |
| Avskrivninger Lukkingsverdi                | Summen av alle transaksjoner av typen **Avskrivning**, **Avskrivningsjustering**, **Særskilte avskrivningsfradrag** og **Ekstraordinær avskrivning** opptil til-datoen som er angitt i rapporten. |
| Opp-/nedskrivinger: Åpningsverdi        | Summen av alle transaksjoner av typen **Skriv opp justering**, **Skriv ned justering** og **Revaluering** opptil fra-datoen som er angitt i rapporten. |
| Opp-/nedskrivinger: Oppskrivninger for periode     | Summen av alle transaksjoner av typen **Skriv opp justering** som ble postert i tidsperioden for rapporten. |
| Opp-/nedskrivinger: Nedskrivninger for periode   | Summen av alle transaksjoner av typen **Skriv ned justering** som ble postert i tidsperioden for rapporten. |
| Opp-/nedskrivinger: Revalueringer for periode  | Summen av alle transaksjoner av typen **Revaluering** som ble postert i tidsperioden for rapporten. |
| Opp-/nedskrivinger: Periodeavhendinger     | Summen av alle tilbakeføringer av oppskrivninger, nedskrivninger og revalueringer som ble postert som hadde en avhendingstransaksjon i tidsperioden for rapporten. |
| Opp-/nedskrivinger: Lukkingsverdi        | Summen av alle transaksjoner av typen **Skriv opp justering**, **Skriv ned justering** og **Revaluering** opptil til-datoen som er angitt i rapporten. |
| Avhendinger: Avhendingsdato                    | Avhendingsdatoen for anleggsmiddeltablået. |
| Avhendinger: Netto bokført verdi ved avhending       | Netto bokført verdi for anleggsmiddelet ved avhendingstidspunktet. |
| Avhendinger: Salgsverdien                       | Salgsverdien for anleggsmiddeltablået med en avhending – salgstransaksjon. |
| Avhendinger: Skrapverdi                      | Skrapverdien for anleggsmiddeltablået med en avhending – skraptransaksjon. |
| Avhendinger: Resultat                      | Resultatverdien som beregnes som en del av avhendingstransaksjonen for anleggsmiddeltablået. |

