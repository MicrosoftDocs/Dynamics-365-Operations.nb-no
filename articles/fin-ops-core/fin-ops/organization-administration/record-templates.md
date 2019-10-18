---
title: Oversikt over postmaler
description: Denne artikkelen introduserer konseptet med postmaler og forklarer hvordan de kan brukes til å opprette poster som deler informasjon.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179306"
---
# <a name="record-templates-overview"></a><span data-ttu-id="99f05-103">Oversikt over postmaler</span><span class="sxs-lookup"><span data-stu-id="99f05-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99f05-104">Denne artikkelen introduserer konseptet med postmaler og forklarer hvordan de kan brukes til å opprette poster som deler informasjon.</span><span class="sxs-lookup"><span data-stu-id="99f05-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="99f05-105">Postmaler kan hjelpe deg å opprette poster mer effektivt. men du kan imidlertid bare opprette postmaler for noen av posttypene.</span><span class="sxs-lookup"><span data-stu-id="99f05-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="99f05-106">Tenk deg for eksempel at du skriver inn informasjon om billeie for leiebilbedrifter som er plassert i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="99f05-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="99f05-107">Siden de fleste kundene sannsynligvis er fra San Francisco-området, vil det være praktisk hvis du kan automatisk fylle ut verdiene for feltene **Status**, **Land** og **Poststed** på leieskjemaet.</span><span class="sxs-lookup"><span data-stu-id="99f05-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="99f05-108">Du kan bare bruke maler for områder som du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="99f05-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="99f05-109">Du kan imidlertid se navnene på alle malene når du oppretter en ny post, og det samme gjelder også for andre brukere hvis du oppretter maler som er tilgjengelige for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="99f05-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="99f05-110">Husk å ta hensyn til dette når du gir malene navn.</span><span class="sxs-lookup"><span data-stu-id="99f05-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="99f05-111">Unngå for eksempel å bruke navn som inneholder ord som provisjon hvis det der konfidensielt at enkelte ansatte i firmaet har provisjonsbasert lønn.</span><span class="sxs-lookup"><span data-stu-id="99f05-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="99f05-112">Når én eller flere maler som du har tilgang til, finnes for et bestemt skjema og du prøver å opprette en ny post i skjemaet, vises siden **Velg en mal for**.</span><span class="sxs-lookup"><span data-stu-id="99f05-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="99f05-113">Når du velger en mal fra listen, opprettes den nye posten med standardinformasjon som er basert på malen du velger.</span><span class="sxs-lookup"><span data-stu-id="99f05-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="99f05-114">Hvis du ikke vil bruke maler når du oppretter nye poster, merker du av for **Ikke spør meg igjen** på siden **Velg en mal for**.</span><span class="sxs-lookup"><span data-stu-id="99f05-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="99f05-115">Hvis du vil vise dialogboksen for valg av mal på nytt, høyreklikker du på **Postinformasjon** og deretter **Vis malvalg**.</span><span class="sxs-lookup"><span data-stu-id="99f05-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
