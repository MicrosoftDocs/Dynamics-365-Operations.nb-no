---
title: Behandle rabatter for betaling
description: Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c617abd6ad715fff658451a7af3e775cf5e83292
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816466"
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