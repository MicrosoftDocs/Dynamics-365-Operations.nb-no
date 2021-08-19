---
title: Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden
description: Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730136"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden

KB-nummer: 4613548

## <a name="symptoms"></a>Symptomer

Det er ingen **Fra dato**-verdi i kategorien **Aktive priser** på **Varepris**-siden.

## <a name="resolution"></a>Oppløsning

**Fra dato**-verdien (gyldig-dato) som er definert på den ventende prisen, blir ikke overført til den aktive prisen.

Når en varekostnadspost angis først, har den statusen *Ventende* og en beregnet effektiv dato. Når du aktiverer varekostnadsposten, oppdateres statusen *Aktiv*, og den effektive datoen oppdateres til aktiveringsdatoen. Derfor er den aktive prisens aktiveringsdato alltid den faktiske datoen for aktiveringen.

Hvis du vil ha mer informasjon, kan du se [Oversikt over etterkalkuleringsversjoner](../../cost-management/costing-versions.md).
