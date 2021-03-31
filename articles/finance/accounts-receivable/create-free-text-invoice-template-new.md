---
title: Opprette en mal for fritekstfaktura
description: Denne fremgangsmåten beskriver hvordan du oppretter en mal for fritekstkundefaktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdcb307686800e0038212982c1eac6f1c14cf8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217488"
---
# <a name="create-a-free-text-invoice-template"></a>Opprette en mal for fritekstfaktura

[!include [banner](../includes/banner.md)]

For denne gjennomgangen må du bruke demonstrasjonsfirmaet USMF. Denne fremgangsmåten er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.

## <a name="create-a-template"></a>Opprett en mal

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

## <a name="save-a-free-text-invoice-as-a-template"></a>Lagre en fritekstfaktura som mal
Du kan også lagre en eksisterende fritekstfaktura som en mal. Når du velger Lagre mal i kategorien Faktura, må du angi et navn og en beskrivelse for malen. Hvis det finnes allerede en mal med det samme navnet, vises en melding om at en mal med dette navnet allerede finnes. Du kan fremdeles klikke OK for å erstatte den. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]