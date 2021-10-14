---
title: Lagerjournaler
description: Dette emnet beskriver hvordan du kan bruke lagerjournaler til å postere ulike typer transaksjoner for aktuell beholdning.
author: yufeihuang
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9370e495bf16ed638646843faaf0ff599fe1abc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573975"
---
# <a name="inventory-journals"></a>Lagerjournaler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan bruke lagerjournaler til å postere ulike typer transaksjoner for aktuell beholdning.

Lagerjournaler i Supply Chain Management brukes til å postere fysiske lagertransaksjoner av forskjellige typer, for eksempel postering av avganger og mottak, lagerbevegelser, oppretting av stykklister og avstemmingen av fysisk lager. Alle disse lagerjournalene brukes på lignende måte, men de er delt inn i forskjellige typer.

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

Når du bruker varetilgangsjournal, kan du legge kostnaden til en vare når du legger til lager, men du må tildele tilleggskostnader manuelt til en bestemt finanskonto ved å angi en motkonto i økonomimodulen når du oppretter journalen. Denne lagerjournaltypen er nyttig hvis du vil overskrive standard bokføringskonti.

### <a name="inventory-adjustment"></a>Lagerjustering

Når du bruker en lagerjusteringsjournal, kan du legge kostnaden til en vare når du legger til lager. De ekstra kostnadene posteres automatisk til en bestemt finanskonto basert på oppsettet av posteringsprofilen for varegruppen. Bruk denne lagerjournaltypen til å oppdatere fortjeneste og tap til lagerantallet når varen bør beholde motkontoen sin for økonomimodulen. Når du posterer en lagerjusteringsjournal, blir det postert et lagermottak eller en lageravgang, lagerverdiene endres, og finanstransaksjoner opprettes.

### <a name="transfer"></a>Overføring

Du kan bruke overføringsjournaler for å overføre varer mellom lokasjoner for lagring, partier eller produktvarianter uten å knytte til kostnadsimplikasjoner. Du kan for eksempel overføre varer fra ett lager til et annet lager i det samme firmaet. Når du bruker en overføringsjournal, må du angi både "fra"- og "til"- lagerdimensjoner (for eksempel for Område og Lager). Lagerbeholdningen for de definerte lagerdimensjonene endres i henhold til dette. Lageroverføringer gjenspeiler den umiddelbare flyttingen av materiale. Lager i transitt spores ikke. Hvis transittlageret må spores, bør du bruke en overføringsordre. Når du posterer en overføringsjournal, opprettes det to lagertransaksjoner for hver journallinje:

-   En lageravgang på "fra"-lokasjonen.
-   Et lagermottak på "til"-lokasjonen.

### <a name="bom"></a>Stykkliste

Når du rapporterer en stykkliste som avsluttet, kan du opprette en stykklistejournal. Når du bruker en stykklistejournal, kan du postere stykklisten direkte. Denne posteringen genererer et lagermottak for produktet sammen med en tilknyttet stykkliste og en lageravgang for produktene som er inkludert i stykklisten. Denne lagerjournaltypen er nyttig i enkle produksjonsscenarioer eller produksjonsscenarioer med høyt volum der ruter er ikke nødvendig.

### <a name="item-arrival"></a>Vareankomst

Du kan bruke vareankomstjournalen til å registrere mottak av varer (for eksempel fra bestillinger). En vareankomstjournal kan opprettes som en del av ankomstbehandlingen fra siden **Ankomstoversikt**, eller du kan manuelt opprette en journaloppføring fra siden **Vareankomst**. Hvis du aktiverer journalnavn for vareankomst for å kontrollere plukklokasjoner, søker Supply Chain Management etter et sted for mottatte varer og, hvis det er plass, genererer lokasjonsmål for innkommende varer.

### <a name="production-input"></a>Produksjonsinnlevering

Produksjonsinnleveringsjournalene fungerer som vareankomstjournalene, men brukes for produksjonsordrer.

### <a name="counting"></a>Opptelling

