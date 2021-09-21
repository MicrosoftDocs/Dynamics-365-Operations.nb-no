---
title: Evaluer alle handlinger for lokasjonsdirektiver med flere SKU-er
description: En ny funksjon er lagt til for å evaluere alle handlinger for lokasjonsdirektiver med flere SKU-er. På denne siden finner du informasjon om hvordan du aktiverer den.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477183"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Flere SKUer-alternativet evaluerer ikke flere lokasjonsdirektivhandlinger

## <a name="symptoms"></a>Symptomer

Lokasjonsdirektiver for *Salgsordre*-arbeidsordretypen og *Plasser*-arbeidstypen evaluerer ikke fler lokasjonsdirektivhandlinger når det **Flere SKU-er** er valgt. Bare den første lokasjonsdirektivhandlingen evalueres.

## <a name="resolution"></a>Løsning

En ny funksjon, *Evaluere alle handlinger for lokasjonsdirektiver med flere SKU-er*, er lagt til i versjon 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Denne funksjonen evaluerer alle handlinger for lokasjonsdirektiver med flere SKU-er. Hvis du trenger denne funksjonen, kan du bruke [Funksjonsbehandling](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til å aktivere den.
