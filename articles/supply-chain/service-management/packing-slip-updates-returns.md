---
title: Følgesedddeloppdateringer for returer
description: Før returnerte varer kan mottas til lager, må følgeseddelen for ordren som varene tilhører, oppdateres.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9b5c7e5726c36aa963e5750c63df20c1e2e6c35
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810708"
---
# <a name="packing-slip-updates-for-returns"></a>Følgesedddeloppdateringer for returer  

[!include [banner](../includes/banner.md)]


Før returnerte varer kan mottas til lager, må følgeseddelen for ordren som varene tilhører, oppdateres. På samme måte som fakturaoppdateringsprosessen er en oppdatering av finanstransaksjonen, er oppdateringsprosessen for følgeseddelen den fysiske oppdateringen av lagerposten, noe som betyr at endringene aktiveres i beholdningen. Når det gjelder returer, implementeres trinnene som er tilordnet til disposisjonshandlingen, når følgeseddelen oppdateres

Følgeseddeloppdateringen kan behandles enten i vareankomstjournalen eller i returordren.

Som et ledd i prosessen for postering av følgesedler kan følgeseddelens referansenummer fra kundens forsendelsesdokumenter knyttes til ordrelinjene. Denne tilknytningen er valgfri og er bare til referanseformål. Det opprettes ikke transaksjonsoppdateringer.

Hvis ikke alle varene som forventes returnert er ankommet, må du inkludere bare det mottatte antallet i følgeseddeloppdateringen. Se bort fra resten av varene i ordren til resten av returforsendelsen ankommer.

Hvis en vare sendes tilbake fra karantene til forsendelses- eller mottaksavdelingen, for eksempel når karanteneinspektøren ikke vet hvor på lageret varene skal lagres, må den tilsvarende følgeseddelen oppdateres for sikre at disposisjonskoden som er angitt som et resultat av karantenen, registreres og følges opp på riktig måte.

Når du oppdaterer en følgeseddel for en returnert vare fra en salgsavtale, oppdateres automatisk salgsavtaleforpliktelsen for denne varen for å gjenspeile endringen i antallet eller beløpet. 

## <a name="see-also"></a>Se også

[Utføre fakturaoppdateringer for returer](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]