---
title: Postmaler
description: "Denne artikkelen introduserer konseptet med postmaler og forklarer hvordan de kan brukes til å opprette poster som deler informasjon."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ef5e95d9d6beed10cd6c80aa131c5cbef85c07a8
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="record-templates"></a><span data-ttu-id="c8e7f-103">Postmaler</span><span class="sxs-lookup"><span data-stu-id="c8e7f-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c8e7f-104">Denne artikkelen introduserer konseptet med postmaler og forklarer hvordan de kan brukes til å opprette poster som deler informasjon.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="c8e7f-105">Postmaler kan bidra til å opprette poster raskere i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c8e7f-106">Du kan opprette postmaler for bare noen av posttypene i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="c8e7f-107">Tenk deg for eksempel at du skriver inn informasjon om billeie for leiebilbedrifter som er plassert i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="c8e7f-108">Siden de fleste kundene sannsynligvis er fra San Francisco-området, vil det være praktisk hvis du kan automatisk fylle ut verdiene for feltene **Status**, **Land** og **Poststed** på leieskjemaet.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="c8e7f-109">Du kan bare søke på maler for de områdene av Finance and Operations du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="c8e7f-110">Du kan imidlertid se navnene på alle malene når du oppretter en ny post, og det samme gjelder også for andre brukere hvis du oppretter maler som er tilgjengelige for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="c8e7f-111">Husk å ta hensyn til dette når du gir malene navn.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="c8e7f-112">Unngå for eksempel å bruke navn som inneholder ord som provisjon hvis det der konfidensielt at enkelte ansatte i firmaet har provisjonsbasert lønn.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="c8e7f-113">Når én eller flere maler som du har tilgang til, finnes for et bestemt skjema og du prøver å opprette en ny post i skjemaet, vises siden **Velg en mal for**.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="c8e7f-114">Når du velger en mal fra listen, opprettes den nye posten med standardinformasjon som er basert på malen du velger.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="c8e7f-115">Hvis du ikke vil bruke maler når du oppretter nye poster, merker du av for **Ikke spør meg igjen** på siden **Velg en mal for**.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="c8e7f-116">Hvis du vil vise dialogboksen for valg av mal på nytt, høyreklikker du på **Postinformasjon** og deretter **Vis malvalg**.</span><span class="sxs-lookup"><span data-stu-id="c8e7f-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




