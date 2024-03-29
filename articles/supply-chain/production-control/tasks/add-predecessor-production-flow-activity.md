---
title: Legge til en foregående aktivitet i en produksjonsflytaktivitet
description: Alle aktiviteter må være sekvensert i en produksjonsflytversjon.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc1aa742013faeeb545d746f9715c639a5b66b9b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575081"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Legge til en foregående aktivitet i en produksjonsflytaktivitet

[!include [banner](../../includes/banner.md)]

Alle aktiviteter må være sekvensert i en produksjonsflytversjon. En aktivitet kan ha én eller flere foregående eller etterfølgende aktiviteter. 

Denne fremgangsmåten viser hvordan du knytter en foregående aktivitet til en aktivitet. 

For å utføre denne oppgaven, trenger du en produksjonsflyt som har en utkastversjon med minst to aktiviteter som kan være koblet. 

Hvis du vil ha mer informasjon, kan du se hvitboken Produksjonsflyter og -aktiviteter i lean manufacturing.


## <a name="find-the-production-flow-and-version"></a>Finne produksjonsflyten og versjonen
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Finn og velg ønsket post i listen.
5. Klikk på Aktiviteter.

## <a name="select-an-activity-and-add-a-predecessor"></a>Velge en aktivitet og legge til en foregående aktivitet
1. Finn og velg ønsket post i listen.
2. Klikk på Legg til foregående aktivitet.
3. Angi eller velg en verdi i feltet Aktivitet.
4. Angi et tall i feltet Forhold for syklustid.
    * Standard syklustidsforhold for en aktivitetsrelasjon er 1. Dette forutsetter at begge aktivitetene kjører med samme hastighet eller takttid. Hvis den foregående aktiviteten kjører med et høyere tempo (lavere takttid), må forholdet være lavere enn 1, og hvis den foregående aktiviteten går langsommere (høyere takttid), er syklustidsforholdet større enn 1.  
5. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]