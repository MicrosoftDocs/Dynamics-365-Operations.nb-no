---
title: Planer basert på tilbud og forespørsel
description: Denne artikkelen beskriver hvordan du definerer hovedplanlegging for å vurdere tilbud og forespørsler om tilbud når planlagte bestillinger genereres.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690092"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Planlegge basert på tilbud og forespørsel

[!include [banner](../../includes/banner.md)]

Tilbud og forespørsler om tilbud representerer mulige eller til og med sannsynlige fremtidige ordrer. Det er derfor fornuftig å vurdere dem under hovedplanleggingen, slik at ekstra forsyning kan planlegges på grunnlag av eksisterende tilbud, og hvor sannsynlig det er at hvert tilbud vil bli en faktisk ordre. Denne artikkelen beskriver hvordan du definerer hovedplanlegging for å vurdere tilbud og tilbudsforespørsler når planlagte bestillinger genereres.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Definere hovedplanlegging for å vurdere salgstilbud og/eller tilbud

Bruk fremgangsmåten nedenfor til å definere hovedplanlegging for å vurdere salgstilbud og/eller tilbud.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende plan i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny.
1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Ta med salgstilbud** – Sett dette alternativet til *Ja*  for å vurdere salgstilbud når den gjeldende planen kjøres. Sett den til *Nei* hvis du vil ignorere dem.
    - **Sannsynlighets-%** – Angi det minste tillitsnivået som kreves for at et tilbud skal inkluderes i hovedplanleggingen. Hovedplanleggingsberegningen omfatter alle tilbud som ble opprettet fra muligheter med denne sannsynlighetsprosenten eller høyere. Hvis du vil inkludere alle tilbud, inkludert tilbud som ikke har en sannsynlighet tilordnet dem, eller ingen tilknyttet salgsmulighet, setter du dette feltet til *0* (null). Hvis du vil ha mer informasjon om sannsynlighet for tilbud, kan du se neste del.
    - **Ta med tilbudsforespørsler** – Sett dette alternativet til *Ja* for å vurdere tilbudsforespørsler når den gjeldende planen kjøres. Sett den til *Nei* hvis du vil ignorere dem. Hvis du velger å vurdere forespørsel, vil systemet opprette planlagte bestillinger for dem, men det vil ikke angi leverandøren før forespørselen er løst. Bestillingsforslag som opprettes for tilbudsforespørsler, kan påvirke antallet i andre planlagte bestillinger.

1. Fortsett å konfigurere hovedplanen på vanlig måte.

## <a name="assign-and-view-probabilities-for-quotations"></a>Tilordne og vise sannsynligheter for tilbud

Som det ble nevnt i den forrige delen, vil en hovedplan bare vurdere tilbud som oppfyller eller overskrider sannsynlighetsterskelen som er definert for planen (hvis en terskel er definert). Sannsynligheten settes imidlertid ikke direkte på hvert tilbud. I stedet arves det fra muligheten som ble brukt til å generere tilbudet. Tilbud som opprettes direkte på **Alle tilbud**-siden, har derfor ikke en sannsynlighet tilknyttet seg eller en tilknyttet salgsmulighet, og de blir aldri vurdert ved hovedplanlegging (med mindre **Sannsynlighet-%**-feltet er satt til *0* \[null\]). Hvis du vil tilordne et sannsynlighetstilbud, må det genereres et tilbud fra en salgsmulighet.

### <a name="create-a-quotation-from-an-opportunity"></a>Opprette salgsmulighet fra en salgsmulighet

Bruk denne fremgangsmåten til å tilordne en sannsynlighet til en salgsmulighet og deretter opprette et tilbud fra denne muligheten.

1. Gå til **Salg og markedsføring \> Relasjoner \> Kundeemner \> Alle kundeemner**.
1. Velg en eksisterende mulighet, eller velg **Ny** i handlingsruten for å opprette en ny.
1. Fyll ut salgsmulighetssiden for å identifisere salgsmuligheten slik du ønsker. Pass på at du angir feltet **Sannsynlighet** til en riktig verdi. Bare hovedplaner som er konfigurert til å lete etter sannsynligheter for denne verdien eller høyere, vil vurdere tilbud som er generert fra denne muligheten.
1. Velg **Lagre** i handlingsruten.
1. I handlingsruten på fanen **Salgsmulighet** i gruppen **Ny** velger du **Salgstilbud** eller **Prosjekttilbud**, avhengig av hvilken type tilbud du vil opprette.
1. Angi feltene etter behov i dialogboksen **Opprett tilbud**, og velg deretter **OK**.
1. Det opprettes et nytt tilbud som åpnes. I hurtigkategorien **Linjer** bruker du verktøylinjen til å legge til salgslinjer eller prosjektlinjer etter behov for å definere innholdet i tilbudet.
1. Velg **Lagre** i handlingsruten. Lukk deretter tilbudet.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Vise sannsynligheten som er tilordnet til et tilbud

Den eneste måten å vise sannsynligheten som er tilordnet et tilbud på, er å åpne muligheten som ble brukt til å opprette tilbudet, slik det beskrives i fremgangsmåten nedenfor.

1. Gå til **Salg og markedsføring \> Salgstilbud \> Alle tilbud**.
1. Hvis **Salgsmulighets-ID**-kolonnen ikke vises (den er skjult i en standardinstallasjon), kan du følge disse trinnene for å vise den midlertidig. (Alternativt, for å beholde kolonnen **Salgsmulighets-ID** tilgjengelig, opprett en [lagret visning](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) som inneholder den.)

    1. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Sett inn kolonner**.
    1. I dialogboksen **Sett inn kolonner** finner du raden der **Felt**-feltet er satt til *Salgsmulighet*, og merker av i avmerkingsboksen **Merk** for den raden.
    1. Velg **Oppdater** for å legge til den valgte kolonnen på siden **Alle tilbud**.

1. I rutenettet finner du raden for det relevante tilbudet. I kolonnen **Salgsmulighets-ID** velger du deretter verdien for den raden.

    > [!NOTE]
    > Hvis du er på jakt etter et prosjekttilbud, må du kanskje velge kolonnehodet **Tilbudstype** og fjerne filteret. I en standardinstallasjon er dette filteret angitt slik at bare salgstilbud vises.

1. Den tilknyttede muligheten åpnes. Nå kan du vise og redigere **Sannsynlighet**-verdien etter behov.
