---
title: Posteringskontoer for avhending av anleggsmiddel
description: Dette emnet forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8501bbb0fc47fb52e100d9086054db4831dae178
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720258"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Posteringskontoer for avhending av anleggsmiddel

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du setter opp bokføringskontoer i økonomimodulen når du avhender anleggsmidler.

Hvis du vil angi posteringskontoer for økonomimodulen som skal brukes når du avhender et anleggsmiddel, velger du **Avhending salg** og **Avhending svinn** i hurtigfanen **Finanskontoer** på siden **Posteringsprofiler for anleggsmidler**.

Når det gjelder begge transaksjonstypene (avhending av et aktiva ved salg eller svinn), krediteres finanskontoen med avhendingsverdien til anleggsmidlene. Debetbeløpet posteres til en motkonto, som kan være en bankkonto (som et eksempel). Hvis anleggsmidler selges til en kunde, brukes kundekontoen i stedet for motkontoen. Hvis du vil ha mer informasjon, kan du se [Fjerne et anleggsmiddel som svinn](dispose-of-a-fixed-asset-as-scrap.md).

Klikk **Avhending** og klikk deretter **Salg** eller **Svinn**. Definer deretter detaljerte kontoer for å tilbakeføre netto bokført verdi for anleggsmidlet. Du kan også angi informasjon i feltet **Poster verdi** og **Salgsverditype** på siden **Avhendingsparametere**. 

Avhendingstransaksjonen for et anleggsmiddel i en lavverdipulje reduserer den netto bokførte verdien av lavverdipuljen med bare det avhendede beløpet. Hvis derimot salgssummen for et anleggsmiddel overskrider den bokførte verdien av lavverdipuljen, reduseres netto bokført verdi til null.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
