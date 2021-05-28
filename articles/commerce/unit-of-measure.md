---
title: Bruke måleenhetsinnstillinger
description: Dette emnet dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022380"
---
# <a name="apply-unit-of-measure-settings"></a>Bruke måleenhetsinnstillinger

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.

Et produkt kan selges i forskjellige enheter, for eksempel "hver", "par" og "dusin." I Commerce Headquarters kan salg per-måleenheten defineres for et produkt, og vises på et e-handelsområde. Hvis for eksempel en forhandler selger et produkt både individuelt og i dusinvis, kan de tilgjengelige måleenhetene vises sammen med annen produktinformasjon.

I illustrasjonen nedenfor er det konfigurert en salg per-måleenhet for et produkt **hv** (hver) i Commerce Headquarters.

![Eksempel på et produkt som er konfigurert med en måleenhet i Commerce Headquarters](./media/Productunit-headquarters.PNG)

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

![Eksempel på en PDP som viser måleenheten](./media/Productunit-PDP.png)

I eksemplet i illustrasjonen nedenfor viser en produktsamlingsmoduls måleenheten (**hv**) for et produkt.

![Eksempel på en produktsamlingsmodul som viser måleenheten](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Handlekurvmodul](add-cart-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kontobehandlingssider og -moduler](account-management.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
