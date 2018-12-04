---
title: "Vanlige spørsmål for Finance and Operations-klienten"
description: "Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Finance and Operations-klienten."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 658d5a1a031f2292dbd445fa7fb345be01c61947
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="finance-and-operations-client-faq"></a>Vanlige spørsmål for Finance and Operations-klienten

[!include [banner](../includes/banner.md)]

Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Finance and Operations-klienten.

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Hvorfor blir ikke symboler lastet inn når jeg bruker Finance and Operations?
-----------------------------------------------------------------

Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte. Prøv denne fremgangsmåten for å løse dette problemet:

-   Hvis du opplever dette problemet i Internet Explorer, klikker du **Verktøy** og deretter **Alternativer for Internett**.  I dialogboksen Alternativer for Internett i kategorien **Personvern** klikker du **Egendefinert nivå** og kontrollerer at alternativet **Nedlasting av skrifter** er valgt.
-   Hvis ikke må du kanskje legge til nettstedet for Finance and Operations i listen over klarerte områder.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg holde fanene i handlingsruten åpne hele tiden?
Vi planlegger å implementere denne funksjonen snart. Brukere kan da velge å holde fanene i handlingsruter åpen hele tiden. Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Hvorfor vises det av og til ulike hurtigmenyer når jeg høyreklikker?
Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny. Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**. Vi kan ikke bygge inn disse kommandoene på hurtigmenyene i Finance and Operations fordi nettlesere av sikkerhetsmessige årsaker ikke gir oss programmatisk tilgang til utklippstavlen i systemet.

Hvis du høyreklikker en feltetikett eller verdien til en skrivebeskyttet kontroll, vises hurtigmenyen for Finance and Operations.

For å gjøre tastaturtilgang enklere planlegger vi å implementere en hurtigtast som åpner hurtigmenyen for Finance and Operations.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Hvor er funksjonen Vis detaljer i Finance and Operations?
Alternativet **Vis detaljer** er tilgjengelig på ulike måter:

-   Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling. Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.
-   **Vis detaljer** er også et alternativ på hurtigmenyer for Finance and Operations. Hvis du vil ha mer informasjon om når hurtigmenyer for Finance and Operations vises når du høyreklikker, kan du se den forrige delen.





