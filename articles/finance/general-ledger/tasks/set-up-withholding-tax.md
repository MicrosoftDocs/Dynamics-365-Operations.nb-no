---
title: Definere kildeskatt
description: Dette emnet forklarer hvordan du definerer kildeskatt.
author: twheeloc
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fbe2343a56210bfbed01c7d39ebb8c98829e32952fa1037a3ae0845776be064
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768273"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]