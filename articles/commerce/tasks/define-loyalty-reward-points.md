---
title: " Definere fordelspoeng"
description: Denne prosedyren hjelper med å definere fordelspoeng.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailLoyaltyRewardPoints
ms.openlocfilehash: 9acd1429d17393f19a5e059b90a48b0b103535d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268899"
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
