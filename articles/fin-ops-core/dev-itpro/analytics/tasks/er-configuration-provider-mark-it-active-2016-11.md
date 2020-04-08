---
title: Opprette konfigurasjonsleverandører og merke dem som aktive
description: Dette emnet forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5f238a492dbc3f9318b1bd1d3ea5657e92b33fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142115"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="7f877-103">Opprette konfigurasjonsleverandører og merke dem som aktive</span><span class="sxs-lookup"><span data-stu-id="7f877-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f877-104">Dette emnet forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="7f877-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="7f877-105">Hver ER-konfigurasjon refererer til leverandøren som forfatteren av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="7f877-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="7f877-106">I dette eksemplet skal du opprette en konfigurasjonsleverandør for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjonsleverandører deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="7f877-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="7f877-107">Opprette en leverandør</span><span class="sxs-lookup"><span data-stu-id="7f877-107">Create a provider</span></span>
1. <span data-ttu-id="7f877-108">Gå til **navigasjonsruten** i øvre venstre hjørne, og velg **Organisasjonsstyring**.</span><span class="sxs-lookup"><span data-stu-id="7f877-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="7f877-109">Gå til **Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7f877-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="7f877-110">Gå til **Relaterte koblinger > Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="7f877-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="7f877-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f877-111">Select **New**.</span></span>
    - <span data-ttu-id="7f877-112">En leverandørpost har et unikt navn og URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="7f877-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="7f877-113">Gå gjennom innholdet på denne siden, og hopp over denne fremgangsmåten hvis en post for Litware, Inc. (https://www.litware.com) allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="7f877-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="7f877-114">I Navn-feltet skriver du inn `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="7f877-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="7f877-115">Skriv inn `https://www.litware.com` i feltet Internett-adresse.</span><span class="sxs-lookup"><span data-stu-id="7f877-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="7f877-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7f877-116">Select **Save**.</span></span>
8. <span data-ttu-id="7f877-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f877-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="7f877-118">Velg som en aktiv leverandør</span><span class="sxs-lookup"><span data-stu-id="7f877-118">Select as an active provider</span></span>
1. <span data-ttu-id="7f877-119">Velg levandøren Litware, Inc. provider.</span><span class="sxs-lookup"><span data-stu-id="7f877-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="7f877-120">Velg **Angi som aktiv**.</span><span class="sxs-lookup"><span data-stu-id="7f877-120">Select **Set active**.</span></span>

![Arbeidsområdesiden Elektronisk rapportering](../media/GER-Task-ActiveProvider-1.png)
