--- 
title: "Opprette en konfigurasjonsleverandør og merke den som aktiv for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="72791-103">Opprette en konfigurasjonsleverandør og merke den som aktiv for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="72791-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72791-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="72791-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="72791-105">Hver ER-konfigurasjon refererer til leverandøren som forfatteren av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="72791-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="72791-106">I dette eksemplet skal du opprette en konfigurasjonsleverandør for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjonsleverandører deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="72791-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="72791-107">Opprette en leverandør</span><span class="sxs-lookup"><span data-stu-id="72791-107">Create a provider</span></span>
1. <span data-ttu-id="72791-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="72791-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="72791-109">Klikk Konfigurasjonsleverandører.</span><span class="sxs-lookup"><span data-stu-id="72791-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="72791-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="72791-110">Click New.</span></span>
    * <span data-ttu-id="72791-111">En leverandørpost har et unikt navn og URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="72791-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="72791-112">Se gjennom innholdet på denne siden, og hopp over denne fremgangsmåten hvis en post for Litware, Inc. (http://www.litware.com) finnes allerede.</span><span class="sxs-lookup"><span data-stu-id="72791-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="72791-113">Skriv inn Litware, Inc. i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="72791-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="72791-114">Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="72791-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="72791-115">Skriv inn "http://www.litware.com" i feltet Internett-adresse.</span><span class="sxs-lookup"><span data-stu-id="72791-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="72791-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="72791-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="72791-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="72791-117">Click Save.</span></span>
7. <span data-ttu-id="72791-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="72791-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="72791-119">Velg som en aktiv leverandør</span><span class="sxs-lookup"><span data-stu-id="72791-119">Select as an active provider</span></span>
1. <span data-ttu-id="72791-120">Velg levandøren Litware, Inc. provider.</span><span class="sxs-lookup"><span data-stu-id="72791-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="72791-121">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="72791-121">Click Set active.</span></span>


