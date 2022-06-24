---
title: Administrere produktkategorier og produkter
description: Denne artikkelen beskriver hvordan forhandleransvarlige kan bruke produktkategorier til å styre relasjoner mellom hierarkiet for Commerce-produkt og detaljer om frigitt produkt.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0871475e0910e0a46544c56083b505ff647fd6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878589"
---
# <a name="manage-product-categories-and-products"></a>Administrere produktkategorier og produkter

[!include [banner](./includes/banner.md)]

Denne artikkelen beskriver en utvidet måte å administrere produktkategorier og produkter i Dynamics 365 Commerce. Forbedringene lar forhandleransvarlige se en struktur av produktegenskaper som deles mellom hierarkiet for produkt og detaljer om frigitt produkt.

Hvis du vil lære mer om hvordan du administrerer produktkategorier, velger du flisen **Hierarki for Commerce-produkt** i **Kategori- og produktstyring**-arbeidsområdet.

Legg merke til den utvidede strukturen for **Hierarki for Commerce-produkt**-siden som vises. I tidligere utgaver av appen, ble produktegenskaper delt inn i *grunnleggende produktegenskaper* og *Detaljhandelproduktegenskaper*, basert på omfanget av anvendelighet. Egenskaper for detaljhandelprodukt er *globale* basert på deres relevans. Med andre ord fordeles samme verdi på alle juridiske enheter for en gitt produktegenskap. Grunnleggende produktegenskaper derimot er *spesifikk for hver juridiske enhet*. Med andre ord kan en gitt grunnleggende produktegenskap være forskjellig på tvers av juridiske enheter, avhengig av individuelle forretningsbehov til hver juridiske enhet.

I den utvidede strukturen for produktkategorien, er produktegenskapene atskilt basert på deres anvendelighet i en gruppe, for å gjenspeile skjemastrukturen til detaljer om frigitt produkt.

![Felt gruppert basert på egenskapenes relevans.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet.

Hvis du vil behandle egenskaper på tvers av alle juridiske enheter, velger du **Vis for alle juridiske enheter** (eller **Rediger for alle juridiske enheter**).

![Vise/redigere for alle juridiske enheter.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Hvis du vil behandle egenskapene for en bestemt juridisk enhet, velger du **Vis for en bestemt juridisk enhet** (eller **Rediger for en bestemt juridisk enhet**).

![Vise/redigere for en bestemt juridisk enhet.](media/ToggleToEditForAllLegalEntities.PNG)

I den forbedrede strukturen for produktkategorien kan en varehandelsleder nå også definere standardverdier for et ekstra sett med produktegenskaper på nivået av den individuelle kategorien. Når produktene da opprettes, arver de standardverdiene for produktegenskapene, basert på tilknytningen til disse egenskapene med en individuell kategori i hierarkiet for produkt. Disse arvede produktegenskaper kan endres for hvert produkt slik at de passer til individuelle forretningsbehov.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Velge egenskaper for å oppdatere produkter på siden for hierarki for Commerce-produkt

Du kan bruke den nye utvidede strukturen for produktegenskaper til å velge oppdaterte produktegenskaper som må overføres til tilknyttede produkter. På **Hierarki for Commerce-produkt**-siden i handlingsruten, velger du **Kategori** og deretter **Oppdater produkter** for å åpne **Oppdater produkter**-dialogboksen.

![Dialogboksen Oppdater produkter.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]