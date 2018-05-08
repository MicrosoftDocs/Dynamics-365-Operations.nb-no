--- 
title: "Definere en betalingsmåte for ISO20022-avtalegiro"
description: "Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3a884837ab0b5a1f4211532969619b54206bbef4
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Definere en betalingsmåte for ISO20022-avtalegiro

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


