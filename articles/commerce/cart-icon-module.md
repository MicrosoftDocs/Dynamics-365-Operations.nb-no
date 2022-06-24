---
title: Handlekurvikonmodul
description: Denne artikkelen dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
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
ms.openlocfilehash: a5b86b0c843a680dd0c46295a69e12d6e3542619
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859119"
---
# <a name="cart-icon-module"></a>Handlekurvikonmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven. Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet. Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden. I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget. Dette reduserer antall sidenavigasjoner, og betalingen blir raskere. 

Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.

![Eksempel på en handlevogn-ikonmodul.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Vis minikurv** – Når denne egenskapen er satt til **Sann**, vises et handlekurvsammendrag (minikurv) når brukeren holder pekeren over handlekurvikonet. Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.
- **Tillat anonym betaling** – Når denne egenskapen er satt til **Sann**, lar minihandlekurven brukere som ikke er logget inn, bruke en gjestekasse til betaling. Denne egenskapen er tilgjengelig i Commerce, versjon 10.0.21, som en del av Commerce-modulbibliotekpakken.
- **Varerekkefølge** – Denne egenskapen kontrollerer i hvilken rekkefølge varer vises i minihandlekurven. Når alternativet **Nye varer legges til øverst i listen** er valgt, vises nye varer som legges til i handlekurven, øverst i listen over minihandlekurvvarer. Når standardalternativet **Nye varer legges til nederst i listen** er valgt, vises nye varer som legges til i handlekurven, nederst i listen over minihandlekurvvarer. Denne egenskapen er tilgjengelig fra og med Commerce, versjon 10.0.21, som en del av Commerce-modulbibliotekpakken.

> [!IMPORTANT]
> Egenskapene **Tillat anonym betaling** og **Varerekkefølge** er tilgjengelige fra og med Commerce, versjon 10.0.21. De krever at Commerce-modulbibliotekpakken versjon 9.31 er installert.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Modulegenskaper og spor i Adventure Works-emnet

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
