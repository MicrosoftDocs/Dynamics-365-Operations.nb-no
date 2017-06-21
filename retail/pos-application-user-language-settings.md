---
title: "Salgsstedsprogram og språkinnstillinger for bruker"
description: "Dette emnet beskriver hvordan du endrer språkinnstillinger i moderne salgssted for detaljhandel (MPOS) og skysalgssted."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b2cbdb8bc65a3bfa84620a50480c503c3bb07991
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="pos-application-and-user-language-settings"></a>Salgsstedsprogram og språkinnstillinger for bruker

[!include[banner](includes/banner.md)]


Dette emnet beskriver hvordan du endrer språkinnstillinger i moderne salgssted for detaljhandel (MPOS) og skysalgssted.

<a name="overview"></a>Oversikt
========

Modern POS (MPOS) og Cloud POS for detaljhandelen støtter miljøer der innstillinger for språk og oversettelser kan variere mellom lageret og brukerinnstillinger. Butikken kan for eksempel være plassert i et område der engelsk er mest vanlig for kundene, men noen arbeidere foretrekker å bruke programmet med franske oversettelser.

## <a name="data-language"></a>Språk for data
Uavhengig av brukerens innstillinger, vil MPOS og Cloud POS alltid bruke butikkens språkinnstillinger for å bestemme oversettelser som brukes for data. Dette sikrer at alle brukere og kunder får en ensartet opplevelse.  Eksempler på data omfatter:

-   Produkter
-   Attributter og verdier
-   Kategorinavn
-   Transaksjonsmottak for utskrift eller sending via e-post
-   Navn på betalingsmåte
-   Linjevisningmeldinger

Butikkens språk brukes også for POS-påloggingshovedskjermen fordi brukeren ikke er kjent før du logger på. Hvis en oversettelse ikke er tilgjengelig for butikkens språk, vil POS gå tilbake til selskapets språk.

### <a name="configuring-the-stores-language-setting"></a>Konfigurere språkinnstillingene for butikken

Butikkens språkinnstillinger settes fra **Alle detaljhandelsbutikker** på siden **Detaljhandel** under **Generelt &gt; Regionale innstillinger &gt; Språk. **Bruk rullegardinlisten for å velge språk for hver butikk.

## <a name="user-interface-language"></a>Språk for brukergrensesnittet
POS-brukerens språkinnstilling bestemmer oversettelser som brukes i brukergrensesnittet for programmet. Dette inkluderer alle etiketter, menyer og lister som ikke anses data. Ett unntak er teksten som vises på POS-knappegrupper. Knappegruppene støtter ikke oversettelser, slik at de alltid vises teksten som er definert på-knappen. For å støtte oversatte knapper, må du kopiere og opprettholder egen knapp rutenett og tilordne dem til brukere etter behov.

### <a name="configuring-the-users-language-setting"></a>Konfigurere språkinnstillingene for brukeren

Salgsstedsbrukerens språkinnstillinger settes fra **Alle arbeidere** på siden **Arbeider** under **Detaljhandel &gt; Språk**.  Det angis ikke i hovedprofilkategorien.  Denne innstillingen brukes ikke av POS. Hvis brukerens språk ikke er angitt eller den er satt til et språk der oversettelsene ikke er tilgjengelige, tilbakestiller Salgsstedet til butikkens språk.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Språket i Brukergrensesnittet** ** **      | **Data-språk (produkter, kvitteringsformater, linjevisning, osv.)** |
| **Firma** | Standard                    | Standard                                                           |
| **Butikk**   | Overstyrer firma          | Overstyrer firma                                                 |
| **Bruker**    | Overstyrer butikk eller firma | Aldri                                                             |






