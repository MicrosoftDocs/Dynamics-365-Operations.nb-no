---
title: Alternativer for å hindre rabatter for detaljhandelsprodukter
description: Det finnes ulike årsaker til hvorfor forhandlere vil forhindre at noen produkter rabatteres, fra en kampanje eller ved salget på salgsstedet.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550750"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Alternativer for å hindre rabatter for detaljhandelsprodukter

[!include [banner](includes/banner.md)]

Det finnes ulike årsaker til hvorfor forhandlere vil forhindre at noen produkter rabatteres, fra en kampanje eller ved salget på salgsstedet.

De følgende alternativene, som finnes på **Detaljhandel**-kategorien for frigitte produkter, gjør at produktet kan konfigureres for å hindre alle eller manuelle rabatter. Innstillingene kan også angis på kategorinivå fra kategorihierarkiet for detaljhandel.

- **Forhindre alle rabatter** – Velg dette alternativet for å forhindre at alle typer rabatter brukes på dette produktet. Dette inkluderer kampanjer som samlerabatt, antalls- og terskelrabatter, i tillegg til rabatter for manuelle linjerabatter og transaksjonsrabatter som brukes under et salg av en POS-bruker.
- **Hindre manuelle rabatter** – Velg dette alternativet for bare å hindre de manuelle linjerabattene eller transaksjonsrabattene som brukes under et salg av en POS-bruker. Produkter med dette alternativet valgt er fremdeles kvalifisert for kampanjer, for eksempel samlerabatt, antalls- og terskelrabatter.

> [!NOTE]
> Disse innstillingene begrenser ikke operasjonen for prisoverstyring, fordi det angir basisprisen og behandles ikke som en rabatt.

[![hindre rabatter-felt](./media/prevent-discounts.png)](./media/prevent-discounts.png)
