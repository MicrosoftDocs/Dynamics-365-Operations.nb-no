---
title: Detaljhandelhierarkier
description: Denne artikkelen beskriver detaljhandelshierarkier i Microsoft Dynamics AX.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5fed76e09ef2a64bc2aad2cf6ad7dcfa290acab1
ms.lasthandoff: 03/31/2017


---

# <a name="retail-hierarchies"></a>Detaljhandelhierarkier

Denne artikkelen beskriver detaljhandelshierarkier i Microsoft Dynamics AX.

Du kan opprette et handelskategorihierarki for å organisere produktene du selger gjennom kanalene dine for detaljhandel. Du kan bruke detaljhandelshierarkier til å kategorisere eller gruppere produkter. Du kan deretter bruke disse produktene til å opprette produktsortimenter og fordelsprogrammer for kunden. Du kan også tilordne produktattributter og egenskaper, tilordne en prissettingsstruktur, ta med produktene i produktkampanjer og bruke produktene for rapportering. Du kan opprette ett handelskategorihierarki som representerer alle produkter og kategorier i organisasjonen og deretter bruke dette kategorihierarkiet til flere formål. Du kan alternativt opprette flere handelskategorihierarkier til spesielle formål, for eksempel produktkampanjer. Når du oppretter et detaljprodukthierarki, må du tilordne en kategorihierarkitype for å identifisere formålet med kategorihierarkiet. Det er for eksempel bare produkthierarkier som er tilordnet typen **Navigasjonshierarki for detaljhandel**, som refereres når du blar gjennom produkter etter kategori elektronisk eller på et salgssted.

## <a name="retail-hierarchy-types"></a>Handelshierarkityper
Tabellen nedenfor viser de tilgjengelige typene detaljhandelskategorihierarkier og det generelle formålet med hver type.

| Kategorihierarkitype       | Formål                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hierarki for detaljhandelprodukt      | Bruk denne hierarkitypen til å definere det overordnede hovedprodukthierarkiet for organisasjonen. Du kan bruke denne hierarkitypen for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet. Bare ett detaljprodukthierarki kan tilordnes denne hierarkitypen.                                       |
| Spesialhierarki for detaljhandel | Bruk denne hierarkitypen hvis du vil opprette flere detaljhandelskategorihierarkier. Om våren har du for eksempel en kampanje for badetøy. Du inkluderer derfor badetøyproduktene i et eget kategorihierarki og bruker kampanjeprisen på de ulike produktkategoriene. |
| Navigasjonshierarki for detaljhandel   | Bruk denne hierarkitypen til å gruppere og ordne produkter i kategorier slik at produktene kan blas gjennom på Internett eller på salgsstedet.                                                                                                                                                                                       |

Ved å bruke et hierarki for detaljhandelkategori til å strukturere produktene, kan du definere og vedlikeholde produktattributter og egenskaper på kategorinivå. Disse attributtene og egenskapene omfatter innstillinger for produktdimensjoner og POS-innstillinger. Alle produkter som du tilordner til kategoriene automatisk, arver attributtene og egenskapene som du definerer. Du kan også kopiere egenskapsinnstillingene for et produkt til flere produkter i en valgt kategori samtidig.


