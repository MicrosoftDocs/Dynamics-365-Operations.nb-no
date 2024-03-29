---
title: Opprette betalingsfakturaer
description: Denne artikkelen forklarer hvordan du oppretter månedlige leiefakturaer. Du kan opprette fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0ac9efaf6d068377053ae36951f4ad808fcb2438
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886423"
---
# <a name="create-payment-invoices"></a>Opprette betalingsfakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Du kan opprette månedlige fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler. Følgende fremgangsmåte viser hvordan du oppretter en individuell oppføring for leiebetaling når parameteren **Betal til leverandør** på siden **Oppsett av leietablå** er aktivert.

1. På siden **Leiesammendrag** velger du en leieavtale, og deretter velger du **Tablåer \> Betalingsplan**.
2. Velg betalingen som må gjøres, og velg deretter **Opprett journal**. Du får en melding om at det ble opprettet en journal mot den valgte betalingen.
3. Velg **Fakturajournaler**, og velg deretter fakturaen som må betales.
4. Se gjennom journaloppføringen på **Linjer**-siden før du posterer den i økonomimodulen.

    > [!NOTE]
    > Leverandørfakturalinjene som opprettes, bruer som standard leverandørposteringsprofilen fra siden **Leverandørparametere**.

5. Velg riktig journal, og velg deretter fakturaen som må betales.

    I dette eksemplet er parameteren **Betal til leverandør** i leietablået aktivert. Fakturaen kommer derfor til å være i fakturajournalen. **Oversikt**-delen viser et sammendrag av journaloppføringen, og **Linjer**-delen viser detaljer om de faktiske journallinjene.
    
   Systemet låser bestemte økonomiske felt fra å bli redigert for å forhindre avvik mellom transaksjonene og planene. Noen av feltene som er låst, inkluderer: **Konto**, **Beløp**, **Finansdimensjoner**, **Valuta** og **Transaksjonstype**. I tillegg kan du ikke legge til eller slette journaloppføringslinjer i noen journaloppføringer for anleggsmiddelleasing, fordi dette kan føre til avvik mellom planene og transaksjonene.

    > [!NOTE]
    > Hvis parameteren **Betal til leverandør** er deaktivert, blir betalingsjournaloppføringer oppført på siden **Aktivaleie** for leietablået, og systemet oppretter en aktivaleieoppføring i stedet for en faktura. Oppføringen for leiebetaling blir postert i journalnavnet som er angitt i feltet **Journal for månedlig leie**.

6. Etter at transaksjonen er postert, kan du vise transaksjonsinformasjonen og den bokførte verdien til leieforpliktelse ved å velge **Gjeldstransaksjoner** i leietablået.

    Det merkes av for **Journal postert** i betalingsplanen, og linjen viser fakturajournalnummeret. Etter at en betalingsjournal og en oppføring for denne journalen er opprettet, må du tilbakeføre oppføringen før den kan opprettes på nytt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
