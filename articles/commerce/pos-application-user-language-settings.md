---
title: Program for salgssted (POS) og språkinnstillinger for bruker
description: Denne artikkelen beskriver hvordan du endrer språkinnstillinger i Modern POS (MPOS) og Cloud POS.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288386"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Program for salgssted (POS) og språkinnstillinger for bruker

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du endrer språkinnstillinger i Modern POS (MPOS) og Cloud POS.

## <a name="overview"></a>Oversikt
Modern POS (MPOS) og Cloud POS støtter miljøer der innstillinger for språk og oversettelser kan variere mellom lageret og brukerinnstillinger. Butikken kan for eksempel være plassert i et område der engelsk er mest vanlig for kundene, men noen arbeidere foretrekker å bruke programmet med franske oversettelser.

## <a name="data-language"></a>Språk for data

Uavhengig av brukerens innstillinger, vil MPOS og Cloud POS alltid bruke butikkens språkinnstillinger for å bestemme oversettelser som brukes for data. Dette sikrer at alle brukere og kunder får en ensartet opplevelse. Eksempler på data omfatter:

- Produkter
- Attributter og verdier
- Kategorinavn
- Transaksjonsmottak for utskrift eller sending via e-post
- Navn på betalingsmåte
- Linjevisningmeldinger

Butikkens språk brukes også for POS-påloggingshovedskjermen fordi brukeren ikke er kjent før du logger på. Hvis en oversettelse ikke er tilgjengelig for butikkens språk, vil POS gå tilbake til selskapets språk.

### <a name="configuring-the-stores-language-setting"></a>Konfigurere språkinnstillingene for butikken

Butikkens språkinnstillinger settes fra **Alle butikker** på siden **Butikk** under **Generelt &gt; Regionale innstillinger &gt; Språk**. Bruk rullegardinlisten for å velge språk for hver butikk.

## <a name="user-interface-language"></a>Språk for brukergrensesnittet

POS-brukerens språkinnstilling bestemmer oversettelser som brukes i brukergrensesnittet for programmet. Dette inkluderer alle etiketter, menyer og lister som ikke anses data. Ett unntak er teksten som vises på POS-knappegrupper. Knappegruppene støtter ikke oversettelser, slik at de alltid vises teksten som er definert på-knappen. For å støtte oversatte knapper, må du kopiere og opprettholder egen knapp rutenett og tilordne dem til brukere etter behov.

### <a name="configuring-the-users-language-setting"></a>Konfigurere språkinnstillingene for brukeren

Salgsstedsbrukerens språkinnstillinger settes fra **Alle arbeidere** på siden **Arbeider** under **Retail og Commerce &gt; Språk**. Den angis ikke i hovedprofilkategorien. Denne innstillingen brukes ikke av salgssted. Hvis brukerens språk ikke er angitt eller den er satt til et språk der oversettelsene ikke er tilgjengelige, tilbakestiller Salgsstedet til butikkens språk.

| &nbsp;      | Språket i Brukergrensesnittet                  | Data-språk (produkter, kvitteringsformater, linjevisning, osv.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Firma** | Standard                    | Standard                                                       |
| **Butikk**   | Overstyrer firma          | Overstyrer firma                                             |
| **Bruker**    | Overstyrer butikk eller firma | Aldri                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
