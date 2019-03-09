---
title: Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter
description: Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "320449"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter

[!include [banner](includes/banner.md)]

> [!NOTE]
> Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner. Hvis du vil ha mer informasjon, kan du se [Fjernede eller avskrevne funksjoner](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).

Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail.

Du kan vise produktanbefalingene på salgsstedsenheten når du bruker Microsoft Dynamics 365 for Retail. *Anbefalinger* er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker. Hvis du vil vise produktanbefalinger, må du legge til en kontroll på transaksjonsskjermen med utforming av skjermoppsett.

## <a name="open-layout-designer"></a>Åpne utforming av oppsett

1. Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.
2. Bruk hurtigfilteret til å finne skjermen du vil legge til kontrollen på. Filtrer for eksempel i feltet **Skjermoppsett-ID** ved å bruke verdien "F2CP16:9M".
3. Finn og velg ønsket post i listen. Velg for eksempel "Navn: F2CP16:9M Skjermoppsett-ID: F2CP16:9M".
4. Klikk **Utforming av oppsett**.
5. Følg instruksjonene for å starte utforming av oppsett. Når du blir spurt etter legitimasjon, angir du den samme legitimasjonen som var i bruk da utforming av oppsett ble startet fra siden **Skjermoppsett**.
6. Når du logger deg på, vises det en side som ligner den nedenfor. Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.

    [![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Velge et visningsalternativ

Det finnes to tilgjengelige konfigurasjonsalternativer. Velg alternativet som passer best for din butikk, og følg resten av instruksjonene for å konfigurere kontrollen. De to alternativene er:

- Anbefalinger er alltid synlige.
- Kategorien **Anbefalinger** vises i rutenettet på høyre side av skjermen.

### <a name="make-recommendations-always-visible"></a>Gjøre anbefalinger alltid synlige

1. Reduser høyden på detaljområdet for transaksjonslinjer slik at det er samme høyde som kundepanelet til venstre.

    [![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. På menyen til venstre drar og slipper du kontrollen for anbefalinger til mellom detaljområdet for transaksjonslinjer og knappegruppen nederst i midten på transaksjonsskjermen. Endre størrelse på kontrollen slik at den passer i dette området.

    [![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)

3. Klikk **X** for å lagre og avslutte utforming av oppsett.
4. Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner** i Dynamics 365 for Retail.
5. Velg  **1090, Kasser** i listen.
6. Klikk **Kjør nå**.

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Legge til kategorien Anbefalinger i knappegruppen på høyre side av skjermen

1. Høyreklikk i det tomme området under den siste kategorien i knappegruppen plassert på høyre side av siden.
2. Klikk på **Tilpass**.

    [![pic-5](./media/pic-5.png)](./media/pic-5.png)

3. Klikk **Ny kategori**.
4. Finn den nye kategorien som du nettopp la til. Du må kanskje rulle nedover.
5. I rullegardinlisten **Innhold** velger du **Anbefalte produkter**.

    [![pic-6](./media/pic-6.png)](./media/pic-6.png)

6. I **Etikett**-feltet, skriv inn et navn for anbefalingsfanen. For eksempel, skriv «Anbefalte produkter».
7. I **Bilde**-feltet velger du bildet som skal vises i kategorien.
8. Klikk **OK**. Den nye kategorien vises i knappegruppen.
9. Klikk **X** for å lagre og avslutte utforming av oppsett.
10. Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner** i Dynamics 365 for Retail.
11. Velg  **1090, Kasser** i listen.
12. Klikk **Kjør nå**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over personlige produktanbefalinger](personalized-product-recommendations.md)