Opptellingsjournaler lar deg rette den gjeldende lagerbeholdningen som er registrert for varer eller varegrupper, og posterer deretter den faktiske fysiske opptellingen slik at du kan foreta justeringene som kreves for å avstemme forskjeller. Du kan knytte opptellingspolicyer med opptellingsgrupper for å gruppere varer med ulike egenskaper, slik at disse elementene kan inkluderes i en opptellingsjournal. Du kan for eksempel angi opptellingsgrupper for å telle varer som har en bestemt frekvens, eller telle varer når beholdningen faller til et bestemt nivå. Hvis du vil ha informasjon om hvordan du definerer opptellingsgrupper, se [Definere prosesser for lageropptelling](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Brikkeopptelling

Brikkeopptellingsjournaler brukes til å tilordne en nummerert kode til et opptellingsparti. Koden bør inneholde et brikkenummer, varenummer og vareantall. For å sikre at en brikke brukes bare én gang, og at alle koder brukes, bør hvert varenummer ha et unikt sett med koder som har sin egen nummerserie. Tre statusverdier kan angis for hver enkelt kode:

-   **Brukt** – Varenummeret telles for denne brikken.
-   **Annullert** – Varenummeret annulleres for denne brikken.
-   **Mangler** – Varenummeret mangler for denne brikken.

Når du posterer en brikkeopptellingsjournal, opprettes en ny opptellingsjournal basert på linjene i brikkeopptellingsjournalen. Hvis du vil ha mer informasjon om brikkeopptelling, se [Lagerbrikkeopptelling](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Arbeide med journaler
En journallinje er bare tilgjengelig for én bruker av gangen. Hvis flere brukere må ha tilgang til journalene samtidig for å opprette journallinjer, må disse brukerne velge journaler som for tiden ikke brukes, for å hindre at informasjonen overskrives. I situasjoner der flere avdelinger bruker samme journaltypen, er det nyttig å opprette flere journalnavn (for eksempel én per avdeling). Det kan også være nyttig å dele journaler slik at hver posteringsrutine angis i sin egen unike lagerjournal. For posteringsrutiner som er tilknyttet lagertransaksjoner, oppretter du én journal for periodiske lagerjusteringer og en annen for lagertelling.

## <a name="posting-journal-lines"></a>Posteringsjournallinjer
Du kan postere journallinjene du oppretter, når som helst før du låser en vare fra flere transaksjoner. Dataene du angir i en journal, forblir i journalen, selv om du lukker journalen uten å postere linjene.

## <a name="data-entity-support-for-inventory-journals"></a>Dataenhetsstøtte for lagerjournaler

Dataenheter støtter følgende typer integrasjonsscenarioer:
-    Synkron tjeneste (OData)
-  Asynkron integrering

Hvis du vil ha mer informasjon, kan du se [Dataenheter](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).

> [!NOTE]
> Ikke alle lagerjournaler er OData-aktivert. Derfor kan du ikke bruke Excel-datakoblingen for å hente data som er publisert, oppdatert og importert tilbake til Supply Chain Management. 

En annen forskjell mellom journaldataenhetene er muligheten til å bruke sammensatte enheter som inneholder både hode- og linjedata. For øyeblikket kan du bruke de sammensatte enhetene for:
-   Lagerjusteringsjournal
-   Beholdningsbevegelsesjournal

Disse to lagerjournalene støtter bare *Initialiser lager*-scenarioet som en del av importprosjektet for databehandling:
-  Når et journalhodenummer ikke er angitt, men en nummerserie er angitt for journaltypen, oppretter automatisk importjobben journalhoder per 1000 linjer. Hvis du for eksempel importerer 2020 linjer, resulterer det i følgende tre journalhoder:
    -  Hode 1: inneholder 1000 linjer
    -  Hode 2: inneholder 1000 linjer
    -  Hode 3: inneholder 20 linjer
-  Det antas at det finnes unik linjeinformasjon per lagerdimensjon, som kan være en produkt-, lagrings- og sporingsdimensjon. Det er derfor ikke mulig å importere journallinjer der bare datofeltet er forskjellig på linjene i det samme importprosjektet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dataenheter](../../fin-ops-core/dev-itpro/data-entities/data-entities.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]