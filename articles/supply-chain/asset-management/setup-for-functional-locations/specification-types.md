---
title: Vedlikeholdsattributtyper
description: Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 283cff931ce665ae09152c8f3d3c976b7c8b66ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808526"
---
# <a name="maintenance-attribute-types"></a>Vedlikeholdsattributtyper

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring. Attributter brukes til å beskrive egenskapene til ulike elementer. Du kan angi attributter for følgende elementer:

- [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md)
- [Opprette arbeidssteder](../functional-locations/create-functional-locations.md)
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]