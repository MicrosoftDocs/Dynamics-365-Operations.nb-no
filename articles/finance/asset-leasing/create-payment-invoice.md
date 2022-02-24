---
title: Opprette betalingsfakturaer
description: Dette emnet forklarer hvordan du oppretter månedlige leiefakturaer. Du kan opprette fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969584"
---
# <a name="create-payment-invoices"></a>Opprette betalingsfakturaer

[!include [banner](../includes/banner.md)]

Du kan opprette månedlige fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler. Følgende fremgangsmåte viser hvordan du oppretter en individuell oppføring for leiebetaling når parameteren **Betal til leverandør** på siden **Oppsett av leietablå** er aktivert.

1. På siden **Leiesammendrag** velger du en leieavtale, og deretter velger du **Tablåer \> Betalingsplan**.
2. Velg betalingen som må gjøres, og velg deretter **Opprett journal**. Du får en melding om at det ble opprettet en journal mot den valgte betalingen.
3. Velg **Fakturajournaler**, og velg deretter fakturaen som må betales.
4. Se gjennom journaloppføringen på **Linjer**-siden før du posterer den i økonomimodulen.

    > [!NOTE]
    > Leverandørfakturalinjene som opprettes, bruer som standard leverandørposteringsprofilen fra siden **Leverandørparametere**.

5. Velg riktig journal, og velg deretter fakturaen som må betales.

    I dette eksemplet er parameteren **Betal til leverandør** i leietablået aktivert. Fakturaen kommer derfor til å være i fakturajournalen. **Oversikt**-delen viser et sammendrag av journaloppføringen, og **Linjer**-delen viser detaljer om de faktiske journallinjene.

    > [!NOTE]
    > Hvis parameteren **Betal til leverandør** er deaktivert, blir betalingsjournaloppføringer oppført på siden **Aktivaleie** for leietablået, og systemet oppretter en aktivaleieoppføring i stedet for en faktura. Oppføringen for leiebetaling blir postert i journalnavnet som er angitt i feltet **Journal for månedlig leie**.

6. Etter at transaksjonen er postert, kan du vise transaksjonsinformasjonen og den bokførte verdien til leieforpliktelse ved å velge **Gjeldstransaksjoner** i leietablået.

    Det merkes av for **Journal postert** i betalingsplanen, og linjen viser fakturajournalnummeret. Etter at en betalingsjournal og en oppføring for denne journalen er opprettet, må du tilbakeføre oppføringen før den kan opprettes på nytt.
