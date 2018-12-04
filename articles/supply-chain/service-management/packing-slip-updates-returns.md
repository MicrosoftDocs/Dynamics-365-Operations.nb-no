---
title: "Følgesedddeloppdateringer for returer"
description: "Før returnerte varer kan mottas til lager, må følgeseddelen for ordren som varene tilhører, oppdateres."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7532c5b1debdb498c2d6bab129208a412387c8fa
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

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

  



