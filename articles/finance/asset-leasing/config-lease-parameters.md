---
title: Konfigurere parametere for leieavtale (forhåndsversjon)
description: Dette emnet beskriver konfigurasjonsinnstillingene for Aktivaleie, for eksempel sikkerhetsinformasjon og regnskapsinnstillinger.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bb8372c5e4a1d7183b5d793b142fed92e833d5a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210439"
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

4. Sett alternativet **Tillat tilbakeføring av avskrivning i en lukket tablåversjon** til **Ja** for å tillate at utgiftstransaksjoner for avskrivning tilbakeføres. Utgiftstransaksjoner kan tilbakeføres selv om tablåversjonen er lukket.

    > [!NOTE]
    > Vi anbefaler at du lar dette alternativet være satt til **Nei**. Innstillingen for dette alternativet brukes som validering og kontroll til å forhindre at en lukket tablåversjon blir avskrevet ved et uhell. Når du har alternativet satt til **Nei**, bidrar du til å holde netto bokført verdi og fremtidige avskrivningsberegninger nøyaktige.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]