---
title: Feilsøke salgstilbud
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgstilbud.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824756"
---
# <a name="troubleshoot-sales-quotations"></a>Feilsøke salgstilbud

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgstilbud.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Jeg kan ikke endre salgsantallet for et salgstilbud for en servicevare.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du prøver å angi et salgsantall (**SalesQty**-feltet) for en vare av *Service*-typen på en salgstilbudslinje, vil du få følgende melding: "Oppdatering er ikke tillatt for feltet Antall".

### <a name="issue-resolution"></a>Problemløsning

Du kan ikke angi et salgsantall for produkter som er servicevarer. Hvis du for eksempel tilbyr en tjeneste som installerer en vare, er det ikke fornuftig å registrere et antall, fordi det ikke finnes noen fysisk vare. Det finnes bare en tjeneste.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]