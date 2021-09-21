---
title: Antallet er ugyldig for enheten %1 når det utføres en delingsplukking
description: Når du utfører en delingsplukking på tvers av flere partier, kan det hende du får en feilmelding om at antallet ikke er gyldig for enheten %1. Denne siden er med på å løse problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477157"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>Antallet er ugyldig når det utføres en delingsplukking på tvers av flere partier

## <a name="symptoms"></a>Symptomer

Du får denne feilmeldingen når du prøver å utføre en *delt plukking* på tvers av flere partier:

> Antallet er ikke gyldig for enheten %1.

## <a name="resolution"></a>Løsning

Lagerarbeideren må bruke *Plukking med mangler*-prosessen i Warehouse Management-mobilappen. Hvis du prøver å plukke flere partier fra samme lokasjon, kan du også bruke **Fullstendig**-alternativet i appen.
