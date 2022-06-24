---
title: Konfigurere et produkt som skal kjøpes gratis
description: Denne artikkelen beskriver hvordan du konfigurerer et produkt slik at det kan kjøpes gratis i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890361"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurere et produkt som skal kjøpes gratis

[!include [banner](includes/banner.md)]


Denne artikkelen beskriver hvordan du konfigurerer et produkt slik at det kan kjøpes gratis i Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Konfigurere produktet

Hvis du vil selge et produkt gratis i Dynamics 365 Commerce, må du sette prisen til 0 (null). I tillegg må du konfigurere innstillingen **Nullpris gyldig**.

Følg denne fremgangsmåten for å konfigurere **Nullpris gyldig**-innstillingen i Commerce headquarters.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Utgitte produkter etter kategori**.
1. Gå til produktet du vil selge gratis. 
1. Sett **Nullpris gyldig**-alternativet til **Ja** i **Commerce**-delen på produktsiden.

Illustrasjonen nedenfor viser et eksempel på et produkt der alternativet **Nullpris gyldig** er satt til **Ja**.

![Eksempel på et produkt der alternativet Nullpris gyldig er satt til Ja.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Konfigurere funksjonalitetsprofilen for online-butikken

Før gratistransaksjoner kan behandles, må du konfigurere innstillingen **Tillat utsjekking uten betalinger** for funksjonalitetsprofilen for butikken, slik at transaksjoner som ikke har betalinger, er tillatt. Hvis du vil ha mer informasjon om hvordan du oppretter funksjonalitetsprofiler, kan du se [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md).

Følg denne fremgangsmåten for å konfigurere **Tillat utsjekking uten betalinger**-innstillingen i Commerce headquarters.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk**.
1. På siden for butikkens funksjonalitetsprofil, under **Utsjekking**, angir du alternativet **Tillat utsjekking uten betalinger** til **Ja**.

Illustrasjonen nedenfor viser et eksempel på en butikkprofil der alternativet **Tillat betaling uten betalinger** er satt til **Ja**.

![Eksempel på en butikkprofil der alternativet Tillat utsjekking uten betalinger er satt til Ja.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Salgsprisbehandling for detaljhandel](price-management.md)

[Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
