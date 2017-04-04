---
title: "Navigasjonssøk"
description: "Denne artikkelen forklarer hvordan du bruker søkefunksjonen til å navigere til sidene i Microsoft Dynamics 365 for operasjoner."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Navigasjonssøk

Denne artikkelen forklarer hvordan du bruker søkefunksjonen til å navigere til sidene i Microsoft Dynamics 365 for operasjoner.

Dynamics 365 for operasjoner gir funksjonalitet for en rekke bransjer og vertikaler. Programmet inneholder en rekke områder og sider for å utføre forskjellige oppgaver. Du kan raskt finne sider som du trenger for å fullføre oppgavene, kan du bruke søkefunksjonen navigasjon. Du bruker denne funksjonen ved å klikke **Søk**-ikonet for å vise **Søk**-boksen. Du kan deretter skrive inn ett eller flere ord i boksen. Systemet søker umiddelbart etter relevante sider i programmet som svarer til ordene du skrev inn. Du kan for eksempel skrive inn «leverandørfaktura», og deretter vises resultater som samsvarer med dette søkeordet. **Obs! ** **Søk**-boksen gjør det enklere å finne og gå til sider. Du kan ikke bruke den til å finne bestemte data eller handlinger. 

[![Søk-boksen](./media/search-box.png)](./media/search-box.png) navigasjon Søk-funksjonen fungerer også som en flott måte å navigere raskt til en bestemt side. For eksempel hvis du er en leverandør clerk som ofte bruker den **betalingsjournal** siden, kan du angi "betalingsjournalen" i søkeboksen. Fordi inndataene er et nøyaktig samsvar for sidetittelen, siden er oppført øverst i søkeresultatene, og du kan raskt navigere til den. 

[![Søk-for-betaling-journal](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Listen over søkeresultater viser tittelen på siden, i tillegg til navigasjon-banen. Dette er med på å gjøre deg oppmerksom på hvor siden er i programmet. Det gjør det også enklere å skille mellom to eller flere lignende sider i resultatene. Når du søker etter en side, sammenlignes inndataene med sidetittelen og navigasjonsbanen. Hvis du angir "kunder" i for eksempel den ** ** søkeboksen, vil du se resultater for sider som er tilgjengelige i kundesamlekontoen området – selv om sidetitlene som ikke inneholder ordet "kunder". 

[![Søk-for-the-word-kunder](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Navigasjonen søke funksjonaliteten er bare aktuell fra en administrasjon og sikkerhet perspektiv:

-   Sider som er aktivert i den gjeldende konfigurasjonen (via konfigurasjonsnøkler).
-   Sider som brukeren har tilgang til basert på brukerens rolle.

Listen over søkeresultater er begrenset til ti elementer. Hvis du ikke finner det du leter etter, i resultatene, kan du prøve søkeord som innskrenker søket. Fra et utviklingsperspektiv er navigasjonssøkefunksjonaliteten svært enkel å bruke siden det praktisk talt er ingen forsinkelse mellom distribusjonen av menyelementer og visningen av dem i søkeresultatene. Så lenge det kobles til menyelementene fra navigasjonsruten eller instrumentbordet, blir de søkbare automatisk. Navigasjonssøkefunksjonaliteten inneholder også en etterlengtet funksjon blant privilegerte brukere: muligheten til å navigere raskt til en side basert på det tekniske skjemanavnet. Mange brukere er så kjent med systemet at de vet de nøyaktige skjemanavnene de arbeider med. Hvis du er en av disse brukerne, kan du skrive inn **skjema:** etterfulgt av navnet på skjemaet du leter etter. Hvis du for eksempel skriver inn **skjema: vendinvoice**, viser søkeresultatene alle sider der skjemanavnet begynner med **vendinvoice**. 

[![Søk for skjemaet vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


