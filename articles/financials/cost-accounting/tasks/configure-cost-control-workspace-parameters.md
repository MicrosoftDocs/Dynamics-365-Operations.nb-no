--- 
title: "Konfigurere parametere for arbeidsområde for kostnadskontroll"
description: "Bruk denne fremgangsmåten til å konfigurere kostnadskontrollarbeidsområdet slik at ledere på ulike nivåer i en organisasjon kan få innsikt i sin kostobjekter, for eksempel kostsentre og produktgrupper."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8ede40951d08e159358b713fc3dde46576a1b4e3
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="configure-cost-control-workspace-parameters"></a>Konfigurere parametere for arbeidsområde for kostnadskontroll

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten til å konfigurere kostnadskontrollarbeidsområdet slik at ledere på ulike nivåer i en organisasjon kan få innsikt i sin kostobjekter, for eksempel kostsentre og produktgrupper. USP2-demofirmaet ble brukt til å opprette denne registreringen.

1. Gå til Kostnadsregnskap > Oppsett > Konfigurasjon av arbeidsområde for kostnadskontroll.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg Ja i feltet Publisert.
    * Hvis du setter dette alternativet til Ja, kan brukere som er tilordnet én av disse rollene se rapporten i kostnadskontrollarbeidsområdet: kostnadsregnskapsleder, regnskapsfører, regnskapsførerfunsksjonær eller kostnadsobjektkontroller. Hvis du setter dette alternativet til Nei, kan bare brukere som er tilordnet én av disse rollene se rapporten i kostnadskontrollarbeidsområdet: kostnadsregnskapsleder, regnskapsfører, eller regnskapsførerfunsksjonær.  
6. Utvid delen Datafiltrering.
7. Angi eller velg en verdi i feltet Kostnadskontrollenhet
8. Angi eller velg en verdi i feltet Opprinnelig budsjettversjon.
9. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.
10. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.
11. Utvid delen Tilordne beregningsposter.
12. Klikk Ny.
13. Merk den valgte raden i listen.
14. Angi eller velg en verdi i feltet Regnskapskalenderperiode.
15. Angi eller velg en verdi i feltet Faktisk versjon.
16. Utvid delen Regnskapsperioder per kolonne.
17. Velg Ja i feltet Gjeldende periode.
18. Utvid delen Kolonner som skal vises for kostnader.
19. Velg Ja i feltet Fast kostnad.
20. Velg Ja i feltet Variabel kostnad.
21. Velg Ja i feltet Total kostnad.
22. Klikk Lagre.
23. Lukk siden.
24. Gå til Kostnadsregnskap > Arbeidsområder > Kostnadskontroll.
25. Velg en oppgave for å se faste, variable, totale og uklassifiserte kostnader for de valgte regnskapsperiodene.
26. Angi eller velg en verdi i feltet Regnskapskalenderperiode.
27. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Når du har valgt et dimensjonshierarki for kostnadsobjektet, utvid dimensjonshierarkiet for kostnadselementer for å vise de ønskede kostnadsverdier. Du kan for eksempel utvide hierarkiet til indirekte produksjonskostnader hvis du vil vise verdien.  


