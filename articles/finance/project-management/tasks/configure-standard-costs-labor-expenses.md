---
title: Konfigurere standardkostnader for arbeid og utgifter
description: Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185411"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardkostnader for arbeid og utgifter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt. Denne oppgaven bruker USSI-datasettet.

1. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.
2. Velg **Ny**.
3. Angi en dato i feltet **Gyldighetsdato**.
4. Angi et tall i **Kostpris**-feltet. Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse. Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.  
5. Velg **Lagre**.
6. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.
7. Velg **Ny**.
8. Angi en dato i feltet **Gyldighetsdato**.
9. Velg et alternativ i feltet **Gjelder for**.
10. Angi et tall i **Prissetting**-feltet. Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori. Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse. Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå. Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.  
11. Velg **Lagre**.
12. Lukk siden.
13. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.
14. Velg **Ny**.
15. Angi en dato i feltet **Gyldighetsdato**.
16. Angi et tall i **Kostpris**-feltet. Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.  
17. Velg **Lagre**.
18. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift)**.
19. Velg **Ny**.
20. Angi en dato i feltet **Gyldighetsdato**.
21. Velg et alternativ i feltet **Gjelder for**.
22. Angi et tall i **Prissetting**-feltet. Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå. Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.  
23. Velg **Lagre**.

