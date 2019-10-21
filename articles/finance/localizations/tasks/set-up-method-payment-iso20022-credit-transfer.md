---
title: Definere en betalingsmåte for ISO20022-kredittoverføring
description: Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174984"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Definere en betalingsmåte for ISO20022-kredittoverføring

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil. 

Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og konfigurere betalingskontoer.

Denne oppgaven ble opprettet med demonstrasjonsdatafirmaet DEMF.

Dette er den tredje prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.

1. Gå til Leverandører > Betalingsoppsett > Betalingsmåter.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien SEPA CT.
3. Klikk Rediger
4. Velg Total i Periode-feltet.
5. Velg Elektronisk betaling i Betalingstype-feltet.
6. Vis delen Filformater.
7. Velg Ja i feltet Generell elektronisk rapportering.
8. Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.
    * I listen velger du verdien ISO20022 kredittoverføring (DE). Hvis listen er tom, er ikke konfigurasjonen for eksportformater for leverandørbetaling importert og aktiv.  
9. Velg Bank i feltet Kontotype.
10. Angi verdiene DEMF OPER i feltet Betalingskonto.
11. Klikk Lagre.
