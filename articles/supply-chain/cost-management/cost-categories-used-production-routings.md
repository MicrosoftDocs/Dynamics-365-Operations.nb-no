---
title: Kostnadskategorier som brukes i produksjonsruting
description: "Denne artikkelen inneholder informasjon om kostnadskategorier som brukes i produksjonsmiljøer som bruker ruting."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 53e038183a10b8732a9a5e0f25aac440c224400e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="cost-categories-used-in-production-routing"></a>Kostnadskategorier som brukes i produksjonsruting

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om kostnadskategorier som brukes i produksjonsmiljøer som bruker ruting.

Kostnadskategorier gjelder for produksjonsmiljøer som bruker ruting. De tilordnes til operasjonsressurser og rutingsoperasjoner for å definere timekostnader og segmentere kostnadsbidrag i de beregnede kostnadene for en produsert vare. Kostnadsgruppene som er tilordnet kostnadskategoriene, klassifiserer bidrag til produksjonskostnader basert på operasjonsressurser og typen aktivitet, for eksempel oppsettstid og kjøretid. Ved å spesifisere tilordninger for kostnadsgrupper kan administrasjonskostnader i produksjonen beregnes basert på rutingsinformasjon. 

**Obs!** I produksjonsmiljøer kalles kostnadskategorier for flere andre ting, som for eksempel arbeidssatskoder eller maskinsatskoder. 

Hver kostnadskategori har tilknyttede kostnadsposter, og har en tilordnet kostnadsgruppe. Forskjellige kostnadskategorier trengs for forskjellige formål i produksjonen.

-   Tilordne forskjellige timebaserte kostnader, avhengig av operasjonsressursen. Kostnadene kan for eksempel være forskjellig for forskjellige typer arbeidskompetanse, maskiner eller produksjonsceller.
-   Tilordne forskjellige timebaserte kostnader for oppsettid eller kjøretid som er knyttet til en ruteoperasjon.
-   Tilordne operasjonsressurskostnader basert på produsert antall i stedet for timebaserte kostnader, for eksempel stykkavlønning som betaling for arbeid.
-   Oppgi kostgruppesegmentering for kostnadsbidrag til en produsert vares beregnede kostnad. Du kan for eksempel segmentere kostnader for arbeid og maskiner.
-   Danne grunnlaget for kostnadsgrupper som brukes i beregningsformler, for eksempel formler for arbeidsrelaterte og maskinrelaterte administrasjonskostnader som står i forhold til oppsett- og kjøretid.

En kostnadskategori kan tilordnes til oppsettid, prosesstid og antall for en ruteoperasjon. Når kostnader eller kostnadsgruppesegmentering for eksempel er forskjellig for oppsett- og prosesstid, bør det defineres forskjellige kostnadskategorier som tilordnes til oppsett- og prosesstiden. Selektiv bruk av kostnadskategorier for oppsettid, prosesstid og antall bestemmes av rutegruppen som er tilordnet til en operasjon. Tilordningen av kostnadskategorier til tid og antall kan gjøres obligatorisk i henhold til policyer for hele firmaet, som er definert på siden **Parametere for produksjonskontroll**. 

Hver kostnadskategori har tilknyttede kostnader, som baseres på definisjonen av kostnadsposter i en etterkalkuleringsversjon. Bruk siden **Kostkategoripris** til å definere kostnadspostene for en angitt etterkalkuleringsversjon og et område. Når kostnadsposten for en kostnadskategori registreres for første gang, har den statusen **Venter** og en tiltenkt gyldighetsdato. Når du aktiverer kostnadsposten, oppdateres statusen til **Gjeldende aktiv**, og den effektive datoen oppdateres til aktiveringsdatoen. Forskjellige kostnadsposter kan gjenspeile forskjellige områder, ikrafttredelsesdatoer eller statuser. Stykklisteberegninger for en fremtidig eller historisk dato bruker kostnadspostene som har den aktuelle gyldighetsdatoen. Den gjeldende aktive kostnadsposten brukes til å estimere produksjonsordrekostnader og vurdere rapportert tid i forhold til en produksjonsordre. 

Kostprisposten for en kostnadskategori kan være områdespesfikk eler gjelde hele firmaet. Hvis du vil gjøre en kostnadspost områdespesifikk, kan du tilordne et område til den. Ellers indikerer en tom verdi at kostnadsposten gjelder for alle områder i firmaet. Siden kostnader kan være forskjellige fra område til område, må kostnadspostene defineres som områdespesifikke. 

En rutingsoperasjon arver generelt kostnadskategoriene som er tilordnet til operasjonsressursen eller hovedoperasjonen. Når en produksjonsordre opprettes, gjenspeiler rutingsoperasjonene i produksjonsruten den valgte ruteversjonen. Du kan overstyre kostnadskategoriene som er tilordnet til operasjonene i produksjonsruten. 

Enkelte typer produksjonsarbeid kan gjelde for prosjekttidsestimater og rapportering. I dette tilfellet kreves en kostnadskategori for produksjon og prosjekter. Du må definere mer prosjektrelatert informasjon når en kostnadskategori er flagget for bruk i prosjekter.




