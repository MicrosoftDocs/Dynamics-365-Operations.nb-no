---
title: Opprette varslingsregler
description: Dette emnet gir informasjon om varsler, og forklarer hvordan du oppretter en varslingsregel, slik at du får melding om hendelser, for eksempel en dato som kommer eller en bestemt endring som forekommer.
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549681"
---
# <a name="create-alert-rules"></a>Opprette varslingsregler

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Komme i gang

Før du oppretter en varslingsregel, må du vurdere når eller i hvilke situasjoner du vil motta varsler. Når du vet hvilke hendelser du vil varsles om, kan du finne siden i Microsoft Dynamics 365 for Finance and Operations der dataene som forårsaker den hendelsen, vises. Hendelsen kan være en dato som kommer, eller en bestemt endring som forekommer. Du må derfor finne siden der datoen er angitt, eller hvor feltet som endres eller den nye posten som opprettes, vises. Etter at du har denne informasjonen, kan du opprette varslingsregelen.

Når du oppretter en varslingsregel, kan du definere vilkår som må oppfylles før varselet utløses. Du kan se på kriterier som et samsvar mellom en hendelse og innfrielsen av bestemte betingelser. Når en hendelse forekommer, begynner systemet å utføre en kontroll i henhold til betingelsene som er definert i Finance and Operations.

## <a name="events"></a>Hendelser

Hendelsen som utløser en varslingsregel kan være en dato som kommer, eller en bestemt endring som forekommer. Utløser for hendelser som er definert i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**. Hendelsene som er tilgjengelige for et bestemt felt, avhenger av utløseren som er valgt.

Hvis du for eksempel definerer en varslingsregel for feltet **Startdato**, er forfallsdatohendelser velegnet. Derfor er hendelsestypen **forfaller om** tilgjengelig for det feltet. For et felt som for eksempel **Kostsenter**, er imidlertid ikke en forfallsdatohendelse velegnet. Derfor er hendelsestypen **forfaller om** ikke tilgjengelig. I stedet er hendelsestypen **er endret** tilgjengelig.

## <a name="event-types"></a>Hendelsestyper

Tre typer hendelser kan oppstå:

- **Hendelser av opprett-type og slett-type** – Disse hendelsene utløser et varsel når en post opprettes eller slettes.
- **Hendelser av oppdater-type** – Disse hendelsene utløser et varsel når data i et bestemt felt endres.
- **Hendelser av forfallsdatotype** – Disse hendelsene utløser et varsel når en dato kommer.
    
Endringer kan startes av en annen bruker. En bruker endrer for eksempel leveringsdatoen for en bestilling. Det kan også forekomme endringer som en del av en prosess. Feltet **Status** på en side endres for eksempel til å gjenspeile livssyklusen til forskjellige prosesser i systemet.

## <a name="conditions"></a>Betingelser

I hurtigfanen **Varsle meg for** i dialogboksen **Opprett varslingsregel** kan du bruke betingelser til å kontrollere når du varsles om hendelser.

Du kan for eksempel angi at systemet skal varsle deg om endringer når statusen for bestillinger endres, men bare hvis statusen samsvarer med et bestemt sett med betingelser. Mer spesifikt ønsker du å bli varslet når statusen for en bestilling er satt til **Mottatt**. Denne endringen i statusen er hendelsen som utløser varselet.

Deretter må du bestemme hvilke bestillinger du ønsker å bli varslet om. Du kan for eksempel velge ett av følgende alternativer. Disse alternativene definerer betingelsene for varslingsregelen.

- **Gjeldende valgte post** – Du mottar et varsel når statusen for en bestemt bestilling endres til **Mottatt**.
- **Alle poster** – Du mottar et varsel når statusen for en bestilling endres for en vare på den aktive siden. Du kan bruke den avanserte filtreringen som er tilgjengelig på siden for å opprette regler for et bestemt sett med poster. Du kan for eksempel opprette et varsel som utløses for alle bestillingene for kundene i en bestemt kundegruppe.
    
## <a name="expiry-of-rule"></a>Utløp av regel

I hurtigfanen **Varsle meg inntil** i dialogboksen **Opprett varslingsregel** kan du angi hvor lenge varslingsregelen skal være aktiv.

## <a name="alert-contents"></a>Varselinnhold

I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi emneteksten og meldingsteksten som varslingsmeldingene skal bruke.

## <a name="user-id"></a>Bruker-ID

I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi hvilken bruker som skal motta varslene. Bruker-IDen er valgt som standard. Dette alternativet er begrenset til administratorer for organisasjonen.

## <a name="create-an-alert-rule"></a>Opprett en varslingsregel

1. Åpne siden som inneholder dataene du vil overvåke.
2. Velg **Opprett varslingsregel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.
3. Velg feltet som skal overvåkes, i feltet **Felt** i dialogboksen **Opprett varslingsregel**.
4. Velg hendelsestypen i feltet **Hendelse**.
5. Velg et alternativ i hurtigfanen **Varsle meg i**.
6. Hvis varslingsregelen blir inaktiv på en bestemt dato, velger du en sluttdato i hurtigfanen **Varsle meg inntil**.
7. Godta standard emneoverskrift for e-postmeldingen eller skriv inn et nytt emne, i feltet **Emne** i hurtigfanen **Varsle meg med**. Teksten brukes som emneoverskrift for e-postmeldingen du mottar når det utløses et varsel.
8. Skriv inn en valgfri melding i feltet **Melding**. Teksten brukes som meldingen du mottar når det utløses et varsel.
9. Velg **OK** for å lagre innstillingene og opprette varslingsregelen.
