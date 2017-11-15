---
title: Produktdimensjoner
description: "Det finnes fire produktdimensjoner – farge, konfigurasjon, størrelse og stil. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 105324f146f28bc61e87dff1089b367958ff9062
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="product-dimensions"></a>Produktdimensjoner

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


Det finnes fire produktdimensjoner – farge, konfigurasjon, størrelse og stil. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.

Produktdimensjoner er egenskaper som brukes til å identifisere en produktvariant. Du kan bruke kombinasjoner av produktdimensjoner til å definere produktvariantene. Du må definere minst én produktdimensjon for en produktstandard for å opprette en produktvariant.
Produktvarianter
----------------

Produktvarianter omtales også som varer. En vare er et materielt produkt, som ikke er det samme som en tjeneste. Det er også mulig å definere en produktstandard tjenestetypen. Når du bruker tjenestetypen, kan du angi produktvarianter som omfatter tjenester. Du kan for eksempel angi en produktstandard for konsulentarbeid og produktvarianter for arbeid som utføres av seniorkonsulenter og juniorkonsulenter.

## <a name="product-dimensions"></a>Produktdimensjoner
Følgende produktdimensjoner er tilgjengelige: konfigurasjon, farge, størrelse og stil. En produktvariant kan genereres basert på produktdimensjonsverdiene.

Produktdimensjonsverdier som størrelse, farge og stil kan opprettes på sidene **Størrelse**, **Farge** og **Stil**, som er tilgjengelige fra følgende steder: **Produktinformasjonsbehandling** &gt; **Oppsett** &gt; **Dimensjons- og variantgrupper** &gt; **Størrelser/farger/stiler**. Produktdimensjonsverdier for konfigurasjonsdimensjonen opprettes vanligvis ved hjelp av produktkonfiguratoren eller den dimensjonsbaserte konfiguratoren. Produktdimensjoner kan også opprettes og vedlikeholdes på **Produktdimensjoner**-siden, som er tilgjengelig fra følgende steder:
-   Klikk på **Produktinformasjonsbehandling** &gt; **Produkter** &gt; **Produktstandarder**. I **handlingsruten** klikker du på **Produktdimensjoner**.
-   Klikk på **Produktinformasjonsbehandling** &gt; **Produkter** &gt; **Alle produkter og produktstandarder**. Velg en produktstandard. I **handlingsruten** klikker du på **Produktdimensjoner**.
-   Klikk på **Behandling av produktinformasjon** &gt; **Frigitte produkter**. Velg en produktstandard. I **handlingsruten** klikker du på **Produkt**. I gruppen **Produktstandard** klikker du **Produktdimensjoner**.

Antallet varianter du kan opprette for en vare, er begrenset av antallet mulige kombinasjoner av produktdimensjoner.
| **Tips!**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Når du for eksempel bruker et produkt på en ordrelinje, velger du produktdimensjonene for å identifisere produktvarianten du vil arbeide med. |

## <a name="example"></a>Eksempel
Et firma selger dongeribukser. Varen dongeribukser bruker produktdimensjonene Farge og Størrelse. Dongeribuksene selges i tre forskjellige farger og seks forskjellige størrelser. Farger: blå, svart, brun, Størrelser: XS, S, M, L, XL, XXL, ikke alle størrelser er tilgjengelige i alle tre fargene. Hvis alle kombinasjonene hadde vært tilgjengelige, hadde det blitt opprettet 18 forskjellige typer dongeribukser. I dette eksemplet produseres bare de følgende ni produktvariantkombinasjonene.

| Farge | Størrelse |
|-------|------|
| Blå  | XS   |
| Blå  | L    |
| Blå  | M    |
| Svart | M    |
| Svart | L    |
| Svart | XL   |
| Brun | L    |
| Brun | XL   |
| Brun | XXL  |






