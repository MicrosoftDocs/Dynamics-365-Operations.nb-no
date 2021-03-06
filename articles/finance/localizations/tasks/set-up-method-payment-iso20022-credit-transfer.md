---
title: Definere en betalingsmåte for ISO20022-kredittoverføring
description: Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 643be31db625d0db12f1df18b9e797013da98ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832478"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Definere en betalingsmåte for ISO20022-kredittoverføring

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]