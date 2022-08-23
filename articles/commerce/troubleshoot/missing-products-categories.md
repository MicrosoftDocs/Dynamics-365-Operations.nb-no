---
title: Produkter og kategorier mangler etter miljøkopi
description: Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8df3f4cca6a7aaad98ffb7f2d284211a4f9589b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277913"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Produkter og kategorier som mangler etter miljøkopi

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.

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
