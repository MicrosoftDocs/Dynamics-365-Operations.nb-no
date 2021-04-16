---
title: Definere en profil for vareankomstoversikt
description: Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt.
author: ShylaThompson
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0394d1b4288dac0ff913b125017571a8c0bc95a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829842"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Definere en profil for vareankomstoversikt

[!include [banner](../../includes/banner.md)]]

Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt. Profil for ankomstoversikt er en samling av regler som skal brukes når en bruker åpner en side for ankomstoversikt. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne fremgangsmåten utføres vanligvis av en mottaksassistent.

1. I navigasjonsruten går du til **Moduler > Beholdningsstyring > Oppsett > Distribusjon > Profiler for ankomstoversikt**.
2. Velg **Ny**. Fordi du nesten alltid vil arbeide i det samme lageret med å laste ut fulle vognlass, bør du opprette en profil for ankomstoversikt for å forenkle prosessen med å registrere mottatte varer.  
3. I feltet **Profilnavn for ankomstoversikt** skriver du inn en verdi.
4. Velg et alternativ i feltet **Vis linjer**. Velg hvilke linjer som skal vises for mottaket:  

    - **Alle** – Vis alle linjer uansett status.   
    - **Pågår** – Vis linjer for mottak der fremdriften er fullstendig eller delvis. Dette betyr at for hver linje er enten hele antallet eller et delantall registrert i en ankomstjournal.   
    - **Ikke fullstendig** – Vis linjer for mottak der fremdriften er ingen eller delvis. Dette betyr at for hver linje er enten ingen eller bare en del av antallet registrert i en ankomstjournal.  

5. Vis eller skjul delen **Ankomstalternativer**.
6. Skriv inn en verdi i feltet **Dager fremover**. Dette angir et filter som viser mottakslinjene som forventes å mottas i løpet av de neste dagene (avhengig av tallet du angir).  
7. Skriv inn en verdi i feltet **Dager bakover**. Dette angir et filter som viser linjene som forventes å mottas et antall dager før dagens dato.  
8. Skriv inn en verdi i feltet **Lagre**. Filtrere på ett eller flere lagre.  
9. Velg en verdi i **Leveringsmåte**-feltet. Dette angir et filter for å vise bare mottakslinjene med denne leveringsmåten.  
10. Velg WHS i **Navn**-feltet.
11. Velg lager 24 i **Lager**-feltet. Dette er standardlageret som skal brukes for registrerte mottakslinjer som bruker denne profilen.  
12. Velg **Rampedør** i **Lokasjon**-feltet. Dette er standardlokasjonen som skal brukes for registrerte mottakslinjer som bruker denne profilen.  
13. Vis eller skjul delen **Detaljer om spørring etter ankomst**.
14. Velg område 2 i feltet **Begrens til område**. Dette angir et filter for å vise bare mottakslinjene med dette området.  
15. Sett alternativet **Bestillinger** til **Ja**. Velg mottakslinjer fra bestillinger.  
16. Sett alternativet **Overføringsordrer** til **Ja**. Velg mottakslinjer fra overføringsordrer.  
17. Velg **Lagre**.
18. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]