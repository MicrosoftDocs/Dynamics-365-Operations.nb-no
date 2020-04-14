---
title: Kundefordelskort og belønningspoeng
description: Dette emnet beskriver integreringen av data om kundefordelskort og belønningspoeng mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172975"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kundefordelskort og belønningspoeng

[!include [banner](../../includes/banner.md)]



Firmaer klassifiserer kunder og tilbyr avanserte tjenester basert på kunders handle- og forbruksmønstre. I Microsoft Dynamics 365-serien med programmer har Dynamics 365 Commerce infrastrukturen og funksjonene for å lette og håndtere kundelojalitetskort, belønningspoeng, lojalitetsbasert prissetting og belønningsbaserte handleopplevelser. Når data om kundefordelskort og belønningspoeng i Commerce er synkronisert med Common Data Service, kan modelldrevne apper i Dynamics 365 bruke disse dataene. Dynamics 365 Customer Service-brukere kan for eksempel bruke dataene til å gi de samme avanserte tjenestene gjennom brukerstøtten.

## <a name="templates"></a>Maler

| Finance and Operations-apper | Modelldrevne apper i Dynamics 365 | beskrivelse |
|-----------------------------|-----------------------------------|-------------|
| Fordelskort                | msdyn\_loyaltycards               | Denne malen synkroniserer informasjon om kundefordelskort. |
| Fordelspoeng       | msdyn\_loyaltyrewardpoints        | Denne malen synkroniserer informasjon om fordelspoeng. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
