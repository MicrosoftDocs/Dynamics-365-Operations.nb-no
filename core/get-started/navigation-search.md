---
title: "Navigasjonssøk"
description: "Denne artikkelen forklarer hvordan du bruker søkefunksjonen til å navigere til sider i Microsoft Dynamics 365 for Operations."
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

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan du bruker søkefunksjonen til å navigere til sider i Microsoft Dynamics 365 for Operations.

Dynamics 365 for Operations inneholder funksjonalitet for en lang rekke bransjer og vertikaler. Programmet inneholder en rekke områder og sider for å utføre forskjellige oppgaver. Du kan raskt finne sider som du trenger for å fullføre oppgavene, kan du bruke søkefunksjonen navigasjon. Du bruker denne funksjonen ved å klikke **Søk**-ikonet for å vise **Søk**-boksen. Du kan deretter skrive inn ett eller flere ord i boksen. Systemet søker umiddelbart etter relevante sider i programmet som svarer til ordene du skrev inn. Du kan for eksempel skrive inn «leverandørfaktura», og deretter vises resultater som samsvarer med dette søkeordet. **Obs! ** **Søk**-boksen gjør det enklere å finne og gå til sider. Du kan ikke bruke den til å finne bestemte data eller handlinger. 

[![søkeboks](./media/search-box.png)](./media/search-box.png) Navigasjonssøkefunksjonen er også flott å bruke til å navigere raskt til en bestemt side. For eksempel hvis du er en leverandør clerk som ofte bruker siden **Betalingsjournal**, kan du angi "betalingsjournal" i søkeboksen. Fordi inndataene er et nøyaktig samsvar for sidetittelen, er siden oppført øverst i søkeresultatene, og du kan raskt navigere til den. 

[![søke-etter-betalingsjournal](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Søkeresultatlisten inneholder sidetittelen og navigasjonsbanen. Dette er med på å gjøre deg oppmerksom på hvor siden er i programmet. Det gjør det også enklere å skille mellom to eller flere lignende sider i resultatene. Når du søker etter en side, sammenlignes inndataene med sidetittelen og navigasjonsbanen. Hvis du for eksempel skriver inn «kunde» i** **søkeboksen, får du resultatene for sidene som er tilgjengelige i Kunde-området, selv om sidetitlene ikke inneholder ordet «kunde». 

[![søke-etter-ordet-kunde](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Sett fra et administrasjons- og sikkerhetsperspektiv viser navigasjonssøkefunksjonaliteten bare følgende:

-   Sider som er aktivert i den gjeldende konfigurasjonen (via konfigurasjonsnøkler).
-   Sider som brukeren har tilgang til basert på brukerens rolle.

Listen over søkeresultater er begrenset til ti elementer. Hvis du ikke finner det du leter etter, i resultatene, kan du prøve søkeord som innskrenker søket. Fra et utviklingsperspektiv er navigasjonssøkefunksjonaliteten svært enkel å bruke siden det praktisk talt er ingen forsinkelse mellom distribusjonen av menyelementer og visningen av dem i søkeresultatene. Så lenge det kobles til menyelementene fra navigasjonsruten eller instrumentbordet, blir de søkbare automatisk. Navigasjonssøkefunksjonaliteten inneholder også en etterlengtet funksjon blant privilegerte brukere: muligheten til å navigere raskt til en side basert på det tekniske skjemanavnet. Mange brukere er så kjent med systemet at de vet de nøyaktige skjemanavnene de arbeider med. Hvis du er en av disse brukerne, kan du skrive inn **skjema:** etterfulgt av navnet på skjemaet du leter etter. Hvis du for eksempel skriver inn **skjema: vendinvoice**, viser søkeresultatene alle sider der skjemanavnet begynner med **vendinvoice**. 

[![search-for-form-vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)




