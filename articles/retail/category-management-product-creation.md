---
title: Produktkategoristyring
description: "Dette emnet beskriver hvordan forhandleransvarlige kan bruke produktkategorier for detaljhandel til å styre relasjoner mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: nb-no
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Utvidet kategori- og produktstyring

[!include[banner](./includes/banner.md)]

Dette emnet beskriver en utvidet måte å administrere produktkategorier for detaljhandel og produkter i Dynamics 365 for Retail. Disse forbedringene lar forhandleransvarlige se en vanlig struktur av produktegenskaper mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt.

Hvis du vil vite mer om hvordan du behandler produktkategorier for detaljhandel, kan du gå til **Hierarki for detaljhandelprodukt** fra arbeidsområdet **Kategori- og produktstyring** og se på den utvidete strukturen for **Detaljhandelproduktkategori**-siden.

![Arbeidsområdet kategori- og produktstyring](media/LaunchRetailProductHierarchy.png)

I tidligere utgaver ble produktegenskaper delt inn i **Grunnleggende produktegenskaper** og **Detaljhandelproduktegenskaper**, basert på omfanget av anvendelighet. **Produktegenskaper for detaljhandel** ble *globale* basert på deres relevans, noe som betyr at for en gitt **Produktegenskap for detaljhandel**, er den samme verdien lik på tvers av alle juridiske enheter. **Grunnleggende produktegenskaper** er *spesifikk for hver juridiske enhet*. Med andre ord kan en gitt **grunnleggende produktegenskap** være forskjellig på tvers av juridiske enheter, basert på individuelle forretningsbehov.

I den utvidede strukturen for detaljhandelproduktkategorien, er produktegenskapene atskilt basert på deres anvendelighet innen en gruppe, for å gjenspeile skjemastrukturen til detaljer om frigitt produkt.

![Gruppering av felt basert på deres relevans](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet. Du gjør dette ved å velge enten **Se/rediger for alle juridiske enheter** eller **Se/rediger for en spesifikk juridisk enhet**.

![Veksle mellom visning for en enkel eller alle juridiske enheter](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Veksle mellom visning for en enkel eller alle juridiske enheter](media/ToggleToEditForAllLegalEntities.PNG)  

Sammenlignet med i tidligere versjoner, kan en varehandelsleder i den nye strukturen for detaljhandelproduktkategorien nå også definere standardverdier for et ekstra sett med egenskaper på nivået av en enkelt kategori. Ved produktoppretting arves disse standardverdiene for produktegenskaper av et produkt, basert på tilknytningen til en individuell kategori fra hierarkiet for detaljhandelprodukt. Disse arvede produktegenskaper kan endres for hvert produkt slik at de passer til individuelle forretningsbehov.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Velg egenskaper for å oppdatere produkter fra skjemaet for detaljert produktkategori 
 
Du kan bruke denne nye utvidede strukturen for produktegenskaper til å velge hvilke produktegenskaper må overføres til tilknyttede produkter. 

![Ny utvidet visning av Oppdater produkter](media/NewUpdateProductsEnhancedView.PNG) 

Forhandleransvarlige kan endre disse arvede produktegenskaper for hvert produkt for å møte individuelle forretningsbehov.


