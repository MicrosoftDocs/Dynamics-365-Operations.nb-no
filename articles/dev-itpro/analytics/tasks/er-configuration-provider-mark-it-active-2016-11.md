--- 
title: "Opprette konfigurasjonsleverandører og merke dem som aktive"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="626b1-103">Opprette konfigurasjonsleverandører og merke dem som aktive</span><span class="sxs-lookup"><span data-stu-id="626b1-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="626b1-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="626b1-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="626b1-105">Hver ER-konfigurasjon refererer til leverandøren som forfatteren av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="626b1-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="626b1-106">I dette eksemplet skal du opprette en konfigurasjonsleverandør for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjonsleverandører deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="626b1-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="626b1-107">Opprette en leverandør</span><span class="sxs-lookup"><span data-stu-id="626b1-107">Create a provider</span></span>
1. <span data-ttu-id="626b1-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="626b1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="626b1-109">Klikk Konfigurasjonsleverandører.</span><span class="sxs-lookup"><span data-stu-id="626b1-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="626b1-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="626b1-110">Click New.</span></span>
    * <span data-ttu-id="626b1-111">En leverandørpost har et unikt navn og URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="626b1-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="626b1-112">Gå gjennom innholdet på denne siden, og hopp over denne fremgangsmåten hvis en post for Litware, Inc. (http://www.litware.com) allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="626b1-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="626b1-113">Skriv inn Litware, Inc. i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="626b1-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="626b1-114">Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="626b1-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="626b1-115">Skriv inn http://www.litware.com i feltet Internett-adresse.</span><span class="sxs-lookup"><span data-stu-id="626b1-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="626b1-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="626b1-116">Click Save.</span></span>
7. <span data-ttu-id="626b1-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="626b1-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="626b1-118">Velg som en aktiv leverandør</span><span class="sxs-lookup"><span data-stu-id="626b1-118">Select as an active provider</span></span>
1. <span data-ttu-id="626b1-119">Velg levandøren Litware, Inc. provider.</span><span class="sxs-lookup"><span data-stu-id="626b1-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="626b1-120">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="626b1-120">Click Set active.</span></span>


