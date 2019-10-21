---
title: Administrere produktkategorier for detaljhandel og produkter
description: Dette emnet beskriver hvordan forhandleransvarlige kan bruke produktkategorier for detaljhandel til å styre relasjoner mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 27870fe6172479b891b885d9e84ca10b250e3399
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019515"
---
# <a name="manage-retail-product-categories-and-products"></a>Administrere produktkategorier og produkter for detaljhandel

[!include [banner](./includes/banner.md)]

Dette emnet beskriver en utvidet måte å administrere produktkategorier og produkter i Dynamics 365 Retail. Forbedringene lar forhandleransvarlige se en struktur av produktegenskaper som deles mellom hierarkiet for produkt og detaljer om frigitt produkt.

Hvis du vil lære mer om hvordan du administrerer produktkategorier, velger du flisen **Hierarki for detaljhandelprodukt** i **Kategori- og produktstyring**-arbeidsområdet.

Legg merke til den utvidede strukturen for **Hierarki for detaljhandelprodukt**-siden som vises. I tidligere utgaver av detaljhandel, ble produktegenskaper delt inn i *grunnleggende produktegenskaper* og *Detaljhandelproduktegenskaper*, basert på omfanget av anvendelighet. Egenskaper for detaljhandelprodukt er *globale* basert på deres relevans. Med andre ord fordeles samme verdi på alle juridiske enheter for en gitt produktegenskap. Grunnleggende produktegenskaper derimot er *spesifikk for hver juridiske enhet*. Med andre ord kan en gitt grunnleggende produktegenskap være forskjellig på tvers av juridiske enheter, avhengig av individuelle forretningsbehov til hver juridiske enhet.

I den utvidede strukturen for produktkategorien, er produktegenskapene atskilt basert på deres anvendelighet i en gruppe, for å gjenspeile skjemastrukturen til detaljer om frigitt produkt.

![Felt gruppert basert på egenskapenes relevans](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet.

Hvis du vil behandle egenskaper på tvers av alle juridiske enheter, velger du **Vis for alle juridiske enheter** (eller **Rediger for alle juridiske enheter**).

![Vise/redigere for alle juridiske enheter](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Hvis du vil behandle egenskapene for en bestemt juridisk enhet, velger du **Vis for en bestemt juridisk enhet** (eller **Rediger for en bestemt juridisk enhet**).

![Vise/redigere for en bestemt juridisk enhet](media/ToggleToEditForAllLegalEntities.PNG)

I den forbedrede strukturen for detaljhandelproduktkategorien kan en varehandelsleder nå også definere standardverdier for et ekstra sett med produktegenskaper på nivået av den individuelle kategorien. Når produktene da opprettes, arver de standardverdiene for produktegenskapene, basert på tilknytningen til disse egenskapene med en individuell kategori i hierarkiet for produkt. Disse arvede produktegenskaper kan endres for hvert produkt slik at de passer til individuelle forretningsbehov.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Velge egenskaper for å oppdatere produkter på siden for hierarki for detaljhandelprodukt

Du kan bruke den nye utvidede strukturen for produktegenskaper til å velge oppdaterte produktegenskaper som må overføres til tilknyttede produkter. På **Hierarki for detaljhandelprodukt**-siden i handlingsruten, velger du **Kategori** og deretter **Oppdater produkter** for å åpne **Oppdater produkter**-dialogboksen.

![Dialogboksen Oppdater produkter](media/NewUpdateProductsEnhancedView.PNG)
