---
title: "Navigasjonssøk"
description: "Dette emnet forklarer hvordan du bruker søkefunksjonen til å navigere til sider i Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: df804f79d6639c118e3e0534a21423f207ceb2c7
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="navigation-search"></a>Navigasjonssøk

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du bruker søkefunksjonen til å navigere til sider i Microsoft Dynamics 365 for Operations.

Dynamics 365 for Operations inneholder funksjonalitet for en lang rekke bransjer og vertikaler. Programmet inneholder en rekke områder og sider for å utføre forskjellige oppgaver. Du kan raskt finne sider som du trenger for å fullføre oppgavene, kan du bruke søkefunksjonen navigasjon. 

Du bruker denne funksjonen ved å klikke **Søk**-ikonet for å vise **Søk**-boksen. Du kan deretter skrive inn ett eller flere ord i boksen. Systemet søker umiddelbart etter relevante sider i programmet som svarer til ordene du skrev inn. Du kan for eksempel skrive inn «leverandørfaktura», og deretter vises resultater som samsvarer med dette søkeordet. 

**Obs!** **Søk**-boksen gjør det enklere å finne og gå til sider. Du kan ikke bruke den til å finne bestemte data eller handlinger. 

[![Søkeboks](media/navigation-search.png "Søkeboks") 

## <a name="quickly-navigate-to-a-particular-page"></a>Navigere raskt til en bestemt side
Navigasjonssøkefunksjonen er også flott å bruke til å navigere raskt til en bestemt side. Hvis du for eksempel er en leverandørassistent som ofte bruker siden **Betalingsjournal**, kan du angi "betalingsjournal" i **søkeboksen**. Fordi inndataene er et nøyaktig samsvar for sidetittelen, er siden oppført øverst i søkeresultatene, og du kan raskt navigere til den. 

Søkeresultatlisten inneholder sidetittelen og navigasjonsbanen. Dette viser plasseringen til siden i programmet. Det gjør det også enklere å skille mellom to eller flere lignende sider i resultatene. 

Når du søker etter en side, sammenlignes inndataene med sidetittelen og navigasjonsbanen. Hvis du for eksempel skriver inn "kunde" i **søkeboksen**, får du resultatene for sidene som er tilgjengelige i Kunde-området, selv om sidetitlene ikke inneholder ordet "kunde". 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Navigere raskt til en side basert på det tekniske skjemanavnet
Navigasjonssøkefunksjonaliteten inneholder også en etterlengtet funksjon blant privilegerte brukere: muligheten til å navigere raskt til en side basert på det tekniske skjemanavnet. Mange brukere er så kjent med systemet at de vet de nøyaktige skjemanavnene de arbeider med. Hvis du er en av disse brukerne, kan du skrive inn **skjema:** etterfulgt av navnet på skjemaet du leter etter. Hvis du for eksempel skriver inn **skjema: vendinvoice**, viser søkeresultatene alle sider der skjemanavnet begynner med **vendinvoice**. 

## <a name="administration-and-security"></a>Administrasjon og sikkerhet
Sett fra et administrasjons- og sikkerhetsperspektiv viser navigasjonssøkefunksjonaliteten bare to resultattyper:

-   Sider som er aktivert i den gjeldende konfigurasjonen (via konfigurasjonsnøkler).
-   Sider som brukeren har tilgang til basert på brukerens rolle.

Listen over søkeresultater er begrenset til ti elementer. Hvis du ikke finner det du leter etter, i resultatene, kan du prøve søkeord som innskrenker søket. 

## <a name="development"></a>Utvikling 
Fra et utviklingsperspektiv er navigasjonssøkefunksjonaliteten enkel å bruke siden det praktisk talt er ingen forsinkelse mellom distribusjonen av menyelementer og visningen av dem i søkeresultatene. Så lenge det kobles til menyelementene fra navigasjonsruten eller instrumentbordet, blir de søkbare automatisk. 

