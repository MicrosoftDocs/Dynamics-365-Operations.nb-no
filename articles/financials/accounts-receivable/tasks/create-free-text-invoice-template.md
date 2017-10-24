--- 
title: Opprette en mal for fritekstfaktura
description: Denne registreringen bruker demonstrasjonsfirmaet USMF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a>Opprette en mal for fritekstfaktura

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne registreringen bruker demonstrasjonsfirmaet USMF. Registreringen er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.

1. Gå til Kunder > Fakturaer > Gjentakende fakturaer > Mallinjer for fritekstfaktura.
    * Bruk dette skjemaet til å opprette maler for fritekstfaktura som kan inneholde fakturalinjer, tillegg, en regnskapsdistribusjonsmal og finanskontoinformasjon.  
2. Klikk Ny for å opprette en ny fritekstfakturamal.
3. Angi en verdi i Malnavn-feltet.
    * "Malnavn" identifiserer unikt en mal for fritekstfaktura. To maler kan ikke ha samme malnavn.  
4. Angi en beskrivelse av malen i Beskrivelse-feltet.
5. Utvid kategorien Fakturalinjer.
6. I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.
7. I Hovedkonto-feltet velger du en inntektskonto.
    * Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.  
8. Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.
    * Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.  
9. Klikk koblingen i den valgte raden i listen.
10. I feltet Vareavgiftsgruppe velger du mva-gruppen for vare for den gjeldende fakturalinjen.
11. Klikk koblingen i den valgte raden i listen.
12. I Enhetspris-feltet angir eller viser du prisen per enhet for fakturalinjen.
    * Dette beløpet multipliseres med Antall-feltet for å bestemme fakturalinjebeløpet.  
13. Legg til en ny linje i malen for fritekstfaktura.
14. I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.
15. I Hovedkonto-feltet velger du en inntektskonto.
    * Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.  
16. Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.
    * Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.  
17. Klikk koblingen i den valgte raden i listen.
18. Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.
    * Mva-gruppen for varesalg for den gjeldende fakturalinjen.  
19. Klikk koblingen i den valgte raden i listen.
20. Angi eller vis antall enheter for fakturalinjen.
    * Dette nummeret multipliseres med verdien i Enhetspris-feltet for å bestemme fakturalinjebeløpet.  
21. Angi eller vis prisen per enhet for fakturalinjen. 
    * Dette beløpet multipliseres med verdien i Antall-feltet for å bestemme fakturalinjebeløpet.  
22. Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer.
    * Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura.  
23. Oppdater regnskapsdistribusjonene for den valgte fakturalinjen.
24. Klikk Lukk.


