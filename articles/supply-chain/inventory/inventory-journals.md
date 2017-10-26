---
title: Lagerjournaler
description: "Denne artikkelen beskriver hvordan du kan bruke lagerjournaler til å postere ulike typer transaksjoner for aktuell beholdning."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6dfb82acb5dafd365d878949b35d4fe6ff58793d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-journals"></a>Lagerjournaler

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Denne artikkelen beskriver hvordan du kan bruke lagerjournaler til å postere ulike typer transaksjoner for aktuell beholdning.

Lagerjournaler i Microsoft Dynamics 365 for Finance and Operations brukes til å postere fysiske lagertransaksjoner av forskjellige typer, for eksempel postering av avganger og mottak, lagerbevegelser, oppretting av stykklister og avstemmingen av fysisk lager. Alle disse lagerjournalene brukes på lignende måte, men de er delt inn i forskjellige typer.

## <a name="types-of-inventory-journals"></a>Typer lagerjournaler
Følgende typer lagerjournaler er tilgjengelige:

-   Bevegelse
-   Lagerjustering
-   Overføring
-   Stykkliste
-   Vareankomst
-   Produksjonsinnlevering
-   Opptelling
-   Brikkeopptelling

### <a name="movement"></a>Bevegelse

Når du bruker varetilgangsjournal, kan du legge kostnaden til en vare når du legger til lager, men du må tildele tilleggskostnader manuelt til en bestemt finanskonto ved å angi en motkonto i økonomimodulen når du oppretter journalen. Denne lagerjournaltypen er nyttig hvis du vil utgiftsføre en vare mot en annen avdeling, eller hvis du vil fjerne varer fra lager for utgiftsformål.

### <a name="inventory-adjustment"></a>Lagerjustering

Når du bruker en lagerjusteringsjournal, kan du legge kostnaden til en vare når du legger til lager. De ekstra kostnadene posteres automatisk til en bestemt finanskonto basert på oppsettet av posteringsprofilen for varegruppen. Bruk denne lagerjournaltypen til å oppdatere fortjeneste og tap til lagerantallet når varen bør beholde motkontoen sin for økonomimodulen. Når du posterer en lagerjusteringsjournal, blir det postert et lagermottak eller en lageravgang, lagerverdiene endres, og finanstransaksjoner opprettes.

### <a name="transfer"></a>Overføring

Du kan bruke overføringsjournaler for å overføre varer mellom lokasjoner for lagring, partier eller produktvarianter uten å knytte til kostnadsimplikasjoner. Du kan for eksempel overføre varer fra ett lager til et annet lager i det samme firmaet. Når du bruker en overføringsjournal, må du angi både "fra"- og "til"- lagerdimensjoner (for eksempel for Område og Lager). Lagerbeholdningen for de definerte lagerdimensjonene endres i henhold til dette. Lageroverføringer gjenspeiler den umiddelbare flyttingen av materiale. Lager i transitt spores ikke. Hvis transittlageret må spores, bør du bruke en overføringsordre. Når du posterer en overføringsjournal, opprettes det to lagertransaksjoner for hver journallinje:

-   En lageravgang på "fra"-lokasjonen
-   Et lagermottak på "til"-lokasjonen

### <a name="bom"></a>Stykkliste

Når du rapporterer en stykkliste som avsluttet, kan du opprette en stykklistejournal. Når du bruker en stykklistejournal, kan du postere stykklisten direkte. Denne posteringen genererer et lagermottak for produktet sammen med en tilknyttet stykkliste og en lageravgang for produktene som er inkludert i stykklisten. Denne lagerjournaltypen er nyttig i enkle produksjonsscenarioer eller produksjonsscenarioer med høyt volum der ruter er ikke nødvendig.

### <a name="item-arrival"></a>Vareankomst

Du kan bruke vareankomstjournalen til å registrere mottak av varer (for eksempel fra bestillinger). En vareankomstjournal kan opprettes som en del av ankomstbehandlingen fra siden **Ankomstoversikt**, eller du kan manuelt opprette en journaloppføring fra siden **Vareankomst**. Hvis du aktiverer journalnavn for vareankomst for å kontrollere plukklokasjoner, søker Finance and Operations etter et sted for mottatte varer og, hvis det er plass, genererer lokasjonsmål for innkommende varer.

### <a name="production-input"></a>Produksjonsinnlevering

Produksjonsinnleveringsjournalene fungerer som vareankomstjournalene, men brukes for produksjonsordrer.

### <a name="counting"></a>Opptelling

Opptellingsjournaler lar deg rette den gjeldende lagerbeholdningen som er registrert for varer eller varegrupper, og posterer deretter den faktiske fysiske opptellingen slik at du kan foreta justeringene som kreves for å avstemme forskjeller. Du kan knytte opptellingspolicyer med opptellingsgrupper for å gruppere varer med ulike egenskaper, slik at disse elementene kan inkluderes i en opptellingsjournal. Du kan for eksempel angi opptellingsgrupper for å telle varer som har en bestemt frekvens, eller telle varer når beholdningen faller til et bestemt nivå. Hvis du vil ha informasjon om hvordan du definerer opptellingsgrupper, se [Definere prosesser for lageropptelling (oppgaveveiledning)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Brikkeopptelling

Brikkeopptellingsjournaler brukes til å tilordne en nummerert kode til et opptellingsparti. Koden bør inneholde et brikkenummer, varenummer og vareantall. For å garantere at en brikke brukes bare én gang, og at alle koder brukes, bør hvert varenummer ha et unikt sett med koder som har sin egen nummerserie. Tre statusverdier kan angis for hver enkelt kode:

-   **Brukt** – Varenummeret telles for denne brikken.
-   **Annullert** – Varenummeret annulleres for denne brikken.
-   **Mangler** – Varenummeret mangler for denne brikken.

Når du posterer en brikkeopptellingsjournal, opprettes en ny opptellingsjournal basert på linjene i brikkeopptellingsjournalen. Hvis du vil ha mer informasjon om brikkeopptelling, se [Lagerbrikkeopptelling](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Arbeide med journaler
En journallinje er bare tilgjengelig for én bruker av gangen. Hvis flere brukere må ha tilgang til journalene samtidig for å opprette journallinjer, må disse brukerne velge journaler som for tiden ikke brukes, for å hindre at informasjonen overskrives. I situasjoner der flere avdelinger bruker samme journaltypen, er det nyttig å opprette flere journalnavn (for eksempel én per avdeling). Det kan også være nyttig å dele journaler slik at hver posteringsrutine angis i sin egen unike lagerjournal. For posteringsrutiner som er tilknyttet lagertransaksjoner, oppretter du én journal for periodiske lagerjusteringer og en annen for lagertelling.

## <a name="posting-journal-lines"></a>Posteringsjournallinjer
Du kan postere journallinjene du oppretter, når som helst før du låser en vare fra flere transaksjoner. Dataene du angir i en journal, forblir i journalen, selv om du lukker journalen uten å postere linjene.

