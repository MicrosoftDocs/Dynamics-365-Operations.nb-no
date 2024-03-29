---
title: Flytting av beholdning med tilknyttet arbeid i Lagerstyring
description: Ved hjelp av flytting av beholdning kan du bestemme hvilke lagermedarbeidere som har tillatelse til å flytte reservert beholdning.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736557"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Flytting av beholdning med tilknyttet arbeid i Lagerstyring

[!include [banner](../includes/banner.md)]

Ved hjelp av flytting av beholdning kan du bestemme hvilke lagermedarbeidere som har tillatelse til å flytte reservert beholdning. Dette gir en fleksibilitet i regulerte lagre der du kan velge å ikke la en arbeider velge en ny plukklokasjon for plukkarbeid som allerede er opprettet. Det kan også la en lagersjef styre hvilke funksjoner noen mindre erfarne arbeidere skal ha.

Fleksibilitet til å administrere lagerarbeidernes daglige oppgaver kan være nyttig i scenarier som disse:

## <a name="scenario-1"></a>Scenario 1

Et firma har et relativt lite mottaksområde, og det er overbelastet med paller og esker som venter på å bli plassert. Det forventes en stor forsendelse samme dag, så mottaksassistenten bestemmer seg for å rydde opp mottaksområdet ved å flytte noen av pallene til et sekundært innkommende oppsamlingsområde.

## <a name="scenario-2"></a>Scenario 2

En erfaren lagermedarbeider ser en salgsmulighet i et lager til å konsolidere varer på ett sted i stedet for å holde dem fordelt over tre lokasjoner nær hverandre med lite antall på hver. Arbeideren ønsker å konsolidere antallet ved å flytte varer fra hver av disse lokasjonen til den samme lokasjonen og på det samme nummerskiltet.

## <a name="scenario-3"></a>Scenario 3

En pall som venter på forsendelse på en oppsamlingslokasjon, for eksempel STADIUM01, som er nær RAMPEDØR01. På grunn av en endring i planene er imidlertid trucken satt til å ankomme RAMPEDØR04. Forsendelsesassistenten er klar over dette, og må være forsikre seg om at trucken ikke må vente på å bli lastet fra STADIUM01. Forsendelsesassistenten bestemmer seg for å flytte varene i den forsendelsen fra STADIUM01 til STADIUM04, som er nærmere til den nye plasseringen.

### <a name="current-limitations"></a>Gjeldende begrensninger

Arbeidsreservasjonene som du kan flytte, er begrenset til ordre, avgang for overføringsordre, mottak for overføringsordre, bestillinge og etterfyllingsarbeid.

Flytting av varer er begrenset for å forhindre deling av arbeidslinjer. Dette betyr at hvis du har en arbeidslinje for 100 stk. av vare A fra lokasjon Lok1, kan du ikke flytte bare 30 stk. av vare A derfra til et annet sted. Dette vil føre til en deling av den eksisternde arbeidslinjen til 30 og 70 fordi lokasjonene nå er forskjellige.

For oppsamlingsscenarier, der nummerskiltet du flytter varene fra eller nummerskiltet du flytter varene til, er angit som målnummerkilt for en arbeidsordre, er bare flytting av hele nummerskiltet tillatt, for å unngå å dele opp målnummerskiltet.

For tiden støttes bare ad hoc-bevegelser. Det betyr at du ikke vil kunne flytte reservert beholdning gjennom menyelementet Flytting etter mal i mobilenheten.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Konfigurer tillatelse til å flytte reservert inventar til enkelte arbeidstakere

For arbeideren som skal ha tillatelse til å flytte reservert beholdning, merker du av for **Tillat flytting av beholdning med tilknyttet arbeid** under **Lagerstyring \> Oppsett \> Arbeider**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
