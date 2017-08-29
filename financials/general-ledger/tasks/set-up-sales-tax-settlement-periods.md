--- 
title: Definer mva-utligningsperioder
description: "Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7aa40362278a0a032e909574a59f842840fb9860
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a>Definer mva-utligningsperioder

[!include[task guide banner](../../includes/task-guide-banner.md)]

Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for. En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall. Alle mva-koder som er knyttet til utligningsperioden, blir utlignet. Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.



Denne oppgaven bruker demonstrasjonsfirmaet USMF.



1. Gå til Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder.
2. Klikk Ny.
3. Angi en verdi i feltet Utligningsperiode.
4. Skriv inn en verdi i feltet Beskrivelse.
5. I Skattemyndighet-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i Betalingsbetingelser-feltet for å åpne oppslaget.
    * Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura. Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.  
9. Finn og velg ønsket post i listen.
10. Klikk koblingen i den valgte raden i listen.
11. Velg en type for utligningsperiodeintervallet.
12. Angi antall enheter i periodeintervallet per periode. Et kvartal har for eksempel 3 måneder.
13. Merk av eller fjern merket i avmerkingsboksen Bruk satsvis behandling for utligning av merverdiavgift.
    * Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen. Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.  
14. Utvid kategorien Periodeintervaller.
15. Klikk Legg til.
16. Merk den valgte raden i listen.
17. Angi en dato i Fra dato-feltet.
18. Angi en dato i Til dato-feltet.
19. Klikk Nytt periodeintervall.
    * Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk. Du kan gå tilbake og legge til nye periodeintervallene etter behov.  
20. Lukk siden.


