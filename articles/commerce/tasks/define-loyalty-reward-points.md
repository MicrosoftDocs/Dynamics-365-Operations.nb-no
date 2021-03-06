---
title: " Definere fordelspoeng"
description: Denne prosedyren hjelper med å definere fordelspoeng.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7f3b19513bb25d1976d2e4d0e235c347c38ccb4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798471"
---
# <a name="define-loyalty-reward-points"></a> Definere fordelspoeng

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å definere fordelspoeng. Du må definere fordelspoeng før du oppretter et fordelsprogram. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kunder > Fordel > Fordelspoeng.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for fordelspoeng.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg et alternativ i feltet Type fordelspoeng.
    * Velg Antall hvis du vil at fordelspoengene skal avrundes til nærmeste heltall. Velg Beløp hvis du vil at fordelspoengene skal avrundes i henhold til valutaavrundingsregler. Hvis du velger Antall, hopper du over neste trinn i prosedyren.  
6. Skriv inn en verdi i Valuta-feltet.
    * Alle utstedte poeng vil ha den valgte valutaen for fordelspoeng av typen Beløp. Dette feltet gjelder ikke for fordelspoeng av typen Antall. Hopp over dette trinnet.  
7. Merk av eller fjern merket for Kan løses inn.
8. Angi et tall i Innløsningsrangering-feltet.
    * Innløsningsrangering brukes når to eller flere innløsbare fordelspoeng kan brukes til å betale for produkter. Hvis de to fordelspoengene har samme innløsningsrangering, må det som må senke antall poeng brukes.  
9. Du må angi en verdi i feltet Verdi for utløpstid.
    * Fordelspoengene utløper angitt antall dager, måneder eller år etter at poengene ble utstedt. Verdien 0 betyr at fordelspoengene aldri utløper.  
10. Velg et alternativ i feltet Enhet for utløpstid.
11. Klikk Lagre.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]