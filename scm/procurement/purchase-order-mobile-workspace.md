---
title: "Kjøpsordregodkjenning mobilt arbeidsområde"
description: "Dette emnet gir informasjon om Kjøpsordregodkjenning mobilt arbeidsområde, som lar deg vise bestillinger og svare på dem gjennom handlinger. Du kan for eksempel godkjenne eller avvise en bestilling."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: a2ab719b971c325be184d1d950f6c03815e4cea2
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Kjøpsordregodkjenning mobilt arbeidsområde
<a id="purchase-order-approval-mobile-workspace" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet **Godkjenning av bestilling**. I dette arbeidsområdet kan du vise bestillinger og svare på dem gjennom handlinger. Du kan for eksempel godkjenne eller avvise en bestilling.
 
## Oversikt
<a id="overview" class="xliff"></a> 
Bestillinger som krever godkjenning, går gjennom en godkjenningsarbeidsflyt. Arbeidsflyten kan inkludere ulike trinn som krever at en eller flere personer utfører en handling. For eksempel kan en person måtte fullføre en oppgave eller godkjenne bestillingen. 

På det mobile arbeidsområdet **Godkjenning av bestilling** kan du lett vise og svare på bestillinger fra en mobil enhet. På dette arbeidsområdet kan du også utføre de samme handlingene i arbeidsflyten som du kan utføre fra Microsoft Dynamics 365 Finance and Operations, Enterprise edition, webklient.

## Forutsetninger
<a id="prerequisites" class="xliff"></a>
Forutsetningene varierer avhengig av hvilken versjon av Finance and Operations som er distribuert i organisasjonen.

### Forutsetninger hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition
<a id="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update" class="xliff"></a> 
Hvis oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition er distribuert i organisasjonen, må systemansvarlig publisere det mobile arbeidsområdet **Godkjenning av bestilling**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere
<a id="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later" class="xliff"></a>
Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger. 

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementer KB 4017918.</td>
<td>Systemansvarlig</td>
<td>KB 4017918 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>Godkjenning av bestilling</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4017918.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet <strong>Godkjenning av bestilling</strong>.</td>
<td>Systemansvarlig</td>
<td>Se <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## Laste ned og installere mobilappen
<a id="download-and-install-the-mobile-app" class="xliff"></a>
Last ned og installer mobilappen Microsoft Dynamics 365 for Unified Operations:

- [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)


## Logge på mobilappen
<a id="sign-in-to-the-mobile-app" class="xliff"></a>

1. Start appen på mobilenheten.
2. Skriv inn URL-adressen til Microsoft Dynamics 365.
3. Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4. Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

![Arbeidsområdet Godkjenning av bestilling i listen over tilgjengelige arbeidsområder](./media/po-workspaces.png)

## Vis bestillinger som er tilordnet til deg
<a id="view-orders-that-are-assigned-to-you" class="xliff"></a>
1. Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.
2. Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.
3. Velg en ordre. På **Ordredetaljer**-siden vises ordrehodeinformasjon og -linjer. Du kan også finne retningslinjer fra arbeidsflytoppgaven.
4. Velg **Regnskapsdistribusjoner** for å åpne siden **Hoderegnskapsdistribusjoner**.
5. Gå tilbake til **Ordredetaljer**-siden, og velg en linje. Du kan også utforske de linjespesifikke regnskapsdistribusjonene fra ordrelinjedetaljene.

## Fullfør en handling på bestillingen
<a id="complete-an-action-on-the-purchase-order" class="xliff"></a>
Når du har vist bestillingen som er tilordnet til deg og lest instruksjonene for arbeidsflyten, bør du være klar til å utføre handlinger.

1. Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.
2. Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.
3. Velg en ordre, og vis detaljsiden.
4. Velg **Handlinger** for å vise de tilgjengelige handlingene. Handlingene som er tilgjengelige, avhenger av oppgaven som er tilordnet til deg.

    | Oppgavehandling    | Godkjenningshandling  |
    |----------------|------------------|
    | Komplett       | Godkjenn          |
    | Retur         | Avvis           |
    | Be om endring | Be om endring   |
    | Deleger       | Deleger         |

5. Velg riktig handling.
6. På **Fullfør oppgave**-siden skriver du inn en kommentar. Legg merke til at hvis du velger **Deleger**-handlingen, må du velge en bruker delegere oppgaven til.
7. Velg **Ferdig**. Når du har oppdatert arbeidsområdet, fjernes bestillingen fra listen. 

