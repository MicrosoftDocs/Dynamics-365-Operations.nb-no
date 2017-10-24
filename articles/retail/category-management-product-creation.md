---
title: Produktkategoriledelse og opprettelse
description: Dette emnet beskriver forbedringene som er gjort i ledelseserfaringen for produktkategorier for detaljhandel. Disse forbedringene lar forhandleransvarlige ha en sammenheng mellom detaljprodukthierarkiet og utgitte produktdetaljer.
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: nb-no
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a>Produktkategoriledelse og opprettelse

[!include[banner](./includes/banner.md)]

Forbedringer som er gjort i ledelseserfaring for produktkategorier for detaljhandel, gjør det mulig for forhandleransvarlige å ha en sammenheng mellom produkthierarkiet for detaljhandel og utgitte produktdetaljer. For å se disse forbedringene i arbeidsområdet **Kategori og produkadminsitrasjon**, velg **Produkthierarki for detalhandel** for å åpne siden **Ny struktur for produktkategori for detaljhandel**. 

I tidligere utgaver ble produktegenskaper delt inn i Grunnleggende produktegenskaper og Detaljhandelproduktegenskaper, basert på omfanget av anvendelighet. Detaljhandelprodukters egenskaper var *globale*. Med andre ord, for en gitt produktegenskap, deles samme verdi over alle juridiske enheter. Basisproduktegenskaper var *juridisk enhetsspesifikke*. Med andre ord kan en gitt produktegenskap være forskjellig på tvers av juridiske enheter, basert på individuelle forretningsbehov.

Med disse forbedringene, for produktegenskaper i produktkategorien Detaljhandel, fortsetter vi å skille feltene, basert på deres anvendelighet innen en gruppe, for å gjenspeile den formelle strukturen for produktdetaljer.

Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet. Bare vel **Se/rediger for alle juridiske enheter** eller **Se/rediger for en spesifikk juridisk enhet** etter behov.

Forhandleransvarlige kan også definere standardverdier for et ekstra sett med produktegenskaper på nivået av en enkelt kategori. Disse egenskapsverdiene er arvet av et produkt, basert på deres tilknytning til en kategori på tidspunktet for produktopprettelsen.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Velg egenskaper for å oppdatere produkter fra skjemaet for detaljert produktkategori

Du kan bruke logiske grupperingsegenskaper til å velge hvilke oppdaterte produktegenskaper som skal dyttes til tilhørende produkter.

Forhandleransvarlige kan endre disse arvede produktegenskaper for hvert produkt for å møte individuelle forretningsbehov.

