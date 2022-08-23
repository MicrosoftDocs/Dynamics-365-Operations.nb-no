---
title: Bruke innstillinger for Legg til produkt i handlevogn
description: Denne artikkelen dekker innstillinger for Legg til i handlekurv og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277034"
---
# <a name="apply-add-product-to-cart-settings"></a>Bruke innstillinger for Legg til produkt i handlevogn

[!include [banner](includes/banner.md)]

Denne artikkelen dekker innstillinger for **Legg til i handlekurv** og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

Forskjellige arbeidsflyter støttes når et produkt legges til i handlekurven på et Dynamics 365 Commerce-e-handelsområde. For eksempel kan områdebrukeren bli ført til kurvsiden. Brukeren kan eventuelt bli værende på gjeldende side, men motta en melding som bekrefter at produktet ble lagt til i handlekurven.

Hvis du vil støtte de ulike arbeidsflytene, er et **Legg til produkt i handlekurv**-felt tilgjengelig i **Innstillinger \> Utvidelser** i Commerce-områdebyggeren. Velg ett av de følgende innstillingsalternativene for å implementere den tilsvarende arbeidsflyten:

- **Naviger til handlekurvside** – Når brukere legger til en vare i kurven, sendes de til handlekurvsiden.
- **Vis varsel** – Når brukere legger til en vare i kurven, vises det en bekreftelsesmelding, og brukerne kan fortsette å søke på siden med produktinformasjon.
- **Vis minikurv** – Når brukere legger til en vare i kurven, vises innholdet i minikurven. Brukerne kan gå gjennom alle varene i handlekurven, og de kan gå videre til kassen hvis de er klare.
- **Vis varsling ved hjelp av Varslinger-modul** – Når brukere legger til en vare i handlekurven, brukes varslingsmodulen til å vise et bekreftelsesvarsel. For at dette innstillingsalternativet skal fungere, må meldingsmodulen legges til i sidehodet.
- **Ikke naviger til handlekurvside** – Når brukere legger til en vare i kurven, forblir de på gjeldende side.

Illustrasjonen nedenfor viser et eksempel på alternativene for **Legg til produkt i handlekurv**-innstillingen i områdebyggeren.

![Eksempel på alternativer for Legg til produkt i handlekurv-innstillingen i områdebyggeren](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Innstillingene for **Legg til produkt i handlekurv**-området er tilgjengelige fra Dynamics 365 Commerce 10.0.11-versjonen. Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Alternativet for **Vis minikurvkurv**-innstillingen er tilgjengelig fra Dynamics 365 Commerce 10.0.20-versjonen. Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Følgende bilde viser et eksempel på bekreftelsesmeldingen "lagt til i handlekurv" på Fabrikam-området.

![Eksempel på bekreftelsesmeldingen "lagt til i handlekurv" på Fabrikam-området](./media/ecommerce-addtocart-notifications.PNG)

Følgende bilde viser et eksempel på bekreftelsesmeldingen "lagt til i handlekurv" på Adventure Works-området.

![Eksempel på bekreftelsesmeldingen "lagt til i handlekurv" på Adventure Works-området](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Butikkvelgermodul](store-selector.md)
