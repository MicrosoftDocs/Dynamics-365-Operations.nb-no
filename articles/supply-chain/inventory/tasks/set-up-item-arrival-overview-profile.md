---
title: Definere en profil for vareankomstoversikt
description: Denne oppgaven fokuserer på oppsettet for en profil for ankomstoversikt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "338021"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Definere en profil for vareankomstoversikt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven fokuserer på oppsettet for en profil for ankomstoversikt. Profil for ankomstoversikt er en samling av regler som skal brukes når en bruker åpner en side for ankomstoversikt. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne fremgangsmåten utføres vanligvis av en mottaksassistent.





1. Gå til Lagerstyring > Oppsett > Distribusjon > Profiler for ankomstoversikt.
2. Klikk Ny.
    * Fordi du nesten alltid vil arbeide i det samme lageret med å laste ut fulle vognlass, bør du opprette en profil for ankomstoversikt for å forenkle prosessen med å registrere mottatte varer.  
3. I feltet Profilnavn for ankomstoversikt skriver du inn en verdi.
4. Velg et alternativ i feltet Vis linjer.
    * Velg hvilke linjer som skal vises for mottaket: Alle – Vis alle linjer uansett status.   Pågår – Vis linjer for mottak der fremdriften er fullstendig eller delvis. Dette betyr at for hver linje er enten hele antallet eller et delantall registrert i en ankomstjournal.   Ikke fullstendig – Vis linjer for mottak der fremdriften er ingen eller delvis. Dette betyr at for hver linje er enten ingen eller bare en del av antallet registrert i en ankomstjournal.  
5. Vis eller skjul delen Ankomstalternativer.
6. Skriv inn en verdi i feltet Dager fremover.
    * Dette angir et filter som viser mottakslinjene som forventes å mottas i løpet av de neste dagene (avhengig av tallet du angir).  
7. Skriv inn en verdi i feltet Dager bakover.
    * Dette angir et filter som viser linjene som forventes å mottas et antall dager før dagens dato.  
8. Skriv inn en verdi i feltet Lagre.
    * Filtrere på ett eller flere lagre.  
9. Velg en verdi i Leveringsmåte-feltet.
    * Dette angir et filter for å vise bare mottakslinjene med denne leveringsmåten.  
10. Velg WHS i Navn-feltet.
11. Velg lager 24 i Lager-feltet.
    * Dette er standardlageret som skal brukes for registrerte mottakslinjer som bruker denne profilen.  
12. Velg Rampedør i Lokasjon-feltet.
    * Dette er standardlokasjonen som skal brukes for registrerte mottakslinjer som bruker denne profilen.  
13. Vis eller skjul delen Detaljer om spørring etter ankomst.
14. Velg område 2 i feltet Begrens til område.
    * Dette angir et filter for å vise bare mottakslinjene med dette området.  
15. Sett alternativet Bestillinger til Ja.
    * Velg mottakslinjer fra bestillinger.  
16. Sett alternativet Overføringsordrer til Ja.
    * Velg mottakslinjer fra overføringsordrer.  
17. Klikk Lagre.
18. Lukk siden.

