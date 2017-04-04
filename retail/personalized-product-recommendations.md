---
title: Oversikt over personlige anbefalinger
description: "Produktanbefalingene kan vises i Dynamics 365 for operasjoner, on the point of salg (POS) enheten. Anbefalingene er elementer som kunden kan være interessert i basert på deres kjøpshistorikk, elementer i sin Ønskeliste og elementer som andre kunder har kjøpt online og i murstein og mørtel butikker. Forhandlere med store kataloger bidra anbefalinger til kunden med produkt-oppdagelse. Ved showcasing produkter rettet mot en kundes interesser og innkjøp vaner, produktanbefalingene kan hjelpe forhandlere med opp-salg og kryss-salg, og kan forbedre oppbevaring av kunden. I Dynamics 365 for operasjoner, er produktanbefalingene drives av kognitive tjenester og opplæring for Microsoft-Azure-maskin."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Oversikt over personlige anbefalinger

Produktanbefalingene kan vises i Dynamics 365 for operasjoner, on the point of salg (POS) enheten. Anbefalingene er elementer som kunden kan være interessert i basert på deres kjøpshistorikk, elementer i sin Ønskeliste og elementer som andre kunder har kjøpt online og i murstein og mørtel butikker. Forhandlere med store kataloger bidra anbefalinger til kunden med produkt-oppdagelse. Ved showcasing produkter rettet mot en kundes interesser og innkjøp vaner, produktanbefalingene kan hjelpe forhandlere med opp-salg og kryss-salg, og kan forbedre oppbevaring av kunden. I Dynamics 365 for operasjoner, er produktanbefalingene drives av kognitive tjenester og opplæring for Microsoft-Azure-maskin.

<a name="scenarios"></a>Scenarier
---------

Produktanbefalingene er aktivert for følgende POS-scenarier. De er tilgjengelige i skyen POS eller moderne POS (MPOS).

1.  På den **Produktbeskrivelse** side:

-   Hvis et lager knytte besøk en **Produktbeskrivelse** sannsynligvis siden når du ser på tidligere transaksjoner på tvers av forskjellige kanaler motoren anbefaling foreslår flere varer som kjøpes sammen.
-   Hvis butikken knytter legger til en kunde i transaksjonen, og deretter går til et **Produktbeskrivelse**, anbefaling-motoren gir tilpassede anbefalinger ved hjelp av kundens transaksjonshistorikk.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  På den **transaksjonen** side:

-   Motoren anbefaling foreslår elementer basert på hele listen med elementene i handlekurven.
-   Hvis butikken knytte legger til en kunde i transaksjonen, anbefaling-motoren gir personlige anbefalinger ved hjelp av kundens transaksjonshistorikk og listen over elementer i kurven.

**Legg merke til** å vise anbefalinger på den **transaksjonen** siden forhandleren må oppdatere skjermoppsett i Dynamics 365 for operasjoner. Den **anbefalinger** kontroll må slippes på den **transaksjonen** siden. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  På den **kundedetaljer** side:
    -   Motoren anbefaling foreslår varer basert på bruker-ID og elementer i kundens Ønskeliste.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 for operasjoner å aktivere anbefalinger for POS
Hvis du vil definere produktanbefalingene, må du gjøre følgende.

1.  Kontroller at du har valgt den riktige **juridisk enhet**.
2.  Gå til **enhet butikken**, velger **Retail sales**, og klikk deretter **Oppdater**. ** ** Dette bruke demodataene (eller data) fra operative databasen og flytte den til enheten lager.
3.  Valgfritt: Hvis du vil vise anbefalinger på skjermen for transaksjonen, kan du gå til ** skjermoppsett, **velge skjermoppsettet, starte den **utforming av skjermoppsett**,** ** og slipp den ** anbefalinger kontroll ** der det er nødvendig.
4.  Gå til **parametere for detaljhandel**, velger **maskin-læring**, velger ** Ja ** under **aktivere POS anbefalinger**.
5.  Hvis du vil se anbefalinger på POS, kjøre global konfigurasjon jobb **1110**. For å gjenspeile endringer i utforming av POS skjermoppsett, kan du kjøre kanal konfigurasjon jobb **1070**.

## <a name="how-does-it-work"></a>[]()Hvordan fungerer det?
Når du oppdaterer den **enhet butikken** enhet, følgende handlinger finner sted.

-   Data i formatet som kreves av kognitive tjenestene er trukket ut fra Dynamics-365 for operasjoner operative databasen og sendes til lageret for enheten.
-   Dataene brukes av Azure Data Factory (ADF) til cleanse data ved hjelp av strukturen skript som en del av ADF aktiviteter. Cleansed data lagres i blob-lagring.
-   Data fra blob-lagring for brukes av kognitive services API til å lære opp en anbefaling modell.

Når du slår på **aktivere anbefalinger** og kjøre konfigurasjon-jobber, følgende handlinger finner sted.

-   Modellen legitimasjon og ID er hentet fra APIen og lagret i Dynamics-365 for operasjoner operative databasen, i filen web.config for AOS og også i retail-server.
-   Modellen legitimasjon og ID er gjort tilgjengelig for CRT slik at kall til produktet anbefalinger fra skyen POS- og MPOS i tilkoblet modus kan opprettholdes.


<a name="see-also"></a>Se også
--------

[Legge til en kontroll for anbefalinger til siden transaksjonen på en POS-enhet](add-recommendations-control-pos-screen.md)


