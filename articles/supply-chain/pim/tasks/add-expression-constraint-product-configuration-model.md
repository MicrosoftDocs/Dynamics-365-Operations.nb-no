---
title: Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920887"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell. Den viser hvordan du kan kreve at hjørnebeskyttelse må brukes på en høyttaler hvis brukeren har valgt en frontgrill i metall. Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.

## <a name="create-an-expression-constraint"></a>Opprette en uttrykksbegrensning

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
3. Finn og velg ønsket post i listen.
    * Dette eksemplet bruker modellen for High-end-høyttaler.  
4. Velg koblingen i den valgte raden i listen.
5. Utvid delen **Begrensninger**.
6. Velg **Legg til**.
7. Velg **Opprett**.
8. Skriv inn en verdi i **Navn**-feltet.

## <a name="enter-expression"></a>Angi uttrykk

1. Velg **Rediger uttrykk**.
    * Hvis du låser opp brukergrensesnittet i oppgaveregistreringen i denne fasen, kan du bruke IntelliSense og listen over symboler til å bygge restriksjonsuttrykket.  
2. I **ConstraintBody**-feltet skriver du inn "Implies[FrontGrill=="Metal", CornerProtection]".
    * Denne uttrykkslogikken sier: Hvis frontgrillen er metall, må alternativet for hjørnebeskyttelse velges.  
3. Velg **Valider**.
    * Valideringsfunksjonen kjøres gjennom begrensningsuttrykket og sjekker for syntaksfeil.  
4. Velg **Lukk**.
5. Velg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]