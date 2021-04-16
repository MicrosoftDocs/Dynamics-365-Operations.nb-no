---
title: Arbeidsordretyper
description: Dette emnet forklarer arbeidsordretypene i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6bdc9d226d8e1aa6960cac38b95b0245e46ee1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825596"
---
# <a name="work-order-types"></a>Arbeidsordretyper

[!include [banner](../../includes/banner.md)]

 

Arbeidsordretyper brukes til å kategorisere arbeidsordrer. Du kan for eksempel ha arbeidsordrer som er knyttet til forebyggende vedlikehold eller korrigerende vedlikehold.

En arbeidsordretype definerer en tilknytning til en livssyklusmodell for arbeidsordrer. En livssyklusmodell for arbeidsordre definerer livssyklustilstandene for arbeidsordre som kan angis i en arbeidsordre. (Eksempler på livssyklustilstander for arbeidsordre inkluderer **Opprettet**, **Pågår** og **Avsluttet**.)

Hvis du vil ha mer informasjon om livssyklustilstander for arbeidsordrer og prosjektstadier, kan du se [i Livssyklustilstand for arbeidsordre](work-order-lifecycle-states.md).

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Arbeidsordretyper**.
2. Velg **Ny** for å opprette en ny arbeidsordretype.
3. Angi en ID for arbeidsordretypen i feltet **Arbeidsordretype**.
4. Angi et navn i **Navn**-feltet.
5. Velg en livssyklusmodell i feltet **Livssyklusmodell for arbeidsordre**.
5. Sett alternativet **Én vedlikeholdsperson** til **Ja** hvis alle arbeidsordrejobber som er relatert til en arbeidsordre av denne typen, skal planlegges til samme vedlikeholdsperson.
6. I **Kostnadstype**-feltet velger du **Korrektiv**, **Forebyggende** eller **Investering** etter behov. Alle arbeidsordrejobber i en arbeidsordre må ha samme kostnadstype.
7. I **Obligatorisk**-delen setter du de relevante alternativene til **Ja** for å angi hvilken feilrelatert eller vedlikeholdsnedetidrelatert informasjon som legges til en arbeidsordre av denne typen.

    > [!NOTE]
    > Alternativene i **Obligatorisk**-delen er knyttet til alternativene i hurtigfanen **Valider** på siden **Livssyklustilstand for arbeidsordre** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklustilstander**).

8. Velg **Lagre**.

![Arbeidsordretyper](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]