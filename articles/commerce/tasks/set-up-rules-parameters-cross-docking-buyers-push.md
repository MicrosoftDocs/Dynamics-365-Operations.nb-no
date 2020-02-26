---
title: " Definere regler og parametere for direkteoverføring og sentralt innkjøp"
description: Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecc3e1ce842e8d3b693b5e81ed665e9f3c00bfb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023525"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Definere regler og parametere for direkteoverføring og sentralt innkjøp

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler. Etterfyllingsregler kan brukes til å kontrollere hvordan produkter distribueres til butikkene når du bruker direkteoverføring og sentralt innkjøp. Etterfyllingsregler kan angis for butikker eller butikkgrupper. Vekten som er definert for hver linje i en regel, styrer hvordan antallene av produkter blir fordelt mellom butikkene når etterfyllingsregler brukes som distribusjonsmetode i direkteoverføring eller sentralt innkjøp. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Etterfyllingsregler.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Etterfyllingsregel.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Klikk Legg til.
7. Merk den valgte raden i listen.
    * Du kan velge Etterfyllingshierarki eller Kanal for typen. Verdien angir om valget i Navn blir et hierarki av kanaler eller en bestemt kanal.  La det for eksempel stå som Etterfyllingshierarki..  
8. Velg en verdi i Navn-feltet.
    * Standardvektverdien fylles ut fra vekten som er definert i lageret.  Vekten kan brukes til etterfyllingsregelen eller du kan angi en ny vekt i Vekt-feltet.  
9. Angi et tall i Vekt-feltet.
10. Klikk Legg til.
11. Merk den valgte raden i listen.
12. Velg Kanal i Type-feltet.
13. Angi eller velg en verdi i Navn-feltet.
14. Angi et tall i Vekt-feltet.
15. Klikk Lagre.

