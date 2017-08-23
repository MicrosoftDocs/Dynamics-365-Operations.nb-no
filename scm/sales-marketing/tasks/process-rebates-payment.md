--- 
title: Behandle rabatter for betaling
description: "Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 73bfc08115a9727cbdcbe9b37e1427e67341dbd8
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="process-rebates-for-payment"></a>Behandle rabatter for betaling

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer. Du kan bruke denne veiledningen i USMF-demofirmaet. Forutsetningen for denne veiledningen er å ha ett eller flere rabattkrav som har statusen for Merk. Hvis du bruker USMF, bør du kjøre veiledningen Generere og behandle kunderabatter før du starter denne veiledningen.


## <a name="convert-rebate-claims-to-credit-note"></a>Konvertere rabattkrav til kreditnota
1. Gå til Alle kunder.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Innkreving i handlingsruten.
5. Klikk Utlign transaksjoner.
6. Klikk Funksjoner.
7. Klikk Rabattprogram.
    * Rabatt-siden viser rabattkravene som du har behandlet i arbeidsområdet for kunderabatt, og som har statusen Merk.    
8. Klikk Rediger.
    * Angi merker i feltet Merk for kravene som du vil inkludere i kreditnotaen.   
9. Klikk Funksjoner.
10. Klikk Opprett kreditnota.
    * Det vises en melding å informere deg om at en journal er postert (dette er kundeforbruksjournalen, som angitt på Kundeparametere-siden). Dette gjør at beløpet for reell gjeld (kredit) flyttes til kundesaldoen. Dette betyr at kundekontoen er kreditert, og avsetningskontoen for rabatt er debitert.  
11. Lukk siden.
12. Klikk Avbryt.
    * Dette oppdaterer siden slik at du kan se oppdateringene.  
13. Klikk Innkreving i handlingsruten.
14. Klikk Utlign transaksjoner.
    * Legg merke til at en transaksjon for negativt beløp, som representerer det totale rabattbeløpet, uten fakturareferanse er lagt til i kundesaldoen.   
15. Klikk Avbryt.


