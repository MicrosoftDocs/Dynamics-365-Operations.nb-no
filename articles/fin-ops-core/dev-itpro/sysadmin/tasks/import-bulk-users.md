---
title: Importere brukere fra Azure Active Directory
description: Denne fremgangsmåten kan brukes av systemansvarlige til å manuelt importere utvalgte brukere eller importere et stort antall brukere fra Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745795"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="3c72f-103">Importere brukere fra Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3c72f-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="3c72f-104">Importere utvalgte brukere</span><span class="sxs-lookup"><span data-stu-id="3c72f-104">Import select users</span></span>

<span data-ttu-id="3c72f-105">Denne fremgangsmåten kan brukes av systemansvarlige til å importere utvalgte brukere fra Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3c72f-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="3c72f-106">Brukeren vil bli importert til det gjeldende øktfirmaet som standardfirma.</span><span class="sxs-lookup"><span data-stu-id="3c72f-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3c72f-107">Endre gjeldende firma hvis det er aktuelt, før du importerer brukere.</span><span class="sxs-lookup"><span data-stu-id="3c72f-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3c72f-108">Gå til **Systemadministrasjon > Brukere > Brukere**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="3c72f-109">Klikk **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-109">Click **Import users**.</span></span>
4. <span data-ttu-id="3c72f-110">Velg brukerne som skal importeres, og velg **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="3c72f-111">Når importen er fullført, må det tilordnes roller til brukerne.</span><span class="sxs-lookup"><span data-stu-id="3c72f-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="3c72f-112">Masseimportere brukere</span><span class="sxs-lookup"><span data-stu-id="3c72f-112">Import users in bulk</span></span>

<span data-ttu-id="3c72f-113">Denne fremgangsmåten kan brukes av systemansvarlige til å importere et stort antall brukere fra Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c72f-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="3c72f-114">Vær oppmerksom på at det ikke er mulig å velge brukere når du bruker alternativet for satsvis import.</span><span class="sxs-lookup"><span data-stu-id="3c72f-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="3c72f-115">Kjøre importen som en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="3c72f-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="3c72f-116">Brukeren vil bli importert til det gjeldende øktfirmaet som standardfirma.</span><span class="sxs-lookup"><span data-stu-id="3c72f-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3c72f-117">Endre gjeldende firma hvis det er aktuelt, før du importerer brukere.</span><span class="sxs-lookup"><span data-stu-id="3c72f-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3c72f-118">Gå til **Systemadministrasjon > Brukere > Brukere**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="3c72f-119">Klikk **Satsvis import**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="3c72f-120">Vis delen **Kjør i bakgrunnen**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="3c72f-121">Velg **Ja** i feltet **Satsvis behandling**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="3c72f-122">Angi eller velg en verdi i feltet **Satsvis gruppe**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="3c72f-123">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="3c72f-123">This is an optional step.</span></span>  
7. <span data-ttu-id="3c72f-124">Velg **Ja** i feltet **Privat**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="3c72f-125">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="3c72f-125">This is an optional step.</span></span>  
8. <span data-ttu-id="3c72f-126">Velg **Ja** i feltet **Kritisk jobb**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="3c72f-127">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="3c72f-127">This is an optional step.</span></span>  
9. <span data-ttu-id="3c72f-128">Velg et alternativ i feltet **Overvåkingskategori**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="3c72f-129">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-129">Click **OK**.</span></span>

<span data-ttu-id="3c72f-130">Når importen er fullført, må det tilordnes roller til brukerne.</span><span class="sxs-lookup"><span data-stu-id="3c72f-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3c72f-131">Kjøre i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="3c72f-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3c72f-132">Velg **Satsvis import**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="3c72f-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c72f-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]