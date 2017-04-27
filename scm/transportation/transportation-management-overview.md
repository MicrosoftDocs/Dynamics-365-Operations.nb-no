---
title: Oversikt over transportstyring
description: Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Operations
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Oversikt over transportstyring

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Operations

Med Transportstyring kan du administrere firmaets transport og identifisere leverandør- og rutingløsninger for innkommende og utgående ordrer. Du kan for eksempel identifisere den raskeste ruten eller den billigste for en forsendelse. I tabellen nedenfor beskrives hovedscenariene for bruk av Transportstyring i Microsoft Dynamics 365 for Operations.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenario</th>
<th>Hvordan Transportstyring kan hjelpe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bruk eksterne logistikkleverandører for transportaktiviteter.</td>
<td>Bruk Transportstuyring til innkommende og utgående transport.</td>
</tr>
<tr class="even">
<td>Firmaets egen flåte er tilgjengelige for levering/henting, og leveringsavgifter sendes videre til kunder.</td>
<td>For utgående prosesser kan du bruke Transportstyring til å finne transporttilleggene og sende dem videre til kundene. Det er imidlertid ikke nødvendig å avstemme transportørfakturaen.</td>
</tr>
<tr class="odd">
<td>Firmaets egen flåte er tilgjengelige for levering/henting, men leveringstillegg sendes ikke videre til kunder, fordi produktprisene inkluderer transport.</td>
<td>Mye av funksjonaliteten i Transportstyring er ikke nødvendig å bruke. Du kan imidlertid bruke Transportstyring for å finne satsene for transport og justere salgsprisen tilsvarende.</td>
</tr>
<tr class="even">
<td>Logistikktjenesten tilbys av en annen juridisk enhet i det samme firmaet.</td>
<td><ul>
<li>Du kan bruke Transportstyring ved å behandle den andre juridiske enheten som enhver annen andre transportør. Du kan ikke automatisere de økonomiske transaksjonene mellom juridiske enheter. Derfor må du behandle disse transaksjonene manuelt (for eksempel ved å opprette en bestilling).</li>
<li>I den juridiske enheten som sørger for logistikktjenestene, kan Transportstyrng brukes til å bestemme transportsatser.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Planlegging av transport i Dynamics 365 for Operations
I Transportstyring kan transportplanlegging baseres på ordrer eller på forsendelsene som opprettes basert på disse ordrene. Forsendelsene finnes alltid på et bestemt tidspunkt, men de kreves ikke for planlegging av transport. Overføringsordrer inngår i det utgående scenariet og kan planlegges sammen med salgsordrer. 

![Laste inn tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Innkommende transport
Når du bestiller varer fra en leverandør og varene må leveres til lageret, kan det være aktuelt å ordne med transporten av varene selv. Du kan bruke Dynamics 365 for Operations til å planlegge transport og mottak av en innkommende last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging av transport for en innkommende last. 

![Forretningsprosessflyt for transport av innkommende last](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Utgående transport
Du kan planlegge og behandle en utgående last for å sende bestemte varer fra lageret for et firma til en kunde. Du kan bruke Dynamics 365 for Operations til å planlegge transport og forsendelse av en utgående last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging og behandling av utgående laster for forsendelse. 

![Planlegge og behandle utgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Lastplanlegging
Dynamics 365 for Operations inneholder strategi for bygging av laster som heter Volumbasert lastplanleggingsstrategi. Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier. Hvis du vil bruke denne strategien, velger du den i feltet **Strategi for lastplanlegging** i hurtigfanen **Oppsett** på siden **Arbeidsområde for lastplanlegging**. I tillegg kan du legge til dine egne strategier for lastplanlegging ved å opprette en ny klasse i applikasjonsobjekttreet (AOT).




