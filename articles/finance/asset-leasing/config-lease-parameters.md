---
title: Konfigurere parametere for leieavtale (forhåndsversjon)
description: Denne artikkelen beskriver konfigurasjonsinnstillingene for Aktivaleie, for eksempel sikkerhetsinformasjon og regnskapsinnstillinger.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e878fa7634cfdcc6c0db19a91e771757c545505b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895087"
---
# <a name="configure-lease-parameters"></a>Konfigurere parametere for leieavtale

[!include [banner](../includes/banner.md)]

Flere konfigurasjonsinnstillinger påvirker hvordan Aktivaleie fungerer. Disse innstillingene omfatter journalnavn, generelle parametere og postering av profilinnstillinger.

1. Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.
2. Velg hurtigfanen **Generelt** i fanen **Leieavtaler**.

    Parameteren **Tillat manuell overstyring av klassifisering** avgjør om leieavtaleklassifiseringen kan overstyres før betalingsplanen er bekreftet.

    Parameteren **Parti på tvers av enheter** fastsetter om du kan postere i andre juridiske enheter fra den gjeldende juridiske enheten. Hvis denne parameteren er aktivert, kan du opprette journaloppføringer for de juridiske enhetene du har tilgang til.

3. Sett alternativet **Tillat sletting av bekreftede leieavtaler** til **Ja** for å tillate at leieavtaler som har bekreftede betalingsplaner, slettes. Leieavtaler kan ikke slettes hvis det er knyttet posterte eller uposterte transaksjoner til dem, uavhengig av innstillingen for dette alternativet. Du kan ikke gjenopprette en leiepost etter at den er slettet. Hvis du laster opp poster for en slettet leieavtale, enten manuelt eller gjennom dataenheter, behandles den opplastede informasjonen som ny, ikke som en oppdatering for en eksisterende leieavtale.

    Hvis du setter dette alternativet til **Ja** og overgangstypen for tablået er **Kumulativt oppdateringsalternativ A eller B**, setter systemet feltet **Trinnvis lånerente** til verdien i feltet **Trinnvis lånerente ved overgang** på siden **Tablåoppsett**. Hvis dette alternativet er satt til **Nei**, settes satsen for hodeleien til verdien i feltet **Trinnvis lånerente** på siden **Tablådetaljer**, uansett hva som er overgangstypen for tablået.

4. Sett alternativet **Tillat tilbakeføring av avskrivning i et lukket tablå** til **Ja** for å tillate at utgiftstransaksjoner for avskrivning tilbakeføres. Utgiftstransaksjoner kan tilbakeføres selv om tablåversjonen er lukket.

    > [!NOTE]
    > Vi anbefaler at du lar dette alternativet være satt til **Nei**. Innstillingen for dette alternativet brukes som validering og kontroll til å forhindre at en lukket tablåversjon blir avskrevet ved et uhell. Når du har alternativet satt til **Nei**, bidrar du til å holde netto bokført verdi og fremtidige avskrivningsberegninger nøyaktige.

5. Sett alternativet **Tillat oppdeling av betalingsbeløp** til **Ja** for å tillate en oppdeling av betalingsbeløpene på hurtigfanen **Linjer i betalingsplan** på **Utleie**-siden. Betalingsoppdelingstypene defineres under **Oppsett** på siden **Betalingsbeløpstyper**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
