---
title: Refundere kunder
description: Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c313c03c6f3504f132a836eb6a67207e5f3c5636d43124c5f16d13992b9b604
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770767"
---
# <a name="reimburse-customers"></a>Refundere kunder

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