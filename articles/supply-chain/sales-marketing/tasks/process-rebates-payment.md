---
title: Behandle rabatter for betaling
description: Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d32d94daef570e37a1a36d948fe18cd4041e46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966161"
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

