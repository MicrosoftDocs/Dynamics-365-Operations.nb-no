---
title: Garantier for eiendeler og anleggsmiddeltyper
description: Dette emnet forklarer hvordan du definerer garantier for aktiva og aktivatyper i Aktivastyring.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27a079e0fdc0fe1644e59a454659d77ec0eb416b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354210"
---
# <a name="warranties-on-assets-and-asset-types"></a>Garantier for eiendeler og anleggsmiddeltyper

[!include [banner](../../includes/banner.md)]

 


Dette emnet forklarer hvordan du definerer garantier for aktiva og aktivatyper i Aktivastyring.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Definere en garanti for en aktivatype

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktivatyper** \> **Aktivatyper**.
2. I venstre rute velger du anleggsmiddeltypen du vil knytte en leverandørgarantiavtale til, og deretter velger du **Standarder for aktivatype**.
3. Velg avtalen i **Leverandørgaranti**-feltet på hurtigfanen **Generelt**.

## <a name="set-up-a-warranty-on-an-asset"></a>Definere en garanti for et aktivum

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.
2. Velg anleggsmidlet, og velg deretter **Rediger**.
3. I hurtigfanen **Leverandør** i delen **Leverandørgaranti**, i feltet **Garanti**, velger du garantiavtalen.
4. Velg start- og sluttdatoer i feltene **Garantistart** og **Garantislutt**.

    > [!IMPORTANT]
    > Hvis en dato er valgt i **Garantistart**-feltet i en arbeidsordre, blir garantien gyldig for arbeidsordren på denne datoen. Når du oppretter en arbeidsordre, settes **Garantistart**-feltet automatisk til opprettelsesdatoen. Du kan imidlertid endre datoen slik at den tilsvarer for eksempel startdatoen for en garantiavtale.
    >
    > ![Siden Arbeidsordre.](media/02-warranty.png)

> [!NOTE]
> Når du oppretter en arbeidsordre for et anleggsmiddel som dekkes av en leverandørgaranti, får du en varsling om garantiavtalen hvis arbeidsordren har en forventet startdato i løpet av garantiperioden. Du kan deretter annullere arbeidsordren etter behov.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]