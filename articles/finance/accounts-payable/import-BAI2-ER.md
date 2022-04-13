---
title: Konfigurere import av avansert bankavstemming ved hjelp av elektronisk rapportering
description: Dette emnet beskriver hvordan du bruker elektronisk rapportering til å konfigurere importprosessen for avansert bankavstemming for BAI2-kontoutdrag.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544505"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Konfigurere import av avansert bankavstemming ved hjelp av elektronisk rapportering

[!include [banner](../includes/banner.md)]

Avansert bankavstemming-funksjonen lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 Finance. Dette emnet beskriver hvordan du definerer funksjonen for import av dine BAI2-bankkontoutdrag.

## <a name="set-up-the-electronic-reporting-configuration"></a>Sett opp konfigurasjonen av elektronisk rapportering

1. Gå til **Arbeidsområder \> Elektronisk rapportering**.
2. Velg **Repositorier** på flisen for **Microsoft**-konfigurasjonsleverandøren.
3. Velg **Global**, og velg deretter **Åpne**.
4. Hvis det må opprettes en tilkobling til repositoriet, velger du den blå koblingen i dialogboksen.
5. I konfigurasjonslisten finner du **Bankkontoutdragsmodell \> Bankkontoutdragsmodell BAI2**.
6. Velg **BAI2**-formatet.
7. På hurtigfanen **Versjoner** velger du den nyeste versjonen, og deretter velger du **Importer**.

## <a name="set-up-the-bank-statement-format"></a>Definer formatet for bankkontoutdrag

1. Gå til **Kontant- og bankbehandling \> Oppsett \> Oppsett for avansert bankavstemming \> Bankkontoutdragsformat**.
2. Velg **Ny**.
3. Angi feltene **Utdragsformat** og **Navn**.
4. Merk av for **Generelt elektronisk importformat**.
5. Sett feltet **Importer konfigurasjon av format** til **BAI2**-formatet.

## <a name="set-up-the-bank-account"></a>Konfigurer bankkontoen

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne bankkontoen.
3. På hurtigfanen **Avstemming** setter du alternativet **Avansert bankavstemming** til **Ja**.
4. Sett feltet **Utdragsformat** til **BAI2**-formatet som ble opprettet tidligere.

## <a name="import-the-bank-statement"></a>Importer bankkontoutdraget

1. Gå til **Kontant- og bankbehandling \> Avstemming av bankkontoutdrag \> Bankkontoutdrag**.
2. Øverst på siden **Bankkontoutdrag** velger du **Importer utdrag**.
3. Sett **Bankkonto**-feltet til bankkontoen i kontoutdraget.
4. Sett feltet **Utdragsformat** til **BAI2**-formatet som ble opprettet tidligere.
5. Velg **Bla gjennom**, og velg **BAI**-filen.
6. Velg **Last opp**.
7. Velg **OK** for å importere den valgte filen.
