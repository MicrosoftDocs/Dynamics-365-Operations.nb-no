---
title: "Vanlige spørsmål om Dynamics 365 for Operations-klienten"
description: "Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Operations-klienten."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 94f5874cb24b53476843f1a073dc9c4cfdb36ac9
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Vanlige spørsmål om Dynamics 365 for Operations-klienten

[!include[banner](../includes/banner.md)]


Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Operations-klienten.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Hvorfor blir ikke symboler lastet inn når jeg bruker Dynamics 365 for Operations?
-----------------------------------------------------------------

Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte. Prøv denne fremgangsmåten for å løse dette problemet:

-   Hvis du opplever dette problemet i Internet Explorer, klikker du **Verktøy** og deretter **Alternativer for Internett**.  I dialogboksen Alternativer for Internett i kategorien **Personvern** klikker du **Egendefinert nivå** og kontrollerer at alternativet **Nedlasting av skrifter** er valgt.
-   Hvis ikke må du kanskje legge til nettstedet for Dynamics 365 for Operations i listen over klarerte områder.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg holde fanene i handlingsruten åpne hele tiden?
Vi planlegger å implementere denne funksjonen snart. Brukere kan da velge å holde fanene i handlingsruter åpen hele tiden. Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Hvorfor vises det av og til ulike hurtigmenyer når jeg høyreklikker?
Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny. Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**. Vi kan ikke bygge inn disse kommandoene på hurtigmenyene i Dynamics 365 for Operations fordi nettlesere av sikkerhetsmessige årsaker ikke gir oss programmatisk tilgang til utklippstavlen i systemet.

Hvis du høyreklikker en feltetikett eller verdien til en skrivebeskyttet kontroll, vises hurtigmenyen for Dynamics 365 for Operations.

For å gjøre tastaturtilgang enklere planlegger vi å implementere en hurtigtast som åpner hurtigmenyen for Dynamics 365 for Operations.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Hvor er funksjonen Vis detaljer i Dynamics 365 for Operations?
Alternativet **Vis detaljer** er tilgjengelig på ulike måter:

-   Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling. Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.
-   **Vis detaljer** er også et alternativ på hurtigmenyer for Dynamics 365 for Operations. Hvis du vil ha mer informasjon om når hurtigmenyer for Dynamics 365 for Operations vises når du høyreklikker, kan du se den forrige delen.





