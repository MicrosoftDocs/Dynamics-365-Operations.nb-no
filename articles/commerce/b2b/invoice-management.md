---
title: Fakturaadministrasjon for B2B-e-handelsnettsteder
description: Denne artikkelen beskriver funksjonene for fakturaadministrasjon på bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274435"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Fakturaadministrasjon for B2B-e-handelsnettsteder

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver funksjonene for fakturaadministrasjon på bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce.

Det er en vanlig praksis for firmaer som håndterer B2B-transaksjoner, å godta ordrer på kundekreditt og deretter sende en faktura til kunder etter at de har oppfylt ordren. Betalingsbetingelser er definert for kunder, og det er kanskje gjeldende rabatter som motiverer kunder til å betale til rett tid eller før tiden. B2B-e-handelsnettsteder lar kundene vise alle fakturaene for å bidra til å øke sannsynligheten for at betalinger mottas i tide. Kunden kan enkelt filtrere fakturaene slik at betalte, ubetalte og delvis betalte fakturaer vises sammen med forfallsdatoene.

![Fakturaer-siden på et B2B-nettsted.](../media/ViewInvoices.png)

> [!NOTE]
> En pålogget bruker kan bare vise og betale sine egne fakturaer. Hvis det er konfigurert en organisasjonskonto på rullegardinmenyen **Fakturakonto** i hurtigfanen **Faktura og levering** for kundeposten i Commerce Headquarters, kan brukeren vise og betale fakturaer for organisasjonskontoen.

En bruker kan velge en ubetalt eller delvis betalt faktura på **Fakturaer**-siden på et B2B-nettsted og deretter velge **Betal faktura**. Den valgte fakturaen legges til i handlekurven, og brukeren kan fortsette med betalingen. Brukeren kan deretter bestemme om fakturaen skal betales helt eller delvis. Brukeren kan ikke bruke betalingsmetoden for a konto til å betale for fakturaer.

> [!NOTE]
> Fakturaer kan bare legges til i handlekurven hvis ingen varer er i den. Varer kan likeledes bare legges til i handlekurven hvis ingen fakturaer er i den. Microsoft planlegger å fjerne denne begrensningen i fremtidige Commerce-versjoner.

![Handlekurv-siden på et B2B-nettsted.](../media/PayInvoice.png)

En bruker kan også velge **Be om faktura** ved siden av en faktura på **Fakturaer**-siden. Brukeren kan på denne måten be om å få fakturadetaljene sendt til den registrerte e-postadressen sin.

![Dialogboksen Be om faktura.](../media/RequestInvoice2.png)

Når en bruker ber om en faktura, flyttes forespørselen til delen **B2B-forespørsler** på **Min konto**-siden. Etter at jobbene **P-0001** og **Synkroniser ordrer og kanalforespørsler** er kjørt i Commerce Headquarters, utløses deretter e-postfakturaen, og statusen for B2B-forespørselen merkes som fullført.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
