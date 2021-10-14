---
title: Synkronisere konserninterne tillegg
description: Dette emnet forklarer synkronisering av konserninterne tillegg
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4854b698c8046fc603454c4d9d7059c938c70b3
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548450"
---
# <a name="synchronize-intercompany-charges"></a>Synkronisere konserninterne tillegg

[!include [banner](../../includes/banner.md)]

Tillegg synkroniseres bare mellom den konserninterne salgsordren og den konserninterne bestillingen, og synkronisering skjer alltid.

Hvis det er merket av for **Tillat prisredigering**-feltet i den konserninterne bestillingen eller den konserninterne salgsordren, kan du legge til et tillegg manuelt i den konserninterne salgsordren eller den konserninterne bestillingen. Hvis ikke kan du ikke det.

Hvis det ikke er merket av for **Tillat prisredigering**-feltet i den konserninterne salgsordren, kan du ikke legge til et tillegg manuelt i den konserninterne salgsordren.

Hvis det ikke er merket av for **Tillat prisredigering**-feltet i den konserninterne bestillingen, kan du ikke legge til et tillegg manuelt i den konserninterne bestillingen.

Hvis feltet **Tillat prisredigering** er aktivert i både den konserninterne bestillingen og salgsordren, kan du legge til tillegg manuelt i begge ordrene. Dette kan imidlertid føre til at mange tillegg legges til feil.

Den anbefalte fremgangsmåten for å unngå denne typen konflikter, er å tillate at tillegg legges til i enten den konserninterne salgsordren eller i den konserninterne bestillingen, men ikke begge deler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
