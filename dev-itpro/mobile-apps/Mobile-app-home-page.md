---
title: Startside for Dynamics 365 for Operations-mobilappen
description: "Dette emnet beskriver Microsoft Dynamics 365 for Operations-mobilappen og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5962fa36b061382e7f0ad55c08c81ac2cebc047d
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Startside for Dynamics 365 for Operations-mobilappen

[!include[banner](../includes/banner.md)]


Dette emnet beskriver Microsoft Dynamics 365 for Operations-mobilappen og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon.

<a name="overview"></a>Oversikt
--------

Microsoft Dynamics 365 for Operations-mobilappen lar organisasjoner gjøre sine forretningsprosesser tilgjengelige på mobilenheter. Når IT-administrator har aktivert funksjonen for mobile arbeidsområder for organisasjonen, kan brukere logger på appen og umiddelbart begynne å kjøre forretningsprosesser fra mobilenhetene. Dynamics 365 for Operations-mobilappen inneholder følgende funksjoner som kan hjelpe med å øke produktiviteten:

-   Brukere kan vise, redigere og behandle forretningsdata, selv om de har uregelmessige nettverkstilkobling eller mobilenhetene er helt frakoblet. Når en enhet oppretter en nettverkstilkobling, synkroniseres automatisk frakoblede dataoperasjoner med Dynamics 365 for Operations.
-   IT-administratorer eller utviklere kan bygge og publisere mobile arbeidsområder som er skreddersydd til organisasjonen. Appen bruker dine eksisterende koderessurser. Derfor trenger du ikke å implementere valideringsprosedyrene, forretningslogikken eller sikkerhetskonfigurasjonen på nytt.
-   IT-administratorer eller utviklere utformer lett mobile arbeidsområder ved hjelp av pek og klikk-arbeidsområdeutformingen som er inkludert i Dynamics 365 for Operations-webklienten.
-   IT-administratorer eller utviklere kan også optimalisere frakoblet-funksjonene for arbeidsområder ved hjelp av utvidelsesrammeverket for forretningslogikk. Fordi dataene fremdeles behandles når en enhet er frakoblet, forblir mobile scenarioer rike og jevne, selv om enheter ikke har konstant nettverkstilkobling.

## <a name="elements-of-the-mobile-app"></a>Elementer i mobilappen
Navigasjon i mobilappen består av fire enkle begreper: instrumentbord, arbeidsområder, sider og handlinger. 

[![Navigasjonsbegreper i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Når du starter appen, går du til **instrumentbord**.
-   På instrumentbordet ser du en liste over **arbeidsområder** som er tilgjengelige i ditt Dynamics 365 for Operations-miljø.
-   I hver arbeidsområdet kan du se en liste over **sider** som er tilgjengelige for arbeidsområdet.
-   Du kan vise data som samles inn fra én eller flere sider i Dynamics 365 for Operations, på én side.
-   Fra en side kan du navigere til andre sider for relaterte data, for eksempel enhetsdetaljer eller linjer.
-   På en side kan du også se en liste over **handlinger** som er tilgjengelige for denne siden.
-   Handlinger lar deg opprette eller redigere eksisterende data.

## <a name="implementation-process"></a>Implementeringsprosess
Illustrasjonen nedenfor viser prosessen for å implementere Dynamics 365 for Operations-mobilappen i organisasjonen. 

![Implementeringsprosess for mobilapper](./media/mobile-implementation-process_4.png)

Tabellen nedenfor inneholder koblinger til ressurser som kan bidra til å implementere Microsoft Dynamics 365 for Operations-mobilappen i organisasjonen. Tallene i den første kolonnen samsvarer med de nummererte trinnene i den forrige illustrasjonen.

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
<td>Implementer Dynamics 365 for Operations for organisasjonen.</td>
<td>Hvis du ikke allerede har Dynamics 365 for Operations distribuert i organisasjonen, kan du se <a href="../deployment/deploy-demo-environment.md">Distribuere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemansvarlig</td>
<td>Laste ned og installere KB-er som aktiverer de mobile arbeidsområdene fra Microsoft.</td>
<td>Se &quot;Forutsetninger&quot;-avsnittet i emnet om det mobile arbeidsområdet som organisasjonen vil bruke:
<ul>
<li><a href="/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobile arbeidsområder for kostnadskontroll</a></li>
<li><a href="/dynamics365/operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Mobilt arbeidsområde for lagerbeholdning</a></li>
<li><a href="/dynamics365/operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Mobile arbeidsområder for salgsordrer</a></li>
<li><a href="/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilt arbeidsområde for leverandørsamarbeid</a></li>
<li><a href="/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobilt arbeidsområde for registrering av prosjekttid</a></li>
<li><a href="/dynamics365/operations/financials/expense-management/expense-management-mobile-workspace">Det mobile arbeidsområdet Reiseregning og utlegg</a></li>
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
<td>Bruk mobilrammeverket for Dynamics 365 for Operations til å opprette egendefinerte mobile arbeidsområder.</td>
<td><ul>
<li><a href="mobile-platform.md">Dynamics 365 for Operations-mobilrammeverk</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">X++-API-er for Dynamics 365 for Operations-arbeidsområde </a></li>
</ul></td>
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
<td><a href="../deployment/apply-deployable-package-system.md">Bruke en distribuerbar pakke på Microsoft Dynamics 365 for Operations-systemet</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systemansvarlig</td>
<td>Publisere de egendefinerte mobile arbeidsområdene som leveres av den uavhengige programvareleverandøren.</td>
<td><a href="publish-mobile-workspace.md">Publisere mobile arbeidsområder</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Bruker</td>
<td>Last ned og installer Dynamics 365 for Operations-mobilappen.</td>
<td><ul>
<li>For Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations på Google Play-butikken</a></li>
<li>For iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations på iTunes-appbutikken</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Bruker</td>
<td>Logg på og bruk Dynamics 365 for Operations-mobilappen. Appen inneholder de mobile arbeidsområdene som er publisert.</td>
<td>Hvis du vil se en oversikt over mobile arbeidsområder fra Microsoft, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er lansert for Dynamics 365 for Operations-mobilappen</a>
</td>
</tr>
</tbody>
</table>






