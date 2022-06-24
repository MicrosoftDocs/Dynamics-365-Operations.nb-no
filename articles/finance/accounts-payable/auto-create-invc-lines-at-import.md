---
title: Generere fakturalinjer ved import av leverandørfakturaer
description: Denne artikkelen beskriver funksjonaliteten for automatisk generering av fakturalinjer på leverandørfakturaer når fakturaer importeres.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e745ab1fb39edf69fabd147e46e1da8cc98ba6e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903514"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generere fakturalinjer ved import av leverandørfakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjonaliteten for automatisk generering av fakturalinjer på leverandørfakturaer når fakturaer importeres.

Noen ganger inneholder leverandørfakturaer begrenset informasjon, som mottakerinformasjon og delsummer. De inneholder imidlertid ingen informasjon for linjeelementer. Når du importerer fakturaer, genereres fakturalinjene automatisk basert på informasjon i den tilsvarende bestillingen.

Følg denne fremgangsmåten for å aktivere automatisk oppretting av fakturalinjer.

1.  Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
2.  Sett alternativet **Opprett fakturalinjer automatisk** til **Ja** under **Automatisk linjeoppretting for importerte fakturaer** i kategorien **Leverandørfaktura automatisk**. 
4.  I feltet **Velg standardantall for automatisk fakturalinjeoppretting** velger du antallet som skal brukes til automatisk generering av fakturalinjer:

    - **Bestilt antall** – Linjer genereres fra bestillingslinjer. Denne verdien er standardverdien.
    - **Produktkvitteringsantall** – Bestillingsnummeret brukes til å finne de relevante produktmottakene. Deretter vil det bruke produktmottaksantallet til å generere fakturalinjer.

## <a name="data-entity-changes"></a>Dataenhetsendringer

For å støtte funksjonaliteten som er beskrevet i denne artikkelen, er dataenheten for **Leverandørfakturahode** forbedret. Tre felt er lagt til:

- **HeaderOnlyImport** – Dette feltet må være satt til **Ja** for at linjer skal genereres for fakturahoder.
- **PurchIdRange** – Listen over bestillingsnumre. Fakturanumrene kan være et område, for eksempel **INV0001.. INV0009** (der to punkter skiller starten og slutten av området) eller diskrete verdier, for eksempel **INV0001, INV0003, INV0006**. Alle bestillinger må tilhøre samme leverandørkonto i fakturahodet. Ellers får du følgende feilmelding: "Kan ikke generere fakturalinjer. Bestillinger har ulike leverandørkontoer."
- **PackingslipRange** – Listen over produktmottaksnumre. Leverandørfakturalinjer kan opprettes fra produktmottak. Produktkvitteringsnumre inkluderes imidlertid vanligvis ikke på leverandørfakturaer. Du må bare angi produktmottaksnumrene i dette feltet hvis du tydelig kan identifisere hvilke produktmottak du har bestemte fakturaer for. Fakturalinjer kan genereres basert på produktmottak. Hvis dette feltet brukes, blir innstillingen i feltet **Velg standardantall for automatisk fakturalinjeoppretting** på siden **Leverandørparametere** ignorert. 

**Begrensning**: Hvis du angir flere produktmottaksnumre, opprettes flere ventende leverandørfakturaer med samme fakturanummer. Du må konsolidere dem manuelt før du behandler fakturaen ytterligere. I fremtidige versjoner planlegger vi å konsolidere fakturaene automatisk, slik at begrensningen blir fjernet.

Alle produktkvitteringer må tilhøre samme leverandørkonto i fakturahodet.

## <a name="result"></a>Resultat

Hvis linjer genereres uten feil, logges følgende melding i historikken for automatisk leverandørfaktura: Opprett fakturalinjer automatisk: Vellykket.

Hvis linjer ikke genereres, logges følgende feilmelding: Opprett fakturalinjer automatisk: Mislykket.
