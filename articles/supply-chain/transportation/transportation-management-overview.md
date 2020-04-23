---
title: Oversikt over transportstyring
description: Dette emnet gir en oversikt over transportstyringsfunksjoner i Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3d8a34195edbae7daf1a9db4e236aad33f98d08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201347"
---
# <a name="transportation-management-overview"></a>Oversikt over transportstyring

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over transportstyringsfunksjoner i Supply Chain Management.

Transportstyring lar deg bruke bedriftens transport, og lar deg også identifisere leverandør- og rutingsløsninger for innkommende og utgående bestillinger. Du kan for eksempel identifisere den raskeste ruten eller den billigste for en forsendelse. I tabellen nedenfor beskrives hovedscenariene for bruk av Transportstyring.

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

## <a name="planning-transportation-in-supply-chain-management"></a>Planlegging av transport i Supply Chain Management
I Transportstyring kan transportplanlegging baseres på ordrer eller på forsendelsene som opprettes basert på disse ordrene. Forsendelsene finnes alltid på et bestemt tidspunkt, men de kreves ikke for planlegging av transport. Overføringsordrer inngår i det utgående scenariet og kan planlegges sammen med salgsordrer. 

![Laste inn tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Innkommende transport
Når du bestiller varer fra en leverandør og varene må leveres til lageret, kan det være aktuelt å ordne med transporten av varene selv. Du kan bruke Supply Chain Management til å planlegge transport og mottak av en innkommende last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging av transport for en innkommende last. 

![Forretningsprosessflyt for transport av innkommende last](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Utgående transport
Du kan planlegge og behandle en utgående last for å sende bestemte varer fra lageret for et firma til en kunde. Du kan bruke Supply Chain Management til å planlegge transport og forsendelse av en utgående last. Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging og behandling av utgående laster for forsendelse. 

![Planlegge og behandle utgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Lastplanlegging
Supply Chain Management inneholder strategi for bygging av last som heter Volumbasert lastplanleggingsstrategi. Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier. Hvis du vil bruke denne strategien, velger du den i feltet **Strategi for lastplanlegging** i hurtigfanen **Oppsett** på siden **Arbeidsområde for lastplanlegging**. I tillegg kan du legge til dine egne strategier for lastplanlegging ved å opprette en ny klasse i applikasjonsobjekttreet (AOT).



