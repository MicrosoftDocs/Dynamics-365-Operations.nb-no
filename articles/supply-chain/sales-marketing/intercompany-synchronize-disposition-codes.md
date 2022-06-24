---
title: Synkronisere disposisjonskoder
description: Denne artikkelen forklarer synkronisering av disposisjonskoder for konsernintern handel
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905667"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Synkronisere konserninterne disposisjonskoder

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tilbyr en funksjon for tilordning av eksternt definerte disposisjonskoder til korresponderende interne disposisjonskoder for å støtte konsernintern retur. Når en konsernintern kjede settes opp, må disposisjonshandlingene i de to firmaene som er tilordnet hverandre, være like. Hvis de er forskjellige, vil synkroniseringsprosessen mislykkes.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Om disposisjonskoder for tretrinns direktereturer

Disposisjonskoder synkroniseres fra den konserninterne salgsordrelinjen til den opprinnelige salgsordrelinjen. Synkroniseringen har imidlertid bare én umiddelbar virkning på den opprinnelige salgsordrelinjen. Dette betyr at tillegg for linjer slettes basert på disposisjonskoden og tillegget som er definert i Firma A. Firma A er firmaet som oppretter returordren.

Alle disposisjonshandlinger støttes på den konserninterne salgsordrelinjen i en tretrinns direkteleveringskjede. I tilfeller der produktet returneres til kunden, bør du derimot bekrefte at leveringsadressen i returordren stemmer overens med kundeleveringsadressen som er angitt i den opprinnelige ordren.

> [!NOTE]
> Disposisjonskoder finnes ikke for bestillinger. Derfor må synkronisering av disposisjonskodene fra den konserninterne salgsordren til den opprinnelige returordren utføres fra salgsordre til salgsordre.

## <a name="replacing-returned-items"></a>Erstatte returnerte varer

Hvis en returnert vare erstattes, og en erstatningsordre tidligere er opprettet i Selskap B, kan disposisjonskode ikke velges og tilleggserstatningsordrer blir ikke opprettet ikke i Selskap A.

## <a name="rules-for-intercompany-direct-deliveries"></a>Roller for konserninterne direkte leveringer

Følgende generelle regler gjelder for opprinnelige returordrer i scenarioer som involverer konserninterne direkteleveringer:

- Hvis den underliggende disposisjonshandlingen på den opprinnelige salgsordrelinjen er Krediter og kasser, Krediter eller Returner til kunde, brukes kreditdisposisjonshandlingen. Handlingskoden Returner til kunde setter imidlertid nettobeløpet til 0 (null) på den eksisterende linjen og på den nylig synkroniserte linjen fra den konserninterne salgsordren. I tillegg synkroniseres aldri svinnlinjer. Når en linje legges til i en konsernintern salgsordre, blir den aldri synkronisert for en salgsordre som har et positivt antall og en disposisjonshandling for Svinn (for eksempel Krediter og kasser eller Erstatt og kasser).
- En underliggende disposisjon for handlingen Krediter og erstatt eller Kasser og erstatt overstyres ikke. Den behandles som disposisjon for handlingen Krediter og erstatt eller Kasser og erstatt. Denne regelen gjelder selv om ingen svinnlinje er opprettet i Selskap A og ingen erstatningsordre er opprettet i Selskap B (firmaet som mottok den returnerte varen). En erstatningsordre opprettes kun i Selskap A når oppdatering av følgeseddel er utført.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
