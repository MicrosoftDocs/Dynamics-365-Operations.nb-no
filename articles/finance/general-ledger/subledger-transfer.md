---
title: Overføring av underfinans til økonomimodul
description: Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som er knyttet til overføring av underfinans i økonomimodulen.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897510"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Overføring av underfinans til økonomimodul

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som er knyttet til reglene for overføring av bunker med underfinansjournaloppføringer.

I versjon 8.1 ble det gjort endringer for å tillate overføring av regler, som avskrev **Synkron**-alternativet. Hvis du vil ha mer informasjon, kan du se [Funksjoner som er fjernet eller avskrevet for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Følgende alternativer er tilgjengelige for overføring av underfinansbunker. 

 - Asynkron – Dette alternativet vil umiddelbart planlegge overføring av regnskapspostene fra underfinans til økonomimodulen. Økonomimodulbilaget vil bli registrert så snart ressurser er ledige for å behandle denne forespørselen på serveren. 

- Planlagt parti – Dette alternativet legger til regnskapsposter fra underfinans som overføres til behandlingskøen i økonomimodulen, der postene blir behandlet i mottatte bestillinger. Økonomimodulbilaget vil bli registrert på det planlagte tidspunktet hvis ressurser er ledige for å behandle denne satsvise jobben på serveren. 
 
I versjon 10.0.8 ble det gjort forbedringer for å forbedre ytelsen til Asynkron-alternativet. Denne funksjonen aktiveres under funksjonsnavnet **Ytelsesoptimalisering for overføring av underfinans til økonomimodul**. 
 
Denne funksjonen forbedrer overføring av data fra underfinans til økonomimodulen. Den gjør prosessen mer effektiv, og den grupperer sammen sett med mindre transaksjoner som skal overføres. Dette gjør det mulig å bruke partiserveren mer effektivt. Denne funksjonen krever at partiserveren er konfigurert, tilkoblet og fungerer for at alternativet for asynkron overføring skal fungere. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]