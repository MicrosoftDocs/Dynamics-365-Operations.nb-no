---
title: Legge til anbefalinger på transaksjonsskjermen
description: Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 38099909f169391c17760ac381af07f0848fc384
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797485"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Legge til anbefalinger i transaksjonsskjermbildet

[!include [banner](includes/banner.md)]


Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 Commerce. Hvis du vil ha mer informasjon om produktanbefalinger, kan du lese [produktanbefalingene i POS-dokumentasjonen](product.md).


Du kan vise produktanbefalingene på salgsstedsenheten når du bruker Commerce. Hvis du vil vise produktanbefalinger, må du legge til en kontroll på transaksjonsskjermen med utforming av skjermoppsett. 

## <a name="open-layout-designer"></a>Åpne utforming av oppsett

1. Gå til **Retail og Commerce** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.
2. Bruk hurtigfilteret til å finne skjermen du vil legge til kontrollen på. Filtrer for eksempel i feltet **Skjermoppsett-ID** ved å bruke verdien **F2CP16:9M**.
3. Finn og velg ønsket post i listen. Velg for eksempel **Navn: F2CP16:9M Skjermoppsett-ID: F2CP16:9M**.
4. Klikk **Utforming av oppsett**.
5. Følg instruksjonene for å starte utforming av oppsett. Når du blir spurt etter legitimasjon, angir du den samme legitimasjonen som var i bruk da utforming av oppsett ble startet fra siden **Skjermoppsett**.
6. Når du logger deg på, vises det en side som ligner den nedenfor. Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.


    [![Utforming av oppsett](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Velge et visningsalternativ

Det finnes to tilgjengelige konfigurasjonsalternativer. Velg alternativet som passer best for din butikk, og følg resten av instruksjonene for å konfigurere kontrollen. De to alternativene er:

- Anbefalinger er alltid synlige.
- Kategorien **Anbefalinger** vises i rutenettet på høyre side av skjermen.

### <a name="make-recommendations-always-visible"></a>Gjøre anbefalinger alltid synlige


1. Reduser høyden på detaljområdet for transaksjonslinjer slik at det er samme høyde som kundepanelet til venstre.


    [![Høyde på detaljområdet for transaksjonslinjer er redusert](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. På menyen til venstre drar og slipper du kontrollen for anbefalinger til mellom detaljområdet for transaksjonslinjer og knappegruppen nederst i midten på transaksjonsskjermen. Endre størrelse på kontrollen slik at den passer i dette området.

    [![Anbefalingskontroll er lagt til i oppsettet](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Klikk **X** for å lagre og avslutte utforming av oppsett.
4. I Commerce går du til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt;**Distribusjonsplaner**.
5. Velg **1090, Kasser** i listen.
6. Klikk **Kjør nå**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Legge til kategorien Anbefalinger i knappegruppen på høyre side av skjermen

1. Høyreklikk i det tomme området under den siste kategorien i knappegruppen plassert på høyre side av siden.

2. Klikk på **Tilpass**.

    [![Tilpasning – Kategorikontroll-dialogboks](./media/pic-5.png)](./media/pic-5.png)

3. Klikk **Ny kategori**.
4. Finn den nye kategorien som du nettopp la til. Du må kanskje rulle nedover.
5. I rullegardinlisten **Innhold** velger du **Anbefalte produkter**.

    [![Valg av Anbefalte produkter i Innhold-feltet](./media/pic-6.png)](./media/pic-6.png)

6. I **Etikett**-feltet, skriv inn et navn for anbefalingsfanen. For eksempel, skriv «Anbefalte produkter».
7. I **Bilde**-feltet velger du bildet som skal vises i kategorien.
8. Klikk **OK**. Den nye kategorien vises i knappegruppen.
9. Klikk **X** for å lagre og avslutte utforming av oppsett.
10. I Commerce går du til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt;**Distribusjonsplaner**.
11. Velg **1090, Kasser** i listen.
12. Klikk **Kjør nå**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Legge til produktanbefalinger på salgssted](product.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]