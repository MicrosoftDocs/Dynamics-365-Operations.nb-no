---
title: Feilsøke delvise frigivelser og delvise leveringer
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645954"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="bef51-103">Feilsøke delvise frigivelser og delvise leveringer</span><span class="sxs-lookup"><span data-stu-id="bef51-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bef51-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bef51-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="bef51-105">Frigivelsesstatusen til en salgsordre forblir Delvis frigitt, selv etter at salgsordren er fakturert.</span><span class="sxs-lookup"><span data-stu-id="bef51-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bef51-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bef51-106">Issue description</span></span>

<span data-ttu-id="bef51-107">En salgsordre er en leveringsordre, men én eller flere varer i den har en annen leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="bef51-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="bef51-108">Når ordren er fakturert, har den fremdeles frigivelsesstatusen *Delvis frigitt*.</span><span class="sxs-lookup"><span data-stu-id="bef51-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="bef51-109">En salgsordre har for eksempel to varer: en for levering og en for plukking.</span><span class="sxs-lookup"><span data-stu-id="bef51-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="bef51-110">Både leveringen og plukkingen er utført.</span><span class="sxs-lookup"><span data-stu-id="bef51-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="bef51-111">Derfor er begge linjene fakturert.</span><span class="sxs-lookup"><span data-stu-id="bef51-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="bef51-112">Frigivelsesstatusen vises imidlertid fremdeles som *Delvis frigitt*, som er villedende.</span><span class="sxs-lookup"><span data-stu-id="bef51-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bef51-113">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bef51-113">Issue resolution</span></span>

<span data-ttu-id="bef51-114">Frigivelsesstatusen gjelder bare for ordrelinjer der varene er aktivert for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="bef51-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="bef51-115">Derfor forblir frigivelsesstatusen *Delvis frigitt* i dette scenarioet.</span><span class="sxs-lookup"><span data-stu-id="bef51-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="bef51-116">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="bef51-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="bef51-117">En utvidelse kan legges til som en del av følgeseddelen og faktureringsprosessen for å oppdatere frigivelsesstatusen.</span><span class="sxs-lookup"><span data-stu-id="bef51-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
