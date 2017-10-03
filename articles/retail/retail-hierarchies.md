---
title: Detaljhandelhierarkier
description: Denne artikkelen beskriver detaljhandelshierarkier i Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: a425680fb4d2e2da8d96acd843694ea9a07e29f0
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---

# <a name="retail-hierarchies"></a>Detaljhandelhierarkier

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver detaljhandelshierarkier i Microsoft Dynamics 365 for Retail.

Du kan opprette et handelskategorihierarki for å organisere produktene du selger gjennom kanalene dine for detaljhandel. Du kan bruke detaljhandelshierarkier til å kategorisere eller gruppere produkter. Du kan deretter bruke disse produktene til å opprette produktsortimenter og fordelsprogrammer for kunden. Du kan også tilordne produktattributter og egenskaper, tilordne en prissettingsstruktur, ta med produktene i produktkampanjer og bruke produktene for rapportering. Du kan opprette ett handelskategorihierarki som representerer alle produkter og kategorier i organisasjonen og deretter bruke dette kategorihierarkiet til flere formål. Du kan alternativt opprette flere handelskategorihierarkier til spesielle formål, for eksempel produktkampanjer. Når du oppretter et detaljprodukthierarki, må du tilordne en kategorihierarkitype for å identifisere formålet med kategorihierarkiet. Det er for eksempel bare produkthierarkier som er tilordnet typen **Navigasjonshierarki for detaljhandel**, som refereres når du blar gjennom produkter etter kategori elektronisk eller på et salgssted.

## <a name="retail-hierarchy-types"></a>Handelshierarkityper
Tabellen nedenfor viser de tilgjengelige typene detaljhandelskategorihierarkier og det generelle formålet med hver type.

| Kategorihierarkitype       | Formål                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hierarki for detaljhandelprodukt      | Bruk denne hierarkitypen til å definere det overordnede hovedprodukthierarkiet for organisasjonen. Du kan bruke denne hierarkitypen for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet. Bare ett detaljprodukthierarki kan tilordnes denne hierarkitypen.                                       |
| Spesialhierarki for detaljhandel | Bruk denne hierarkitypen hvis du vil opprette flere detaljhandelskategorihierarkier. Om våren har du for eksempel en kampanje for badetøy. Du inkluderer derfor badetøyproduktene i et eget kategorihierarki og bruker kampanjeprisen på de ulike produktkategoriene. |
| Navigasjonshierarki for detaljhandel   | Bruk denne hierarkitypen til å gruppere og ordne produkter i kategorier slik at produktene kan blas gjennom på Internett eller på salgsstedet.                                                                                                                                                                                       |

Ved å bruke et hierarki for detaljhandelkategori til å strukturere produktene, kan du definere og vedlikeholde produktattributter og egenskaper på kategorinivå. Disse attributtene og egenskapene omfatter innstillinger for produktdimensjoner og POS-innstillinger. Alle produkter som du tilordner til kategoriene automatisk, arver attributtene og egenskapene som du definerer. Du kan også kopiere egenskapsinnstillingene for et produkt til flere produkter i en valgt kategori samtidig.




