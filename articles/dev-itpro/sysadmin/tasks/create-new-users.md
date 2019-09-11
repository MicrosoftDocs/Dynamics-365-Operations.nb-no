---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916490"
---
# <a name="create-new-users"></a><span data-ttu-id="0d0b5-103">Opprette nye brukere</span><span class="sxs-lookup"><span data-stu-id="0d0b5-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d0b5-104">Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="0d0b5-105">Systemansvarlige kan fullføre denne fremgangsmåten for å legge til brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="0d0b5-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="0d0b5-107">Legge til en ny bruker</span><span class="sxs-lookup"><span data-stu-id="0d0b5-107">Add a new user</span></span>
1. <span data-ttu-id="0d0b5-108">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="0d0b5-109">Klikk **Ny** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="0d0b5-110">Skriv inn en verdi i **Bruker-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="0d0b5-111">Angi en unik identifikator for brukeren.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="0d0b5-112">En bruker-ID er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-112">A user ID is required.</span></span>  
4. <span data-ttu-id="0d0b5-113">Skriv inn en verdi i feltet **Brukernavn**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="0d0b5-114">Angi navnet på brukeren.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="0d0b5-115">Skriv inn en verdi i feltet **Domene**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="0d0b5-116">Angi brukerens domene.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="0d0b5-117">Skriv inn en verdi i feltet **Alias**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="0d0b5-118">Angi brukerens alias.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="0d0b5-119">Klikk rullegardinknappen i feltet **Firma** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0d0b5-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="0d0b5-121">Klikk **Tilordne roller** i delen **Brukerens roller**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="0d0b5-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0d0b5-123">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-123">Click **OK**.</span></span>
12. <span data-ttu-id="0d0b5-124">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="0d0b5-125">Importer brukere</span><span class="sxs-lookup"><span data-stu-id="0d0b5-125">Import users</span></span>
1. <span data-ttu-id="0d0b5-126">Klikk **Importer brukere** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="0d0b5-127">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0d0b5-128">Klikk **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-128">Click **Import users**.</span></span>
4. <span data-ttu-id="0d0b5-129">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-129">Click **Close**.</span></span>

