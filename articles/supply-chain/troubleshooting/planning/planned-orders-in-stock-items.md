---
title: Planlagte bestillinger genereres for på lager med produksjonsordrer
description: Planlagte ordrer genereres selv om du har varer på lager og produksjonsordrer allerede finnes for dem
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477249"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Planlagte bestillinger genereres for på lager med produksjonsordrer

## <a name="symptoms"></a>Symptomer

Planlagte ordrer genereres selv om du har varer på lager og produksjonsordrer allerede finnes for dem.

## <a name="resolution"></a>Løsning

Det kan hende at du kan løse dette problemet ved å øke verdien **Positive dager** for de relevante gruppene på siden **Dekningsgruppe**. Denne endringen vil føre til at systemet fastslår om lagerbeholdningen kan brukes for behovet. Da vil det ikke bli generert en ny planlagt ordre for varene som er på lager.
