---
title: Legg til plassering og partsrelasjonstyper
description: Dette emnet forklarer hvordan du legger til en ny plassering og partsrelasjonstype.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf971bc6cf4b11de6381e369235d582678d074fc
ms.openlocfilehash: 8de914e0fb853cdc9aa36e55a02156757793abc3
ms.contentlocale: nb-no
ms.lasthandoff: 06/12/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a><span data-ttu-id="fffe8-103">Legg til nye plasseringsroller og partsrelasjonstyper</span><span class="sxs-lookup"><span data-stu-id="fffe8-103">Add new location roles and party relationship types</span></span> 

## <a name="add-new-location-roles"></a><span data-ttu-id="fffe8-104">Legge til nye lokasjonsroller</span><span class="sxs-lookup"><span data-stu-id="fffe8-104">Add new location roles</span></span>

<span data-ttu-id="fffe8-105">Det er to måter å legge til nye lokasjonsroller for adresse og kontaktinformasjon:</span><span class="sxs-lookup"><span data-stu-id="fffe8-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="fffe8-106">Legg til via **Adresse- og kontaktinformasjonsformål**-siden.</span><span class="sxs-lookup"><span data-stu-id="fffe8-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="fffe8-107">Den nye rollen vil bli lagret i **LogisticsLocationRole**-tabellen med type = 0, som angir at rollen ikke er en systemrolle definert i den **LogisticsLocationRoleType**-opplistingen og dens utvidelser.</span><span class="sxs-lookup"><span data-stu-id="fffe8-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="fffe8-108">En bruker skal kunne bruke denne rollen ved oppretting av adresse- og kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="fffe8-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Adresse- og innholdsinformasjonsformål](media/Address-Contact.PNG)

-  <span data-ttu-id="fffe8-110">Legg den til i **LogisticsLocationRoleType**-opplistingsutvidelsen, og la den fylles ut gjennom databasesynkroniseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="fffe8-111">Opprett en utvidelse til **LogisticsLocationRoleType**-opplistingen, og legg til den nye rollen i utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="fffe8-113">Opprett en ny ressursfil for den nye rollen, og tilordne deretter en verdi for de tilhørende egenskapene.</span><span class="sxs-lookup"><span data-stu-id="fffe8-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Ny ressursfil](media/Resource.PNG)
        
    3.  <span data-ttu-id="fffe8-115">Opprett en datapopulasjonsklasse, og angi en håndteringsmetode for å fylle ut den nye rollen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Datautfylling](media/Dirdata.PNG)

    4.  <span data-ttu-id="fffe8-117">Hvis du vil teste utfylling av den nye lokasjonsrollen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertLogisticsLocationRoles() i Main().</span><span class="sxs-lookup"><span data-stu-id="fffe8-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="fffe8-118">Når denne prosessen er fullført, kan du se den nye rollen utfylt i **LogisticsLocationRole**-tabellen med typen \> 0.</span><span class="sxs-lookup"><span data-stu-id="fffe8-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="fffe8-119">Den nye rollen vises på siden **Adresse- og kontaktinformasjonsformål**.</span><span class="sxs-lookup"><span data-stu-id="fffe8-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Sett inn ny plassering](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a><span data-ttu-id="fffe8-121">Legg til nye partsrelasjonstyper</span><span class="sxs-lookup"><span data-stu-id="fffe8-121">Add new party relationship types</span></span> 

<span data-ttu-id="fffe8-122">Det finnes to metoder å legge til en ny relasjonstype:</span><span class="sxs-lookup"><span data-stu-id="fffe8-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="fffe8-123">Legg den til via **Relasjonstyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="fffe8-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="fffe8-124">Den nye relasjonen vil bli lagret i **DirRelationshipTypeTable** med systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="fffe8-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Relasjonstyper](media/Relationship.PNG)

-  <span data-ttu-id="fffe8-126">Legg den til i utvidelsen for **DirSystemRelationshipType**-opplistingen, og la den fylles ut gjennom databasesynkroniseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="fffe8-127">Opprett en utvidelse til **DirSystemRelationshipType**-opplistingen, og legg til den nye relasjonstypen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="fffe8-128">Opprett en initialisering for denne nye typen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-128">Create an initializer for this new type.</span></span> <span data-ttu-id="fffe8-129">Du finner flere eksempler i kjernekoden, der én av dem er **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="fffe8-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="fffe8-130">Dette er en initialiseringsklasse for partsrelasjonstypen "Underordnet".</span><span class="sxs-lookup"><span data-stu-id="fffe8-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="fffe8-131">Du kan begynne med initialiseringen ved å kopiere og lime inn denne koden og oppdatere de merkede områdene.</span><span class="sxs-lookup"><span data-stu-id="fffe8-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="fffe8-133">Hvis du vil teste utfylling av den nye relasjonstypen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertDirRelationshipTypes() i Main().</span><span class="sxs-lookup"><span data-stu-id="fffe8-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="fffe8-134">Du skal kunne se den nye relasjonstypen i **DirRelationshipTypeTable**, og den nye relasjonstypen skal vises på **Relasjonstyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="fffe8-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Runnable-klasse](media/Runnable.PNG)

