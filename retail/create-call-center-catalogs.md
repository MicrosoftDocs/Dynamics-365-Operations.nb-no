---
title: Opprette en telefonsenterkatalog
description: "Denne artikkelen gir en oversikt over prosessen for å opprette en katalog for et kundesenter."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 857d280ab6d846c19102dd053a2c5f27fe14654c
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-call-center-catalog"></a>Opprette en telefonsenterkatalog

[!include[banner](includes/banner.md)]


Denne artikkelen gir en oversikt over prosessen for å opprette en katalog for et kundesenter. 

I et telefonsenter kan du bruke produktkataloger til å identifisere produktene du vil tilby kundene. Telefonsentre bruker vanligvis trykte kataloger. Utforming og produksjonen av en trykt katalog håndteres utenfor Microsoft Dynamics 365 for Operations. Du kan imidlertid opprette og lagre en digital versjon av en katalog i Detaljhandel og handel i Dynamics 365 for Operations ved hjelp av de samme skjemaene du bruker til å definere detaljhandelskataloger for nettbutikker. Før du kan opprette en katalog, må du definere produktsortimenter og tilordne sortimentene til et telefonsenter. Deretter legger du til produkter i katalogen ved å velge produkter fra disse assortementene. Når produkter er lagt til i katalogen, og katalogen er fullstendig, må du validere katalogen for å kontrollere dataene. Deretter må du sende katalogen til vurdering og godkjenning. Når katalogen er godkjent, kan den publiseres. Når det opprettes en telefonsenterkatalog, kan du ta et øyeblikksbilde av katalogdataene når katalogen publiseres. Denne funksjonen for øyeblikksbilde gir deg tilgang til en bestemt versjon av katalogen selv om katalogen er endret og oppdatert senere. Telefonsenterkataloger kan også defineres slik at de omfatter følgende valgfrie funksjoner.

-   **Kildekoder**  – koder som brukes til å spore kunderesponsen på bestemte katalogutsendelser.
-   **Gratisprodukter** – produkter som er inkludert i en kundes ordre uten ekstra kostnad. Disse produktene legges automatisk til ordren automatisk når kildekoden for katalogen angis i ordren.
-   **Skript** – Tekster som en telefonsenterarbeider leser for en kunde når det opprettes en salgsordre. Skript kan inkludere hilsener eller kjøpsforslag.
-   **Mersalgs- og kryssalgsvarer** - Varer som vises som et forslag når et bestemt produkt er lagt til i ordren.

Disse alternativene må defineres før katalogen godkjennes og publiseres.

## <a name="prerequisites"></a>Nødvendig programvare
Følgende oppgaver må være fullført før du starter:

-   Definer produkter og produktsortimenter.
-   Definer detaljprodukter.
-   Definer et sortiment.
-   Opprett et telefonsenter.
-   Definer et telefonsenter.
-   Legg til telefonsenteret i et organisasjonshierarki.
-   Opprett eller endre et organisasjonshierarki.

## <a name="create-a-catalog"></a>Opprette en katalog
Du må først opprette en katalog, legge til produkter i katalogen, og deretter se gjennom og oppdatere attributtene for produktene.

## <a name="validate-the-catalog"></a>Valider katalogen
Når du er ferdig med å opprette katalogen, må du validere den. Valideringsprosessen kontrollerer at dataene som kreves for kanalattributter og produktattributter, er fullstendige og gyldige, og at katalogen kan publiseres.

## <a name="submit-the-catalog-for-review-and-approval"></a>Send katalogen til gjennomgang og godkjenning
Når en katalog er validert, kan du sende den til vurdering og godkjenning. En katalog må være godkjent før den kan publiseres. Du kan konfigurere en arbeidsflyt slik at kataloger enten godkjennes automatisk eller må godkjennes manuelt.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Valgfritt: Legg til kildekoder, gratis produkter og skript
Du kan også legge til følgende varer i en telefonsenterkatalog. Disse varene er valgfrie.

-   **Kildekoder** kan brukes av firmaer som leverer trykte kataloger, for å spore kundenes tilbakemelding på bestemte kataloger. Kildekoder trykkes ofte på baksiden av en katalog, og er angitt i salgsordren når en kunde kjøper noe. Hvis du vil legge til en kildekode i katalogen, må du først opprette et målmarked. Målmarkedet er vanligvis tilordnet en utsendelsesliste som eies eller leies ut.
-   **Gratisprodukter** er kampanjevarer som er inkludert gratis med kundens ordre når det refereres til katalogen.
-   **Skript** kan brukes til å lede arbeiderens samhandling med kunder i konteksten for en katalog eller et produkt i en katalog.

## <a name="publish-the-catalog"></a>Publiser katalogen
Når du publiserer en katalog for et telefonsenter, fullfører du produktinformasjonen i katalogen. Publisering angir også at katalogen er klar til flere handlinger du vil utføre. Du kan for eksempel opprette en trykt katalog. Du kan publisere katalogene manuelt, eller du kan bruke en partiprosess til å publisere i henhold til en tidsplan. Før du kan publisere en katalog, må katalogen valideres og godkjennes. Hvis du vil endre katalogen etter at den er publisert, kan du tilbakekalle katalogen og deretter publisere den på nytt.



