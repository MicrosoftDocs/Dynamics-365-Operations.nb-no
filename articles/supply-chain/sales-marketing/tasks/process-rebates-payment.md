---
title: Behandle rabatter for betaling
description: Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.
author: Henrikan
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce813f0f5d9aa750828b524dd9fdf9b4a9f0854
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572487"
---
# <a name="process-rebates-for-payment"></a>Behandle rabatter for betaling

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer. Du kan bruke denne veiledningen i USMF-demofirmaet. Forutsetningen for denne veiledningen er å ha ett eller flere rabattkrav som har statusen for Merk. Hvis du bruker USMF, bør du kjøre veiledningen Generere og behandle kunderabatter før du starter denne veiledningen.


## <a name="convert-rebate-claims-to-credit-note"></a>Konvertere rabattkrav til kreditnota
1. Gå til Alle kunder.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Klikk på Innkreving i handlingsruten.
5. Klikk på Utlign transaksjoner.
6. Klikk på Funksjoner.
7. Klikk på Rabattprogram.
    * Rabatt-siden viser rabattkravene som du har behandlet i arbeidsområdet for kunderabatt, og som har statusen Merk.    
8. Klikk på Rediger.
    * Angi merker i feltet Merk for kravene som du vil inkludere i kreditnotaen.   
9. Klikk på Funksjoner.
10. Klikk på Opprett kreditnota.
    * Det vises en melding å informere deg om at en journal er postert (dette er kundeforbruksjournalen, som angitt på Kundeparametere-siden). Dette gjør at beløpet for reell gjeld (kredit) flyttes til kundesaldoen. Dette betyr at kundekontoen er kreditert, og avsetningskontoen for rabatt er debitert.  
11. Lukk siden.
12. Klikk på Avbryt.
    * Dette oppdaterer siden slik at du kan se oppdateringene.  
13. Klikk på Innkreving i handlingsruten.
14. Klikk på Utlign transaksjoner.
    * Legg merke til at en transaksjon for negativt beløp, som representerer det totale rabattbeløpet, uten fakturareferanse er lagt til i kundesaldoen.   
15. Klikk på Avbryt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]