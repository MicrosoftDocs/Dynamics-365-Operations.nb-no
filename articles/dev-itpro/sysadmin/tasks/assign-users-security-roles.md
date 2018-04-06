--- 
title: Tilordne brukere til sikkerhetsroller
description: "For å få tilgang til Microsoft Dynamics 365 for Finance and Operations, må brukere tilordnes sikkerhetsroller."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a>Tilordne brukere til sikkerhetsroller

[!include[task guide banner](../../includes/task-guide-banner.md)]

For å få tilgang til Microsoft Dynamics 365 for Finance and Operations, må brukere tilordnes sikkerhetsroller. Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="automatically-assign-users-to-roles"></a>Tilordne brukere automatisk til roller
1. Gå til Systemadministrasjon > Sikkerhet > Tilordne brukere til roller.
2. Velg Regnskapsansvarlig i treet.
    * Velg rollen som du vil konfigurere regelen for. Velg regnskapsansvarlig i dette eksemplet.  
3. Klikk Legg til regel for å åpne nedtrekksdialogen.
4. Finn og velg ønsket post i listen.
    * Velg spørringen som skal brukes for denne regelen.  
5. Klikk koblingen i den valgte raden i listen.
6. Klikk Rediger spørring.
    * Rediger spørringen etter behov.  
7. Klikk OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Utelate brukere fra automatisk rolletilordning
1. Lukk siden.
2. Gå til Systemadministrasjon > Sikkerhet > Tilordne brukere til roller.
3. Velg Regnskapsansvarlig i treet.
    * Velg en rolle. Velg regnskapsansvarlig i dette eksemplet.  
4. Klikk Tilordne/utelate brukere manuelt.
5. Merk den valgte raden i listen.
    * Velg en bruker.  
6. Klikk Utelat fra rolle.
    * Klikk Utelat fra rolle for å utelate de valgte brukerne fra rollen. Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for og klikker deretter Tilbakestill status. Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt. Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen. I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.  


