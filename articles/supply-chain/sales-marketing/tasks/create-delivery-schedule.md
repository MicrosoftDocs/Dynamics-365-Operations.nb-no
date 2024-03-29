---
title: Opprette leveringsplan
description: Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en salgsordre.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97dbbcc7173dcece9aea833551e8f985246bdbb2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578974"
---
# <a name="create-delivery-schedule"></a>Opprette leveringsplan

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en salgsordre. En leveringsplan brukes når et antall i en ordre eller et tilbud blir bedt om å bli levert i flere leveranser. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="create-delivery-schedule"></a>Opprette leveringsplan
1. Gå til Alle salgsordrer.
2. Klikk på Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
4. Klikk på OK.
5. Angi eller velg en verdi i Varenummer-feltet.
6. Angi et nummer i feltet Antall som er større enn 1.
7. Klikk på Salgsordrelinje.
8. Klikk på Leveringsplan.
    * Siden Leveringsplan er stedet der du kan angi antall leveranser der det totale antallet på ordrelinjen skal leveres til kunden.    
    * Som standard kopieres det totale antallet og andre leveringsdetaljer for den opprinnelige salgsordrelinjen til den første leveringslinjen for planen. I dette eksemplet skal vi opprette en tidsplan for to forsendelser, der datoen for den andre forsendelsen er forskjøvet med en uke fra den første.  
9. Angi et tall som er en del av det totale antallet, i Antall-feltet.
10. Klikk på Ny.
11. Angi restantallet i Antall-feltet.
12. Angi en dato som er én uke fremover fra datoen for den første leveringslinjen, i feltet Ønsket forsendelsesdato.
    * De to alternativene i hurtigfanen Gebyrkonvertering styrer hvordan du vil at tilleggene skal fordeles over leveringsplanlinjene, når de er tilordnet til den opprinnelige ordrelinjen. Hvis du velger Kopier bruttobeløp, kopieres det samme beløpet til hver linje. Alternativet Tildel til leveringslinjer deler tillegget likt på tvers av leveringslinjene.  
    * Bare faste gebyrer kan deles, mens variable kostnader fortsatt blir kopiert til linjene.  
13. Flytt markøren bort fra den andre leveringslinjen for å oppdatere siden.
    * Du kan holde oversikt over det totale antallet som er tildelt til leveringsplanlinjene, ved å se på feltene Total og Gjenværende. Når det gjenstående antallet er null, er det fullstendige antallet fra den opprinnelige linjen tildelt til tidsplanen.   
14. Klikk på OK.
    * Leveringsplanen er nå kopiert til ordrelinjene.   
    * Den opprinnelige ordrelinjen, kalt en kommersiell linje, er konvertert til en ordrelinje med flere leveringer. Den er merket med et eget ikon og fungerer som et hode for leveringslinjene.  
    * De to nye linjene, referert til som leveringslinjer, utgjør en leveringsplan. Ordren behandles mot disse linjene og ikke den opprinnelige linjen. Hvis dokumenter, for eksempel plukklister, følgesedler eller fakturaer, skrives ut, vises bare leveringslinjene.   
    * Leveringslinjene kan ha andre leveringsdatoer, antall, leveringsmåter og lagerdimensjoner, for eksempel område og lager. Produktdimensjonene må imidlertid alltid samsvare med dem på den kommersielle linjen, og kan ikke endres.  
15. Angi et nummer i feltet Antall som er større enn det gjeldende nummeret.
16. Velg den kommersielle linjen for å se effekten av omberegningen av antall.
17. Klikk på Plukk og pakk i handlingsruten.
18. Klikk på Poster følgeseddel.
19. Utvid seksjonen Parametere.
20. Velg Alle i feltet Antall.
    * Legg merke til at følgeseddelen opprettes for de to leveringsplanlinjene og ikke den opprinnelige ordrelinjen.  
21. Velg Ja i feltet Skriv ut pakkseddel.
22. Klikk på OK.
23. Klikk på Ja.
24. Lukk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]