---
title: Leverandørinnstillinger lagt til for Netto innkjøpspris
description: Dette emnet beskriver de nye feltene som blir lagt til på den eksisterende leverandørsiden når du aktiverer modulen Netto innkjøpspris. Du bruker disse feltene til å definere leverandørene du vil bruke sammen med funksjoner for Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 3a288517f77d1618f94f8539506d01a108e63fa5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829769"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Leverandørinnstillinger lagt til for Netto innkjøpspris

[!include [banner](../../includes/banner.md)]

Når du aktiverer modulen **Netto innkjøpspris**, blir flere nye felt lagt til på den eksiderende siden **Leverandører**. Du bruker disse feltene til å definere leverandørene du vil bruke sammen med funksjoner for Netto innkjøpspris.

Hvis du vil definere de aktuelle feltene, går du til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**. Åpne en eksisterende leverandør, eller opprett en ny, og velg deretter hurtigfanen **Diverse detaljer**. Alle de nye feltene som modulen **Netto innkjøpspris** legger til, vises under overskriften **Sjøreiser**. Tabellen nedenfor beskriver disse feltene.

| Felt | beskrivelse |
|---|---|
| Forsendelsestype | <p>Velg leverandørens rolle i forhold til Netto innkjøpspris:</p><ul><li>**Ingen** – Leverandøren har ingen spesifikk rolle som er knyttet til nettokostnad. Denne verdien er standardinnstillingen, fordi de fleste leverandører sannsynligvis ikke vil ha noen spesifikk rolle.</li><li>**Forsendelsesfirma** – Leverandøren er et forsendelsesfirma. Leverandører som har denne forsendelsestypen, kan velges i feltet **Forsendelsesfirma** på siden **Sjøreiser**.</li><li>**Tollmekler** – Leverandøren er en tollmeklarer. Leverandører som har denne forsendelsestypen, kan velges i feltet **Tollmekler** på siden **Folioer**.</li><li>**Agent** – Leverandøren er en agent. Leverandører som har denne forsendelsestypen, kan velges i feltet **Agent** på sidene **Leverandører** og **Bestillinger**.</li></ul> |
| Kostnadstypegruppe | Tilordne leverandøren til en kosttypegruppe slik at du kan velge [automatiske kostnader](auto-cost-setup.md). |
| Fra-havn | Velg opprinnelsesstedet for sjøreisen. |
| Agent | Standardagenten når det foretas innkjøp fra leverandøren. |
| Importer leverandør av etterkalkulering | <p>Angi om leverandøren er en leverandør for Netto innkjøpspris.</p><p>**Tips:** Du kan bruke dette feltet sammen med sikkerhet på postnivå for å begrense bestillingene som vises når det opprettes en sjøreise.</p> |
| Forsendelsesfirma | Velg standard forsendelsesfirma som brukes når det opprettes bestillinger for leverandøren. |
| Leverandør av tjenester | Angi om leverandøren er leverandør av tjenester. |
| Gruppe for over-/undertoleranse | Velg standard over-/undertoleransegruppe for leverandøren. |
