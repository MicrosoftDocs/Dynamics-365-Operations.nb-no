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
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026794"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden

KB-nummer: 4613548

## <a name="symptoms"></a>Symptomer

Det er ingen **Fra dato**-verdi i kategorien **Aktive priser** på **Varepris**-siden.

## <a name="resolution"></a>Oppløsning

**Fra dato**-verdien (gyldig-dato) som er definert på den ventende prisen, blir ikke overført til den aktive prisen.

Når en varekostnadspost angis først, har den statusen *Ventende* og en beregnet effektiv dato. Når du aktiverer varekostnadsposten, oppdateres statusen *Aktiv*, og den effektive datoen oppdateres til aktiveringsdatoen. Derfor er den aktive prisens aktiveringsdato alltid den faktiske datoen for aktiveringen.

Hvis du vil ha mer informasjon, kan du se [Oversikt over etterkalkuleringsversjoner](../../cost-management/costing-versions.md).
