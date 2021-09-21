---
title: Det tas ikke hensyn til lagerbeholdning for varer over partigrensen
description: Noen sporingsmaler tar ikke hensyn til gjeldende lagerbeholdning for varer over partigrensen. Parti- eller serienummeret må angis på behovsordren.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477200"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Sporingsmaler tar ikke hensyn til lagerbeholdning for varer over partigrensen

## <a name="symptoms"></a>Symptomer

Sporingsmaler som har kriteriet *Vurder sporbeholdning*, tar ikke hensyn til gjeldende lagerbeholdning for *parti-over*-varer. De vurderer det bare hvis partinummeret er angitt på salgsordrelinjen.

Når du bruker *parti-under*-varer, vurderes imidlertid den gjeldende lagerbeholdningen som forventet.

Hvis du vil ha mer informasjon, kan du se [Lagersporing](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Løsning

Sporingsmalhodet kan defineres for behovsstrategien *Bestilt*, *Reservert* eller *Frigitt*. Når det gjelder strategien for *bestilt* etterspørsel, gjelder de samme reservasjonshierarkikravene som gjelder for reservering eller frigivelse for lagerprosesser. For varer som har *parti-over*- og *serie-under*-reservasjonshierarkier, må derfor parti- eller serienummeret angis på behovsordren (salg eller overføring).

Du kan også bruke strategien for *reservert* etterspørsel til å velge parti- eller serienummeret før lagerets sporbehov genereres.
