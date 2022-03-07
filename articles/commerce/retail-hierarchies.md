---
title: Commerce-hierarkier
description: Denne artikkelen beskriver hierarkier i Dynamics 365 Commerce.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 60534536476cfbe7a4f254923785ab1eb0001a3eaf7630dec75f28f07dff30d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716173"
---
# <a name="commerce-hierarchies"></a>Commerce-hierarkier

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hierarkier i Dynamics 365 Commerce.

Du kan opprette et kategorihierarki for å organisere produktene du selger gjennom kanalene dine. Du kan bruke produkthierarkier til å kategorisere eller gruppere produkter. Du kan deretter bruke disse produktene til å opprette produktsortimenter og fordelsprogrammer for kunden. Du kan også tilordne produktattributter og egenskaper, tilordne en prissettingsstruktur, ta med produktene i produktkampanjer og bruke produktene for rapportering. Du kan opprette ett kategorihierarki som representerer alle produkter og kategorier i organisasjonen og deretter bruke dette kategorihierarkiet til flere formål. Du kan alternativt opprette flere kategorihierarkier til spesielle formål, for eksempel produktkampanjer. Når du oppretter et produkthierarki, må du tilordne en kategorihierarkitype for å identifisere formålet med kategorihierarkiet. Det er for eksempel bare produkthierarkier som er tilordnet typen **Navigasjonshierarki for handel**, som refereres når du blar gjennom produkter etter kategori elektronisk eller på et salgssted.

## <a name="hierarchy-types"></a>Hierarkityper

Tabellen nedenfor viser de tilgjengelige typene kategorihierarkier og det generelle formålet med hver type.

| Kategorihierarkitype       | Formål |
|-------------------------------|---------|
| Produkthierarki      | Bruk denne hierarkitypen til å definere det overordnede hovedprodukthierarkiet for organisasjonen. Du kan bruke denne hierarkitypen for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet. Bare ett produkthierarki kan tilordnes denne hierarkitypen. |
| Spesialhierarki | Bruk denne hierarkitypen hvis du vil opprette flere kategorihierarkier. Om våren har du for eksempel en kampanje for badetøy. Du inkluderer derfor badetøyproduktene i et eget kategorihierarki og bruker kampanjeprisen på de ulike produktkategoriene. |
| Navigeringshierarki   | Bruk denne hierarkitypen til å gruppere og ordne produkter i kategorier slik at produktene kan blas gjennom på Internett eller på salgsstedet. |

Ved å bruke et kategorihierarki til å strukturere produktene kan du definere og vedlikeholde produktattributter og egenskaper på kategorinivå. Disse attributtene og egenskapene omfatter innstillinger for produktdimensjoner og POS-innstillinger. Alle produkter som du tilordner til kategoriene automatisk, arver attributtene og egenskapene som du definerer. Du kan også kopiere egenskapsinnstillingene for et produkt til flere produkter i en valgt kategori samtidig.


[!INCLUDE[footer-include](../includes/footer-banner.md)]