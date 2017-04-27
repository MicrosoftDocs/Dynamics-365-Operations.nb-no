---
title: Posteringskontoer for avhending av anleggsmidler
description: "Denne artikkelen forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 670a67de2287fa5d0be29463f6f456b27fd88000
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Posteringskontoer for avhending av anleggsmidler

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler.

På siden Posteringsprofiler for anleggsmidler i hurtigkategorien Finanskontoer velger du Avhendingssalg og salg og Avhending svinn for å konfigurere postering til finansmodulen.

Når det gjelder begge transaksjonstypene, krediteres finanskontoen med avhendingsverdien til anleggsmidlene. Debetbeløpet posteres til en motkonto, som for eksempel kan være en bankkonto. Hvis anleggsmidler selges til en kunde, brukes kundekontoen i stedet for motkontoen.

Klikk Avhending og klikk deretter Salg eller Svinn. Definer deretter detaljerte kontoer for å tilbakeføre netto bokført verdi for anleggsmidlet. Du kan også angi informasjon i feltet Postert verdi og Salgsverditype på siden Avhendingsparametere. 

Avhendingstransaksjonen for et anleggsmiddel i en lavverdipulje reduserer den netto bokførte verdien av lavverdipuljen med bare det avhendede beløpet. Hvis derimot salgssummen for et anleggsmiddel overskrider den bokførte verdien av lavverdipuljen, reduseres netto bokført verdi til null.






