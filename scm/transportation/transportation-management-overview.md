---
title: Oversikt over transportstyring
description: Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Finance and Operations
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 2fbea4f5e86a6bef98be5df3a2b69aac36e371e5
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Oversikt over transportstyring
<a id="transportation-management-overview" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Finance and Operations

Med Transportstyring kan du administrere firmaets transport og identifisere leverandør- og rutingløsninger for innkommende og utgående ordrer. Du kan for eksempel identifisere den raskeste ruten eller den billigste for en forsendelse. I tabellen nedenfor beskrives hovedscenariene for bruk av Transportstyring i Microsoft Dynamics 365 for Finance and Operations.

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

## Planlegge transport i Finance og Operations
<a id="planning-transportation-in-finance-and-operations" class="xliff"></a>
I Transportstyring kan transportplanlegging baseres på ordrer eller på forsendelsene som opprettes basert på disse ordrene. Forsendelsene finnes alltid på et bestemt tidspunkt, men de kreves ikke for planlegging av transport. Overføringsordrer inngår i det utgående scenariet og kan planlegges sammen med salgsordrer. 

![Laste inn tegning](./media/Load-drawing1-1024x477.jpg)

## Innkommende transport
<a id="inbound-transportation" class="xliff"></a>
Når du bestiller varer fra en leverandør og varene må leveres til lageret, kan det være aktuelt å ordne med transporten av varene selv. Du kan bruke Dynamics 365 for Operations til å planlegge transport og mottak av en innkommende last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging av transport for en innkommende last. 

![Forretningsprosessflyt for transport av innkommende last](./media/Businessprocessflowforinboundloadtransportation.jpg)

## Utgående transport
<a id="outbound-transportation" class="xliff"></a>
Du kan planlegge og behandle en utgående last for å sende bestemte varer fra lageret for et firma til en kunde. Du kan bruke Dynamics 365 for Operations til å planlegge transport forsendelse av en utgående last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging og behandling av utgående laster for forsendelse. 

![Planlegge og behandle utgående laster](./media/Planningandprocessingoutboundloads.jpg)

## Lastplanlegging
<a id="load-building" class="xliff"></a>
Finance and Operations inneholder strategi for bygging av laster som heter Volumbasert lastplanleggingsstrategi. Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier. Hvis du vil bruke denne strategien, velger du den i feltet **Strategi for lastplanlegging** i hurtigfanen **Oppsett** på siden **Arbeidsområde for lastplanlegging**. I tillegg kan du legge til dine egne strategier for lastplanlegging ved å opprette en ny klasse i applikasjonsobjekttreet (AOT).




