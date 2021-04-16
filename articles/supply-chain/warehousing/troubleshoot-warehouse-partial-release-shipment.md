---
title: Feilsøke delvise frigivelser og delvise leveringer
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828160"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="6873a-103">Feilsøke delvise frigivelser og delvise leveringer</span><span class="sxs-lookup"><span data-stu-id="6873a-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6873a-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6873a-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="6873a-105">Frigivelsesstatusen til en salgsordre forblir Delvis frigitt, selv etter at salgsordren er fakturert.</span><span class="sxs-lookup"><span data-stu-id="6873a-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6873a-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6873a-106">Issue description</span></span>

<span data-ttu-id="6873a-107">En salgsordre er en leveringsordre, men én eller flere varer i den har en annen leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="6873a-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="6873a-108">Når ordren er fakturert, har den fremdeles frigivelsesstatusen *Delvis frigitt*.</span><span class="sxs-lookup"><span data-stu-id="6873a-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="6873a-109">En salgsordre har for eksempel to varer: en for levering og en for plukking.</span><span class="sxs-lookup"><span data-stu-id="6873a-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="6873a-110">Både leveringen og plukkingen er utført.</span><span class="sxs-lookup"><span data-stu-id="6873a-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="6873a-111">Derfor er begge linjene fakturert.</span><span class="sxs-lookup"><span data-stu-id="6873a-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="6873a-112">Frigivelsesstatusen vises imidlertid fremdeles som *Delvis frigitt*, som er villedende.</span><span class="sxs-lookup"><span data-stu-id="6873a-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6873a-113">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="6873a-113">Issue resolution</span></span>

<span data-ttu-id="6873a-114">Frigivelsesstatusen gjelder bare for ordrelinjer der varene er aktivert for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="6873a-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="6873a-115">Derfor forblir frigivelsesstatusen *Delvis frigitt* i dette scenarioet.</span><span class="sxs-lookup"><span data-stu-id="6873a-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="6873a-116">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="6873a-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="6873a-117">En utvidelse kan legges til som en del av følgeseddelen og faktureringsprosessen for å oppdatere frigivelsesstatusen.</span><span class="sxs-lookup"><span data-stu-id="6873a-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]