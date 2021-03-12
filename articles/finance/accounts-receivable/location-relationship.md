---
title: Legg til plassering og partsrelasjonstyper
description: Dette emnet forklarer hvordan du legger til en ny plassering og partsrelasjonstype.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 00810576d36339bf7ce0657b1577e1e322c36bf0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979095"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="5b2ca-103">Legg til plassering og partsrelasjonstyper</span><span class="sxs-lookup"><span data-stu-id="5b2ca-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="5b2ca-104">Legg til lokasjonsroller</span><span class="sxs-lookup"><span data-stu-id="5b2ca-104">Add location roles</span></span>

<span data-ttu-id="5b2ca-105">Det er to måter å legge til nye lokasjonsroller for adresse og kontaktinformasjon:</span><span class="sxs-lookup"><span data-stu-id="5b2ca-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="5b2ca-106">Legg til via **Adresse- og kontaktinformasjonsformål**-siden.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="5b2ca-107">Den nye rollen vil bli lagret i **LogisticsLocationRole**-tabellen med type = 0, som angir at rollen ikke er en systemrolle definert i den **LogisticsLocationRoleType**-opplistingen og dens utvidelser.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="5b2ca-108">En bruker skal kunne bruke denne rollen ved oppretting av adresse- og kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Adresse- og innholdsinformasjonsformål](media/Address-Contact.PNG)

-  <span data-ttu-id="5b2ca-110">Legg den til i **LogisticsLocationRoleType**-opplistingsutvidelsen, og la den fylles ut gjennom databasesynkroniseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="5b2ca-111">Opprett en utvidelse til **LogisticsLocationRoleType**-opplistingen, og legg til den nye rollen i utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Utvidelse til LogisticsLocationRoleType-opplistingen](media/Logistics.PNG)

    2. <span data-ttu-id="5b2ca-113">Opprett en ny ressursfil for den nye rollen, og tilordne deretter en verdi for de tilhørende egenskapene.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Ny ressursfil](media/Resource.PNG)
        
    3.  <span data-ttu-id="5b2ca-115">Opprett en datapopulasjonsklasse, og angi en håndteringsmetode for å fylle ut den nye rollen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Datautfylling](media/Dirdata.PNG)

    4.  <span data-ttu-id="5b2ca-117">Hvis du vil teste utfylling av den nye lokasjonsrollen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertLogisticsLocationRoles() i Main().</span><span class="sxs-lookup"><span data-stu-id="5b2ca-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="5b2ca-118">Når denne prosessen er fullført, kan du se den nye rollen utfylt i **LogisticsLocationRole**-tabellen med typen \> 0.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="5b2ca-119">Den nye rollen vises på siden **Adresse- og kontaktinformasjonsformål**.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Sett inn ny plassering](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="5b2ca-121">Legg til partsrelasjonstyper</span><span class="sxs-lookup"><span data-stu-id="5b2ca-121">Add party relationship types</span></span> 

<span data-ttu-id="5b2ca-122">Det finnes to metoder å legge til en ny relasjonstype:</span><span class="sxs-lookup"><span data-stu-id="5b2ca-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="5b2ca-123">Legg den til via **Relasjonstyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="5b2ca-124">Den nye relasjonen vil bli lagret i **DirRelationshipTypeTable** med systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Relasjonstyper](media/Relationship.PNG)

-  <span data-ttu-id="5b2ca-126">Legg den til i utvidelsen for **DirSystemRelationshipType**-opplistingen, og la den fylles ut gjennom databasesynkroniseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="5b2ca-127">Opprett en utvidelse til **DirSystemRelationshipType**-opplistingen, og legg til den nye relasjonstypen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="5b2ca-128">Opprett en initialisering for denne nye typen.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-128">Create an initializer for this new type.</span></span> <span data-ttu-id="5b2ca-129">Du finner flere eksempler i kjernekoden, der én av dem er **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="5b2ca-130">Dette er en initialiseringsklasse for partsrelasjonstypen "Underordnet".</span><span class="sxs-lookup"><span data-stu-id="5b2ca-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="5b2ca-131">Du kan begynne med initialiseringen ved å kopiere og lime inn denne koden og oppdatere de merkede områdene.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild-initialisering](media/DirRelationship.PNG)

    3.  <span data-ttu-id="5b2ca-133">Hvis du vil teste utfylling av den nye relasjonstypen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertDirRelationshipTypes() i Main().</span><span class="sxs-lookup"><span data-stu-id="5b2ca-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="5b2ca-134">Du skal kunne se den nye relasjonstypen i **DirRelationshipTypeTable**, og den nye relasjonstypen skal vises på **Relasjonstyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Runnable-klasse](media/Runnable.PNG)
