--- 
title: Tilordne en mal for fritekstfaktura til en kunde
description: Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Tilordne en mal for fritekstfaktura til en kunde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde. Denne oppgaven bruker USMF-demofirmaet og er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.

1. Gå til Kunder > Kunder > Alle kunder.
2. Finn og velg ønsket post i listen.
3. Klikk Faktura i handlingsruten.
4. Klikk Gjentakende fakturalinjer.
    * Bruk denne siden til å tilordne mallinjer for fritekstfaktura til kunder og angi hvor ofte fakturaer skal sendes til kunden.  
5. Klikk Ny for å tilordne en ny mal til kunden.
6. Velg malen for fritekstfaktura du vil tilordne til kunden.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Angi datoen som den første fakturaen skal genereres på.
    * Angi en gjentakende sluttdato.  
    * Velg ett av følgende: Ingen sluttdato – fakturaer genereres helt til malen blir fjernet fra kundekontoen.  Sluttdato for fakturering – velg dette alternativet og angi den siste datoen som fakturaen kan genereres på.  
    * Maksimalt akkumulert beløp før fakturagenerering stopper.  
    * Angi det maksimale akkumulerte beløpet som kan nås ved hjelp av den valgte malen. Hvis du for eksempel angir 1 000,00 og genererer månedlige fakturaer for 100,00 hver, stopper genereringen av fakturaer når den tiende fakturaen er generert.  
    * Generer gjentakende fakturaer ved å bruke standardverdiene fra kundekontoen eller malen for fritekstfaktura.  
    * Velg om du vil bruke malen for fritekstfaktura eller kundekontoen for å bestemme standardverdiene for språket, posteringsprofilen, merverdiavgiftsgruppen, merverdiavgiftgruppen for vare, listekoden, land/område for levering, valuta, betalingsbetingelser, betalingsmåten, betalingsspesifikasjoner, betalingsplanen, kontantrabatt, finansdimensjoner og girokort når fakturaer opprettes.  
10. Velg mønsteret for regelmessighet.
    * Daglig – Velg dette alternativet og angi antall dager i feltet Per. Hvis du for eksempel angir 15, genereres en faktura hver 15. dag for denne kunden.  Ukentlig – Velg dette alternativet og angi antall uker i feltet Per. Hvis du for eksempel angir 2, genereres en faktura annenhver uke for denne kunden.  Månedlig – Velg dette alternativet og angi antall måneder i feltet Per. Hvis du for eksempel angir 6, genereres en faktura hver sjette måned for denne kunden.  Årlig – Velg dette alternativet og angi antall år i feltet Per. Hvis du for eksempel angir 2, genereres en faktura annethvert år for denne kunden.  
11. Angi et tall i feltet Per.


