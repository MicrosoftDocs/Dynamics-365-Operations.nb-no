---
title: Flytting av beholdning med tilknyttet arbeid i Lagerstyring
description: Dette emnet beskriver hvordan du definerer og bruker stykkplukkingsbekreftelse fra en mobilenhet.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: d2db0431a3f749cbdaf35cc5108851f1e116bc96
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Flytting av beholdning med tilknyttet arbeid i Lagerstyring
<a id="movement-of-inventory-with-associated-work-in-warehouse-management" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Ved hjelp av flytting av beholdning kan du bestemme hvilke lagermedarbeidere som har tillatelse til å flytte reservert beholdning. Dette gir en fleksibilitet i regulerte lagre der du kan velge å ikke la en arbeider velge en ny plukklokasjon for plukkarbeid som allerede er opprettet. Det kan også la en lagersjef styre hvilke funksjoner noen mindre erfarne arbeidere skal ha.

Fleksibilitet til å administrere lagerarbeidernes daglige oppgaver kan være nyttig i scenarier som disse:

## Scenario 1
<a id="scenario-1" class="xliff"></a>
Et firma har et relativt lite mottaksområde, og det er overbelastet med paller og esker som venter på å bli plassert. Det forventes en stor forsendelse samme dag, så mottaksassistenten bestemmer seg for å rydde opp mottaksområdet ved å flytte noen av pallene til et sekundært innkommende oppsamlingsområde.

## Scenario 2
<a id="scenario-2" class="xliff"></a>
En erfaren lagermedarbeider ser en salgsmulighet i et lager til å konsolidere varer på ett sted i stedet for å holde dem fordelt over 3 i lokasjoner nær hverandre med lite antall på hver. Arbeideren ønsker å konsolidere antallet ved å flytte varer fra hver av disse lokasjonen til den samme lokasjonen og på det samme nummerskiltet.

## Scenario 3
<a id="scenario-3" class="xliff"></a>
En pall som venter på forsendelse på en oppsamlingslokasjon, for eksempel STADIUM01, som er nær RAMPEDØR01. På grunn av en endring i planene er imidlertid trucken satt til å ankomme RAMPEDØR04. Forsendelsesassistenten er klar over dette, og må være forsikre seg om at trucken ikke må vente på å bli lastet fra STADIUM01. Forsendelsesassistenten bestemmer seg for å flytte varene i den forsendelsen fra STADIUM01 til STADIUM04, som er nærmere til den nye plasseringen.

### Gjeldende begrensninger
<a id="current-limitations" class="xliff"></a>

Arbeidsreservasjonene som du kan flytte, er begrenset til ordre, avgang for overføringsordre, mottak for overføringsordre, bestillinge og etterfyllingsarbeid.

Flytting av varer er begrenset for å forhindre deling av arbeidslinjer. Dette betyr at hvis du har en arbeidslinje for 100 stk. av vare A fra lokasjon Lok1, kan du ikke flytte bare 30 stk. av vare A derfra til et annet sted. Dette vil føre til en deling av den eksisternde arbeidslinjen til 30 og 70 fordi lokasjonene nå er forskjellige.

For oppsamlingsscenarier, der nummerskiltet du flytter varene fra eller nummerskiltet du flytter varene til, er angit som målnummerkilt for en arbeidsordre, er bare flytting av hele nummerskiltet tillatt, for å unngå å dele opp målnummerskiltet.
For tiden støttes bare ad hoc-bevegelser. Det betyr at du ikke vil kunne flytte reservert beholdning gjennom menyelementet Flytting etter mal i mobilenheten.

### Definere tillatelse til å flytte reservert beholdning for individuelle arbeidere
<a id="set-up-the-permission-to-move-reserved-inventory-for-individual-workers" class="xliff"></a>

For arbeideren som skal ha tillatelse til å flytte reservert beholdning, merker du av for **Tillat flytting av beholdning med tilknyttet arbeid** under **Lagerstyring** > **Oppsett** > **Arbeider**.  

### Tilbakeføring
<a id="backported" class="xliff"></a>

Denne funksjonen er også tilbakeført til Microsoft Dynamics AX 2012 R3 og er tilgjengelig som en del av CU12.
Den kan også lastes ned alene gjennom KB-nummer 3192548. 


