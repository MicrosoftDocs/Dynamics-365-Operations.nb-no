---
title: "Legge til en kontroll for anbefalinger til siden transaksjonen på en POS-enhet"
description: "Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger til skjermbildet transaksjonen på et punkt av salg (POS) enheten bruker utforming av skjermoppsett i Microsoft Dynamics 365 for operasjoner."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Legge til en kontroll for anbefalinger til siden transaksjonen på en POS-enhet

Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger til skjermbildet transaksjonen på et punkt av salg (POS) enheten bruker utforming av skjermoppsett i Microsoft Dynamics 365 for operasjoner.

Du kan vise produktanbefalingene på POS-enheten når du bruker Microsoft Dynamics 365 for operasjoner. *Anbefalinger* elementer som kunden kan være interessert i basert på deres kjøpshistorikk, elementer i sin Ønskeliste og elementer som andre kunder har kjøpt online og i murstein og mørtel butikker. Hvis du vil vise produkt anbefalinger, må du legge til en kontroll i transaksjonen skjermen med utforming av skjermoppsett.

## <a name="open-layout-designer"></a>Åpne sideoppsett
1.  Gå til **Retail og commerce**&gt;**kanaloppsett**&gt;**installasjonsprogrammet for POS**&gt;**POS**&gt;**skjerm oppsett**.
2.  Bruke rask filteret til å finne skjermen som du vil legge til kontrollen. For eksempel filtrere etter de **skjerm oppsett-ID** bruker en verdi på 'F2CP16:9M'-feltet.
3.  Finn og velg ønsket post i listen. Velg for eksempel ' navn: F2CP16:9M skjermoppsett-ID: F2CP16:9M'.
4.  Klikk **oppsett designer**.
5.  Følg instruksjonene for å starte oppsettet-designer. Når du blir spurt etter legitimasjon, angir du legitimasjonen som var i bruk da oppsettet utformeren ble startet fra **skjerm oppsett** siden.
6.  Når du logger deg på, vises det en side som ligner den nedenfor. Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Velg et visningsalternativ
-----------------------

Det finnes to alternativer for konfigurasjoner. Velg alternativet som passer best for din butikk, og Følg resten av instruksjonene for å konfigurere kontrollen. Det er to alternativer:
-   Anbefalinger er alltid synlig.
-   A **anbefalinger** kategorien vises i rutenettet på høyre side av skjermen.

#### <a name="to-make-recommendations-always-visible"></a>Til å foreta anbefalinger alltid synlig

1.  Reduser høyden på transaksjonen linjer detaljer-området slik at det er samme høyde som kunde-panelet til venstre. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  På menyen til venstre, dra og slipp anbefalinger kontrollen til mellom transaksjonen linje detaljer og knappegruppen i midten nederst på skjermen for transaksjonen. Endre størrelse på kontrollen slik at den passer i dette området. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klikk på **X** til å lagre og avslutte sideoppsett.
4.  I Dynamics 365 for operasjoner, kan du gå til **Retail og commerce**&gt;**Retail IT**&gt;**distribusjon planer**.
5.  I-listen velger du **1090 registrerer**.
6.  Klikk **kjører nå**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Legge til en kategori for anbefalinger i knappegruppen på høyre side av skjermen

1.  Høyreklikk i det tomme området under siste kategorien i knappegruppen plassert på høyre side av siden.
2.  Klikk **tilpasse**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klikk **ny fane**.
4.  Finn den nye kategorien som du nettopp la til. Du må kanskje rulle nedover.
5.  I den **innholdet** rullegardinlisten, velger **anbefalte produkter**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  I den **etiketten** skriver du inn et navn for kategorien anbefalinger. Skriv for eksempel anbefales-produkter.
7.  I den **bilde**, velger du bildet som skal vises i kategorien.
8.  Click **OK**. Den nye kategorien vises i knappegruppen.
9.  Klikk på **X** til å lagre og avslutte sideoppsett.
10. I Dynamics 365 for operasjoner, kan du gå til **Retail og commerce**&gt;**Retail IT**&gt;**distribusjon planer**.
11. I-listen velger du **1090 registrerer**.
12. Klikk **kjører nå**.


<a name="see-also"></a>Se også
--------

[Oversikt over personlige anbefalinger](personalized-product-recommendations.md)


