---
title: Tilordne brukere til sikkerhetsroller
description: For å få tilgang til økonomi- og driftsapper må brukere tilordnes sikkerhetsroller.
author: Peakerbl
ms.date: 02/09/2022
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
ms.openlocfilehash: 36874b996cc5708f6fd7fbc45251f3066b5b1c97
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105544"
---
# <a name="manage-users-and-security-roles"></a>Administrere brukere og sikkerhetsroller

[!include [banner](../../includes/banner.md)]

For å bruke noe annet enn vanlige funksjoner i økonomi- og driftsapper må brukerne tilordnes sikkerhetsroller. Du kan tilordne brukere til roller automatisk basert på regler og forretningsdata, utelate brukere fra automatisk rolletilordning eller legge til brukere i roller manuelt.

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
Denne fremgangsmåten forklarer hvordan du utelater brukere fra automatisk rolletilordning.

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

## <a name="manually-remove-users-from-roles"></a>Fjerne brukere fra roller manuelt
Brukere som manuelt tilordnes til sikkerhets roller, må også fjernes manuelt av administratoren. Disse brukerne fjernes ikke fra roller etter regler for automatisk rolletilordning.

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.
2. Slik fjerner du én bruker:
   1. Velg en rolle i treet. 
   2. Velg brukeren som skal fjernes, i området **Brukere som er tilordnet til rolle**.
   3. Velg **Fjern**, og derved fjernes brukeren fra rollen.
3. Slik fjerner du flere brukere:
   1. Velg en rolle i treet. 
   2. Velg **Tilordne/utelat brukere manuelt** i området **Brukere som er tilordnet til rolle**.
   3. I listen **Tilordne brukere til, eller utelat brukere fra rolle** har brukere som ikke er tilordnet til rollen, **Ingen** i kolonnen **Tilordningsmodus**. Velg brukerne som skal utelates fra rollen.
   4. Velg **Utelat fra rolle** i **Handlingsrute**. Kolonnen **Tilordningsmodus** er nå oppdatert til **Manuell**, og brukerne er nå utelatt fra rollen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
