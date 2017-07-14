---
title: Etterdaterte sjekker
description: "Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Etterdaterte sjekker er sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato. Derfor kan ikke veksles sjekken før den angitte datoen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: f7cf2b7996d113f0f883b39f3603de8236e8ad2c
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Etterdaterte sjekker
<a id="postdated-checks" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Etterdaterte sjekker er sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato. Derfor kan ikke veksles sjekken før den angitte datoen.

Microsoft Dynamics 365 for Finance and Operations støtter hele forvaltningssyklusen for etterdaterte sjekker i både Kunder og Leverandører, som vist i følgende tabell.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenario</th>
<th>Detaljer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Definere etterdaterte sjekker</td>
<td>Du må definere en ny betalingsmåte og angi betalingsrutiner for å slette kontoer for utstedte sjekker, mottatte sjekker og kildeskatt.</td>
</tr>
<tr class="even">
<td>Registrere og postere en etterdatert sjekk for en leverandør</td>
<td>Registrere detaljer om en etterdaterte sjekk du utsteder til en leverandør. Når betalingen er postert, er leverandøren gjenkjent, men bankkontoen ennå ikke kredit. I stedet brukes en avregningskonto for dette formålet.</td>
</tr>
<tr class="odd">
<td>Registrere og postere en etterdatert sjekk for en kunde</td>
<td>Registrer informasjonen i en etterdatert sjekk som du mottar fra en kunde. Når betalingen er postert, er kunden kredit, men bankkontoen ikke ennå debet. I stedet brukes en avregningskonto for dette formålet.</td>
</tr>
<tr class="even">
<td>Registrere og postere en erstatning for etterdatert sjekk for en kunde eller leverandør</td>
<td>
Hvis den opprinnelige sjekken til en leverandør eller kunde blir mistet eller skadet, kan du utstede en erstatning for den etterdaterte sjekken. Når du registrerer sjekkdetaljene, må du oppgi en referanse til den opprinnelige sjekken og angi at den nye sjekken er en erstatning for den opprinnelige. Du kan også postere erstatningssjekken.</td>
</tr>
<tr class="odd">
<td>Overføre en etterdatert kundesjekk til en leverandør</td>
<td>Når du får en etterdatert sjekk fra en kunde, kan du overføre denne sjekken til en leverandør som betaling.</td>
</tr>
<tr class="even">
<td>Utligne en etterdatert sjekk for en kunde eller en leverandør</td>
<td>Utligne en etterdatert sjekk som er postert til en mellomkonto for en kunde eller leverandør når sjekken forfaller. Når sjekken er utlignet, er banken til slutt debet eller kredit mot avregningskontoen som ble brukt tidligere.</td>
</tr>
<tr class="odd">
<td>Avbryte en etterdatert sjekk for en leverandør</td>
<td>Du kan avbryte en postert etterdatert sjekk i disse situasjonene: – Sjekken returneres av banken.
- Sjekken brukes på feil faktura.
- Det er gjort en kontantbetaling mot sjekken.
</td>
</tr>
<tr class="even">
<td>Stoppe betaling av en etterdatert sjekk</td>
<td>Du kan stoppe betaling av en etterdatert sjekk som ble utstedt til en leverandør, på grunn av for eksempel utilstrekkelige midler, endring av vilkårene i avtalen med leverandøren, mottak av defekte varer fra leverandøren, eller retur av varer til leverandøren. Du kan bare stoppe betaling av sjekker som ikke er avregnet.</td>
</tr>
</tbody>
</table>







