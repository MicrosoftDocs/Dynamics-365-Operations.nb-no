--- 
title: Opprette nye brukere
description: "Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-new-users"></a><span data-ttu-id="e2f99-103">Opprette nye brukere</span><span class="sxs-lookup"><span data-stu-id="e2f99-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2f99-104">Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.</span><span class="sxs-lookup"><span data-stu-id="e2f99-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="e2f99-105">Systemansvarlige kan fullføre denne fremgangsmåten for å legge til brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="e2f99-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="e2f99-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e2f99-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="e2f99-107">Legge til en ny bruker</span><span class="sxs-lookup"><span data-stu-id="e2f99-107">Add a new user</span></span>
1. <span data-ttu-id="e2f99-108">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="e2f99-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e2f99-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e2f99-109">Click New.</span></span>
3. <span data-ttu-id="e2f99-110">Skriv inn en verdi i Bruker-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="e2f99-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="e2f99-111">Angi en unik identifikator for brukeren.</span><span class="sxs-lookup"><span data-stu-id="e2f99-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="e2f99-112">En bruker-ID er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e2f99-112">A user ID is required.</span></span>  
4. <span data-ttu-id="e2f99-113">Skriv inn en verdi i feltet Brukernavn.</span><span class="sxs-lookup"><span data-stu-id="e2f99-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="e2f99-114">Angi navnet på brukeren.</span><span class="sxs-lookup"><span data-stu-id="e2f99-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="e2f99-115">Skriv inn en verdi i feltet Domene.</span><span class="sxs-lookup"><span data-stu-id="e2f99-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="e2f99-116">Angi brukerens domene.</span><span class="sxs-lookup"><span data-stu-id="e2f99-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="e2f99-117">Skriv inn en verdi i feltet Alias.</span><span class="sxs-lookup"><span data-stu-id="e2f99-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="e2f99-118">Angi brukerens alias.</span><span class="sxs-lookup"><span data-stu-id="e2f99-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="e2f99-119">Klikk rullegardinknappen i feltet Firma for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e2f99-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e2f99-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e2f99-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e2f99-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e2f99-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2f99-122">Velge brukerens firma</span><span class="sxs-lookup"><span data-stu-id="e2f99-122">Select the user's company</span></span>  
10. <span data-ttu-id="e2f99-123">Klikk Tilordne roller.</span><span class="sxs-lookup"><span data-stu-id="e2f99-123">Click Assign roles.</span></span>
11. <span data-ttu-id="e2f99-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e2f99-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e2f99-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e2f99-125">Click OK.</span></span>
13. <span data-ttu-id="e2f99-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e2f99-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="e2f99-127">Importer brukere</span><span class="sxs-lookup"><span data-stu-id="e2f99-127">Import users</span></span>
1. <span data-ttu-id="e2f99-128">Klikk Importer brukere.</span><span class="sxs-lookup"><span data-stu-id="e2f99-128">Click Import users.</span></span>
2. <span data-ttu-id="e2f99-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e2f99-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e2f99-130">Klikk Importer brukere.</span><span class="sxs-lookup"><span data-stu-id="e2f99-130">Click Import users.</span></span>
4. <span data-ttu-id="e2f99-131">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="e2f99-131">Click Close.</span></span>


