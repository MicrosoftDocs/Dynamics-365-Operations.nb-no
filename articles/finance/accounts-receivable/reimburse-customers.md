---
title: Refundere kunder
description: Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 892b089edb16ba560f588c086d37faafdf16958d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891789"
---
# <a name="reimburse-customers"></a>Refunder kunder

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet. 

Tabellen nedenfor viser forutsetninger som må være på plass før du starter.

| Forutsetning                                                            | Beskrivelse |
|-------------------------------------------------------------------------|-------------|
| Angi det minste refusjonsbeløpet for den juridiske enheten.          | Angi det minste beløpet som kan refunderes for kunders overbetaling, i **Minimumsrefusjon**-feltet i **Generelt**-området på **Kundeparametere**-siden. |
| Valgfritt: Legg til en leverandørkonto i hver kunde som kan refunderes. | Velg leverandørkontoen for kunden i **Leverandørkonto**-feltet i hurtigfanen **Diverse detaljer** på **Kunder**-siden. |

Når du oppretter refusjonstransaksjoner, opprettes en leverandørfaktura for beløpet i kreditsaldoen. Refusjonsprosessen fjerner kreditsaldoen for kundekontoen og oppretter en forfalt saldo for leverandørkontoen som tilsvarer kunden.

1. I Kunder kjører du **Refusjon**-prosessen (**Kunder \> Periodiske oppgaver \> Refusjon**).
2. Hvis du vil gruppere alle transaksjoner, uansett finansdimensjoner, setter du **Summer kunde** til **Ja**. Hvis du bare vil gruppere transaksjoner som har like finansdimensjoner, setter du alternativet til **Nei**.
3. Velg **Ta med kunder med utestående debettransaksjoner** for å velge kunder som har ikke-utlignede debetbeløp.
4. Hvis du vil refundere bestemte kundekontoer, går du til hurtigfanen **Poster som skal inkluderes** og velger **Filter**, og deretter angir du kundekontoene i spørringen.

    Kreditbeløpene overføres til leverandørkontoene til kundene og behandles som ordinære betalinger. Hvis en kunde ikke har en leverandørkonto, opprettes det automatisk en engangsleverandørkonto for kunden.

5. Hvis du vil vise refusjonstransaksjonene som ble opprettet, bruker du **Refusjon**-rapporten (**Kunder \> Forespørsler og rapporter \> Refusjon-rapporten**).
6. Opprett en betaling for leverandørfakturaer som ble opprettet av refusjonsprosessen, i Leverandører. Du finner mer informasjon om hvordan du betaler leverandører, i [Oversikt over leverandørbetaling](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
