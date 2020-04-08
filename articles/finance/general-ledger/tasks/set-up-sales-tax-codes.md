---
title: Definer mva-koder
description: Dette emnet forklarer hvordan du definerer merverdiavgiftskoder i Dynamics 365 Finance.
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
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144749"
---
# <a name="set-up-sales-tax-codes"></a>Definer mva-koder

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du definerer merverdiavgiftskoder. Mva-koder opprettes for hver indirekte merverdiavgift eller annen avgift som den juridiske enheten er forpliktet til å beregne, samle inn og betale til skattemyndighetene.

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

