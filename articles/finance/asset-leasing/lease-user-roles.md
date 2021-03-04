---
title: Tilordne leiebrukerroller
description: Dette emnet beskriver sikkerhetsrollene som brukes i aktivaleie. Det forklarer også hvordan du tilordner brukere til disse rollene.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446604"
---
# <a name="assign-lease-user-roles"></a>Tilordne leiebrukerroller

[!include [banner](../includes/banner.md)]

Dette emnet beskriver sikkerhetsrollene som brukes i aktivaleie. Det forklarer også hvordan du tilordner brukere til disse rollene.

Tre brukerroller skiller adgang til aktivaleie. Én rolle er velegnet til vedlikehold av leieavtaler, én er velegnet for visning av leieavtaler, og én er velegnet for å utføre leieassistentoppgaver. Hver rolle har bestemte tillatelser for alle leiesider, og hver av dem gir brukere muligheten til å vise, opprette, redigere eller slette leieavtaler, i henhold til deres jobbplikter.

| Rolle           | beskrivelse |
|----------------|-------------|
| Vedlikeholde leieavtale | Brukere i denne rollen kan legge til, redigere, slette og vise leieavtaler. Denne rollen er utformet for daglige brukere som har oppgaver som omfatter oppretting og postering av månedlige journaloppføringer, og tillegging av nye leieavtaler. Denne rollen gir tilgang til alle aktivaleiefunksjoner. |
| Vise leie     | Brukere i denne rollen kan bare vise leieposter, tidsplaner og kjøre rapporter. De kan ikke opprette nye leieavtaler, redigere eksisterende leieavtaler eller opprette journaloppføringer mot leieavtaler. Rollen er utformet for brukere som bare trenger å vise leieavtaler, leietidsplaner og transaksjonene som skjer mot disse leieavtalene. |
| Leieassistent    | Brukere i denne rollen kan bare opprette nye leieavtaler. De kan ikke redigere eller slette eksisterende leieavtaler, vise leieplaner eller postere leiejournaloppføringer. Denne rollen er utformet for brukere som arbeider i en dataregistreringskapasitet. |

Følg disse trinnene for å tilordne brukere til rollene som brukes i aktivaleie.

1. Gå til **Systemadministrasjon \> Sikkerhet \> Tilordne brukere til roller**.
2. Velg rollen **Vedlikehold leieavtale**, **Leieassistent** eller **Vis leie**, og velg deretter **Tilordne/utelate brukere manuelt**.
3. Velg brukeren du vil tilordne til rollen, og velg deretter **Tilordne til rolle**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]