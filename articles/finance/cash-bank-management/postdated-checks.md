---
title: Etterdaterte sjekker
description: Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker. Etterdaterte sjekker utstedes for å foreta og motta betalinger på en fremtidig dato.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: kfend
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d32ed9de66bc92e17c5515a4266f41aaeb9f2c1
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151379"
---
# <a name="postdated-checks"></a>Etterdaterte sjekker

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker. Etterdaterte sjekker er sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato. Derfor kan ikke veksles sjekken før den angitte datoen.

Dynamics 365 Finance støtter hele forvaltningssyklusen for etterdaterte sjekker i både Kunder og Leverandører, som vist i følgende tabell.
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
<td>Registrere detaljer om en etterdaterte sjekk du utsteder til en leverandør. Når betalingen er postert, er leverandøren gjenkjent, men bankkontoen ennå ikke kredit. I stedet brukes en avregningskonto for dette formålet. </td>
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
<td>Du kan avbryte en postert etterdatert sjekk i disse situasjonene: - Sjekken returneres av banken.
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



Hvis du vil ha mer informasjon, se følgende emner:

[Definere etterdaterte sjekker](tasks/set-up-postdated-checks.md)

[Registrere og postere en etterdatert sjekk for en kunde](tasks/register-post-postdated-check-customer.md)

[Utligne en etterdatert sjekk fra en kunde](tasks/settle-postdated-check-customer.md)

[Registrere og postere en etterdatert sjekk for en leverandør](tasks/register-post-postdated-check-vendor.md) 

[Utligne en etterdatert sjekk for en leverandør](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
