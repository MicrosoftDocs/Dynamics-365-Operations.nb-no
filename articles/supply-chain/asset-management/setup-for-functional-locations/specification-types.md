---
title: Vedlikeholdsattributtyper
description: Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 067d1085d9afa04cb76b78393a8a8b9834ce4d8c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250950"
---
# <a name="maintenance-attribute-types"></a>Vedlikeholdsattributtyper

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring. Attributter brukes til å beskrive egenskapene til ulike elementer. Du kan angi attributter for følgende elementer:

- [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md)
- [Arbeidssteder](../functional-locations/create-functional-locations.md)
- [Aktivatyper](../setup-for-objects/object-types.md)
- Aktiva

Attributtene du kan definere, varierer avhengig av elementet. Hvis du for eksempel vil ha et arbeidssted, kan du definere attributter for konfigurasjonen og den fysiske størrelsen på stedet. For en aktivatype eller et aktivum kan du definere attributter for motorvolum, strømforbruk og maksimal lastekapasitet under ulike forhold.

## <a name="create-attribute-types"></a>Opprette attributtyper

Du kan opprette dine egne attributtyper. I tillegg kan du overføre produktdimensjoner til siden **Attributtyper**.

1. Velg **Aktivastyring** \> **Oppsett** \> **Attributtyper**.
2. Første gang du definerer attributtverdier, velger du **Opprett produktdimensjoner** for å overføre standard produktdimensjoner automatisk.
3. Velg **Ny** for å opprette en ny attributtype.
4. I **Attributtype**-feltet angir du et navn på attributtypen.
5. Angi en beskrivelse i **Beskrivelse**-feltet.
6. I **Enhet**-feltet velger du den aktuelle attributtenheten etter behov.
7. I **Datatype**-feltet velger du en datatype for enheten.
8. Hvis du valgte **Streng** som datatype, følger du denne fremgangsmåten for å opprette verdier for attributtypen:

    1. Velg attributtypen, og velg deretter **Verdier**.
    2. I **Attributtverdier**-feltet velger du **Ny**.
    3. Velg en attributtype (dimensjon) i **Attributtype**-feltet.
    4. Angi en relatert verdi i feltet **Verdi**.
    5. Angi en beskrivelse i **Beskrivelse**-feltet.
    6. Lagre posten.
    7. Gå tilbake til siden **Attributtyper**.

9. Lagre posten.

    Feltet **Arbeidsstedstyper** viser antall arbeidssteder som bruker attributtypen. Feltet **Aktivatyper** viser antall aktivatyper som bruker den.
