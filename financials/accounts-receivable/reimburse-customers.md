---
title: Refundere kunder
description: "Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3201166eb7054205647a54ed80f98968fcfda6e
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="reimburse-customers"></a>Refundere kunder

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet. 

Tabellen nedenfor viser forutsetninger som må være på plass før du starter.

| Forutsetning                                                            | Beskrivelse                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Angi det minste refusjonsbeløpet for den juridiske enheten.          | Angi det minste beløpet som kan refunderes for kunders overbetaling, i **Minimumsrefusjon**-feltet i **Generelt**-området på **Kundeparametere**-siden. |
| Valgfritt: Legg til en leverandørkonto i hver kunde som kan refunderes. | Velg leverandørkontoen for kunden i **Leverandørkonto**-feltet i hurtigfanen **Diverse detaljer** på **Kunder**-siden.                                           |

Når du oppretter refusjonstransaksjoner, opprettes en leverandørfaktura for beløpet i kreditsaldoen. Refusjonsprosessen fjerner kreditsaldoen for kundekontoen og oppretter en forfalt saldo for leverandørkontoen som tilsvarer kunden.

1.  Kjør **Refusjon**-prosessen i Kunder.
2.  Følg ett av disse trinnene:
    -   Klikk **Velg**, og angi kundekontoene i spørringen for å refundere bestemte kundekontoer.
    -   Klikk **OK** for å refundere alle kundekontoer.

    Kreditbeløpene overføres til leverandørkontoene til kundene og behandles som ordinære betalinger. Hvis en kunde ikke har en leverandørkonto, opprettes det automatisk en engangsleverandørkonto for kunden.
3.  Hvis du vil vise refusjonstransaksjonene som ble opprettet, bruker du **Refusjon**-siden.
4.  Opprett en betaling for leverandørfakturaer som ble opprettet av refusjonsprosessen, i Leverandører.





