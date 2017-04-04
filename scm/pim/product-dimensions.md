---
title: Produktdimensjoner
description: "Det finnes fire produktdimensjoner - farge, konfigurasjon, størrelse og stil. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Produktdimensjoner

Det finnes fire produktdimensjoner - farge, konfigurasjon, størrelse og stil. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.

Produktdimensjoner er egenskaper som brukes til å identifisere en produktvariant. Du kan bruke kombinasjoner av produktdimensjoner til å definere produktvariantene. Du må definere minst én produktdimensjon for en produktstandard for å opprette en produktvariant.
Produktvarianter
----------------

Produktvarianter omtales også som varer. En vare er et materielt produkt, som ikke er det samme som en tjeneste. Det er også mulig å definere en mal for produktet med tjenestetypen. Når du bruker tjenestetypen, kan du angi produktvarianter som omfatter tjenester. Du kan for eksempel angi en produktstandard for konsulentarbeid og produktvarianter for arbeid som utføres av seniorkonsulenter og juniorkonsulenter.

## <a name="product-dimensions"></a>Produktdimensjoner
Følgende produktdimensjoner er tilgjengelige: konfigurasjon, farge, størrelse og stil. En produktvariant kan genereres basert på produkt-dimensjonsverdier.

Produkt dimensjoner verdier slik for eksempel størrelse, farge og stil som kan opprettes på den **størrelse**, **farge** og **stil** sider, som er tilgjengelig fra følgende steder: **behandling av produktinformasjon**&gt;**Setup**&gt;**dimensjon og variant grupper**&gt;**farger/størrelser/stiler**. Produktdimensjonsverdier for konfigurasjonsdimensjonen opprettes vanligvis ved hjelp av produktkonfiguratoren eller den dimensjonsbaserte konfiguratoren. Produktdimensjoner kan også opprettes og vedlikeholdes på **Produktdimensjoner**-siden, som er tilgjengelig fra følgende steder:
-   Klikk **produktinformasjonsbehandling**&gt;**produkter**&gt;**produktstandarder**. På den **handlingsruten**, klikker du **produktdimensjoner**.
-   Klikk **produktinformasjonsbehandling**&gt;**produkter**&gt;**alle produkter og produktstandarder**. Velg en produktstandard. På den **handlingsruten**, klikker du **produktdimensjoner**.
-   Klikk **produktinformasjonsbehandling**&gt;**utgitt produkter**. Velg en produktstandard. På den **handlingsruten**, klikker du **produkt**. I gruppen **Produktstandard** klikker du **Produktdimensjoner**.

Antallet varianter du kan opprette for en vare, er begrenset av antallet mulige kombinasjoner av produktdimensjoner.
| **Tips! **                                                                                                                                              |
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




