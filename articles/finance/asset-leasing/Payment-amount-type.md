---
title: Legg til betalingsbeløpstyper
description: Dette emnet forklarer hvordan du definerer betalingsbeløpstyper i aktivaleie.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968325"
---
# <a name="add-payment-amount-types"></a>Legg til betalingsbeløpstyper

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du definerer betalingsbeløpstyper i aktivaleie. På denne måten kan du spesifisere leiebetalingsbeløpet i stedet for å legge til engangsbeløpet i betalingsplanlinjene.

Følg denne fremgangsmåten for å legge til betalingsbeløpstyper.

1. Gå til **Aktivaleie \> Oppsett \> Betalingsbeløpstyper**.
2. Velg **Ny**.
3. Angi den nye betalingstypen og en beskrivelse.

> [!NOTE]
> For IFRS 16-indeksrevaluering må du opprette en betalingsbeløpstype og merke den som **Brukes til IRFS 16-indeksrevaluering**. Denne betalingsbeløpstypen brukes når indeksrevalueringsprosessen kjøres mot IFRS 16-boken, og den vil vurdere endringene som skjedde på grunn av indeksrevalueringsprosessen.
>
> Når alternativet **Betalingsoppdeling** i leien er satt til **Ja**, og hvis indeksrevaluering for IFRS 16 kjøres, men det ikke er noen betalingstype for IFRS 16, fullføres ikke prosessen.

Bare én post kan merkes som **Brukes til IFRS 16-indeksrevaluering**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
