---
title: Definere mva-utligningsperioder
description: Dette emnet forklarer hvordan du definerer mva-utligningsperioder i Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944783"
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
11. Merk eller fjern merket i avmerkingsboksen **Hindre generering av transaksjoner for motregningsavgift**. Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall. Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.
12. Utvid kategorien **Periodeintervaller**.
13. Velg **Legg til**.
14. Angi en dato i **Fra dato**-feltet på den nye raden.
15. Angi en dato i **Til dato**-feltet.
16. Velg **Nytt periodeintervall**. Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk. Du kan gå tilbake og legge til nye periodeintervallene etter behov.  
17. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
