---
title: 'Definere delvis prosess for syklustelling for lokasjon '
description: Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen.
author: ShylaThompson
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcda301934c6ccc06f17ed8ae13c52754336d2ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830912"
---
# <a name="define-partial-location-cycle-counting-process"></a>Definere delvis prosess for syklustelling for lokasjon  

[!include [banner](../../includes/banner.md)]

Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen. Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid. Vanligvis utfører en lagersjef konfigurasjonsoppgavene. Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.


## <a name="create-a-cycle-counting-work-template"></a>Opprette en mal for syklustellingsarbeid
1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.
2. Velg "Syklustelling" i feltet Arbeidsordretype.
3. Klikk på Ny.
4. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
5. Merk den valgte raden i listen.
6. Angi en verdi i feltet Arbeidsmal.
7. Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.
8. Angi eller velg en verdi i feltet ID for arbeidsutvalg.
9. Angi et tall i Arbiesdprioritet-feltet.
10. Klikk på Lagre.
11. Klikk på Ny.
12. Merk den valgte raden i listen.
13. Velg Opptelling i Arbeidstype-feltet.
14. Angi eller velg en verdi i feltet Arbeidsklasse-ID.
15. Klikk på Lagre.
16. Klikk på Arbeidslinjeinndelinger.
17. Klikk på Ny.
18. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
19. Klikk på Lagre.
20. Lukk siden.
21. Lukk siden.

## <a name="create-a-cycle-counting-plan"></a>Opprette en syklustellingplan
1. Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.
2. Klikk på Ny.
3. Skriv inn en verdi i feltet ID for syklustellingsplan.
4. Skriv inn en verdi i Beskrivelse-feltet.
5. Angi et tall i feltet Største antall syklustellinger.
6. Angi eller velg en verdi i feltet Arbeidsmal.
7. Klikk på Ny.
8. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
9. Skriv inn en verdi i feltet Beskrivelse.
10. Klikk på Lagre.
11. Klikk på Definer produktspørring.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i Kriterier-feltet.
14. Klikk på OK.
15. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]