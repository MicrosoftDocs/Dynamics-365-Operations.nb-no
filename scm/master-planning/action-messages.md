---
title: udokumentert
description: En handlingsmelding er et systemgenerert forslag til endring av en eksisterende planlagt eller autorisert ordre.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c011ac5dbba5e98ff9f743237b02a69ea2b36a9d
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="action-messages"></a>Handlingsmeldinger

[!include[banner](../includes/banner.md)]


En handlingsmelding er et systemgenerert forslag til endring av en eksisterende planlagt eller autorisert ordre.

## <a name="introduction"></a>Innledning

Handlingsmeldinger genereres av hovedplanleggingsberegningen som svar på endrede krav. Forsendelsesdatoen eller antallet kan for eksempel være endret på en salgsordre som du allerede har opprettet en bestilling for slik at behovet kan dekkes. I så fall genereres én eller flere handlingsmeldinger av hovedplanleggingsberegningen for å oppdatere bestillingen. Du bestemmer om du vil gjøre endringene som foreslås.

Du kan konfigurere hvordan handlingsmeldinger skal beregnes for en dekningsgruppe som du legger ved en vare.

## <a name="select-action-messages"></a>Velge handlingsmeldinger

På **Dekningsgrupper**-siden kan du velge handlingsmeldingene som du vil at systemet skal generere, og dekningsgruppene eller -varene som meldingen gjelder for. Du kan velge følgende handlingsmeldinger:

| Melding             | Beskrivelse                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fremskynd**         | Hvis du velger denne meldingen, vil systemet generere handlingsmeldinger, når det er nødvendig, for å flytte ordrer til en tidligere dato. I feltet **Fremskyndingsmargin** kan du også angi maksimalt antall dager mellom mottak og avgang uten fremskyndelseshandling. |
| **Utsett**        | Hvis du velger denne meldingen, vil systemet generere handlingsmeldinger, når det er nødvendig, for å flytte ordrer til en senere dato. I feltet **Utsettelsesmargin** kan du også angi maksimalt antall dager mellom mottak og avgang uten utsettelseshandling.       |
| **Nedskriv**        | Hvis du velger denne meldingen, bør produksjonsordrer, bestillinger og andre mottakstransaksjoner reduseres for å unngå for store lagernivåer.                                                                                                   |
| **Oppskriv**        | Hvis du velger denne meldingen, bør produksjonsordrer, bestillinger og andre mottakstransaksjoner økes for å forhindre for lave lagernivåer.                                                                                                    |
| **Avledede handlinger** | Hvis du velger denne meldingen, opprettes handlingsmeldinger for avledede behov, for eksempel handlinger for komponentordrer som oppfyller produksjonen.                                                                                                   |






