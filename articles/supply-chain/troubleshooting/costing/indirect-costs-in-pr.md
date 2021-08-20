---
title: Rapporten om Indirekte kostnader i prosess omfatter slettede produksjonsordrer
description: Rapporten Indirekte kostnader i prosess presenterer informasjon om produksjonsordrer som ble delvis behandlet og senere slettet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751775"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Rapporten om Indirekte kostnader i prosess omfatter slettede produksjonsordrer

KB-nummer: 4612748

## <a name="symptoms"></a>Symptomer

Rapporten **Indirekte kostnader i prosess** presenterer informasjon om produksjonsordrer som ble delvis behandlet og senere slettet.

## <a name="resolution"></a>Oppløsning

Når du tilbakefører en produksjonsordre, tilbakeføres også alle transaksjonene for denne produksjonsordren. Når du sletter produksjonsordren, fastholder underfinanstabellene og økonomimodulen alle transaksjoner som er tilknyttet den. Rapportene vil vise transaksjonene i underfinanstabellene. For den angitte produksjonsordren bør nettoverdien være 0,00.
