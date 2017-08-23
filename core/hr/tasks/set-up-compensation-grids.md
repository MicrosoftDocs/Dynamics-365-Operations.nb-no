--- 
title: Konfigurer kompensasjonsrutenett
description: "Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 33a95e4366dc352f28202155be7fc0b8f4c99e4a
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-compensation-grids"></a>Konfigurer kompensasjonsrutenett

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner. Kompensasjonsrutenett kan deles mellom flere planer eller kopieres når du oppretter en ny kompensasjonsplan.  Før du oppretter et kompensasjonsrutenett må nivåer og referansepunkt være definert. Dette eksemplet oppretter en ny klasse-type for kompensasjonsrutenettet ved hjelp av demodata for nivåene og referansepunktene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-information-about-the-compensation-grid"></a>Definere informasjon om kompensasjonsrutenettet
1. Gå til Personale > Kompensasjon > Fast kompensasjon > Kompensasjonsrutenett.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Rutenett.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg et alternativ i Type-feltet.
6. Angi eller velg en verdi i feltet Referanseoppsett.
7. Angi eller velg en verdi i feltet Valuta.
8. Skriv inn en verdi i Valuta-feltet.
9. Angi en dato i feltet Gyldighetsdato.

## <a name="add-levels-to-the-compensation-structure"></a>Legge til nivåer i kompensasjonsstrukturen
1. Klikk Kompensasjonsstruktur.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Nivå.
4. Klikk Ny.
5. Merk den valgte raden i listen.
6. Angi eller velg en verdi i feltet Nivå.
7. Klikk Ny.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet Nivå.
10. Klikk Ny.
11. Merk den valgte raden i listen.
12. Angi eller velg en verdi i feltet Nivå.
13. Klikk Ny.
14. Merk den valgte raden i listen.
15. Angi eller velg en verdi i feltet Nivå.

## <a name="fill-in-the-compensation-structure-with-values"></a>Fylle ut kompensasjonsstrukturen med verdier
1. Merk den valgte raden i listen.
    * Nå kan kompensasjonsverdiene settes inn manuelt i hvert felt i tabellen, eller masseendringsfunksjonaliteten kan brukes til å enkelt fylle ut flere felt og utføre enkle beregninger.  
2. Klikk Masseendring.
    * Vi vil først bruke verdien for midtpunktet i det første nivået for dette rutenettet på alle feltene i tabellen. Dette vil være grunnlaget for kompensasjonsmatrisen.  
3. Velg et alternativ i feltet Justeringstype.
4. Angi et tall i Justeringsbeløp-feltet.
5. Merk eller fjern merking for alle rader i listen.
6. Klikk Bruk på rutenett.
    * Nå skal vi bruke masseendringsfunksjonen til å øke beløpene i hvert etterfølgende nivå med en bestemt prosent eller beløp. I dette eksemplet skal hver klasse en 12,5 % spredning mellom midtpunktene.  
7. Velg et alternativ i feltet Justeringstype.
8. Angi et tall i Justeringsbeløp-feltet.
9. Finn og velg ønsket post i listen.
10. Finn og velg ønsket post i listen.
11. Finn og velg ønsket post i listen.
12. Finn og velg ønsket post i listen.
13. Klikk Bruk på rutenett.
14. Finn og velg ønsket post i listen.
15. Finn og velg ønsket post i listen.
16. Finn og velg ønsket post i listen.
17. Klikk Bruk på rutenett.
18. Finn og velg ønsket post i listen.
19. Finn og velg ønsket post i listen.
20. Klikk Bruk på rutenett.
21. Finn og velg ønsket post i listen.
22. Klikk Bruk på rutenett.
    * Nå skal vi bruke masseendringsfunksjonen til å justere Minimum og maksimum referansepunkt for hvert nivå. Dette eksemplet bruker en 50 % spredning slik Minimum referansepunkt blir justert -20 % og maksimalt blir justert +20 %.  
23. Angi et tall i Justeringsbeløp-feltet.
24. Angi eller velg en verdi i feltet Referansepunkt.
25. Merk eller fjern merking for alle rader i listen.
26. Klikk Bruk på rutenett.
27. Angi et tall i Justeringsbeløp-feltet.
28. Angi eller velg en verdi i feltet Referansepunkt.
29. Merk eller fjern merking for alle rader i listen.
30. Klikk Bruk på rutenett.


