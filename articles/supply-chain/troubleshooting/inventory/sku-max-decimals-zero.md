---
title: Maksimalt antall desimaler for lagerføringsenheten er 0
description: 'Når du prøver å postere en lagertransaksjon eller lagerreservasjon, får du meldingen: "Maksimalt antall desimaler for lagerføringsenheten er 0".'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477239"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Maksimalt antall desimaler for lagerføringsenheten er 0


## <a name="symptoms"></a>Symptomer

Når du prøver å postere en lagertransaksjon eller en lagerreservering, får du følgende feilmelding:

> Maksimalt antall desimaler for lagerføringsenheten er 0.

Dette problemet oppstår når lagertransaksjonsantallet er angitt som en desimalverdi som er under presisjonsnivået som feltet støtter. Et antall på *0,5* er for eksempel angitt for en lagertransaksjon, men bare heltallsantall støttes. Verdien må derfor være *1* i stedet for *0,5*.

## <a name="resolution"></a>Løsning

1. Kjør følgende skript på SQL Server-forekomsten for å avrunde antall i lagertransaksjonene. Dette skriptet retter verdiene i **inventTrans**-tabellen.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Kjør en konsekvenskontroll for lagerbeholdning der alternativet **Rett feil** er aktivert. Denne kontrollen retter verdiene i **inventSum**-tabellen.

> [!IMPORTANT]
> Det anbefales på det sterkeste at du redigerer skriptet nøye etter behov for miljøet, tester det i et testmiljø og kontrollerer de resulterende dataene før du kjører skriptet i et produksjonsmiljø.
