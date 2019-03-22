---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/01/2019
ms.locfileid: "773225"
---
# <a name="workflow-system"></a>Arbeidsflytsystem

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Varslinger

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor mottas flere varslinger når et arbeidselement avvises?
Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist. Et annet arbeidselement opprettes og tilordnes til avsenderen. Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet. 

Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring. Vi ser på måter å forbedre dette på i fremtidige versjoner.
