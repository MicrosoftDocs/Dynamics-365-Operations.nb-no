---
title: Produkter og kategorier mangler etter miljøkopi
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801729"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Produkter og kategorier som mangler etter miljøkopi

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.

## <a name="description"></a>beskrivelse

Når et område kopieres fra ett miljø til et annet eller i samme miljø, mangler produktene og kategoriene fra området. Produktene og kategoriene mangler i e-handelbutikken og fra kategorien **Produkter** i Commerce-områdebyggeren.

## <a name="resolution"></a>Oppløsning

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Tilordne kanaldriftsenhetsnummeret til et nykopiert område i Commerce-områdebyggeren

Hvis du vil tilordne kanaldriftsenhetsnummeret (OUN) til et nykopiert område i Commerce-områdebyggeren, gjør du følgende.

1. Velg det nykopierte området.
1. Velg **Kanaler** under **Områdeinnstillinger**.
1. Ved siden av kanalnavnet velger du ellipsen (**...**), og deretter velger du **Endre kanal for nettbutikk**.
1. Velg kanalen du vil tilordne til det nykopierte området, i dialogboksen **Endre kanal for nettbutikk**, og velg deretter **OK**.
1. Velg **Lagre og publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](../associate-site-online-store.md)
