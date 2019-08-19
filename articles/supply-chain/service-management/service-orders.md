---
title: Serviceordrer
description: En serviceordre representerer et besøk av en servicetekniker hos en kunde på en bestemt dato.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d347556d25831bb3f9175e8606e0b41d98bdd8
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743261"
---
# <a name="service-orders"></a>Serviceordrer   

[!include [banner](../includes/banner.md)]


En serviceordre representerer et besøk av en servicetekniker hos en kunde på en bestemt dato. Hver serviceordre består av en eller flere serviceordrelinjer. Serviceordrelinjer representerer antall arbeidstimer som må utføres av serviceteknikere, og relaterte varer, utgifter og gebyrer.

Du kan knytte oppgaver og objekter til en serviceordrelinje. Du kan deretter gruppere serviceordrelinjer etter oppgaven eller objektet. Du kan også knytte varer som er oppgitt i lageret til serviceordrelinjene.

## <a name="create-service-orders"></a>Opprette serviceordrer

Du kan opprette serviceordrer basert på en serviceavtale og linjene som er inkludert i denne avtalen. Du kan imidlertid bare opprette serviceordrer som er knyttet til en serviceavtale i perioden som er angitt i avtalen. Hvis en serviceavtale er gyldig for 2011-kalenderåret, kan du for eksempel opprette serviceordrer for den avtalen fra 1. januar 2011, og 31. desember 2011.

Du kan også opprette serviceordrer enkeltvis, uten å knytte dem til en avtale. Disse serviceordrene kan brukes til å håndtere uplanlagte eller enkeltstående servicebesøk. I mars måned ønsker kunden din for eksempel at service skal utføres på to maskiner i tillegg til maskinene som er angitt i serviceavtalen. For denne aktiviteten du oppretter serviceordrer, men knytte ikke dem til en avtale.


> [!NOTE]
> <P>Hvis du vil opprette serviceordrer som ikke er knyttet til en serviceavtale, må du merke av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>.</P>

**Scenario**

Dette scenariet beskriver en annen situasjon der det er nyttig å opprette en serviceordre som ikke er knyttet til en serviceavtale.

Firmaets fordelingsansvarlig mottar en telefon med forespørsel om øyeblikkelig hjelp med en heis. Det er ikke tid til å opprette en serviceavtale og et prosjekt for servicen. Derfor fordelingsansvarlig oppretter en serviceordre direkte i **Serviceordrer**-skjemaet, knytter serviceordren til et eksisterende prosjekt, og oppretter serviceordrelinjene. Fordelingsansvarlig oppretter også en oppgave eller en objektrelasjon for en eksisterende serviceordre for å registrere arbeid som ikke er tilknyttet serviceavtalen. Hvis du vil ha mer informasjon, se [Opprette serviceordrer manuelt](create-service-orders-manually.md) og [Opprette serviceoppgaverelasjoner](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Overvåk fremdriften til serviceordren

Hvis du vil overvåke fremdriften til en salgsordre gjennom ulike grupper og arbeidsprosesser, kan du sette opp et system med stadier og årsakskoder for serviceordrer. For hvert stadium kan du angi handlingene som er tillatt. Hvis du vil ha mer informasjon, kan du se [Opprette årsakskoder](create-reason-codes.md).

**Eksempel**

En serviceordre godkjennes av fordelingsansvarlig. Fordelingsansvarlig oppdaterer stadiet til serviceordren og angir en årsakskode som indikerer at serviceordren er frigitt til serviceteknikeren. Serviceteknikeren reiser til kundens sted og utfører servicen.

## <a name="specify-item-requirements-for-service-orders"></a>Angi varebehov for serviceordrer

Du kan angi lagervarer som kreves for serviceordrer. Serviceordren må imidlertid være tilknyttet et prosjekt. Varebehov for serviceordrer behandles via et prosjekt. 

**Eksempel**

Serviceordrene som er opprettet fra serviceavtalen behandles av fordelingsansvarlig. For den første serviceordren oppdager fordelingsansvarlig at serviceteknikeren trenger en viktig reservedel som ikke finnes i lagerbeholdningen. Derfor oppretter fordelingsansvarlig et varebehov for reservedelen direkte fra serviceordren.

## <a name="move-and-post-lines"></a>Flytte og postere linjer

En servicetekniker kommer tilbake fra et servicebesøk og endrer deretter og oppdaterer serviceordrelinjene. I løpet av servicebesøket utførte teknikeren en servicejobb som var planlagt for det neste servicebesøket. Derfor flytter teknikeren linjene fra neste servicebesøk til gjeldende servicebesøk. Teknikeren posterer deretter serviceordren. Hvis du vil ha mer informasjon, se [Flytte serviceordrelinjer](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Annuller serviceordrer

En av de andre serviceordrene som ble generert for januar, foreldes fordi jobben blir annullert. Derfor annullerer servicefordelingsansvarlig serviceordren. Hvis du vil ha mer informasjon, se [Annullere serviceordrer](cancel-service-orders.md).

## <a name="post-from-projects"></a>Postere fra prosjekter

På slutten av hver uke vil fordelingsansvarlig postere alle serviceordrer som er tilknyttet et bestemt prosjekt. Derfor fordelingsansvarlig finner det relevante prosjektet i **Prosjekter**-skjemaet og posterer serviceordrene som er fullført. Hvis du vil ha mer informasjon, se [Postere serviceordrer (klasseskjema)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Slett serviceordrer

I løpet av årets andre halvdel bestemmer kunden seg for at servicebesøkene er for sjeldne. Du må opprette en ny serie med hyppigere servicebesøk for resten av tiden som gjenstår på serviceavtalen. Derfor må du slette de eksisterende serviceordrene og opprette nye serviceordrer. Hvis du vil ha mer informasjon, se [Slette serviceordrer](delete-service-orders.md).

## <a name="see-also"></a>Se også

[Serviceordrer (skjema)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  


