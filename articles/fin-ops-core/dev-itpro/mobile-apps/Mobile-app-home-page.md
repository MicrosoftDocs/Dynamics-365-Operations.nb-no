---
title: Startside for mobilapp
description: Denne artikkelen beskriver økonomi- og driftsmobilappen (Dynamics 365) og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon.
author: sericks007
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.custom: intro-internal
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.openlocfilehash: a0979df7c0cd685f810c0ab743fbede740e7aacb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284076"
---
# <a name="mobile-app-home-page"></a>Startside for mobilapp

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

Denne artikkelen beskriver **økonomi- og driftsmobilappen (Dynamics 365)** og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon.

## <a name="overview"></a>Oversikt

Mobilappen lar organisasjoner gjøre sine forretningsprosesser tilgjengelige på mobilenheter. Når IT-administrator har aktivert mobile arbeidsområder for organisasjonen, kan brukere logger på appen og umiddelbart begynne å kjøre forretningsprosesser fra mobilenhetene. Mobilappen inneholder følgende funksjoner som kan hjelpe med å øke produktiviteten:

- Brukere kan vise, redigere og behandle forretningsdata, selv om de har uregelmessige nettverkstilkobling eller mobilenhetene er helt frakoblet. Når en enhet oppretter en nettverkstilkobling, synkroniseres automatisk frakoblede dataoperasjoner.
- IT-administratorer eller utviklere kan bygge og publisere mobile arbeidsområder som er skreddersydd til organisasjonen. Appen bruker dine eksisterende koderessurser. Derfor trenger du ikke å implementere valideringsprosedyrene, forretningslogikken eller sikkerhetskonfigurasjonen på nytt.
- IT-administratorer eller utviklere kan lett utforme mobile arbeidsområder ved hjelp av pek og klikk-arbeidsområdeutformingen som er inkludert i webklienten.
- IT-administratorer eller utviklere kan også optimalisere frakoblet-funksjonene for arbeidsområder ved hjelp av utvidelsesrammeverket for forretningslogikk. Fordi dataene fremdeles behandles når en enhet er frakoblet, forblir mobile scenarioer rike og jevne, selv om enheter ikke har konstant nettverkstilkobling.

## <a name="elements-of-the-mobile-app"></a>Elementer i mobilappen
Navigasjon i mobilappen består av fire grunnleggende begreper: instrumentbord, arbeidsområder, sider og handlinger. 

[![Navigasjonsbegreper i mobilappen.](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Når du starter appen, går du til **instrumentbord**.
2. På instrumentbordet kan du se en liste over **arbeidsområder** som er publisert.
3. I hver arbeidsområdet kan du se en liste over **sider** som er tilgjengelige for arbeidsområdet.
4. Når du er på en side, kan du utføre flere handlinger. Her er noen eksempler:

    - Vis detaljerte data.
    - Naviger til andre sider for relaterte data, for eksempel enhetsdetaljer eller linjer.
    - Se en liste over **handlinger** som er tilgjengelige for denne siden. Handlinger lar deg opprette eller redigere eksisterende data.

## <a name="implementation-process"></a>Implementeringsprosess
Illustrasjonen nedenfor viser prosessen med implementing av både mobile arbeidsområder som leveres av Microsoft, og egendefinerte mobile arbeidsområder. 

[![Implementeringsprosess for mobilapper.](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

Tabellen nedenfor inneholder koblinger til ressurser som kan hjelpe deg med å implementere både mobile arbeidsområder som leveres av Microsoft, og egendefinerte mobile arbeidsområder. Tallene i den første kolonnen samsvarer med de nummererte trinnene i den forrige illustrasjonen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Trinn</th>
<th>Rolle</th>
<th>Handling</th>
<th>Ressurser som hjelper deg med å fullføre handlingen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Systemansvarlig</td>
<td>Implementere økonomi og driftsappen i organisasjonen.</td>
<td><ul><li>Hvis du ennå ikke har distribuert en versjon av Microsoft Dynamics 365, kan du se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</li><li>Hvis du vil se en oversikt over mobile arbeidsområder som kan brukes, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er utgitt</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemansvarlig</td>
<td><strong>Hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611:</strong> Last ned og installer KB-er som aktiverer de mobile arbeidsområdene fra Microsoft.</td>
<td>Hvis du vil ha mer informasjon, se følgende emner:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobile arbeidsområder for kostnadskontroll</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobilt arbeidsområde for lagerbeholdning</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobile arbeidsområder for salgsordrer</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilt arbeidsområde for leverandørsamarbeid</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Mobilt arbeidsområde for registrering av prosjekttid</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Mobilt arbeidsområde for reiseregninger og utlegg</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systemansvarlig</td>
<td>Publisere de mobile arbeidsområdene som leveres av Microsoft.</td>
<td><a href="publish-mobile-workspace.md">Publisere mobile arbeidsområder</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Utvikler eller uavhengig programvareleverandør (ISV)</td>
<td>Bruk mobilplattformen til å opprette egendefinerte mobile arbeidsområder.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobil plattform</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Opprett en distribuerbar pakke som inneholder egendefinerte mobile arbeidsområder, og laste opp pakken til Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Opprette en distribuerbar pakke</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systemansvarlig</td>
<td>Bruk den distribuerbare pakken som inneholder de egendefinerte arbeidsområdene fra den uavhengige programvareleverandøren.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Bruke en distribuerbar pakke</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systemansvarlig</td>
<td>Publisere de egendefinerte mobile arbeidsområdene som leveres av den uavhengige programvareleverandøren.</td>
<td><a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Bruker</td>
<td>Last ned og installer mobilappen.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Økonomi- og driftsapp for Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Økonomi- og driftsapp for iOS</a><BR/>
(Windows Phone støttes ikke)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Bruker</td>
<td>Logg på og bruk mobilappen. Appen inneholder de mobile arbeidsområdene som er publisert av systemadministrator.</td>
<td>Hvis du vil se en oversikt over mobile arbeidsområder som Microsoft leverer, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er utgitt</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>Feilsøking
[Ressurser for mobil plattform](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

