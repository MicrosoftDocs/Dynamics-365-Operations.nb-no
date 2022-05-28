---
title: Definer og behandle mellombetalinger
description: Dette emnet forklarer hvordan du definerer og behandler mellombetalinger for kunder. En mellombetaling er en betaling som posteres til økonomimodulen i to trinn.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca93d99ce04e607b137a2755d507022a33ab1be8
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734198"
---
# <a name="set-up-and-process-bridged-payments"></a>Definer og behandle mellombetalinger

[!include [banner](../includes/banner.md)]

En mellombetaling er en betaling som posteres til økonomimodulen i to trinn. Denne fremgangsmåten brukes vanligvis når betalingsmåten er angitt til **Bank**, og du må postere transaksjoner til bankkontoen bare når transaksjonen har tømt banken. Du kan imidlertid også bruke det for en finanskonto. I dette tilfellet flytter systemet beløpet fra en hovedkonto til en annen hovedkonto når mellomposteringen behandles.

Du kan opprette mellombetalinger fra enten Leverandør eller fra Kunder. Selv om dette emnet beskriver hvordan du konfigurerer mellompostering for kunder, er trinnene for leverandørtransaksjoner ganske like.

## <a name="set-up-bridging-posting"></a>Definer mellompostering

Før du kan bruke mellompostering, må du definere en eller flere betalingsmåter, slik at de bruker metoden **Mellompostering**. Du må deretter velge en mellomkonto.

1. Gå til **Kunder &gt; Betalingsoppsett &gt; Betalingsmåter**.
2. Velg en eksisterende betalingsmåte som du skal aktivere mellompostering for. Du kan også opprette en ny betalingsmåte.
3. Merk av for **Mellompostering**.
4. I feltet **Mellomkonto** velger du hovedkontoen som betalingene skal posteres til, før de tømmes til bankkontoen.
5. Lukk siden.

## <a name="process-and-transfer-bridging-posting"></a>Behandle og overføre mellompostering

Følg denne fremgangsmåten for å opprette og behandle mellompostering.

1. Gå til **Kunder &gt; Betalinger &gt; Kundebetalingsjournal**.
2. Velg **Ny** for å opprette en journal.
3. Velg et navn i **Navn**-feltet.
4. Legg til linjer i kundebetalingsjournalen, og velg betalingsmåten som er konfigurert for mellompostering.
5. Poster journalen. Transaksjonene blir postert til hovedkontoen du valgte i feltet **Mellomkonto** i forrige fremgangsmåte.

Når transaksjonene har tømt banken, og du vil overføre betalingen fra mellomkontoen til betalingskontoen som er angitt for betalingsmåten, følger du denne fremgangsmåten.

1. Gå til **Økonomimodul &gt; Journaloppføringer &gt; Økonomijournaler**.
2. Velg **Ny** for å opprette en journal.
3. Velg et navn i **Navn**-feltet.
4. Velg **Linjer** for å åpne journaldetaljene.
5. Velg **Funksjoner &gt; Velg mellomtransaksjoner**.
6. Merk hver betaling som er avregnet, og velg deretter **Godta**.
7. Poster journalen.
