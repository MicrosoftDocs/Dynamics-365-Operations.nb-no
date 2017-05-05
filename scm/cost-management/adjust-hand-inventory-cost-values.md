---
title: Justere kostnadsverdier for lagerbeholdning
description: "Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Justere kostnadsverdier for lagerbeholdning

[!include[banner](../includes/banner.md)]


Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt.

Du kan bruke siden **Justering av lagerbeholdning** til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt. **Obs!** Du åpner siden **Justering av lagerbeholdning** ved å velge posten for en fullført lagerlukkingsprosess på siden **Lukking og justering** og deretter klikke **Justering** &gt; **Beholdning**. **Eksempel:** Du har følgende transaksjoner i februar:

-   1. februar: Et økonomisk lagermottak av et antall på 2 til en kostnad på USD 10,00
-   5. februar: Et økonomisk lagermottak av et antall på 1 til en kostnad på USD 13,00
-   19. februar: En økonomisk lageravgang av et antall på 1 til en løpende gjennomsnittlig kostnad på USD 11,00

Denne varen ble definert med først-inn-først-ut-lagermodellen, og lagerlukkingen ble utført per 28. februar. Den økonomiske avgangstransaksjonen på USD 11,00 vil bli utlignet til det økonomiske mottaket datert 1. februar, og en justering på USD 1,00 blir foretatt. Følgende lagermottak vil dermed inneholde åpne lagerantall:

-   1. februar: Et antall på 1 til en kostnad på USD 10,00
-   5. februar: Et antall på 1 til en kostnad på USD 13,00

Når du skal definere disse to varenes kost til USD 15,00, bruker du alternativet for lagerjustering til å justere åpne lagerantall per siste lagerlukkingsperiode. **Obs! ** Posteringsdatoen for lagerjusteringstransaksjonen blir datoen for den siste lagerlukkingen. Denne datoen kan ikke endres.



