---
title: Endre sorteringsrekkefølgen for varehandelsenheter
description: I denne artikkelen forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter i Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265843"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Endre sorteringsrekkefølgen for varehandelsenheter


[!Include [banner](includes/banner.md)]

Forhandlere vurderer produktgjenkjenning som et primært verktøy for kundeinteraksjon på tvers av alle kanaler. Det er flere funksjoner som kan hjelpe kundene med å oppdage produkter på en enkel måte. Kunder kan for eksempel bla gjennom kategorier, søke og filtrere.

I denne artikkelen forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter. Det forklarer også hvordan du endrer sorteringsrekkefølgen.

## <a name="overview"></a>Oversikt

I Commerce justeres sorteringen av ulike enheter som gjelder handelsrelaterte enheter, med eksisterende kundescenarioer, og det kreves ikke lenger utvidelser fra implementeringspartnere.

I Commerce versjoner 10.0.5 og tidligere var sorteringsrekkefølgen for kategorier i navigasjonshierarkiet alfabetisk. Den nåværende funksjonen for sorteringsrekkefølge gjør at ledere kan konfigurere sorteringsrekkefølgen for ulike varehandelsrelaterte enheter på tvers av alle sluttbrukerklienter. Disse klientene inkluderer hovedkontorer og telefonsentre.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Konfigurer visningsrekkefølgen for kategorier i produkthierarkiet

Før du kan fullføre denne prosedyren, må du installere demodata i miljøet.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Handelsprodukthierarki**.
2. Klikk **Rediger kategorihierarki**.
3. Klikk **Rediger**.
4. Utvid **ALL \> Action Sports** i treet.
5. Utvid **ALL \> Team Sports** i treet.
6. Angi et tall i **Visningsrekkefølge**-feltet. (Nummeret kan være negativt.)
7. Gjenta trinn 4 til og med 6 for eventuelle tilleggskategorier du vil endre rekkefølgen på.

Visningsrekkefølgen for kanalnavigasjonshierarkiet vil gjenspeiles i hovedkontoret for handelsprodukthierarkiet og frigitte produkter etter kategori.

![Egendefinert sortering av produkthierarki med negative verdier.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Egendefinert sortering av frigitte produkter etter kategori basert på produkthierarkiet.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurer visningsrekkefølgen for kategorier i kanalnavigasjonshierarkiet

Før du kan fullføre denne prosedyren, må du installere demodata i miljøet.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Navigasjonskategorier for kanal**.
2. I listen velger du **navigasjonshierarkiet for klær**.
3. Klikk **Rediger kategorihierarki**.
4. Klikk på **Rediger**.
5. Velg **Fashion \> Womenswear \> Women's Shoes** i treet.
6. Angi et tall i **Visningsrekkefølge**-feltet.
7. Velg **Fashion \> Womenswear \> Tops** i treet.

På samme måte kan du definere sorteringsrekkefølgen for underkategoriene.

8. Velg **Fashion \> Menswear \> Casual Shirts** i treet.
9. Angi et tall i **Visningsrekkefølge**-feltet.
10. Velg **Fashion \> Menswear \> Coats & Jackets** i treet.
11. Angi et tall i **Visningsrekkefølge**-feltet.
12. Gjenta for eventuelle tilleggskategorier du vil endre rekkefølgen på.

Visningsrekkefølgen for kanalnavigasjonshierarkiet gjenspeiles i hovedkontor, katalog og kanaler.

![Egendefinert sortering av navigasjonshierarki for kanal.](./media/ChannelNavCustomSorted.png)

![Egendefinert sortering av navigasjonshierarki for katalog basert på kanalnavigasjonshierarkiet.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Salgssted med egendefinert sortering av kategorier.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Som standard er funksjonen **Aktiver visningsrekkefølge for handelsenheter** slått av. Bruk [Funksjonsbehandling](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere den. Når du aktiverer funksjonen, kjører du **Global konfigurasjon -1110** CDX-jobben fra distribusjonsplanen.
> Hvis kategorirekkefølgen i salgsstedet ikke oppdateres, aktiverer du enheten på nytt. Kategoriinformasjon hentes når enhetsaktiveringen utføres, så enheten må kanskje fylle ut kategoriinformasjonen på nytt med oppdaterte visningsordrer. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
