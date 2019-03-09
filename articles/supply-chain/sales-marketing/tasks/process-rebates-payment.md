---
title: Behandle rabatter for betaling
description: Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2d97a59ae782af0a3d5ab71903961ef244a8e62
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "363321"
---
# <a name="process-rebates-for-payment"></a>Behandle rabatter for betaling

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

