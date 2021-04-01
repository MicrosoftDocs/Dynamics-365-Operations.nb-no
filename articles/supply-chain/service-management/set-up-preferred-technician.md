---
title: Definere en foretrukket tekniker
description: Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b2554197c1963cdd7ba0871edb532661d10945
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256069"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="7bdba-103">Definere en foretrukket tekniker</span><span class="sxs-lookup"><span data-stu-id="7bdba-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7bdba-104">Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="7bdba-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="7bdba-105">Det er imidlertid lurt å legge til arbeideren i det aktuelle fordelingsteamet, slik at arbeideren er inkludert i **Tjenestefordeling**.</span><span class="sxs-lookup"><span data-stu-id="7bdba-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="7bdba-106">Tilordne en ansatt til en fordelingsgruppe</span><span class="sxs-lookup"><span data-stu-id="7bdba-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="7bdba-107">Klikk på **Personale** \> **Felles** \> **Arbeidere** \> **Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="7bdba-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="7bdba-108">Dobbeltklikk en arbeider for å åpne siden med arbeiderdetaljer.</span><span class="sxs-lookup"><span data-stu-id="7bdba-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="7bdba-109">I **handlingsruten** klikker du **Oppsett** \>**Fordelingsteam** for å åpne skjemaet **Fordel arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="7bdba-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="7bdba-110">I **Fordelingsteam**-feltet velger du teamet du vil tilordne arbeideren til.</span><span class="sxs-lookup"><span data-stu-id="7bdba-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="7bdba-111">Tilordne en foretrukket tekniker til en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="7bdba-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="7bdba-112">Klikk på **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="7bdba-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="7bdba-113">Dobbeltklikk en serviceavtale for å åpne detaljskjemaet.</span><span class="sxs-lookup"><span data-stu-id="7bdba-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="7bdba-114">I fanen **Generelt** velger du feltet **Foretrukket tekniker**, og deretter velger du et medlem i det aktuelle fordelingsteamet som den foretrukne teknikeren for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="7bdba-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="7bdba-115">Tilordne en foretrukket tekniker til en serviceordre</span><span class="sxs-lookup"><span data-stu-id="7bdba-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="7bdba-116">Klikk på **Servicestyring** \> **Periodisk** \> **Tjenestefordeling**.</span><span class="sxs-lookup"><span data-stu-id="7bdba-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="7bdba-117">I skjemaet <STRONG>Tjenestefordeling</STRONG> angir du et datointervall for fordelingsaktiviteter du vil vise.</span><span class="sxs-lookup"><span data-stu-id="7bdba-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="7bdba-118">Velg også om lukkede aktiviteter skal vises og om fordelingsaktivitetslisten skal begrenses til grupper du tilhører eller har tillatelse til å overvåke.</span><span class="sxs-lookup"><span data-stu-id="7bdba-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="7bdba-119">Klikk på <STRONG>OK</STRONG> for å åpne skjemaet <STRONG>Tjenestefordeling</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7bdba-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="7bdba-120">Velg serviceaktivitetslinjen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="7bdba-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="7bdba-121">I fanen **Relatert** bruker du **Arbeider**-listen til å tilordne et medlem av korrekt fordelingsgruppe til foretrukket tekniker for serviceutkallingen.</span><span class="sxs-lookup"><span data-stu-id="7bdba-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bdba-122">Se også</span><span class="sxs-lookup"><span data-stu-id="7bdba-122">See also</span></span>

[<span data-ttu-id="7bdba-123">Oversikt over å utvikle og etablere serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="7bdba-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="7bdba-124">Opprette serviceordrer manuelt</span><span class="sxs-lookup"><span data-stu-id="7bdba-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="7bdba-125">[Serviceavtaler (skjema)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="7bdba-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]