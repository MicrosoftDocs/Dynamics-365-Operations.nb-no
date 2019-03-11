---
title: Opprette salgsordrefakturaer
description: Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "353316"
---
# <a name="create-sales-order-invoices"></a>Opprette salgsordrefakturaer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Opprette en faktura fra en salgsordre
1. Gå til Kunder > Ordrer > Salgsordrer som er sendt, men ikke fakturert.
2. Velg en salgsordre fra listen. 
3. Klikk Faktura i handlingsruten.
4. Klikk Faktura.
    * Legg merke til at denne salgsordren har flere følgesedler tilknyttet. Den viser bare ordet <multiple> i stedet for følgeseddelnummeret.  
5. Utvid seksjonen Parametere.
    * Postering må settes til Ja for å postere fakturaen. Du kan også slå av postering, og du kan bare skrive ut fakturaen. Du kan imidlertid oppnå samme resultat ved å opprette en proformafaktura i stedet for en faktura.  
    * Dette alternativet brukes for satsvise jobber. Spørringen kjøres når den satsvise jobben kjøres.    
6. Velg Etter i feltet Skriv ut.
7. Velg Ja for å skrive ut fakturaen.
    * Utskriftsbehandling kan skrive ut flere eksemplarer av fakturaen, og også sende fakturaen via e-post som en PDF-fil.  
8. Velg Summer i feltet Skriv ut tillegg.
9. I feltet Kontroller kredittgrense velger du Saldo.
10. Klikk Avbryt.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinere ordrer til én enkelt faktura
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Finn en kunde som har flere fakturaer som er åpne.
3. Velg en åpen salgsordre.
4. Velg en ny åpen salgsordre for den samme kunden.
5. Klikk Faktura i handlingsruten.
6. Klikk Faktura.
7. Utvid seksjonen Parametere.
8. Velg Alle i feltet Antall.
    * Legg merke til at det finnes to fakturaer som er oppført i oversiktsdelen. Nå skal vi slå dem sammen til én enkelt faktura.  
9. I samleoppdateringen for feltet velger du "Fakturakonto".
10. Klikk Ordre for å slå sammen salgsordrene til én enkelt faktura.
    * De to ordrene er nå slått sammen til én enkelt faktura.   
11. Klikk Avbryt.
12. Klikk Ja.

## <a name="post-invoices-in-a-batch"></a>Postere fakturaer i en satsvis jobb
1. Gå til Kunder > Fakturaer > Partifakturering > Faktura.
2. Klikk Velg.
3. Klikk OK.
4. Klikk Parti.
5. Klikk på Ja for å aktivere satsvis behandling.
6. Klikk Regelmessighet.
7. Velg Dager
8. Klikk OK.
9. Klikk OK.
10. Klikk Avbryt.
11. Klikk Ja.

