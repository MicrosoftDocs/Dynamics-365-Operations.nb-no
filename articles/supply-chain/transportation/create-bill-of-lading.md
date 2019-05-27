---
title: Opprett et fraktbrev
description: Dette emnet beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552075"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="4e178-103">Opprett et fraktbrev</span><span class="sxs-lookup"><span data-stu-id="4e178-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e178-104">Dette emnet beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="4e178-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="4e178-105">Et fraktbrev er et juridisk dokument mellom firmaet som leverer varene, og transportøren.</span><span class="sxs-lookup"><span data-stu-id="4e178-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="4e178-106">Dokumentet følger med de leverte varene og fungerer som en kvittering for forsendelsen når varene blir levert til målet.</span><span class="sxs-lookup"><span data-stu-id="4e178-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="4e178-107">Hvis du bruker lagerstyring, er det to måter å generere et fraktbrev på:</span><span class="sxs-lookup"><span data-stu-id="4e178-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="4e178-108">Opprette rapporten manuelt på **Fraktbrev**-siden.</span><span class="sxs-lookup"><span data-stu-id="4e178-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="4e178-109">Generere rapporten fra **arbeidsområdet for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="4e178-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="4e178-110">Hvis du genererer fraktbrevet fra **arbeidsområdet for lastplanlegging**, må laststatusen være **Sendt.**</span><span class="sxs-lookup"><span data-stu-id="4e178-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="4e178-111">Hvis det er mer enn én forsendelse i lasten, opprettes et fraktbrev for hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="4e178-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="4e178-112">Når et fraktbrev er opprettet, kan du kan gjøre endringer i det på **Fraktbrev**-siden.</span><span class="sxs-lookup"><span data-stu-id="4e178-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="4e178-113">Hovedfraktbrev</span><span class="sxs-lookup"><span data-stu-id="4e178-113">Master bill of lading</span></span>
<span data-ttu-id="4e178-114">Hvis det er mer enn én forsendelse i lasten, kan du generere et hovedfraktbrev.</span><span class="sxs-lookup"><span data-stu-id="4e178-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="4e178-115">Dette har samme oppsett og informasjon som et fraktbrev, men inneholder en oppsummering av alle forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="4e178-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="4e178-116">Hvis alternativet **Opprett et hovedfraktbrev når det er mer enn én forsendelse i en last** er satt til **Ja** på **Parametere for transportstyring**-siden, genereres automatisk et hovedfraktbrev hvis du oppretter et fraktbrev fra **Arbeidsområde for lastplanlegging**, og det er mer enn én forsendelse.</span><span class="sxs-lookup"><span data-stu-id="4e178-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="4e178-117">Du kan også få en oversikt over fraktbrev ved å klikke **Relatert informasjon** &gt; **Fraktbrev**.</span><span class="sxs-lookup"><span data-stu-id="4e178-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="4e178-118">Hvis du oppretter fraktbrev manuelt, kan du opprette et hovedfraktbrev på **Fraktbrev**-siden.</span><span class="sxs-lookup"><span data-stu-id="4e178-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



