---
title: Feilsøke salgstilbud
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgstilbud.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974766"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="97276-103">Feilsøke salgstilbud</span><span class="sxs-lookup"><span data-stu-id="97276-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="97276-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="97276-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="97276-105">Jeg kan ikke endre salgsantallet for et salgstilbud for en servicevare.</span><span class="sxs-lookup"><span data-stu-id="97276-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="97276-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="97276-106">Issue description</span></span>

<span data-ttu-id="97276-107">Hvis du prøver å angi et salgsantall (**SalesQty**-feltet) for en vare av *Service*-typen på en salgstilbudslinje, vil du få følgende melding: "Oppdatering er ikke tillatt for feltet Antall".</span><span class="sxs-lookup"><span data-stu-id="97276-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97276-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="97276-108">Issue resolution</span></span>

<span data-ttu-id="97276-109">Du kan ikke angi et salgsantall for produkter som er servicevarer.</span><span class="sxs-lookup"><span data-stu-id="97276-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="97276-110">Hvis du for eksempel tilbyr en tjeneste som installerer en vare, er det ikke fornuftig å registrere et antall, fordi det ikke finnes noen fysisk vare.</span><span class="sxs-lookup"><span data-stu-id="97276-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="97276-111">Det finnes bare en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="97276-111">There is only a service.</span></span>

