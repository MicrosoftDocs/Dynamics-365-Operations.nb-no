---
title: Bruke måleenhetsinnstillinger
description: Denne artikkelen dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275578"
---
# <a name="apply-unit-of-measure-settings"></a>Bruke måleenhetsinnstillinger

[!include [banner](includes/banner.md)]

Denne artikkelen dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.

Et produkt kan selges i forskjellige enheter, for eksempel "hver", "par" og "dusin." I Commerce Headquarters kan salg per-måleenheten defineres for et produkt, og vises på et e-handelsområde. Hvis for eksempel en forhandler selger et produkt både individuelt og i dusinvis, kan de tilgjengelige måleenhetene vises sammen med annen produktinformasjon.

I illustrasjonen nedenfor er det konfigurert en salg per-måleenhet for et produkt **hv** (hver) i Commerce Headquarters.

![Eksempel på et produkt som er konfigurert med en måleenhet i Commerce Headquarters.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Støtte for bruk og visning av måleenheten er tilgjengelig fra Commerce versjon 10.0.19.

## <a name="unit-of-measure-settings"></a>Måleenhetsinnstillinger

Visningsinnstillinger for måleenhet defineres i Commerce-områdebygger på **Områdeinnstillinger \> Tillegg \> Vis måleenheter for produkter**. Det finnes tre innstillinger som støttes:

- **Ikke vis** – Når denne innstillingen er valgt, viser ikke e-handelsområdet måleenheten for produktet. Denne virkemåten er standard.
- **Vis i produktkjøpsopplevelsen**– Når denne innstillingen er valgt, vises måleenheten på produktdetaljer, handlekurv, kassen, ordrehistorikk og ordredetaljer.
- **Vis i produktlesing og kjøpsopplevelse** – Når denne innstillingen er valgt, vises måleenheten på sidene for produktkjøpsopplevelse og også under produktlesingsopplevelsen. Som en del av denne virkemåten vises måleenheter i søkeresultater og i produktsamlingsmoduler.

> [!IMPORTANT]
> Visningsinnstillinger for måleenhet er tilgjengelige i Commerce versjon 10.0.19. Hvis du oppdaterer fra en eldre versjon av Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner, kan du se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Moduler som bruker måleenhetsinnstillinger

Moduler som bruker måleenhetsinnstillingene, omfatter modulene kjøpsboks, ønskeliste, handlekurv, handlekurvikon, søkeresultatcontainer, produktsamling, utsjekking og moduler med ordredetaljer.

I eksemplet i illustrasjonen nedenfor viser en produktdetaljside (PDP) måleenheten (**hv**) for et produkt.

![Eksempel på en PDP som viser måleenheten.](./media/Productunit-PDP.png)

I eksemplet i illustrasjonen nedenfor viser en produktsamlingsmoduls måleenheten (**hv**) for et produkt.

![Eksempel på en produktsamlingsmodul som viser måleenheten.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Handlekurvmodul](add-cart-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kontobehandlingssider og -moduler](account-management.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
