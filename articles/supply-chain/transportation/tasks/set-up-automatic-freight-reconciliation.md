---
title: Definere automatisk fraktavstemming
description: Denne fremgangsmåten viser hvordan du setter opp data for automatisk fraktavstemming.
author: Weijiesa
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ab338f5f231ddded88e08fbf4d31b18750fd03e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672717"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Definere automatisk fraktavstemming

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp data for automatisk fraktavstemming. Dette gjøres vanligvis av en lagersjef. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.


## <a name="set-up-the-freight-bill-type"></a>Definere fraktbrevtypen
1. Gå til Transportstyring > Oppsett > Fraktavstemming > Fraktbrevtype.
    * Fraktbrevtypen definerer hvordan fraktbrev og transportørfakturaer skal sammenlignes.  
2. Klikk på Ny.
3. Skriv inn en verdi i feltet Fraktbrevtype.
4. I Motormontering-feltet skriver du inn Microsoft.Dynamics.Ax.Tms.dll.
    * Dette er standard kodebibliotek for samsvarsmotoren for transportstyring.  
5. I Motorklasse-feltet skriver du inn Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.
    * Dette er standard klasse for samsvarsmotoren for transportstyring.  
6. Klikk på Ny.
7. I Beskrivelse-feltet velger du verdien som skal samsvare på fraktbrevet og transportørfakturaen.  
8. I feltet Samsvar nødvendig velger du Ja.
    * Hvis du setter dette feltet til Ja, betyr det at verdien som er valgt i Beskrivelse-feltet, må samsvare med både fraktbrevet og transportørfakturaen. Hvis du setter det til Nei, kan feltet være tomt på én av disse.  
9. Klikk på Lagre.

## <a name="set-up-the-freight-bill-type-assignment"></a>Definere tilordningen av fraktbrevtype
1. Lukk siden.
2. Gå til Transportstyring > Oppsett > Fraktavstemming > Tilordninger av fraktbrevtype.
    * Fraktbrevtypetilordningen brukes til å angi hvilken fraktbrevtype som skal brukes for en bestemt transportør.   
3. Klikk på Ny.
4. Angi eller velg en verdi i feltet Modus.
5. Angi eller velg en verdi i feltet Transportør.
6. I Fraktbrevtype-feltet velger du fraktbrevtypen du opprettet tidligere.
7. Lukk siden.

## <a name="set-up-the-audit-master"></a>Konfigurere revisjonsstandarden
1. Gå til Transportstyring > Oppsett > Fraktavstemming > Revisjonsstandard.
    * Revisjonsstandarden definerer toleransegrensene for automatisk fraktavstemming. Den angir hvor stor forskjell det kan være mellom pengebeløpet på fraktbrevet og transportørfakturaen og likevel tillate avstemming. Den definerer også hvordan avvik skal håndteres.  
2. Klikk på Ny.
3. Angi en verdi i feltet Revisjonsstandard-ID.
4. Velg samme transportør som du gjorde tidligere, i feltet Transportør.
5. I Fraktbrevtype-feltet velger du fraktbrevtypen du opprettet tidligere.
6. Utvid delen Toleranse.
7. Angi et tall i feltet Minste toleransenivå.
8. Angi et tall i feltet Største toleransenivå.
9. Utvid delen Resultat.
10. Angi eller velg en verdi i feltet Årsakskode for overbetaling.
    * Hvis pengebeløpene er forskjellige på fraktbrevet og transportørfakturaen, angir årsakskodene for over- og underbetaling kontoene som forskjellen skal registreres på, så lenge differansen er innenfor toleransenivåene.  
11. Angi eller velg en verdi i feltet Årsakskode for underbetaling.
12. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]