---
title: Aktivaprodusenter og -modeller
description: Dette emnet forklarer hvordan du definerer aktivaprodusenter og beslektede modeller i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783495"
---
# <a name="asset-manufacturers-and-models"></a>Aktivaprodusenter og -modeller

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet forklarer hvordan du definerer aktivaprodusenter og beslektede modeller i Aktivastyring. Modeller kan være relatert til aktivatyper.

## <a name="set-up-product-model-relations"></a>Definere relasjoner mellom produkter og modeller

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Produsent og modell**.
2. Velg **Ny** for å opprette et nytt produkt.
3. I feltet **Produsent** angir du et navn på aktivaprodusenten.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. På hurtigfanen **Modeller** velger du **Legg til** for å opprette en aktivamodell som skal være relatert til aktivaprodusenten.
6. I feltet **Modell** angir du et navn på aktivamodellen.
7. Angi en beskrivelse i **Beskrivelse**-feltet.
8. I feltet **Aktivatype** velger du aktivatypen som produsentmodellen skal være knyttet til.

    > [!NOTE]
    > Du kan også definere relasjoner for aktivatyper, -produsenter og -modeller i oppslaget **Aktivatyper**. Hvis du vil ha mer informasjon, kan du se [Opprette aktivatype](../setup-for-objects/object-types.md).

    På hurtigfanen **Detaljer** viser **Modeller**-feltet antallet aktivamodeller som er definert for den valgte aktivaprodusenten. **Aktiva**-feltet viser antall aktiva som bruker den valgte produsenten.
    
    **Aktiva**-feltet viser antall objekter som bruker produsentmodellen.

> [!NOTE]
> En aktivatype kan ikke ha relasjoner mellom aktivaprodusent og -modell, den kan være relatert til én aktivaprodusentmodell, eller den kan være relatert til flere aktivaprodusentmodeller. Hvis en aktivatype er knyttet til minst én produsentmodell, kan bare kombinasjonene som er definert i oppslaget **Produsentmodell** velges på disse Aktivastyring-sidene, der en kombinasjon av en aktivatype, -produsent og -modell kan defineres. Disse sidene omfatter **Alle aktiva**, **Tjenestenivåer for aktiva**, **Jobbtypestandarder** og **Vedlikeholdsbudsjettlinjer**. Hvis enkelte aktivatyper ikke er knyttet til noen produsentmodell, vises bare disse aktivatypene og produsentmodellene som heller ikke har en relasjon til aktivatyper, på sidene.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Velge en produsent og modell på et objekt

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.
2. Velg koblingen for aktivumet i **Aktiva**-kolonnen. Siden **Detaljer** vises.
3. Velg **Rediger**.
4. På hurtigfanen **Generelt** velger du verdier i feltene **Produsent** og **Modell**.