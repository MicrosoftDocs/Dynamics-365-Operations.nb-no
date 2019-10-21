---
title: Produktanbefalinger på salgssted
description: Dette emnet beskriver hvordan du bruker produktanbefalinger på en salgsstedsenhet (POS).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278392"
---
# <a name="product-recommendations-on-pos"></a>Produktanbefalinger på salgssted

[!include [banner](includes/banner.md)]

Det mest sentrale i produktanbefalinger et transformasjonsrettet forretningsprogram som strekker seg over alle detaljhandelsområder for å skape rike, engasjerende og tilpassede produktgjenkjenningsopplevelser. Hvis du vil implementere denne funksjonen på salgsstedet, følger du fremgangsmåten for [hvordan du legger til anbefalinger i POS-enhetene.](add-recommendations-control-pos-screen.md) 

Hvis du vil ha mer informasjon om funksjoner for produktanbefalinger, kan du lese [oversikt over produktanbefalinger.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarier

Produktanbefalingene er aktivert for følgende POS-scenarier. De er tilgjengelige i Cloud POS eller Modern POS (MPOS).

1. På **Produktdetaljer**-siden:

    - • Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingstjenesten flere varer som sannsynligvis kjøpes sammen.

    [![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)

2. På **Transaksjon**-siden:

    - • Anbefalingsmotoren foreslår varer basert på hele listen med varer i handlekurven, som ofte kjøpes sammen.

    > [!NOTE]
    > For å vise anbefalinger på **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 for Retail. **Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.

    [![Anbefalinger på siden Transaksjoner](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 Retail for å aktivere anbefalinger for salgssted

Gjør følgende for å konfigurere produktanbefalinger:

1. Kontroller at tjenesten er oppdatert til **10.0.6-builden**.
2. Følg instruksjonene om hvordan du [aktiverer produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhet.
3. Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.
4. Gå til **Forhandlerparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.
5. Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**. For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Feilsøke problemer der du allerede har aktivert produktanbefalingene

- Gå til **Detaljhandelsparametere** \> **Anbefalingsliste** \> **Deaktiver produktanbefalingene** og kjør **Global konfigurasjon for jobben \[9999\]**. 
- Hvis du har lagt **kontroll for anbefalinger** til din transaksjonsskjerm ved hjelp av **utforming av skjermoppsett**, må fjerne den også.
- Hvis du har flere spørsmål, kan du gå til [Vanlige spørsmål om anbefalinger](../commerce/faq-recommendations.md) for mer informasjon.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet](add-recommendations-control-pos-screen.md)
[Oversikt over produktanbefalings](../commerce/product-recommendations.md)
[Aktivere produktanbefalinger](../commerce/enable-product-recommendations.md) 
