---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793087"
---
# <a name="cart-icon-module"></a>Handlekurvikonmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven. Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet. Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden. I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget. Dette reduserer antall sidenavigasjoner, og betalingen blir raskere. 

> [!NOTE]
> Støtte for handlekurvikon-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.

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

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]