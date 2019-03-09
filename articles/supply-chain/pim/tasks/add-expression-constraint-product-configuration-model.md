---
title: Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "360584"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell. Den viser hvordan du kan kreve at hjørnebeskyttelse må brukes på en høyttaler hvis brukeren har valgt en frontgrill i metall. Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.


## <a name="create-an-expression-constraint"></a>Opprette en uttrykksbegrensning
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. Finn og velg ønsket post i listen.
    * Dette eksemplet bruker modellen for High-end-høyttaler.  
4. Klikk koblingen i den valgte raden i listen.
5. Utvid delen Begrensninger.
6. Klikk Legg til.
7. Klikk Opprett.
8. Skriv inn en verdi i Navn-feltet.

## <a name="enter-expression"></a>Angi uttrykk
1. Klikk Rediger uttrykk.
    * Hvis du låser opp brukergrensesnittet i oppgaveregistreringen i denne fasen, kan du bruke IntelliSense og listen over symboler til å bygge restriksjonsuttrykket.  
2. I ConstraintBody-feltet skriver du inn "Implies[FrontGrill=="Metal", CornerProtection]".
    * Denne uttrykkslogikken sier: Hvis frontgrillen er metall, må alternativet for hjørnebeskyttelse velges.  
3. Klikk Valider.
    * Valideringsfunksjonen kjøres gjennom begrensningsuttrykket og sjekker for syntaksfeil.  
4. Klikk Lukk.
5. Klikk OK.

