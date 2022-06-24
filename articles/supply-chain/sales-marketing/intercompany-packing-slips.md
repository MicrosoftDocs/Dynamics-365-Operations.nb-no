---
title: Konserninterne følgesedler
description: Denne artikkelen beskriver hvordan du genererer og skriver ut følgesedler for konserninterne transaksjoner
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3516058bbf925df4b0a0c75286a3d97457cc1e69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900861"
---
# <a name="intercompany-packing-slips"></a>Konserninterne følgesedler

## <a name="generate-intercompany-packing-slips"></a>Generere konserninterne følgesedler

[!include [banner](../../includes/banner.md)]

Hvis du jobber med direktelevering, genereres alltid følgeseddelen automatisk på både den konserninterne bestillingen og på den originale salgsordren når du genererer følgeseddelen på den konserninterne salgsordren. Den konserninterne bestillingsfakturaen er basert på følgeseddelen til den internkonserne bestillingen som ble generert tidligere.

Hvis du oppdaterer følgeseddelen på den konserninterne salgsordren, reflekteres disse oppdateringene på både den konserninterne bestillingen og den originale salgsordren.

Hvis du ikke jobber med direktelevering, må du generere følgeseddelen manuelt på den konserninterne salgsordren eller den konserninterne bestillingen, og på den originale salgsordren.

## <a name="print-intercompany-packing-slips"></a>Skrive ut konserninterne følgesedler

[!include [banner](../../includes/banner.md)]

Hvis du jobber med direktelevering, kan følgeseddelen for den konserninterne bestillingen og den originale salgsordren automatisk skrives ut når du postere følgeseddelen på den konserninterne salgsordren.

Hvis du vil skrive ut følgesedler automatisk, velger du begge feltene for **Skriv ut følgesedler automatisk** på **Konsernintern**-siden for bestillinger.

Hvis du oppdaterer følgeseddelen på den konserninterne salgsordren, reflekteres endringene automatisk på den konserninterne bestillingen og den originale salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
