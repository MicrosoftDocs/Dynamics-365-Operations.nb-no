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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ae7d6bb04dbf06b9b05d9f5610895fced650b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994446"
---
# <a name="set-up-withholding-tax"></a>Definere kildeskatt

[!include [banner](../../includes/banner.md)]

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

