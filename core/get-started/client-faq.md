---
title: "Dynamics 365 for operasjoner klienten vanlige spørsmål"
description: "Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for operasjoner-klienten."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 2c99b2e1f7ddecb61be62832ca1a8d3ac1fd21a8
ms.lasthandoff: 03/31/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Dynamics 365 for operasjoner klienten vanlige spørsmål

Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for operasjoner-klienten.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Hvorfor er ikke symboler lastet inn når jeg bruker Dynamics 365 for operasjoner?
-----------------------------------------------------------------

Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte. Prøv denne fremgangsmåten for å løse dette problemet:

-   Hvis du opplever dette problemet i Internet Explorer, klikker du **verktøy**, og klikk deretter **alternativer for Internett**.  I dialogboksen Alternativer for Internett på den **personvern**, klikk **Egendefinert nivå**, og kontroller at det **nedlasting av skrifter** alternativet.
-   Hvis ikke, må du kanskje legge til Dynamics-365 for operasjoner området i listen over klarerte områder.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg beholde handlingsruten faner åpne hele tiden?
Vi planlegger å implementere denne funksjonen snart. Brukere kan deretter velge å holde fanene på handlingen ruter åpen hele tiden. Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Hvorfor vises ulike hurtigmenyer noen ganger når jeg rightclick?
Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny. Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**. Vi kan ikke bygge inn disse kommandoene i Dynamics-365 for operasjoner hurtigmenyer fordi av sikkerhetsgrunner lesere ikke tillater oss å få programmatisk tilgang til systemet utklippstavla.

Hvis du høyreklikker en feltetikett eller verdien for en skrivebeskyttet kontroll, vil du se Dynamics-365 for hurtigmenyen for operasjoner.

Hvis du vil gjøre tastaturet enklere, planlegger vi å implementere en hurtigtast i fremtiden som vil åpne Dynamics-365 for hurtigmenyen for operasjoner.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Hvor er funksjonen Vis detaljer i Dynamics 365 for operasjoner?
Alternativet **Vis detaljer** er tilgjengelig på ulike måter:

-   Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling. Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.
-   **Vis detaljer om** er også et alternativ på Dynamics 365 for hurtigmenyer for operasjoner. Hvis du vil ha mer informasjon om når Dynamics 365 for operasjoner hurtigmenyer vises når du høyreklikker, kan du se den forrige delen.



