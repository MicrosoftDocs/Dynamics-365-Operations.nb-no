---
title: "Salgsstedsprogram og språkinnstillinger for bruker"
description: "Dette emnet beskriver hvordan du endrer språkinnstillingene i Retail moderne POS (MPOS) og sky POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Salgsstedsprogram og språkinnstillinger for bruker

Dette emnet beskriver hvordan du endrer språkinnstillingene i Retail moderne POS (MPOS) og sky POS.

<a name="overview"></a>Oversikt
========

Detaljhandel moderne POS (MPOS) og sky POS støtter miljøer der innstillinger for språk og oversettelser kan variere mellom lager- og -innstillinger. Butikken kan for eksempel være plassert i et område der engelsk er mest vanlig for sine kunder, men noen arbeidere foretrekker å bruke programmet med franske oversettelser.

## <a name="data-language"></a>Språk for data
Uavhengig av brukerens innstillinger, vil MPOS og sky POS alltid bruke butikkens Språkinnstillinger for å bestemme oversettelser som brukes for data. Dette sikrer at alle brukere og kunder får en ensartet opplevelse.  Eksempler på data:

-   Produkter
-   Attributter og verdier
-   Kategorinavn
-   Transaksjonsmottak for utskrift eller sending via e-post
-   Navn på betalingsmåte
-   Linjevisningmeldinger

Butikkens språk brukes også for POS pålogging hovedskjermen fordi brukeren ikke er kjent før du logger på. Hvis en oversettelse ikke er tilgjengelig for butikkens språk, vil Salgsstedet tilbake til selskapets språk.

### <a name="configuring-the-stores-language-setting"></a>Konfigurere språkinnstillingene for butikken

Språkinnstillingen for butikkens angis fra **alle forretninger** på den **forhandler** side ** Generelt &gt;regionale innstillinger &gt;språk. ** Bruke rullegardinlisten ned til å velge språk for hver butikk.

## <a name="user-interface-language"></a>Språk for brukergrensesnittet
POS-brukerens språkinnstillingen bestemmer oversettelser som brukes i brukergrensesnittet for programmet. Dette inkluderer alle etiketter, menyer og lister som ikke anses data. Ett unntak er teksten som vises på POS-knappegrupper. Knappegruppene støtter ikke oversettelser, slik at de alltid vises teksten som er definert på-knappen. For å støtte oversatte knapper, må du kopiere og opprettholder egen knapp rutenett og tilordne dem til brukere etter behov.

### <a name="configuring-the-users-language-setting"></a>Konfigurere språkinnstillingene for brukeren

POS-brukerens språk settes fra **alle arbeidere** på den **arbeider** side **Retail &gt;språk**.  Det er ikke angitt i profilen hovedkategorien.  Denne innstillingen brukes ikke ved POS. Hvis brukerens språk ikke er angitt eller den er satt til et språk der oversettelsene ikke er tilgjengelige, tilbakestiller Salgsstedet til butikkens språk.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **UI-språket** ** **      | **Data-språk (produkter, kvitteringsformater, linjevisning, osv.)** |
| **Firma** | Standard                    | Standard                                                           |
| **Butikk**   | Overstyrer firma          | Overstyrer firma                                                 |
| **User**    | Overstyrer butikk eller firma | Aldri                                                             |




