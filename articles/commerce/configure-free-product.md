---
title: Konfigurere et produkt som skal kjøpes gratis
description: Denne artikkelen beskriver hvordan du konfigurerer et produkt slik at det kan kjøpes gratis i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280371"
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
