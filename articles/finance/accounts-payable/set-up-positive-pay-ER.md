---
title: Definer og generer positive betalingsfiler ved hjelp av elektronisk rapportering
description: Dette emnet forklarer hvordan du konfigurerer positiv betaling ved hjelp av elektronisk rapportering.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544489"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Definer positive betalingsfiler ved hjelp av elektronisk rapportering

Definer positiv betaling for å generere en elektronisk liste over sjekker som leveres til banken. Når sjekken presenteres til banken, sammenligner banken deretter sjekken med listen over sjekker. Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken. Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.

## <a name="set-up-the-electronic-reporting-configuration"></a>Sett opp konfigurasjonen av elektronisk rapportering

1. Gå til **Arbeidsområder \> Elektronisk rapportering**.
2. Velg **Repositorier** på flisen for **Microsoft**-konfigurasjonsleverandøren.
3. Velg **Global**, og velg deretter **Åpne**.
4. Hvis det må opprettes en tilkobling til repositoriet, velger du den blå koblingen i dialogboksen.
5. I konfigurasjonslisten finner du og velger **Positiv betalingsmodell \> Positivt betalingsformat**.
6. På hurtigfanen **Versjoner** velger du den nyeste versjonen, og deretter velger du **Importer**.

## <a name="set-up-a-positive-pay-format"></a>Definer et positivt betalingsformat

1. Gå til **Kontant- og bankbehandling \> Oppsett \> Positive betalingsformater**.
2. Velg **Ny**.
3. Angi feltene **Betalingsformat** og **Beskrivelse**.
4. Merk av for **Generelt elektronisk eksportformat**.
5. Sett feltet **Eksportformatkonfigurasjon** til **Positivt betalingsformat**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Tilordne et positivt betalingsformat til en bankkonto

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne bankkontoen.
3. På hurtigfanen **Generelt** angir du feltet **Positivt betalingsformat** til formatet som ble opprettet tidligere.
4. Sett feltet **Startdato for positiv betaling** til gjeldende dato.

## <a name="generate-a-positive-pay-file"></a>Generer en positiv betalingsfil

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne en bankkonto som positiv betaling er satt opp for.
3. Velg **Behandle betalinger \> Positiv betaling \> Positiv betalingsfil**.
4. Angi **Frist**-feltet. Sjekker som ble generert før denne datoen, vil bli inkludert.

Den resulterende XML-filen lastes ned.
