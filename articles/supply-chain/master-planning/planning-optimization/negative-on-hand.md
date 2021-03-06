---
title: Planlegging med negative lagerbeholdningsantall
description: Dette emnet forklarer hvordan negativ beholdning håndteres når du bruker planleggingsoptimalisering.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1c403e23309dda36dd1c99e22bbae0aa2d6d76a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813105"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planlegging med negative lagerbeholdningsantall

[!include [banner](../../includes/banner.md)]

Hvis systemet viser et negativt antall av lagerbeholdningen, behandler planleggingsmotoren antallet som 0 (null) for å unngå overforsyning. Slik fungerer denne funksjonaliteten:

1. Funksjonen for planleggingsoptimalisering samler opp beholdningsantall på det laveste nivået av dekningsdimensjoner. (Hvis *sted* for eksempel ikke er en dekningsdimensjon, samler planleggingsoptimalisering lagerbeholdningsantall på nivået *lager*.)
1. Hvis det samlede lagerbeholdningsantallet på det laveste nivået av dekningsdimensjoner er negativt, forutsetter systemet at beholdningsantallet virkelig er 0 (null).

> [!IMPORTANT]
> Planleggingssystemet kan bare være like nøyaktig som inndataene. Hvis inndataene er unøyaktige, vil negative lagerposter vise at beholdningsinformasjonen i Microsoft Dynamics 365 Supply Chain Management ikke er synkronisert med den virkelige verden. Derfor vil planleggingsresultatet bli feil. Hvis du vil ha et nøyaktig planleggingsresultat, må du minimere antallet poster som viser et negativt beholdningsantall.

## <a name="example-1"></a>Eksempel 1

Lager 13 konfigureres på følgende måte:

- **Dekningskode:** Min/maks
- **Minimum:** 15 stykker (stk.)
- **Maksimum:** 25 stk.

Det laveste nivået av dekningsdimensjoner er *lager*, og følgende lagerbeholdninger registreres på nivået *sted*:

- **Område 1, lager 13, sted 1:** 20 stk.
- **Område 1, lager 13, sted 2:** &minus;8 stk.

Derfor er det totale beholdningsantallet 12 stk. for lager 13. (= 20 stk. &minus; 8 stk.).

I dette tilfellet bruker planleggingsmotoren et samlet lagerbeholdningsantall på 12 stk. for lager 13.

Resultatet er en planlagt bestilling på 13 stk. (= 25 stk. &minus; 12 stk.) for å fylle på lager 13 fra 12 stk. til 25 stk.

## <a name="example-2"></a>Eksempel 2

Lager 13 konfigureres på følgende måte:

- **Dekningskode:** Min/maks
- **Minimum:** 15 stk.
- **Maksimum:** 25 stk.

Det laveste nivået av dekningsdimensjoner er *lager*, og følgende lagerbeholdninger registreres på nivået *sted*:

- **Område 1, lager 13, sted 1:** 4 stk.
- **Område 1, lager 13, sted 2:** &minus;8 stk.

Derfor er det totale beholdningsantallet &minus;4 stk. for lager 13. (= 4 stk. &minus; 8 stk.). Det er med andre ord mindre enn 0 (null).

I dette tilfellet forutsetter planleggingsmotoren at beholdningen for lager 13 er 0 stk. i stedet for &minus;4 stk.

Resultatet er en planlagt bestilling på 25 stk. (= 25 stk. &minus; 0 stk.) for å fylle på lager 13 fra 0 stk. til 25 stk.

## <a name="related-resources"></a>Relaterte ressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]