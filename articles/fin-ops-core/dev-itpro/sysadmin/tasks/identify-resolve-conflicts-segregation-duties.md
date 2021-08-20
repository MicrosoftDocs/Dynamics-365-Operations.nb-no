---
title: Identifisere og løse konflikter i arbeidsdeling
description: Dette emnet forklarer hvordan du identifiserer og løser konflikter i arbeidsdelinger.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0638699c0e569bbe67024a87d6c55729642557cb085ee899aa98aa0022b12840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748318"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifisere og løse konflikter i arbeidsdeling

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du identifiserer og løser konflikter i arbeidsdelinger. Du kan definere regler for å skille plikter som må utføres av forskjellige brukere. Dette konseptet kalles arbeidsdeling. Når definisjonen av en sikkerhetsrolle eller rolletildelingene til en bruker bryter reglene, logges konflikten. Alle konflikter må løses av administratoren. Fullfør fremgangsmåten nedenfor for å identifisere og løse konflikter.

Etter at en regel er lagt til, kontrollerer du at alle eksisterende roller samsvarer med reglene. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollere at eksisterende roller og plikter følger nye regler for arbeidsdeling
1. Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Arbeidsdelingsregler**.
3. Velg **Valider plikter og roller**. Hvis en rolle bryter reglene, vises en melding som inneholder navnet på regelen og rollen og navnene på pliktene som er i konflikt med hverandre. Roller i konflikt må endres ved hjelp av **Sikkerhetskonfigurasjon** og kan ikke inneholde plikter i konflikt. Hvis ingen roller bryter en valgt regel, får du en melding som angir at alle roller er i samsvar.   

> [!NOTE]
> Valideringen utføres bare for den valgte regelen. Det er viktig å validere samsvar for hver regel.   

Når du oppretter eller endrer en rolle, blir reglene for arbeidsdeling håndhevet automatisk. Du kan ikke tilordne plikter i konflikt til en rolle.

Kontroller deretter alle eksisterende rolletilordninger er i samsvar.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Bekrefte at brukerrolletilordninger samsvarer med nye regler for arbeidsdeling
1. Gå til **Systemadministrasjon > Sikkerhet > Arbeidsdeling > Bekreft overholdelse av brukerrolletilordninger**.
2. Velg **OK**. En varsling viser resultatet av valideringen. Konflikter logges på siden **Uløste konflikter for arbeidsdeling**.   

Når du tilordner brukere til roller, blir reglene for arbeidsdeling håndhevet automatisk. Hvis du prøver å tilordne en bruker til roller som inneholder plikter i konflikt, får du en feilmelding. Du må deretter løse konflikten ved å avslå eller tillate den ekstra rolletilordningen. Den ekstra rollen tilordnes etter at tilordningen har blitt tillatt. 

> [!NOTE]
> Konflikter kontrolleres for øyeblikket ikke for brukere som får tilordnet roller basert på Active Directory Domain-gruppene.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Vise og løse tilordninger av brukerroller i konflikt
1. Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Uløste konflikter for arbeidsdeling**. 
2. Velg en konflikt, og velg deretter én av følgende handlinger: 

  - **Avslå tilordning**: Dette avslår tilordningen av brukeren til den ekstra sikkerhetsrollen. Hvis du nekter en automatisk rolletilordning, merkes brukeren som utelatt fra rollen. Den utelatte brukeren får ikke tilgangen som er knyttet til rollen, og kan ikke tilordnes til rollen før administratoren fjerner utelatelsen. 
-  **Tillat tilordning**: Dette overstyrer konflikten og lar brukeren bli tilordnet til den ekstra sikkerhetsrollen. Hvis du overstyrer en konflikt, må du angi en årsak i feltet **Årsak til overstyring**. Alle overstyrte rolletilordninger kan vises på siden **Arbeidsdelingskonflikter**.  

> [!NOTE]
> Hvis det vises flere konflikter for samme bruker, velger du brukerposten og evaluerer tilordnede roller på **Brukere**-siden. For å unngå denne konflikten validerer du hver regel etter at den er lagt til eller endret.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]