---
title: Tilordne en mal for fritekstfaktura til en kunde
description: Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49074c11659ae30fd2decdb93b4721441edff2c5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780589"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Tilordne en mal for fritekstfaktura til en kunde

[!include [banner](../../includes/banner.md)]

Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde. Denne oppgaven bruker USMF-demofirmaet og er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.

1. I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.
2. Finn og velg ønsket post i listen.
3. Klikk **Faktura** i **handlingsruten**.
4. Klikk **Gjentakende fakturalinjer**. Bruk denne siden til å tilordne mallinjer for fritekstfaktura til kunder og angi hvor ofte fakturaer skal sendes til kunden.  
5. Klikk **Ny** for å tilordne en ny mal til kunden.
6. I **Mal**-feltet velger du malen for fritekstfaktura du vil tilordne til kunden.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. I feltet **Startdato for fakturering** angir du datoen for når den første fakturaen skal genereres.
10. Angi en gjentakende sluttdato i delen **Gjentakende slutt**.  
    Velg ett av følgende: 
    - **Ingen sluttdato** – fakturaer genereres helt til malen blir fjernet fra kundekontoen.
    - **Sluttdato for fakturering** – velg dette alternativet og angi den siste datoen som fakturaen kan genereres på.  
11. I feltet **Maksimalt akkumulert beløp** angir du det maksimale akkumulerte beløpet for avslutning av fakturagenerering. Angi det maksimale akkumulerte beløpet som kan nås ved hjelp av den valgte malen. Hvis du for eksempel angir 1 000,00 og genererer månedlige fakturaer for 100,00 hver, stopper genereringen av fakturaer når den tiende fakturaen er generert.  
12. I delen **Generer gjentakende fakturaer ved å bruke standardverdiene** velger du kundekontoen eller malen for fritekstfaktura. Velg om du vil bruke malen for fritekstfaktura eller kundekontoen for å bestemme standardverdiene for språket, posteringsprofilen, merverdiavgiftsgruppen, merverdiavgiftgruppen for vare, listekoden, land/område for levering, valuta, betalingsbetingelser, betalingsmåten, betalingsspesifikasjoner, betalingsplanen, kontantrabatt, finansdimensjoner og girokort når fakturaer opprettes.  
13. Velg gjentakelsesmønsteret i feltet **Gjentakelsesmønster**.
    - **Daglig** – Velg dette alternativet og angi antall dager i feltet Per. Hvis du for eksempel angir 15, genereres en faktura hver 15. dag for denne kunden.
    - **Ukentlig** – Velg dette alternativet og angi antall uker i feltet Per. Hvis du for eksempel angir 2, genereres en faktura annenhver uke for denne kunden.
    - **Månedlig** – Velg dette alternativet og angi antall måneder i feltet Per. Hvis du for eksempel angir 6, genereres en faktura hver sjette måned for denne kunden.
    - **Årlig** – Velg dette alternativet og angi antall år i feltet Per. Hvis du for eksempel angir 2, genereres en faktura annethvert år for denne kunden.  
14. Angi et tall i feltet **Per**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
