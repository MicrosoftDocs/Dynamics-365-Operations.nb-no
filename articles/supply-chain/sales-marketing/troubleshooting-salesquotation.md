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
ms.openlocfilehash: 92b77c1b7de1f5c946e677c810c0d0e43427473e7ba26679df23f7663946dbc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765400"
---
# <a name="troubleshoot-sales-quotations"></a>Feilsøke salgstilbud

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgstilbud.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Jeg kan ikke endre salgsantallet for et salgstilbud for en servicevare.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du prøver å angi et salgsantall (**SalesQty**-feltet) for en vare av *Service*-typen på en salgstilbudslinje, vil du få følgende melding: "Oppdatering er ikke tillatt for feltet Antall".

### <a name="issue-resolution"></a>Problemløsning

Du kan ikke angi et salgsantall for produkter som er servicevarer. Hvis du for eksempel tilbyr en tjeneste som installerer en vare, er det ikke fornuftig å registrere et antall, fordi det ikke finnes noen fysisk vare. Det finnes bare en tjeneste.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]