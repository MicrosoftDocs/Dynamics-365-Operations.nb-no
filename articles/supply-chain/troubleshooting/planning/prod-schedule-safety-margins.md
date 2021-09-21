---
title: Produksjonsplanlegging tar ikke hensyn til sikkerhetsmarginene
description: Produksjonsplanlegging tar ikke hensyn til sikkerhetsmarginene som er angitt for varedekningen for tilknyttet forsyning
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477179"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Produksjonsplanlegging tar ikke hensyn til sikkerhetsmarginene

## <a name="symptoms"></a>Symptomer

Hovedplanleggingen anser sikkerhetsmarginene. Sikkerhetsmarginer ignoreres imidlertid når planlagte produksjonsordrer planlegges.

## <a name="resolution"></a>Løsning

Marger vurderes bare under hovedplanlegging, ikke under manuell planlegging. Marger er utformet for å fungere som en buffer i planleggingsfasen for å gi litt margin for den faktiske prosessen.

Hvis du vil oppnå ønsket resultat, kan du fjerne marginen. Ruten må deretter oppdateres slik at den inneholder ønsket tid (for eksempel køtid). Samtidig skal både hovedplanlegging og manuell planlegging gi samme resultat.
