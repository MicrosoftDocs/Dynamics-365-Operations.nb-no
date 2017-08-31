--- 
title: "Legge til en foregående aktivitet i en produksjonsflytaktivitet"
description: "Alle aktiviteter må være sekvensert i en produksjonsflytversjon."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c1afd6a5c2eb5235a42fc9aeea0c8aed6d33e0c9
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Legge til en foregående aktivitet i en produksjonsflytaktivitet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Alle aktiviteter må være sekvensert i en produksjonsflytversjon. En aktivitet kan ha én eller flere foregående eller etterfølgende aktiviteter. 

Denne fremgangsmåten viser hvordan du knytter en foregående aktivitet til en aktivitet. 

For å utføre denne oppgaven, trenger du en produksjonsflyt som har en utkastversjon med minst to aktiviteter som kan være koblet. 

Hvis du vil ha mer informasjon, kan du se hvitboken Produksjonsflyter og -aktiviteter i lean manufacturing.


## <a name="find-the-production-flow-and-version"></a>Finne produksjonsflyten og versjonen
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Finn og velg ønsket post i listen.
5. Klikk Aktiviteter.

## <a name="select-an-activity-and-add-a-predecessor"></a>Velge en aktivitet og legge til en foregående aktivitet
1. Finn og velg ønsket post i listen.
2. Klikk Legg til foregående aktivitet.
3. Angi eller velg en verdi i feltet Aktivitet.
4. Angi et tall i feltet Forhold for syklustid.
    * Standard syklustidsforhold for en aktivitetsrelasjon er 1. Dette forutsetter at begge aktivitetene kjører med samme hastighet eller takttid. Hvis den foregående aktiviteten kjører med et høyere tempo (lavere takttid), må forholdet være lavere enn 1, og hvis den foregående aktiviteten går langsommere (høyere takttid), er syklustidsforholdet større enn 1.  
5. Klikk OK.


