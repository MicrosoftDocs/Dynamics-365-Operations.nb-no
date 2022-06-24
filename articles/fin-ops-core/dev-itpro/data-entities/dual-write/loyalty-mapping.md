---
title: Kundefordelskort og belønningspoeng
description: Denne artikkelen beskriver integreringen av data om kundefordelskort og belønningspoeng i dobbeltskriving.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 383a1b8e9a7497a47a6ce8561253124853095b0a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890132"
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
