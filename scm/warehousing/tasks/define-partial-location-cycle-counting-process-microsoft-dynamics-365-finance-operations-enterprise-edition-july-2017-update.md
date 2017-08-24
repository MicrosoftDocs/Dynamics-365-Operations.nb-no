--- 
title: 'Definere delvis prosess for syklustelling for lokasjon '
description: "Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 507a1147fea62c12490291362d365224efeda97e
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="define-partial-location-cycle-counting-process"></a>Definere delvis prosess for syklustelling for lokasjon  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen. Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid. Vanligvis utfører en lagersjef konfigurasjonsoppgavene. Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.


## <a name="create-a-cycle-counting-work-template"></a>Opprette en mal for syklustellingsarbeid
1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.
2. Velg "Syklustelling" i feltet Arbeidsordretype.
3. Klikk Ny.
4. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
5. Merk den valgte raden i listen.
6. Angi en verdi i feltet Arbeidsmal.
7. Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.
8. Angi eller velg en verdi i feltet ID for arbeidsutvalg.
9. Angi et tall i Arbiesdprioritet-feltet.
10. Klikk Lagre.
11. Klikk Ny.
12. Merk den valgte raden i listen.
13. Velg Opptelling i Arbeidstype-feltet.
14. Angi eller velg en verdi i feltet Arbeidsklasse-ID.
15. Klikk Lagre.
16. Klikk Arbeidslinjeinndelinger.
17. Klikk Ny.
18. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
19. Klikk Lagre.
20. Lukk siden.
21. Lukk siden.

## <a name="create-a-cycle-counting-plan"></a>Opprette en syklustellingplan
1. Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for syklustellingsplan.
4. Skriv inn en verdi i Beskrivelse-feltet.
5. Angi et tall i feltet Største antall syklustellinger.
6. Angi eller velg en verdi i feltet Arbeidsmal.
7. Klikk Ny.
8. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
9. Skriv inn en verdi i feltet Beskrivelse.
10. Klikk Lagre.
11. Klikk Definer produktspørring.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i Kriterier-feltet.
14. Klikk OK.
15. Lukk siden.


