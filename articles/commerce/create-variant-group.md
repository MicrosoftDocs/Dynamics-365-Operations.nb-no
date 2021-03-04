---
title: Opprette en variantgruppe
description: Dette emnet beskriver hvordan du oppretter en størrelses-, stil- eller fargevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d9279e1076796bb455429e5ff004c89ec5829e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414642"
---
# <a name="create-a-variant-group"></a>Opprette en variantgruppe


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en størrelses-, stil- eller fargevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce støtter flere varianter for produkter. Det ideelle er å definere variantgrupper for forskjellige produktkategorier. En størrelsesgruppe kan for eksempel opprettes for t-skjorter med størrelser ekstra liten, liten, middels, stor og ekstra stor. Alternativt kan det opprettes en fargegruppe som inneholder alle tilgjengelige farger av et produkt. Variantgrupper må legges til før produkter legges til.

I dette emnet skal vi opprette og konfigurere en størrelsesgruppe. Lignende prosedyrer kan brukes til å legge til og konfigurere stilgrupper og fargegrupper.

## <a name="create-a-size-group"></a>Opprette en størrelsesgruppe

Hvis du vil opprette en størrelsesgruppe, følger du disse trinnene.
 
1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper**.
1. I handlingsruten velger du **Ny**.
1. I **Størrelsesgruppe**-boksen angir du et navn for størrelsesgruppen.
1. I **Beskrivelse**-boksen angir du en passende beskrivelse.
1. Velg **Lagre** i handlingsruten.

## <a name="add-attributes-to-the-size-group"></a>Legge til attributter i størrelsesgruppen

Bruk følgende fremgangsmåte for å legge til attributter i en størrelsesgruppe.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper**
1. Velg en størrelsesgruppe i navigasjonsruten.
1. Under **Størrelsesgruppelinjer** velger du **Legg til**.
1. I **Størrelse**-boksen angir du en streng som representerer størrelsen (for eksempel "XL").
1. I **Størrelsesnavn**-boksen angir du inn et navn på størrelsen (for eksempel "Ekstra stor").
1. I **Etterfyllingsvekt**-boksen angir du et nummer som representerer etterfyllingsvekten.
1. I **Nummer i strekkode**-boksen angir du et nummer som representerer strekkoden.
1. I **Visningsrekkefølge**-boksen angir du et nummer som representerer visningsrekkefølgen.
1. Når du er ferdig med å legge til størrelser, velger du **Lagre** i handlingsruten.

Det følgende bildet viser et eksempel på en størrelsesgruppe for "vanlige skjortestørrelser".

![Opprette størrelsesgruppe](media/create-variant-group.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktinformasjon](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Definere detaljhandelsprodukter](set-up-retail-products.md)

[Produktdimensjoner](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]