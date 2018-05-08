--- 
title: Opprett en fritekstfaktura
description: Denne veiledningen beskriver hvordan du oppretter en fritekstfaktura.
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: nb-no
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a>Opprett en fritekstfaktura

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen beskriver hvordan du oppretter en fritekstfaktura. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Kunder > Fakturaer > Alle fritekstfakturaer.
2. Klikk Ny.
3. Velg en verdi i Kundekonto-feltet.
    * Fakturakontoen er som standard den samme kontoen som brukes for kundekontoen.   
    * Regnskapsstatusen starter med Pågår hvis fakturaen ikke er postert.   
    * Fakturanummeret tilordnes når fakturaen posteres.  
    * Hvis du bruker SEPA-mandater, fylles avtalegiromandatet automatisk ut med et mandat når du velger kundekontoen.  
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi et kontonummer uten dimensjoner i Hovedkonto-feltet.
    * Du kan også angi ett eller flere tegn for hovedkontoen og bruke oppslaget til å finne kontoen din. Du vil angi dimensjoner senere i denne veiledningen.  
6. Vis hurtigfanen Linjedetaljer slik at du kan legge til dimensjoner i hovedkontoen.
7. Klikk kategorien Finansdimensjonslinje.
    * Dimensjonene gjelder bare for den valgte linjen.    
    * Mva-gruppen fylles ut fra kunden. Hvis kunden ikke har en mva-gruppe, brukes mva-gruppen fra hovedkontoen.  
    * Mva-gruppen for varer fylles ut fra hovedkontoen. Hvis hovedkontoen ikke har en mva-gruppe for varer, brukes mva-gruppen for varer i mva-parameterne for økonomimodul.    
8. Angi et tall i feltet Antall.
    * Antallet er valgfritt.  
9. Angi et tall i feltet Enhetspris.
    * Enhetsprisen er valgfri.  
    * Beløpet beregnes som antallet ganger enhetsprisen. Du kan imidlertid overstyre dette, og angi et beløp.  
10. Hvis du vil vise merverdiavgiften som er beregnet for fakturaen, klikker du Merverdiavgift.
    * Du kan vise mva-beløpene på denne siden, eller du kan overstyre beløpene i kategorien Justering.  
11. Klikk OK.
12. Klikk Tillegg for å legge til et tillegg på fakturaen. 
13. Skriv inn en verdi i Tilleggskode-feltet.
14. Angi et tall i Gebyrverdi-feltet.
15. Lukk siden.
16. Klikk Totaler for å vise detaljer for sammendrag og totaler.
17. Klikk Lukk.
18. Klikk Poster for å postere fakturaen. Du kan avbryte før du posterer.
    * Slik endrer du når fakturaene skal skrives ut: Velg Gjeldende for å skrive ut hver faktura når den oppdateres, eller velg Etter for å skrive ut når alle fakturaene er oppdatert.  
    * Hvis du vil endre hvordan kundens kredittgrense kontrolleres før postering, kan du endre kredittgrensetypen.  
    * Velg Ja hvis du vil skrive ut fakturaen.  
    * Velg Ja hvis du vil postere fakturaen. Du kan skrive ut fakturaen uten postering.  
19. Klikk OK.


