---
title: Posteringskontoer for avhending av anleggsmiddel
description: Dette emnet forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e00c00b0cb7058858fde3774941911ce20fb6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567534"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Posteringskontoer for avhending av anleggsmiddel

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler.

På siden Posteringsprofiler for anleggsmidler i hurtigkategorien Finanskontoer velger du Avhendingssalg og salg og Avhending svinn for å konfigurere postering til finansmodulen.

Når det gjelder begge transaksjonstypene, krediteres finanskontoen med avhendingsverdien til anleggsmidlene. Debetbeløpet posteres til en motkonto, som for eksempel kan være en bankkonto. Hvis anleggsmidler selges til en kunde, brukes kundekontoen i stedet for motkontoen.

Klikk Avhending og klikk deretter Salg eller Svinn. Definer deretter detaljerte kontoer for å tilbakeføre netto bokført verdi for anleggsmidlet. Du kan også angi informasjon i feltet Postert verdi og Salgsverditype på siden Avhendingsparametere. 

Avhendingstransaksjonen for et anleggsmiddel i en lavverdipulje reduserer den netto bokførte verdien av lavverdipuljen med bare det avhendede beløpet. Hvis derimot salgssummen for et anleggsmiddel overskrider den bokførte verdien av lavverdipuljen, reduseres netto bokført verdi til null.





