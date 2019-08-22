---
title: Konfigurere standardkostnader for arbeid og utgifter
description: Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845900"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardkostnader for arbeid og utgifter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt. Denne oppgaven bruker USSI-datasettet.

1. Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time).
2. Klikk Ny.
3. Angi en dato i feltet Gyldighetsdato.
4. Angi et tall i Kostpris-feltet.
    * Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse. Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.  
5. Klikk Lagre.
6. Lukk siden.
7. Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time).
8. Klikk Ny.
9. Angi en dato i feltet Gyldighetsdato.
10. Velg et alternativ i feltet Gjelder for.
11. Angi et tall i Prissetting-feltet.
    * Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori. Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse. Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå. Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.  
12. Klikk Lagre.
13. Lukk siden.
14. Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift).
15. Klikk Ny.
16. Angi en dato i feltet Gyldighetsdato.
17. Angi et tall i Kostpris-feltet.
    * Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.  
18. Klikk Lagre.
19. Lukk siden.
20. Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift).
21. Klikk Ny.
22. Angi en dato i feltet Gyldighetsdato.
23. Velg et alternativ i feltet Gjelder for.
24. Angi et tall i Prissetting-feltet.
    * Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå. Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.  
25. Klikk Lagre.

