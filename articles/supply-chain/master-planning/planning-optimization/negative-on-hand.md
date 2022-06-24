---
title: Planlegging med negative lagerbeholdningsantall
description: Denne artikkelen forklarer hvordan negativ beholdning håndteres når du bruker planleggingsoptimalisering.
author: t-benebo
ms.date: 07/22/2021
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
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04006bb12142be69c84bc8085dd82fc99280e90b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856142"
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

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Planlegging når det finnes en reservering mot negativ lagerbeholdning

Hvis du justerer lager mens det finnes fysiske reserveringer, kan du forårsake en situasjon der en ordre er fysisk reservert mot negativt lager. Fordi det finnes en fysisk reservering, må du i så fall ha forsyning for å dekke det reserverte antallet. Etterfylling er derfor nødvendig slik at systemet enten vil opprette en planlagt bestilling for å etterfylle antallet som ikke kunne dekkes av den eksisterende lagerbeholdningen, eller dekke det med en eksisterende ordre for varen.

Eksemplet nedenfor illustrerer dette scenarioet.

### <a name="example"></a>Eksempel

Systemet konfigureres på følgende måte:

- Produktet *FG* finnes og har *10* stk. av lagerbeholdning.
- Produktkonfigurasjonen tillater fysisk negativt lager.
- Det finnes en salgsordre for et antall på *10* stk. av produktet *FG*.
- Salgsordreantallet er fysisk reservert mot eksisterende lagerbeholdning.

Deretter justerer du antallet av produktet *FG*, slik at lagerbeholdningen blir 5. Fordi beholdningen for produktlageret er 5, reserveres salgsordreantallet nå mot antall som ikke er tilgjengelig i beholdningen (det vil være likt hvis beholdningen er 0. I så fall vil salgsordren reserveres mot negativt lager). Hvis du kjører en hovedplanlegging nå, blir det opprettet en planlagt ordre for antallet 5 for *FG* for å forsyne salgsordren, fordi planleggingsoptimalisering alltid vil bruke eksisterende forsyning eller opprette en ny planlagt ordre for å forsyne den fysiske reserveringen.

## <a name="related-resources"></a>Relaterte ressurser

- [Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)
- [Kom i gang med planleggingsoptimalisering](get-started.md)
- [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Vise planhistorikk og planleggingslogger](plan-history-logs.md)
- [Annullere en planleggingsjobb](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
