---
title: Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569655"
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