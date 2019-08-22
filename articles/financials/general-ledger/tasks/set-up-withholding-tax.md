---
title: Definere kildeskatt
description: Dette emnet forklarer hvordan du definerer kildeskatt.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834740"
---
# <a name="set-up-withholding-tax"></a>Definere kildeskatt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du definerer kildeskatt. *Kildeskatt* er en leverandørskatt som ikke fører til merverditransaksjoner. Withholding tax som beregnes for leverandørbetaling, er gjeld. Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax. Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.

1. Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Kildeskattkode**.
4. Angi navnet på kildeskattkoden i feltet **Navn på kildeskatt**.
5. Velg hovedkontoen for postering av kildeskattgjelden i **Hovedkonto**-feltet.
6. Velg **Lagre**.
7. Velg **Verdier**, og marker den ønskede posten i listen.
8. Angi en prosent som brukes til beregning av kildeskatten, i **Verdi**-feltet.
9. Velg **Lagre**.
10. Lukk siden.
11. Velg **Lagre**.
12. Lukk siden.
13. Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper**.
14. Velg **Ny**.
15. Angi identifikatoren til kildeskattgruppen i feltet **Kildeskattgruppe**.
16. I **Beskrivelse**-feltet skriver du inn navnet på kildeskattgruppen.
17. Velg kildeskattkoden i **Kildeskattkode**-feltet.
18. Velg **Lagre**.
19. Lukk siden.

