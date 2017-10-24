--- 
title: " Opprette telefonsenterordrer"
description: "Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a> Opprette telefonsenterordrer

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT og er ment for selgere. Forhåndskrav: Brukeren som utfører prosedyren, er satt opp som telefonsenterbrukere og katalogen for Fabrikam annethvert år publiseres med minst én kildekode.

1. Gå til Detaljhandel og handel > Kunder > Kundestøtte.
2. Angi søkekriteriene for å slå opp kunden, i Søketekst-feltet.
    * I denne eksempelprosedyren skriver du inn Karin og trykker TAB.  
3. Klikk Søk.
    * Siden det bare finnes én kunde med navnet Karin i demonstrasjonsdataene, velges de automatisk.  
4. Klikk Ny salgsordre.
5. Vis eller skjul delen Salgsordrehode.
6. Velg kildekoden for katalogen.
    * Hvis det ikke finnes aktive kildekoder, kan du lukke Kilde-feltet og hoppe over dette trinnet.  
7. Klikk Legg til linje.
8. I Varenummer-feltet angir du varesøkeordet.
    * I denne eksempelprosedyren angir du et delvis varenummer, 8111, og trykker TAB. Søkevinduet vil dermed vises.  
9. Velg produktet som skal legges til salgsordren.
10. Angi salgsantallet.
11. Klikk Opprett.
12. Klikk Fullfør for å registrere kundebetalingen.
13. Klikk Legg til.
    * Koblingen Legg til er i Betalinger-fanen. Vis Betalinger-fanen hvis den er skjult.  
14. Velg betalingsmåten.
    * Velg kontantbetalingsmåten for denne prosedyren.  
15. Lukk siden.
16. Angi beløpet.
    * I denne prosedyren angir du et beløp som er likt ordresaldoen som vises på sammendragssiden for salgsordren til venstre i beløpsfeltet. Dermed kan du fullføre ordren som fullt betalt.  
17. Klikk OK.
18. Klikk Send.


