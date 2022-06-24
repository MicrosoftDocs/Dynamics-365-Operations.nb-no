---
title: Revaluere leiebetalinger som er koblet til en indeksrente
description: Denne artikkelen beskriver justeringen som gjøres for leieforpliktelsen for en bruksrettseiendel når variable leiebetalinger endres på grunn av en endring i indeksrenten.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903254"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Revaluere leiebetalinger som er koblet til en indeksrente

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver justeringen som gjøres for leieforpliktelsen for en bruksrettseiendel når variable leiebetalinger endres på grunn av en endring i indeksrenten. Leieforpliktelsen og bruksrettseiendelene vil bli justert for til kontoen for de nye betalingsbeløp. Under Accounting Standards Codification-emne 842 (ASC 842), som er standard i regnskapsnormen Generally Accepted Accounting Principles i USA (US GAAP), endres bare de variable betalingene når betalinger økes eller reduseres på grunn av en endring i indeksrenten, med mindre det er flere endringer i kontantstrømmene. Disse tilleggsendringene kan inkludere en endring i leievilkårene som er knyttet til rentesatser. Hvis du vil ha mer informasjon, se ASC 842-10-55-225 og avsnitt 42(b) i International Financial Reporting Standard 16 (IFRS 16).

## <a name="adjust-lease-payments"></a>Justere leiebetalinger

Følg disse trinnene for å revaluere leiebetalinger som er koblet til en indeksrente.

1. Hvis du vil kjøre prosessen for revaluering av leieindeks, går du til **Aktivaleie \> Periodisk \> Revaluering av indeksrente**.

    Siden for **Revaluering av indeksrente** vises og viser alle tidligere prosesser for revaluering av leieindeks som har blitt kjørt. Informasjonen på denne siden inkluderer prosess-IDen som ble generert fra nummerserieoppsettet, den juridiske enheten, antallet leietablåer som ble justert, total gjeldsjustering for IFRS 16-leieavtaler og de totale variable betalingene som ble justert for ASC 842-leieavtaler.

2. Hvis du vil kjøre revalueringen, går du til handlingsruten og velger **revaluering av leieindeks**.

    Dialogboksen for **parametere for revaluering av indeks** vises. Her kan du filtrere og velge hvilke leieavtaler, leiegrupper eller andre kriterier du vil bruke når du velger leieavtalene som skal revalueres. I tillegg, i kategorien **Kjør i bakgrunnen**, kan du definere prosessen for revaluering av indeks, slik at den kjøres i en satsvis jobb.

4. Velg filtrene for å velge leieavtaler som skal inkluderes i bakgrunnsbehandlingen, og velg deretter **OK**.

    Dialogboksen for **forhåndsvisning av revaluering av indeksrente** vises og viser leieavtalene som skal revalueres. Den viser også aktiva- og gjeldsjusteringer eller de variable betalingsjusteringene.

5. Hvis du vil hindre at leieavtaler revalueres, velger du leieavtalene som **skal** revalueres. Hvis du ikke velger noen leieavtaler, revalueres alle leieavtalene. Når du er ferdig, velger du **OK** for å revaluere leiebetalingene.
6. Hvis du vil vise transaksjonene som ble opprettet for en bestemt prosess for revaluering av indeks, velger du prosess-IDen, og deretter velger du **Transaksjoner**.

    Det vises en dialogboks med detaljer om transaksjonene som ble opprettet under behandling.

> [!NOTE]
> Bare leieavtaler som har en revalueringsdato som er på eller før systemdatoen, kan revalueres. Systemet ignorerer automatisk alle leieavtaler som har en revalueringsdato som er senere enn systemdatoen.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842-leieavtaler – revaluering av indeks

Hvis du vil vise virkningene av prosessen for revaluering av leie i ASC 842-leieavtaler, åpner du betalingsplanen for en leieavtale. Siden viser bare de variable betalingene som er gjort på eller etter at revalueringsdatoen ble endret på grunn av revalueringen av indeksen. Nedbetalings- og avskrivningsplanene forblir uendret. Når du oppretter en faktura som har en variabel betaling, blir den variable betalingen debitert til posteringskontoen for variabel betaling. Det variable betalingsbeløpet legges til i kreditoppføringen som posteres direkte til leverandøren, eller posteres til gjeldskontoen, avhengig av oppsettet for leietablået.

Betalingsplanlinjene på leiedetaljsiden oppdateres automatisk med en ny linje som angir den nye indekseringsrenten. I tillegg viser en kolonne om linjen ble opprettet manuelt eller via indeksrevalueringsprosessen.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-leieavtaler – revaluering av indeks

Hvis du vil vise virkningene av prosessen for revaluering av leie i IFRS 16-leieavtaler, åpner du leiedetaljene for en justert leieavtale. Feltene for **Leieperiode** og **Aktivalevetid** er oppdatert for å vise tiden fra oppstartsdatoen eller endringsdatoen til revalueringsdatoen. I tillegg er betalingsplanlinjene oppdatert for å gjenspeile de nye betalingene for leieavtalen, den nye indeksrenten og hvordan linjen ble opprettet.

Du kan vise den nygenererte betalingsplanen som starter på revalueringsdatoen, og vise det totale oppdaterte betalingsbeløpet. Det er også opprettet en ny nedbetalingsplan for leieforpliktelse og en avskrivningsplan for aktiva for å gjenspeile den justerte betalingsplanen.

Journaloppføringen har automatisk postert justeringsjournaloppføringen til kontoen for endringen i leiebetalinger som er knyttet til revalueringen av indeks.

> [!NOTE]
> Hvis alternativet **Oppdeling av betalingsbeløp** er aktivert på hurtigfanen **Generelt** på siden **Leiedetaljer**, og det tilknyttede tablået er IFRS 16, vil indeksrevalueringsprosessen automatisk legge til en post i dialogboksen **Oppdeling av betalingsbeløp**. Beløpet gjenspeiler endringen som ble gjort i betalingen på grunn av indeksrevaluering. Posten merkes som **Brukes til IRFS 16-indeksrevaluering**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
