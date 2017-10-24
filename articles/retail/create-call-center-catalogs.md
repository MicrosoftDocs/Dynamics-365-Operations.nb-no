---
title: Opprette en telefonsenterkatalog
description: "Denne artikkelen gir en oversikt over prosessen for å opprette en katalog for et kundesenter."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-call-center-catalog"></a>Opprette en telefonsenterkatalog

[!include[banner](includes/banner.md)]


Denne artikkelen gir en oversikt over prosessen for å opprette en katalog for et kundesenter. 

I et telefonsenter kan du bruke produktkataloger til å identifisere produktene du vil tilby kundene. Telefonsentre bruker vanligvis trykte kataloger. Utforming og produksjonen av en trykt katalog håndteres utenfor Microsoft Dynamics 365 for Retail. Du kan imidlertid opprette og lagre en digital versjon av en katalog ved hjelp av de samme skjemaene du bruker til å definere detaljhandelskataloger for nettbutikker. Før du kan opprette en katalog, må du definere produktsortimenter og tilordne sortimentene til et telefonsenter. Deretter legger du til produkter i katalogen ved å velge produkter fra disse assortementene. Når produkter er lagt til i katalogen, og katalogen er fullstendig, må du validere katalogen for å kontrollere dataene. Deretter må du sende katalogen til vurdering og godkjenning. Når katalogen er godkjent, kan den publiseres. Når det opprettes en telefonsenterkatalog, kan du ta et øyeblikksbilde av katalogdataene når katalogen publiseres. Denne funksjonen for øyeblikksbilde gir deg tilgang til en bestemt versjon av katalogen selv om katalogen er endret og oppdatert senere. Telefonsenterkataloger kan også defineres slik at de omfatter følgende valgfrie funksjoner.

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




