---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661153"
---
# <a name="cart-icon-module"></a>Handlekurvikonmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven. Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet. Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden. I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget. Dette reduserer antall sidenavigasjoner, og betalingen blir raskere. 

Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.

![Eksempel på en handlevogn-ikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet. Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.

## <a name="add-a-cart-icon-module-to-a-page"></a>Legge til en handlekurvikonmodul på en side

Hvis du vil legge til en handlekurvikonmodul, kan du se [Hodemodul](author-header-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Modul for leveringsalternativer](delivery-options-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)
