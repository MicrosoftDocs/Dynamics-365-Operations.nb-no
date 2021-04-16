---
title: Enhetlig nummerserie for jobb-ID-er
description: Denne funksjonen gir en enkelt, felles nummerserie som genererer jobb-ID-er for produksjonskontrollen, produksjonsutførelsen og tids- og fremmøtemodulene.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824948"
---
# <a name="unified-number-sequence-for-job-ids"></a>Enhetlig nummerserie for jobb-ID-er

[!include [banner](../includes/banner.md)]

Denne funksjonen gir en enkelt, felles nummerserie som genererer jobb-ID-er for produksjonskontrollen, produksjonsutførelsen og tids- og fremmøtemodulene. Tidligere kunne du velge en forskjellig nummerserie for hver av disse modulene, noe som kunne føre til konflikt mellom jobb-ID-er hvis to eller flere av disse sekvensene brukte et identisk format. En slik konflikt kan føre til at data blir skadet.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funksjonen for systemet

Hvis systemet ikke allerede inneholder funksjonen som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Enhetlig nummerserie for jobb-ID-er*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Konfigurer den enhetlige nummerserien for jobb-ID-er

Når denne funksjonen er aktivert, vil de eksisterende **Jobbidentifikasjon**-nummersekvensinnstillingene på parametersiden for modulene Produksjonskontroll, Produksjonsutførelse og Tid og fremmøte bli avskrevet, og et nytt felt, **Enhetlig jobb-ID**, blir lagt til. Verdien for **Enhetlig jobb-ID** deles av alle de tre modulene, slik at alle modulene refererer til samme nummerserie. Jobb-ID-er vil derfor være unike i alle de tre modulene, og det vil aldri oppstå en konflikt.

Slik konfigurerer du den enhetlige nummerserien for jobb-ID-er:

1. Slå på funksjonen som beskrevet i den forrige delen.
1. Du kan enten identifisere nummerserien du vil bruke for de enhetlige jobb-ID-ene, eller opprette en ny. Hvis du vil ha mer informasjon, kan du se [Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Gå til siden **Parametere for produksjonskontroll**, **Parametere for produksjonsutførelse** eller **Parametere for timeregistrering**. Det har ingen betydning hvilken du velger, fordi når du angir denne innstillingen på en av disse sidene, vil alle de andre sidene oppdateres automatisk.
1. Åpne **Nummerserier**-fanen på den valgte parametersiden.
1. Tilordne **nummerseriekoden** som du identifiserte tidligere, til raden **Enhetlige jobb-ID-er** i rutenettet.
