---
title: Overføring av underfinans til økonomimodul
description: Dette emnet beskriver funksjoner som er knyttet til overføring av underfinans i økonomimodulen.
author: rcarlson
ms.date: 12/08/2021
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
ms.openlocfilehash: 213bbc2541c614aa26b0c830431818fb99c7682d
ms.sourcegitcommit: f5885999e008a49fe072d95f15e239905c24918a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2021
ms.locfileid: "7900736"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Overføring av underfinans til økonomimodul

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er knyttet til reglene for overføring av bunker med underfinansjournaloppføringer.

I versjon 8.1 ble det gjort endringer for å tillate overføring av regler, som avskrev **Synkron**-alternativet. Hvis du vil ha mer informasjon, kan du se [Funksjoner som er fjernet eller avskrevet for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Følgende alternativer er tilgjengelige for overføring av underfinansbunker:

- **Asynkron** – Overføring regnskapspostene fra underfinans til økonomimodulen planlegges øyeblikkelig. Økonomimodulbilaget vil bli registrert så snart ressurser er ledige for å behandle forespørselen på serveren.
- **Planlagt bunke** – Regnskapspostene fra underfinans som må overføres, legges til i behandlingskøen i økonomimodulen. Oppføringene i køen behandles i den rekkefølgen de mottas i. Hvert økonomimodulbilag oppdaterer kontoene på det planlagte tidspunktet hvis ressurser er ledige for å behandle den satsvise jobben på serveren.

I versjon 10.0.8 ble det gjort forbedringer for å forbedre ytelsen til **Asynkron**-alternativet. Denne funksjonen aktiveres under funksjonsnavnet **Ytelsesoptimalisering for overføring av underfinans til økonomimodul**.

Funksjonaliteten for asynkron overføring av underfinansbunker bidrar til å forbedre overføringen av data fra underregnskapet til økonomimodulen. Ved å gruppere sett med mindre transaksjoner og overføre transaksjonene i grupper, behandler funksjonaliteten transaksjoner mer effektivt. Når transaksjoner grupperes, brukes ressursene på den satsvise serveren mer effektivt.

Asynkron overføring av underfinansbunker krever at den satsvise serveren konfigureres, er tilkoblet og fungerer, fordi satsvise oppgaver opprettes for umiddelbar utføring på den satsvise serveren. Når funksjonen **Ytelsesoptimalisering for overføring av underfinans til økonomimodul** er aktivert, må også den satsvise systemjobben **Prosessautomasjon** med navnet **Avspørringssystem for prosessautomatisering** være aktivert. Hvis du vil ha mer informasjon, se [Prosessautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Effektivitetsendringen på det satsvise nivået bruker en enkelt gjentakende satsvis jobb for alle juridiske enheter i systemet. Ved kjøretid opprettes det en ny satsvis jobb for å behandle de nødvendige postene som ennå ikke er overført. Du kan styre flere innstillinger fra siden **Prosessautomatisering** i systemadministrasjon. På den siden kan du endre bakgrunnsprosessen, endre frekvensen og definere en hvilemodusperiode.

Hvis du vil ha mer informasjon om oppsettet for prosessautomatisering, kan du se [Prosessautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
