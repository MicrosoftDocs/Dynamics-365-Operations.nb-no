---
title: Vurderingsprofiler
description: Dette emnet beskriver hvordan du setter opp data for vurderingsprofiler.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973966"
---
# <a name="rating-profiles"></a>Vurderingsprofiler

En vurderingsprofil ligner en logistikkontrakt (men ikke en gyldig kontrakt). Den brukes til å fastsette transporttariffer for last. 

Hver vurderingsprofil er unik for en transportør. I profilen kan du tilknytte transportøren til en vurderingsstandard. Vurderingsstandarden definerer tilordningen av satsgrunnlag og satsgrunnlaget. Satsgrunnlaget angir satsen til transportøren.

Du kan definere en vurderingsprofil ved hjelp av et generisk side som gir en oversikt over alle eksisterende vurderingsprofiler. Du kan også definere en vurderingsprofil direkte fra transportøren. I begge tilfeller er informasjonen du angir for vurderingsprofilen, den samme.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Opprette eller redigere en vurderingsprofil på Vurderingsprofiler-siden

På siden **Vurderingsprofiler** kan du se gjennom alle tilgjengelige vurderingsprofiler. Du kan også redigere eksisterende profiler og opprette nye profiler.

1. Gå til **Transportstyring \> Oppsett \> Vurdering \> Vurderingsprofil**.
1. Velg **Ny** i handlingsruten for å legge til en ny vurderingsprofil i rutenettet, eller velg **Rediger** for å redigere en eksisterende profil.
1. I raden for den nye eller eksisterende vurderingsprofilen angir du følgende felt:

    - **Vurderingsprofil** – Angi en unik identifikator (ID) for vurderingsprofilen.
    - **Navn** – Angi et beskrivende navn for vurderingsprofilen.
    - **Transportør** – Velg en transportør. Vurderingsprofilen du konfigurerer, vises også på **Transportører**-siden for den valgte transportøren.
    - **Område** og **Lager** – Velg et område og lager.
    - **Ratemotor** – Velg ratemotoren for vurderingsprofilen.
    - **Vurderingsstandard** – Velg vurderingsstandarden for vurderingsprofilen. Du kan bruke vurderingsstandarden til å definere en satsgrunnlagstype og et satsgrunnlag. Hvis du vil ha mer informasjon, kan du se [Definere vurderingsstandarder](set-up-rate-masters.md).
    - **Transittidmotor** – Velg transittidmotoren for vurderingsprofilen.
    - **Drivstoffindeks for transportør** – Velg vurderingsprofilens drivstoffindeks for transportør.
    - **Startdato og -klokkeslett for virkning** og **Sluttdato og -klokkeslett for virkning** – Definer perioden når vurderingsprofilen skal være aktiv.

1. Velg **Lagre** i handlingsruten.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Opprette en vurderingsprofil direkte på Transportører-siden

1. Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.
1. Velg en transportør i listen.
1. Velg **Ny** i hurtigfanen **Vurderingsprofiler** for å opprette en vurderingsprofil.
1. Angi feltene for den nye vurderingsprofilen. Disse feltene tilsvarer feltene på siden **Vurderingsprofiler**, som beskrevet i forrige del av dette emnet.

> [!NOTE]
> Profiler som opprettes på **Transportører**-siden, vises også på **Vurderingsprofiler**-siden.
