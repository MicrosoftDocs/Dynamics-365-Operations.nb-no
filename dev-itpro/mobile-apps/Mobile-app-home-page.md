---
title: Startside for mobilapp
description: "Dette emnet beskriver mobilappen Microsoft Dynamics 365 for enhetlig drift og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 663a03dc37cc1631bd285a76ef564993a34ed057
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# <a name="mobile-app-home-page"></a>Startside for mobilapp

[!include[banner](../includes/banner.md)]

Dette emnet beskriver mobilappen Microsoft Dynamics 365 for enhetlig drift og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon.

> [!NOTE]
> Mobilappen var tidligere kalt *Microsoft Dynamics 365 for Finance and operations*.

<a name="overview"></a>Oversikt
--------

Mobilappen lar organisasjoner gjøre sine forretningsprosesser tilgjengelige på mobilenheter. Når IT-administrator har aktivert mobile arbeidsområder for organisasjonen, kan brukere logger på appen og umiddelbart begynne å kjøre forretningsprosesser fra mobilenhetene. Mobilappen inneholder følgende funksjoner som kan hjelpe med å øke produktiviteten:

- Brukere kan vise, redigere og behandle forretningsdata, selv om de har uregelmessige nettverkstilkobling eller mobilenhetene er helt frakoblet. Når en enhet etablerer en nettverkstilkobling på nytt, synkroniserer frakoblede dataoperasjoner automatisk med Dynamics 365 for Finance and Operations, Enterprise edition eller Microsoft Dynamics 365 for Finance and Operations.
- IT-administratorer eller utviklere kan bygge og publisere mobile arbeidsområder som er skreddersydd til organisasjonen. Appen bruker dine eksisterende koderessurser. Derfor trenger du ikke å implementere valideringsprosedyrene, forretningslogikken eller sikkerhetskonfigurasjonen på nytt.
- IT-administratorer eller utviklere kan lett utforme mobile arbeidsområder ved hjelp av pek og klikk-arbeidsområdeutformingen som er inkludert i webklienten.
- IT-administratorer eller utviklere kan også optimalisere frakoblet-funksjonene for arbeidsområder ved hjelp av utvidelsesrammeverket for forretningslogikk. Fordi dataene fremdeles behandles når en enhet er frakoblet, forblir mobile scenarioer rike og jevne, selv om enheter ikke har konstant nettverkstilkobling.

## <a name="elements-of-the-mobile-app"></a>Elementer i mobilappen
Navigasjon i mobilappen består av fire grunnleggende begreper: instrumentbord, arbeidsområder, sider og handlinger. 

[![Navigasjonsbegreper i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Når du starter appen, går du til **instrumentbord**.
2. På instrumentbordet kan du se en liste over **arbeidsområder** som er publisert.
3. I hver arbeidsområdet kan du se en liste over **sider** som er tilgjengelige for arbeidsområdet.
4. Når du er på en side, kan du utføre flere handlinger. Her er noen eksempler:

    - Vis detaljerte data.
    - Naviger til andre sider for relaterte data, for eksempel enhetsdetaljer eller linjer.
    - Se en liste over **handlinger** som er tilgjengelige for denne siden. Handlinger lar deg opprette eller redigere eksisterende data.

## <a name="implementation-process"></a>Implementeringsprosess
Illustrasjonen nedenfor viser prosessen med implementing av både mobile arbeidsområder som leveres av Microsoft, og egendefinerte mobile arbeidsområder. 

![Implementeringsprosess for mobilapper](./media/Mobile-implementation-process-5.png)

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
<td>Implementer Finance and Operations eller Finance and Operations i organisasjonen.</td>
<td><ul><li>Hvis du ennå ikke har distribuert en versjon av Microsoft Dynamics 365, kan du se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</li><li>Hvis du vil se en oversikt over mobile arbeidsområder som kan brukes, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er utgitt</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemansvarlig</td>
<td><strong>Hvis du bruker Microsoft Dynamics 365 for Finance and Operations versjon 1611:</strong> Last ned og installer KB-er som aktiverer de mobile arbeidsområdene som leveres av Microsoft.</td>
<td>Hvis du vil ha mer informasjon, se følgende emner:
<ul>

<li><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobile arbeidsområder for kostnadskontroll</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Mobilt arbeidsområde for lagerbeholdning</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Mobile arbeidsområder for salgsordrer</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilt arbeidsområde for leverandørsamarbeid</a></li>
<li><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">Mobilt arbeidsområde for registrering av prosjekttid</a></li>
<li><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">Det mobile arbeidsområdet Reiseregning og utlegg</a></li>

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
<td>Bruk mobilrammeverket til å opprette egendefinerte mobile arbeidsområder.</td>
<td><ul>
<li><a href="mobile-platform.md">Mobilrammeverk</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">API-er for Arbeidsområde X++</a></li>
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
<td><a href="../deployment/apply-deployable-package-system.md">Bruke en distribuerbar pakke</a></td>
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
<td>Last ned og installer mobilappen.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android-telefoner</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhone</a></li></ul>
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

