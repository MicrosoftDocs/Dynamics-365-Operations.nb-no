---
title: Definer mva-koder
description: Dette emnet forklarer hvordan du definerer merverdiavgiftskoder i Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834836"
---
# <a name="set-up-sales-tax-codes"></a>Definer mva-koder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du definerer merverdiavgiftskoder i Dynamics 365 for Finance and Operations. Mva-koder opprettes for hver indirekte merverdiavgift eller annen avgift som den juridiske enheten er forpliktet til å beregne, samle inn og betale til skattemyndighetene.

Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Avgift > Indirekte avgifter > Merverdiavgift > Mva-koder**.
2. Velg **Ny**.
3. Skriv inn en verdi i **Mva-kode**-feltet.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg en **utligningsperiode** ved å åpne rullegardinlisten for å angi hvilken skattemyndighet og i hvilke intervaller denne merverdiavgiften må rapporteres og betales.
6. Velg en **finansposteringsgruppe** for å angi hovedkontoene for å postere merverdiavgift til økonomimodul.
7. Vis hurtigfanen **Beregning**. Den inneholder flere felt som kontrollerer hvordan mva-beløp skal beregnes. Fyll ut disse feltene etter behov.  
8. I **handlingsruten** øverst i grensesnittet velger du **Mva-kode**.
9. Velg **Verdier**.
10. Angi verdien for denne mva-koden i **Verdi**-kolonnen.
    - Hvis Beløp per enhet er valg i hurtigfanen **Beregning** i Opprinnelse-feltet, ganges verdien med antallet på transaksjonen for å beregne mva-beløpet.  Hvis mva-koden ikke er en enhetsbasert avgift, er verdien en prosent som er brukt på opprinnelsen for denne mva-koden for å beregne mva-beløpet.     
11. Velg **Lagre**.
12. Lukk siden.
13. Velg **Lagre**.

