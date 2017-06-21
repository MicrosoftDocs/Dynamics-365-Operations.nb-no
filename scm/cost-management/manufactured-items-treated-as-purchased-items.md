---
title: "Definere produkter som kan være produsert eller fremskaffet"
description: "Produkter kan ha forskjellige kildeinndelinger: de kan være produsert eller fremskaffet (kjøpt). Denne artikkelen beskriver noen vanlige poeng som må vurderes når du konfigurerer produkter som støtter flere leverandører."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4a2eb04a7cd788914aa461047e20b7b9cbad5e1
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Definere produkter som kan være produsert eller fremskaffet

[!include[banner](../includes/banner.md)]


Produkter kan ha forskjellige kildeinndelinger: de kan være produsert eller fremskaffet (kjøpt). Denne artikkelen beskriver noen vanlige poeng som må vurderes når du konfigurerer produkter som støtter flere leverandører. 

Flere leverandører brukes vanligvis for en kjøpt vare som noen ganger produseres, eller når en vare som primært er en produsert vare endres slik at det nå primært er en innkjøpt vare. Varen utpekes først som en produsert vare slik at stykkliste- og ruteinformasjon kan defineres, og for å støtte produksjonsordrer for varen. Produksjonstypen bør settes til **Stykkliste** (eller for prosessproduksjon, **Formel** eller **Koprodukt**).

Når du bruker standardkostnad, kan varekostnadsposten beregnes for den produserte varen. Varekostposten vil imidlertid ikke alltid stemme overens med standardkostprisen du ønsker å bruke til innkjøpsformål. I dette tilfellet må standardkostprisen registreres og aktiveres manuelt for varekostnadsposten. For kostnadsberegningen kan du vurdere å bruke en spesiell stykkliste og rute som representerer forsyningsblandingen av produktet i løpet av en regnskapsperiode, for å redusere avvikene over tid. I tillegg kan en produsert vare fra ett område overføres til et annet område. Derfor må varekostnaden manuelt registreres og aktiveres for området som varen blir overført til. Når du bruker den produserte varen som en komponent i produkter på et høyere nivå, bør komponentens kostnader behandles som en innkjøpt vare. Denne retningslinjen gjelder uansett om komponentens kostnader beregnes eller registreres manuelt. Det vil si at en stykklisteberegning bør beregne varens kostnad som om den var en innkjøpt komponent, i stedet for å beregne kostnader på grunnlag av varens stykkliste- og ruteinformasjon. Du kan hindre at slike beregninger utføres ved å velge flagget for **Stopp nedbryting**, som er innebygd i stykklisteberegningsgruppen som er tilordnet til varen. Du kan hindre at hovedplanleggingsberegninger bryter ned behov via varen ved å angi nedbrytingshorisonten til 0 dager i varedekning eller i dekningsgruppen. Hovedplanleggingsberegningen vil deretter behandle varen som en innkjøpt vare, og vil ikke utføre flere beregninger for varens stykkliste og ruteinformasjon.






