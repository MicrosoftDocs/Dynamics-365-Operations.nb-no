---
title: Definer mva-utligningsperioder
description: Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862994"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Definer mva-utligningsperioder

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    > [!NOTE]
    > For øyeblikket støttes ikke dette i Østerrike, Belgia, Spania, Italia, Japan og Nederland.
14. Merk eller fjern merket i avmerkingsboksen Hindre generering av transaksjoner for motregningsavgift.
    * Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall. Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.
15. Utvid kategorien Periodeintervaller.
16. Klikk Legg til.
17. Merk den valgte raden i listen.
18. Angi en dato i Fra dato-feltet.
19. Angi en dato i Til dato-feltet.
20. Klikk Nytt periodeintervall.
    * Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk. Du kan gå tilbake og legge til nye periodeintervallene etter behov.  
21. Lukk siden.

