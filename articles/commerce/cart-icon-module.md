---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479310"
---
# <a name="cart-icon-module"></a>Handlekurvikonmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven. Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet. Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden. I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget. Dette reduserer antall sidenavigasjoner, og betalingen blir raskere. 

Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.

![Eksempel på en handlevogn-ikonmodul.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet. Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.

## <a name="module-properties-in-the-adventure-works-theme"></a>Modulegenskaper i Adventure Works-emnet

I Adventure Works-emnet inneholder handlekurvikonmodulen to ekstra spor for minikurven. Disse sporene er inkludert som moduldefinisjonsforlengelse.

- **Tomme handlekurvkampanjer** – Dette sporet tar en innholdsblokkmodul. Når handlekurven er tom, vises den angitte innholdsblokkmodulen. Innholdsblokkmodulen kan brukes til kampanjer, markedsføringsinnhold og koblinger til kategorisider for å hjelpe kunder med å fortsette med handlereisen.
- **Kampanjeinnhold** – Denne sporet kan brukes til å fremme kampanjer, for eksempel "Gratis forsendelse på ordrer over USD 100." Innholdsblokk-, tekstblokk- og bildelistemoduler kan brukes i kampanjeinnholdssporet.

Dette bildet viser et eksempel på en handlekurvikonmodul i Adventure Works-emnet som viser kampanjeinnhold på minikurven.

![Eksempel på en handlekurv-ikonmodul i Adventure Works-emnet](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works-temasporene er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.

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
