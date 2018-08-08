--- 
title: "Opprette en rekvisisjon som bruker en tilbudsforespørsel"
description: "Denne veiledningen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Opprette en rekvisisjon som bruker en tilbudsforespørsel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF, og du må være logget på som administrator for å fullføre alle trinnene. Oppgavene i denne veiledningen utføres vanligvis av innkjøpsansvarlige.


## <a name="create-a-requisition"></a>Opprette en rekvisisjon
1. Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi en dato i feltet Ønsket dato.
5. Angi en dato i feltet Regnskapsdato.
6. Klikk OK.
7. Angi eller velg en verdi i feltet Årsak.
8. Klikk Legg til linje.
9. Velg en kategori i treet i Innkjøpskategori-feltet, og klikk deretter OK.
10. Skriv inn en verdi i feltet Produktnavn.
11. Angi et tall i feltet Antall.
12. Angi eller velg en verdi i Enhet-feltet.
13. Klikk Lagre.
14. Klikk Arbeidsflyt for å åpne nedtrekksdialogen.
15. Klikk Send.
16. Lukk siden.
17. Klikk Send.

## <a name="reassign-a-workflow-task"></a>Tilordne en arbeidsflytoppgave på nytt
    * Den neste oppgaven er å opprette en tilbudsforespørsel for å få bud fra leverandører for produktet. I demonstrasjonsdataene for USMF er rekvisisjonsarbeidsflyten definert med en regel slik at hvis en leverandør ikke er valgt, eller enhetsprisen er 0 for en linje, tilordnes en oppgave til en bestemt arbeider for å opprette en tilbudsforespørsel. Du må tilordne oppgaven på nytt til en annen bruker (deg selv) for å fortsette med denne veiledningen. Du kan bare gjøre dette hvis du er logget på som administrator.  
1. Klikk Arbeidsflyt for å åpne nedtrekksdialogen.
2. Klikk Vis logg.
3. Oppdater siden.
4. Vis delen Sporingsdetaljer.
5. I treet velger du linjen som begynner med Linjeelementarbeidsflyt aktivert på.
6. Klikk Vis arbeidsflytdetaljer.
7. Vis delen Arbeidselementer.
8. Klikk Tilordne på nytt.
9. Velg Administrator i Bruker-feltet.
10. Klikk Tilordne på nytt.
11. Lukk siden.
12. Lukk siden.

## <a name="create-an-rfq"></a>Opprette en tilbudsforespørsel
1. Oppdater siden.
2. Klikk Svar på tilbudsforespørsel.
3. Velg USMF i feltet Kjøpende juridisk enhet.
    * Du må velge samme juridiske enheten som er på rekvisisjonslinjen.  
4. Merk den valgte raden i listen.
    * Hvis du har flere linjer på innkjøpsrekvisisjonen din, velger du alle linjene som du vil legge til i tilbudsforespørselen.  
5. Klikk OK.
6. Oppdater siden.
7. Åpne faktaboksen, og vis deretter delen Relaterte dokumenter.
    * Faktaboks er kanskje allerede åpen. Se etter ikonet med en pil, til høyre for veksleknapper Linjer/hode. Hvis pilen peker mot høyre, er faktaboksen allerede åpen. Hvis pilen peker mot venstre, klikker du den for å åpne faktaboksen.  
8. Klikk koblingen i Tilbudsforespørsel-feltet for å åpne tilbudsforespørselen som nettopp ble opprettet.
9. Klikk Overskrift.
10. Klikk Legg til.
11. Angi eller velg en verdi i Leverandørkonto-feltet.
12. Klikk Legg til.
13. Angi eller velg en verdi i Leverandørkonto-feltet.
14. Klikk Send.
15. Klikk OK.
16. Klikk Angi svar.
17. Klikk Svar i handlingsruten.
18. Klikk Kopier data for å svare.
    * Dette kopierer data, for eksempel antall og datoer, fra tilbudsforespørselen til svaret.  
19. Angi et tall i feltet Enhetspris.
    * Dette er prisen du har mottatt fra leverandøren. Du kan også angi tilleggsinformasjon fra leverandøren.  
20. Klikk Godta.
21. Klikk OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Kontrollere at leverandøren prisen er overfør til rekvisisjonen
1. Lukk siden.
2. Klikk Linjer.
3. Klikk Relatert informasjon.
4. Klikk Innkjøpsrekvisisjonslinjer.
5. Velg linjen som ble overført til tilbudsforespørselen.
    * Kontroller at prisen og leverandøren er kopiert til rekvisisjonen.  
6. Klikk Arbeidsflyt for å åpne nedtrekksdialogen.
7. Klikk Fullført.
8. Lukk siden.
9. Klikk Fullført.


