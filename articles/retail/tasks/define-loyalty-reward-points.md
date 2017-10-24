--- 
title: " Definere fordelspoeng"
description: "Denne prosedyren hjelper med å definere fordelspoeng."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05237a0ba3aa785432c8b1fc36284a47f9aabd4a
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-reward-points"></a> Definere fordelspoeng

[!include[task guide banner](../includes/task-guide-banner.md)]

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


