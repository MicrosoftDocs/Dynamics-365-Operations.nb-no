---
title: Personlige produktanbefalinger
description: Dette emnet inneholder informasjon om Dynamics 365 for Retail-produktanbefalingene som kan vises salgsstedsenheten.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: d6706cbb7630aeb230bc9eb1c187397897c9de68
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559564"
---
# <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger

[!include [banner](includes/banner.md)]

> [!NOTE]
> Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner. Hvis du vil ha mer informasjon, kan du se [Fjernede eller avskrevne funksjoner](../dev-itpro/migration-upgrade/deprecated-features.md).

Produktanbefalingene kan vises i Dynamics 365 for Retail på salgsstedsenheten. Anbefalingene er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker. For forhandlere med store kataloger bidrar anbefalinger kunden med å oppdage produkter. Ved å presentere produkter som er rettet mot en kundes interesser og kjøpsvaner, kan produktanbefalinger bidra til mersalg og kryssalg for forhandlere og forbedring av kundebevaring. I Dynamics 365 for Retail er produktanbefalinger drevet av kognitive tjenester og Microsoft Azure machine learning.

## <a name="scenarios"></a>Scenarier

Produktanbefalingene er aktivert for følgende POS-scenarier. De er tilgjengelige i Cloud POS eller Modern POS (MPOS).

1. På **Produktdetaljer**-siden:

    - Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingsmotoren flere varer som sannsynligvis kjøpes sammen.
    - Hvis den butikkansatte legger til en kunde i transaksjonen og deretter går til en **Produktdetaljer**-side, gir anbefalingsmotoren anbefalinger ved hjelp av kundens transaksjonshistorikk.

    [![proddetails](./media/proddetails.png)](./media/proddetails.png)

2. På **Transaksjon**-siden:

    - Anbefalingsmotoren foreslår varer basert på hele varelisten i handlekurven.
    - Hvis den butikkansatte legger til en kunde i transaksjonen, gir anbefalingsmotoren personlige anbefalinger ved hjelp av kundens transaksjonshistorikk og varelisten i handlekurven.

    > [!NOTE]
    > For å vise anbefalinger på **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 for Retail. **Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.

    [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3. På **Kundedetaljer**-siden:

    - Anbefalingsmotoren foreslår varer basert på bruker-ID og varene på kundens ønskeliste.

    [![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 for Retail for å aktivere anbefalinger for salgssted

Hvis du vil sette opp produktanbefalinger, må du gjøre følgende.

1. Kontroller at du har valgt riktig **Juridisk enhet**.
2. Gå til **Enhetslager**, velger **Detaljhandelsalg**, og klikk deretter på **Oppdater**. Dette bruker demonstrasjonsdataene (eller dataene) fra den operative databasen og flytter dem til enhetsbutikken.
3. Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.
4. Gå til **Forhandlerparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.
5. Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**. For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.

## <a name="how-does-it-work"></a>Hvordan fungerer det?

Når du oppdaterer den **Enhetslager**, følgende handlinger finner sted.

- Data i formatet som kreves av de kognitive tjenestene, er trukket ut fra Dynamics 365 for Retail-operativ database og sendes til enhetslageret.
- Dataene brukes av Azure Data Factory (ADF) til å rense data ved hjelp av strukturskript som en del av ADF-aktiviteter. Rensede data lagres i blob-lagring.
- Data fra blob-lagring brukes av kognitive services API til å lære opp en anbefalingsmodell.

Når du slår på **Aktiver anbefalinger** og kjører konfigurasjonjobbene, følgende handlinger finner sted.

- Modellens legitimasjon og ID hentes fra API-en og lagres i Dynamics 365 for Retail operativ database, i filen web.config for AOS og også i detaljhandelsserveren.
- Modellens legitimasjon og ID gjøres tilgjengelig for CRT slik at kall til produktanbefalinger fra Cloud POS og MPOS i tilkoblet modus kan opprettholdes.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Feilsøke problemer der du allerede har aktivert produktanbefalingene

- Gå til **detaljhandelsparametere** \> **maskinopplæring** \> **deaktiver produktanbefalingene** og kjør **Global konfigurasjon for jobben \[1110\]**. Hvis du ikke finner kategorien **maskinopplæring**, kan du kontakte kundestøtte for Dynamics.
- Hvis du har lagt **kontroll for anbefalinger** til din transaksjonsskjerm ved hjelp av **utforming av skjermoppsett**, må fjerne den også.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet](add-recommendations-control-pos-screen.md)
