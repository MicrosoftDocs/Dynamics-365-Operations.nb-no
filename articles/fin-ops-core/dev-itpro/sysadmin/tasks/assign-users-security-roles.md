---
title: Tilordne brukere til sikkerhetsroller
description: Brukere må tilordnes sikkerhetsroller for å få tilgang til Finance and Operations-apper.
author: Peakerbl
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745891"
---
# <a name="assign-users-to-security-roles"></a>Tilordne brukere til sikkerhetsroller

[!include [banner](../../includes/banner.md)]

For å bruke noe annet enn vanlige funksjoner i Finance and Operations må brukerne tilordnes sikkerhetsroller. Du kan tilordne brukere til roller automatisk basert på regler og forretningsdata, utelate brukere fra automatisk rolletilordning eller legge til brukere i roller manuelt.

## <a name="automatically-assign-users-to-roles"></a>Tilordne brukere automatisk til roller
Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata. 
1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
2. Velg Regnskapsansvarlig i treet. Velg rollen som du vil konfigurere regelen for. Velg regnskapsansvarlig i dette eksemplet. 
3. Velg **Legg til regel** for å åpne dialogmenyen.
4. Finn og velg ønsket post i listen **Velg en spørring**. Velg spørringen som skal brukes for denne regelen.  
5. Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.
6. Velg **Rediger spørring**. Rediger spørringen etter behov.  
7. Velg **OK**.
8. Velg **Kjør automatisk rolletilordning**.
9. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere** (ideelt i en egen webleserkategori).
10. Gå gjennom rollene som er tilordnet ulike brukere for å bekrefte at rolletildelingsspørringen var riktig. Juster og kjør på nytt om nødvendig.

## <a name="exclude-users-from-automatic-role-assignment"></a>Utelate brukere fra automatisk rolletilordning
1. Lukk siden.
2. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
3. Velg Regnskapsansvarlig i treet. Velg en rolle. Velg regnskapsansvarlig i dette eksemplet.  
4. Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.
5. Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**. Velg en bruker.  
6. Velg **Utelat fra rolle** i **Handlingsrute**.
7. Velg **Utelat fra rolle** for å utelate de valgte brukerne fra rollen. Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**. Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk. Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen. I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.  

## <a name="manually-assign-users-to-roles"></a>Tilordne brukere til roller manuelt
Brukere som manuelt tilordnes til sikkerhets roller, må også fjernes manuelt av administratoren. Disse brukerne fjernes ikke fra roller etter regler for automatisk rolletilordning.

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
2. I treet velger du en rolle, og i menyen **Tilordne/utelate brukere manuelt** velger du **Tilordne/utelate brukere manuelt**.
4. I listen **Tilordne brukere til, eller utelat brukere fra rolle** vises brukere som ikke er tilordnet rollen, i modusen **Tilordningsmodus** er angitt til **Ingen**. Velg én eller flere brukere som skal tilordnes rollen.
5. I **Handlingsrute** velger du **Tilordne til rolle**. **Tilordningsmodus** er oppdatert til **Manuell**, og brukerne har nå en ny rolle tilordnet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]