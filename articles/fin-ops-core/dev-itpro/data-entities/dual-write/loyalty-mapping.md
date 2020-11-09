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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998020"
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
