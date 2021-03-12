---
title: Definere mva-utligningsperioder
description: Dette emnet forklarer hvordan du definerer mva-utligningsperioder i Dynamics 365 Finance.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8683f3b6e10efe6e975ae6bc3d7863f884bb9a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994471"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Definere mva-utligningsperioder

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du definerer mva-utligningsperioder. Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for. En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall. Alle mva-koder som er knyttet til utligningsperioden, blir utlignet. Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.

Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. I navigasjonsruten går du til **Moduler > Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder**.
2. Velg **Ny**.
3. Angi en verdi i feltet **Utligningsperiode**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. I **Skattemyndighet**-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.
6. Finn og velg ønsket post i listen.
7. Velg det ønskede oppslaget på rullegardinmenyen i feltet **Betalingsbetingelser**. Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura. Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.  
8. Velg en type for utligningsperiodeintervallet.
9. Angi antall enheter i periodeintervallet per periode. Et kvartal har for eksempel 3 måneder.
10. Merk av eller fjern merket i avmerkingsboksen **Bruk satsvis behandling for utligning av merverdiavgift**. Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen. Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.  
    > [!NOTE]
    > For øyeblikket støttes ikke dette i Spania, Japan og Nederland.
11. Merk eller fjern merket i avmerkingsboksen **Hindre generering av transaksjoner for motregningsavgift**. Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall. Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.
12. Utvid kategorien **Periodeintervaller**.
13. Velg **Legg til**.
14. Angi en dato i **Fra dato**-feltet på den nye raden.
15. Angi en dato i **Til dato**-feltet.
16. Velg **Nytt periodeintervall**. Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk. Du kan gå tilbake og legge til nye periodeintervallene etter behov.  
17. Lukk siden.

