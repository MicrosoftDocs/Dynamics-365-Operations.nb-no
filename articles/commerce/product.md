---
title: Legge til produktanbefalinger på salgssted
description: Denne artikkelen beskriver hvordan du bruker produktanbefalinger på en salgsstedsenhet (POS).
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460063"
---
# <a name="add-product-recommendations-on-pos"></a>Legge til produktanbefalinger i POS

[!include [banner](includes/banner.md)]

Det mest sentrale i produktanbefalinger et transformasjonsrettet forretningsprogram som strekker seg over alle handelsområder for å skape rike, engasjerende og tilpassede produktgjenkjenningsopplevelser. Hvis du vil implementere denne funksjonen på salgsstedet, følger du fremgangsmåten for [hvordan du legger til anbefalinger i POS-enhetene.](add-recommendations-control-pos-screen.md) 

Hvis du vil ha mer informasjon om funksjoner for produktanbefalinger, kan du lese [oversikt over produktanbefalinger.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarier

Produktanbefalingene er aktivert for følgende POS-scenarier. De er tilgjengelige i Cloud POS eller Modern POS (MPOS).

1. På **Produktdetaljer**-siden:

    - Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingstjenesten flere varer som sannsynligvis kjøpes sammen. Avhengig av tilleggene for tjenesten kan forhandlerne vise anbefalinger av typen **Kjøp lignende utseender** og **Kjøp lignende beskrivelse** for produkter, i tillegg til tilpassede anbefalinger for brukere som har en tidligere kjøpshistorikk.

    [![Anbefalinger på siden Produktdetaljer.](./media/proddetails.png)](./media/proddetails.png)

2. På **Transaksjon**-siden:

    - Anbefalingsmotoren foreslår varer basert på hele listen med varer i handlekurven, som ofte kjøpes sammen.

    > [!NOTE]
    > For å vise anbefalinger på **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 Commerce. **Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.

    [![Anbefalinger på siden Transaksjoner.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurere Commerce for å aktivere anbefalinger for salgssted 

Når du skal definere produktanbefalinger, må du bekrefte at du har fullført klargjøringsprosessen for produktanbefalinger i Commerce ved å følge trinnene i [Aktiver produktanbefalinger](../commerce/enable-product-recommendations.md). Som standard vises anbefalinger både på siden **Produktdetaljer** og på siden **Kundedetaljer** etter at du har fullført klargjøringstrinnene og dataene er lagt inn. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Legge til anbefalinger i transaksjonsskjermbildet

1. Følg trinnene under [Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md) for å legge til anbefalinger.
1. Hvis du vil gjenspeile endringer som ble gjort i utformingen av skjermoppsettet på salgsstedet, kan du kjøre kanalkonfigurasjonsjobb **1070** i Commerce headquarters.

> [!NOTE] 
> Hvis du vil aktivere anbefalinger på salgsstedet ved hjelp av den kommadelte RecoMock-filen (CSV), må du distribuere CSV-filen i Microsoft Dynamics Lifecycle Services-aktivabiblioteket (LCS) før du konfigurerer oppsettbehandlingen. Hvis du bruker RecoMock CSV-filen, trenger du ikke aktivere anbefalinger. CSV-filen er bare tilgjengelig for demoformål. Dette anbefales for kunder eller løsningsarkitekter som ønsker å etterligne utseendet til anbefalingslister for demoformål uten å måtte kjøpe en ekstra lagerenhet (SKU).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
