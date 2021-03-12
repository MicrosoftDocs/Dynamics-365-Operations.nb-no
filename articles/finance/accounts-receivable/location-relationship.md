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
# <a name="add-location-and-party-relationship-types"></a>Legg til plassering og partsrelasjonstyper 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Legg til lokasjonsroller

Det er to måter å legge til nye lokasjonsroller for adresse og kontaktinformasjon:

-  Legg til via **Adresse- og kontaktinformasjonsformål**-siden. Den nye rollen vil bli lagret i **LogisticsLocationRole**-tabellen med type = 0, som angir at rollen ikke er en systemrolle definert i den **LogisticsLocationRoleType**-opplistingen og dens utvidelser. En bruker skal kunne bruke denne rollen ved oppretting av adresse- og kontaktinformasjon.

    ![Adresse- og innholdsinformasjonsformål](media/Address-Contact.PNG)

-  Legg den til i **LogisticsLocationRoleType**-opplistingsutvidelsen, og la den fylles ut gjennom databasesynkroniseringsprosessen.

    1.  Opprett en utvidelse til **LogisticsLocationRoleType**-opplistingen, og legg til den nye rollen i utvidelsen. 
  
        ![Utvidelse til LogisticsLocationRoleType-opplistingen](media/Logistics.PNG)

    2. Opprett en ny ressursfil for den nye rollen, og tilordne deretter en verdi for de tilhørende egenskapene.
     
     ![Ny ressursfil](media/Resource.PNG)
        
    3.  Opprett en datapopulasjonsklasse, og angi en håndteringsmetode for å fylle ut den nye rollen. 

        ![Datautfylling](media/Dirdata.PNG)

    4.  Hvis du vil teste utfylling av den nye lokasjonsrollen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertLogisticsLocationRoles() i Main(). Når denne prosessen er fullført, kan du se den nye rollen utfylt i **LogisticsLocationRole**-tabellen med typen \> 0. Den nye rollen vises på siden **Adresse- og kontaktinformasjonsformål**.

        ![Sett inn ny plassering](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Legg til partsrelasjonstyper 

Det finnes to metoder å legge til en ny relasjonstype:

-   Legg den til via **Relasjonstyper**-siden. Den nye relasjonen vil bli lagret i **DirRelationshipTypeTable** med systemtype = 0.

    ![Relasjonstyper](media/Relationship.PNG)

-  Legg den til i utvidelsen for **DirSystemRelationshipType**-opplistingen, og la den fylles ut gjennom databasesynkroniseringsprosessen.

    1.  Opprett en utvidelse til **DirSystemRelationshipType**-opplistingen, og legg til den nye relasjonstypen.

    2. Opprett en initialisering for denne nye typen. Du finner flere eksempler i kjernekoden, der én av dem er **DirRelationshipTypeChildInitialize**. Dette er en initialiseringsklasse for partsrelasjonstypen "Underordnet". Du kan begynne med initialiseringen ved å kopiere og lime inn denne koden og oppdatere de merkede områdene.
    
    ![DirRelationshipChild-initialisering](media/DirRelationship.PNG)

    3.  Hvis du vil teste utfylling av den nye relasjonstypen, kan du opprette en kjørbar klasse og kalle DirDataPopulation::insertDirRelationshipTypes() i Main(). Du skal kunne se den nye relasjonstypen i **DirRelationshipTypeTable**, og den nye relasjonstypen skal vises på **Relasjonstyper**-siden.

        ![Runnable-klasse](media/Runnable.PNG)
