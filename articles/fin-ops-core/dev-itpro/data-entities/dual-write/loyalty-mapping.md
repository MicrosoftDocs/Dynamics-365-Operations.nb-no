---
title: Kundefordelskort og belønningspoeng
description: Denne artikkelen beskriver integreringen av data om kundefordelskort og belønningspoeng i dobbeltskriving.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 399682b3042c32fbf6fa200213f1b4982ed97174
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289122"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kundefordelskort og belønningspoeng

[!include [banner](../../includes/banner.md)]



Firmaer klassifiserer kunder og tilbyr avanserte tjenester basert på kunders handle- og forbruksmønstre. Eksempelvis har Dynamics 365 Commerce infrastrukturen og funksjonene for å lette og håndtere kundelojalitetskort, belønningspoeng, lojalitetsbasert prissetting og belønningsbaserte handleopplevelser. Når data om kundefordelskort og belønningspoeng i Commerce er synkronisert med Dataverse, kan kundeengasjementapper bruke disse dataene. Dynamics 365 Customer Service-brukere kan for eksempel bruke dataene til å gi de samme avanserte tjenestene gjennom brukerstøtten.

## <a name="templates"></a>Maler

Finance and Operations-apper | Kundeengasjementsapper     | beskrivelse
|-----------------------------|-----------------------------------|-------------|
[Fordelskort](mapping-reference.md#149) | msdyn_loyaltycards | Denne malen synkroniserer informasjon om kundefordelskort. |
[Fordelsnivåer](mapping-reference.md#226) | msdyn_loyaltylevels | Denne malen synkroniserer informasjon om fordelspoeng. |
[Fordelspoeng](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
