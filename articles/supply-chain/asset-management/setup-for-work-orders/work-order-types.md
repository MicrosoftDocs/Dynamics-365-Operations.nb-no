---
title: Arbeidsordretyper
description: Dette emnet forklarer arbeidsordretypene i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9111ffa552059883696cf8248a02dfe70bc12ee7
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021535"
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
