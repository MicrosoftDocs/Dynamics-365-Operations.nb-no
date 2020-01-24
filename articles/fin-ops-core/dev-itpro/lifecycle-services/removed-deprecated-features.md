---
title: Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning Microsoft Dynamics Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885461"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)

[!include[banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller avskrevet for Microsoft Dynamics Lifecycle Services (LCS).

- En *fjernet* funksjon er ikke lenger tilgjengelig i tjenesten.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.

## <a name="october-2019-announcements"></a>Oktober 2019-kunngjøringer

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Flytdiagrammer for forretningsprosessmodelerer

<table>
<tbody>
<tr>
<td><strong>Årsak til avskrivning/fjerning</strong></td>
<td>Vi avskriver flytskjemakomponenten i BPM (Forretningsprosessmodelerer), fordi eldre utforming forårsaket lav bruk.</td>
</tr>
<tr>
<td><strong>Erstattet med en annen funksjon?</strong></td>
<td>Nei</td>
</tr>
<tr>
<td><strong>Berørte områder</strong></td>
<td>Forretningsprosessmodelerer</td>
</tr>
<tr>
<td><strong>Status</strong></td>
<td>Avskrevet: Komponenten flytdiagram i BPM forventes å bli fjernet i begynnelsen av februar 2020. Følgende funksjonalitet blir fjernet:
<ul>
<li>Eksisterende flytskjemaer vil ikke være tilgjengelige for visning eller redigering. Figuregenskapene som er tilknyttet flytskjemaaktiviteter, vil heller ikke være tilgjengelige, fordi hele <strong>flytskjema</strong>-kategorien vil bli fjernet. Disse flytskjemaene inneholder både standard flytskjemaer som genereres automatisk og tilpassede flytskjemaer som endres basert på disse standard flytskjemaene.</li>
<li>Den eldre funksjonen for tilpassings-/gapanalyse vil ikke være tilgjengelig. Derfor blir ingen gapliste automatisk opprettet eller tilgjengelig for eksport.
<p><strong>Merk:</strong> Denne funksjonen ble tidligere avskrevet og erstattet av Microsoft Azure DevOps-integrasjoner.</p>
</li>
<li>Versjonsloggen for flytskjemaet vil ikke være tilgjengelig.</li>
</ul>
</td>
</tr>
</tbody>
</table>
