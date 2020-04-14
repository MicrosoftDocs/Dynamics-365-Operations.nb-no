---
title: Definere en betalingsmåte for ISO20022-avtalegiro
description: Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143438"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Definere en betalingsmåte for ISO20022-avtalegiro

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering. 



Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og betalingskontoer.



Denne fremgangsmåten ble opprettet med demonstrasjonsdatafirmaet DEMF.



Dette er den tredje av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.

1. Gå til Kunder > Betalingsoppsett > Betalingsmåter.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.
3. Klikk Rediger
4. Angi verdiene DEMF OPER i feltet Betalingskonto.
5. Vis delen Filformater.
6. Velg Ja i feltet Generell elektronisk rapportering.
7. Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.
    * I listen velger du ISO20022-avtalegiro (DE).  Hvis listen er tom, er ikke konfigurasjonen for eksportformater for kundebetaling importert og aktiv.  
8. I feltet Krever mandat velger du Ja.
    * Velg parameteren Krever mandat for kundebetalingsformater, som krever at mandatinformasjon tas med i betalingsmeldingen, som SEPA-avtalegiro.  
9. Klikk Lagre.

