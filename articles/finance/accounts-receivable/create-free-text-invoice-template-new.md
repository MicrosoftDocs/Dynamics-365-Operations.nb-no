---
title: Opprette en mal for fritekstfaktura
description: Denne fremgangsmåten beskriver hvordan du oppretter en mal for fritekstkundefaktura.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182535"
---
# <a name="create-a-free-text-invoice-template"></a>Opprette en mal for fritekstfaktura

[!include [banner](../includes/banner.md)]

For denne gjennomgangen må du bruke demonstrasjonsfirmaet USMF. Denne fremgangsmåten er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.

## <a name="create-a-template"></a>Opprett en mal

1. Gå til **Kunder > Fakturaer > Gjentakende fakturaer > Mallinjer for fritekstfaktura**.
    * Bruk denne siden til å opprette maler for fritekstfaktura som kan inneholde fakturalinjer, tillegg, en regnskapsdistribusjonsmal og finanskontoinformasjon.  
2. Klikk på **Ny** for å opprette en ny mal for fritekstfaktura.
3. Skriv inn en verdi i **Malnavn**-feltet.
    * "Malnavn" identifiserer unikt en mal for fritekstfaktura. To maler kan ikke ha samme malnavn.  
4. Angi en beskrivelse av malen i **Beskrivelse**-feltet.
5. Utvid **Fakturalinjer**-fanen.
6. I **Beskrivelse**-feltet angir du en beskrivelse av fakturalinjen.
7. I **Hovedkonto**-feltet velger du en inntektskonto.
    * Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på siden **Kundeposteringsprofiler**.  
8. Klikk på rullegardinknappen i feltet **Mva-gruppe** for å åpne oppslaget.
    * Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.  
9. Klikk på koblingen i den valgte raden i listen.
10. I feltet **Vareavgiftsgruppe** velger du mva-gruppen for vare for den gjeldende fakturalinjen.
11. Klikk på koblingen i den valgte raden i listen.
12. I **Enhetspris**-feltet angir eller viser du prisen per enhet for fakturalinjen.
    * Dette beløpet multipliseres med **Antall**-feltet for å bestemme fakturalinjebeløpet.  
13. Legg til en ny linje i malen for fritekstfaktura.
14. I **Beskrivelse**-feltet angir du en beskrivelse av fakturalinjen.
15. I **Hovedkonto**-feltet velger du en inntektskonto.
    * Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på siden **Kundeposteringsprofiler**.  
16. Klikk på rullegardinknappen i feltet **Mva-gruppe** for å åpne oppslaget.
    * Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.  
17. Klikk på koblingen i den valgte raden i listen.
18. Klikk på rullegardinknappen i feltet **Merverdiavgiftsgruppe for vare** for å åpne oppslaget.
    * Mva-gruppen for varesalg for den gjeldende fakturalinjen.  
19. Klikk på koblingen i den valgte raden i listen.
20. Angi eller vis antall enheter for fakturalinjen.
    * Dette nummeret multipliseres med verdien i Enhetspris-feltet for å bestemme fakturalinjebeløpet.  
21. Angi eller vis prisen per enhet for fakturalinjen. 
    * Dette beløpet multipliseres med verdien i **Antall**-feltet for å bestemme fakturalinjebeløpet.  
22. Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer.
    * Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura.  
23. Oppdater regnskapsdistribusjonene for den valgte fakturalinjen.
24. Klikk på **Lukk**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Lagre en fritekstfaktura som mal
Du kan også lagre en eksisterende fritekstfaktura som en mal. Når du velger **Lagre i mal** i **Faktura**-fanen, må du angi et navn og en beskrivelse for malen. Hvis det finnes allerede en mal med det samme navnet, vises en melding om at en mal med dette navnet allerede finnes. Du kan fremdeles klikke **OK** for å erstatte den. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
