---
title: Kan ikke angi servicevareantallet på en salgstilbudslinje
description: Når du arbeider med salgstilbud, kan du ikke angi et salgsantall for produkter som er servicevarer, fordi det ikke er noen fysiske varer som skal telles.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477241"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Kan ikke endre salgsantallet til en servicevare på en salgstilbudslinje

## <a name="symptoms"></a>Symptomer

Hvis du prøver å angi et salgsantall (**SalesQty**-feltet) for en vare av *Service*-typen på en salgstilbudslinje, vil du få følgende melding:

> Oppdatering er ikke tillatt for feltet Antall.

## <a name="cause"></a>Årsak

Denne virkemåten er standard. Du kan ikke angi et salgsantall for produkter som er servicevarer. Hvis du for eksempel tilbyr en tjeneste som installerer en vare, er det ikke fornuftig å registrere et antall, fordi det ikke finnes noen fysisk vare å telle. Det finnes bare en tjeneste.
