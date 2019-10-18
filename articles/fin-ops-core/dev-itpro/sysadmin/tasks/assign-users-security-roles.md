---
title: Tilordne brukere til sikkerhetsroller
description: For å få tilgang til Finance and Operations-apper må brukere tilordnes sikkerhetsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180973"
---
# <a name="assign-users-to-security-roles"></a>Tilordne brukere til sikkerhetsroller

[!include [task guide banner](../../includes/task-guide-banner.md)]

For å bruke noe annet enn vanlige funksjoner må brukerne tilordnes sikkerhetsroller. Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata. 

## <a name="automatically-assign-users-to-roles"></a>Tilordne brukere automatisk til roller
1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
2. Velg Regnskapsansvarlig i treet. Velg rollen som du vil konfigurere regelen for. Velg regnskapsansvarlig i dette eksemplet. 
3. Klikk på **Legg til regel** for å åpne nedtrekksdialogen.
4. Finn og velg ønsket post i listen **Velg en spørring**. Velg spørringen som skal brukes for denne regelen.  
5. Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.
6. Klikk på **Rediger spørring**. Rediger spørringen etter behov.  
7. Klikk **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Utelate brukere fra automatisk rolletilordning
1. Lukk siden.
2. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
3. Velg Regnskapsansvarlig i treet. Velg en rolle. Velg regnskapsansvarlig i dette eksemplet.  
4. Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.
5. Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**. Velg en bruker.  
6. Velg **Utelat fra rolle** i **Handlingsrute**.
    
    Klikk på **Utelat fra rolle** for å utelate de valgte brukerne fra rollen. Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**. Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt. Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen. I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.  
