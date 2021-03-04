---
title: Endre sorteringsrekkefølgen for varehandelsenheter
description: I dette emnet forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414651"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Endre sorteringsrekkefølgen for varehandelsenheter


[!include [banner](includes/banner.md)]

Forhandlere vurderer produktgjenkjenning som et primært verktøy for kundeinteraksjon på tvers av alle kanaler. Forskjellige funksjoner kan hjelpe kunder å oppdage produkter på en enkel måte. De kan for eksempel bla gjennom kategorier, søke og filtrere.

I dette emnet forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter. Det forklarer også hvordan du endrer sorteringsrekkefølgen.

## <a name="overview"></a>Oversikt

Støtten for sortering av ulike varehandelsrelaterte enheter er forbedret. Denne støtten er nå bedre justert med eksisterende kundescenarier som tidligere krevde utvidelser fra implementeringspartnere.

I versjoner av Retail som er tidligere enn versjon 10.0.5, var sorteringsrekkefølgen for kategorier i navigasjonshierarkiet alfabetisk. Den nye egendefinerte funksjonen for sorteringsrekkefølge gjør at ledere kan konfigurere sorteringsrekkefølgen for ulike varehandelsrelaterte enheter på tvers av alle sluttbrukerklienter. Disse klientene inkluderer hovedkontorer og telefonsentre.

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

![Egendefinert sortering av produkthierarki med negative verdier](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Egendefinert sortering av frigitte produkter etter kategori basert på produkthierarkiet](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurer visningsrekkefølgen for kategorier i kanalnavigasjonshierarkiet

Før du kan fullføre denne prosedyren, må du installere demodata i miljøet.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Navigasjonskategorier for kanal**.
2. I listen velger du **navigasjonshierarkiet for klær**.
3. Klikk **Rediger kategorihierarki**.
4. Klikk **Rediger**.
5. Velg **Fashion \> Womenswear \> Womens Shoes** i treet.
6. Angi et tall i **Visningsrekkefølge**-feltet.
7. Velg **Fashion \> Womenswear \> Tops** i treet.

    På samme måte kan du definere sorteringsrekkefølgen for under kategoriene.

8. Velg **Fashion \> Menswear \> Casual Shirts** i treet.
9. Angi et tall i **Visningsrekkefølge**-feltet.
10. Velg **Fashion \> Menswear \> Coats & Jackets** i treet.
11. Angi et tall i **Visningsrekkefølge**-feltet.
12. Gjenta for eventuelle tilleggskategorier du vil endre rekkefølgen på.

Visningsrekkefølgen for kanalnavigasjonshierarkiet gjenspeiles i hovedkontor, katalog og kanaler.

![Egendefinert sortering av navigasjonshierarki for kanal](./media/ChannelNavCustomSorted.png)

![Egendefinert sortering av navigasjonshierarki for katalog basert på kanalnavigasjonshierarkiet](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Salgssted med egendefinert sortering av kategorier](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Funksjonen for egendefinert sortering er deaktivert som standard. Hvis du vil vite hvordan du aktiverer denne funksjonen og andre funksjoner, kan du se [Funksjonsbehandling](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]