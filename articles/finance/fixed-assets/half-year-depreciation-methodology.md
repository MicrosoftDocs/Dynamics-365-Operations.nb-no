---
title: Metodologi for avskrivningskonvensjon for et halvt år
description: Dette emnet beskriver metoden som brukes ved beregning av anleggsmidler som bruker halvårsavskrivning, som beregner seks måneder med avskrivning i løpet av et anleggsmiddelets første og siste år i bruk.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d0e33128c37e970ebf5af87bd601ae30aef96952
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818590"
---
# <a name="half-year-depreciation-convention-methodology"></a>Metodologi for avskrivningskonvensjon for et halvt år

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver metoden som brukes i anleggsmidler til å beregne avskrivninger ved hjelp av halvårskonvensjon. Halvårskonvensjonen beregner seks måneder med avskrivninger i løpet av et anleggsmiddels første og siste år i bruk. Hvis du vil ha mer informasjon om avskrivningskonvensjoner, kan du se [Avskrivningsmetoder og -konvensjoner](Fixed-asset-depreciation-conventions.md). 

Når du bruker avskrivningskonvensjonen med seks måneder, bruker systemet anskaffelsesåret eller året som anleggsmiddelet ble tatt i bruk, beregner deretter fem år med avskrivninger fra dette året, og legger deretter til seks måneder. Hvis du vil illustrere denne prosessen, kan du vurdere et anleggsmiddel som ble anskaffet til prisen 50 000 og tatt i bruk i april 2020. Anta også at anleggsmiddelet har fem års levetid.

Det første året i bruk avsluttes i desember 2020, som betyr at slutten av anleggsmiddelets levetid vil være i desember 2024. Avskrivningskonvensjonen i halvåret vil legge til seks måneder i anleggsmiddelets levetid, noe som betyr at levetiden avsluttes i juni 2025. 

> Årlig avskrivning 50 000/5 = 10 000 månedlig avskrivning 10 000/12 = 833,33 <br>
> Første års avskrivning 10 000/2 = 5 000 og den neste månedlige avskrivningen 5 000/9 = 555,56

   [![Avskrivningsplan for avskrivningskonvensjon i halvt år](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

De utvidede avskrivningsperiodene som er lagt til av halvårskonvensjonen, gir mer nøyaktig tildeling av avskriving. Avskrivningen på seks måneder representerer avskrivningsutgifter mer likt, som er nyttig for rapportering i resultatregnskapet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]