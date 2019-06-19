---
title: Prosjektsalgsordrer
description: Dette emnet forklarer hvordan du oppretter prosjektbaserte salgsordrer for Etter regning-prosjekter.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529908"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Prosjektsalgsordrer for Etter regning-prosjekter

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du oppretter en salgsordre for et prosjekt. Salgsordrer kan bare opprettes for prosjekter av typen **Etter regning**.

Hvis et Etter regning-prosjekt har flere finansieringskilder i prosjektkontrakten, må du aktivere parameteren **Tillat salgsordrer for prosjekter med flere finansieringskilder** på siden **Parametere for prosjektstyring og regnskap**. 

> [!NOTE]
> - Støtte for prosjektsalgsordrer med flere finansieringskilder er tilgjengelig fra og med programversjon 10.0.2 og høyere.
> - Parameteren for å aktivere støtte for prosjektsalgsordrer med flere finansieringskilder vil bli fjernet i april 2020-frigivelsesbølgen. Etter dette vil funksjonaliteten alltid være aktivert.

Du kan opprette prosjektbaserte salgsordrer på to måter:

- Gå til selve prosjektet. I handlingsruten velger du **Behandle > Vareoppgaver > Salgsordre**. Prosjektinformasjonen settes som standard til salgsordren fra prosjektet. Hvis prosjektkontrakten har mer enn én finansieringskilde, må du velge finansieringskilden for å angi kunden for salgsordren. Hvis det er bare én finansieringskilde for prosjektet, angis kunden automatisk.
- Gå til listesiden **Alle salgsordrer**, og opprett en ny salgsordre. Du må velge prosjektet for salgsordren. Når prosjektet er valgt, angis kunden fra finansieringskilden, eller du må velge finansieringskilden hvis prosjektkontrakten har flere finansieringskilder.
