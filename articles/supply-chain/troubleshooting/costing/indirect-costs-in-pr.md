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
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026780"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Rapporten om Indirekte kostnader i prosess omfatter slettede produksjonsordrer

KB-nummer: 4612748

## <a name="symptoms"></a>Symptomer

Rapporten **Indirekte kostnader i prosess** presenterer informasjon om produksjonsordrer som ble delvis behandlet og senere slettet.

## <a name="resolution"></a>Oppløsning

Når du tilbakefører en produksjonsordre, tilbakeføres også alle transaksjonene for denne produksjonsordren. Når du sletter produksjonsordren, fastholder underfinanstabellene og økonomimodulen alle transaksjoner som er tilknyttet den. Rapportene vil vise transaksjonene i underfinanstabellene. For den angitte produksjonsordren bør nettoverdien være 0,00.
