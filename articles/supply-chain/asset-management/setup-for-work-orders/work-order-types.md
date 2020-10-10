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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888791"
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
5. Velg en livsløpsmodell i feltet **Livsløpsmodell for arbeidsordre**.
5. Sett alternativet **Én vedlikeholdsperson** til **Ja** hvis alle arbeidsordrejobber som er relatert til en arbeidsordre av denne typen, skal planlegges til samme vedlikeholdsarbeider.
6. I **Kostnadstype**-feltet velger du **Korrektiv**, **Forebyggende**eller **Investering** etter behov. Alle arbeidsordrejobber i en arbeidsordre må ha samme kostnadstype.
7. I **Obligatorisk**-delen setter du de relevante alternativene til **Ja** for å angi hvilken feilrelatert eller vedlikeholdsnedetidrelatert informasjon som legges til en arbeidsordre av denne typen.

    > [!NOTE]
    > Alternativene i **Obligatorisk**-delen er knyttet til alternativene i hurtigfanen **Valider** på siden **Livssyklustilstand for arbeidsordre** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklustilstander**).

8. Velg **Lagre**.

![Arbeidsordretyper](media/16-setup-for-work-orders.png)
