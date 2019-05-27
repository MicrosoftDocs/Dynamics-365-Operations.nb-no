---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509297"
---
# <a name="workflow-system"></a>Arbeidsflytsystem

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Varslinger

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor mottas flere varslinger når et arbeidselement avvises?
Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist. Et annet arbeidselement opprettes og tilordnes til avsenderen. Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet. 

Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring. Vi ser på måter å forbedre dette på i fremtidige versjoner.

### <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes arbeidsflyteksportene mine?
Det er for øyeblikket en begrensning i funksjonen for arbeidsflyteksport som hindrer at arbeidsflytnavn overskrider 48 tegn. Hvis du bruker et navn som er lengre enn 48 tegn, kan det resultere i feilen «Serveren kan ikke godkjenne forespørselen» og/eller hindre at en fil blir eksportert uten en filtype. Følgende blogginnlegg gir mer informasjon [Feilsøke arbeidsflyteksport](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
