---
title: Oversikt over personlige produktanbefalinger
description: "Produktanbefalingene kan vises i Dynamics 365 for Retail på salgsstedsenheten. Anbefalingene er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker. For forhandlere med store kataloger bidrar anbefalinger kunden med å oppdage produkter. Ved å presentere produkter som er rettet mot en kundes interesser og kjøpsvaner, kan produktanbefalinger bidra til mersalg og kryssalg for forhandlere og forbedring av kundebevaring. I Dynamics 365 for Retail er produktanbefalingene drevet av kognitive tjenester og Microsoft Azure Machine Learning."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a>Oversikt over personlige produktanbefalinger

[!include[banner](includes/banner.md)]


> [!NOTE]
> Denne funksjonen er for tiden tilgjengelig bare for sandkasse og produksjons (høy tilgjengelighet) -distribusjonstopologier. 

Produktanbefalingene kan vises i Dynamics 365 for Retail på salgsstedsenheten. Anbefalingene er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker. For forhandlere med store kataloger bidrar anbefalinger kunden med å oppdage produkter. Ved å presentere produkter som er rettet mot en kundes interesser og kjøpsvaner, kan produktanbefalinger bidra til mersalg og kryssalg for forhandlere og forbedring av kundebevaring. I Dynamics 365 for Retail er produktanbefalingene drevet av kognitive tjenester og Microsoft Azure Machine Learning.


<a name="scenarios"></a>Scenarier
---------

Produktanbefalingene er aktivert for følgende POS-scenarier. De er tilgjengelige i Cloud POS eller Modern POS (MPOS).

1.  På **Produktdetaljer**-siden:

-   Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingsmotoren flere varer som sannsynligvis kjøpes sammen.
-   Hvis den butikkansatte legger til en kunde i transaksjonen og deretter går til en **Produktdetaljer**-side, gir anbefalingsmotoren anbefalinger ved hjelp av kundens transaksjonshistorikk.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  På **Transaksjon**-siden:

-   Anbefalingsmotoren foreslår varer basert på hele varelisten i handlekurven.
-   Hvis den butikkansatte legger til en kunde i transaksjonen, gir anbefalingsmotoren personlige anbefalinger ved hjelp av kundens transaksjonshistorikk og varelistsen i handlekurven.

> [!NOTE]
> For å vise anbefalinger i **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 for Retail. **Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  På **Kundedetaljer**-siden:
    -   Anbefalingsmotoren foreslår varer basert på bruker-ID og varene på kundens ønskeliste.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 for Retail for å aktivere POS-anbefalinger
Hvis du vil sette opp produktanbefalinger, må du gjøre følgende.

1.  Kontroller at du har valgt riktig **Juridisk enhet**.
2.  Naviger til **Enhetslager**, velg **Forhandlersalg**, og klikk deretter **Oppdater**. Dette vil bruke demodata (eller dine data) fra din operative database og flytte den til Enhetslageret.
3.  Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.
4.  Gå til **Forhandlerparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.
5.  Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**. For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.

## <a name="how-does-it-work"></a>[]()Hvordan fungerer det?
Når du oppdaterer den **Enhetslager**, følgende handlinger finner sted.

-   Data i formatet som kreves av de kognitive tjenestene er trukket ut fra Dynamics 365 for Retail operativ database og sendes til enhetslageret.
-   Dataene brukes av Azure Data Factory (ADF) til å rense data ved hjelp av strukturskript som en del av ADF-aktiviteter. Rensede data lagres i blob-lagring.
-   Data fra blob-lagring brukes av kognitive services API til å lære opp en anbefalingsmodell.

Når du slår på **Aktiver anbefalinger** og kjører konfigurasjonjobbene, følgende handlinger finner sted.

-   Modellens legitimasjon og ID hentes fra API-en og lagres i Dynamics 365 for Retail operativ database, i filen web.config for AOS og også i detaljhandelsserveren.
-   Modellens legitimasjon og ID gjøres tilgjengelig for CRT slik at kall til produktanbefalinger fra Cloud POS og MPOS i tilkoblet modus kan opprettholdes.


<a name="see-also"></a>Se også
--------

[Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet](add-recommendations-control-pos-screen.md)




