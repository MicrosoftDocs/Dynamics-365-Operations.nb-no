---
title: Opprette salgsordrer
description: Denne fremgangsmåten viser hvordan du oppretter en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8af0333d979ba3a4e12d4f22b1225f3b72d66a7a
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2019
ms.locfileid: "352120"
---
# <a name="create-sales-orders"></a>Opprette salgsordrer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en salgsordre. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Salgsordrer opprettes vanligvis av en salgsordrebehandler. 




## <a name="enter-sales-order-header-details"></a>Angi topptekstdetaljer for salgsordre
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg kundeposten i listen.
    * I dette eksemplet kan du velge kundenummer USA-004.  
5. Klikk koblingen i den valgte raden i listen.
6. Klikk OK.

## <a name="enter-sales-order-line-details"></a>Angi detaljer for salgsordrelinje
    * Produktene som selges av organisasjon din, kan leveres i ulike varianter differensiert etter dimensjoner, for eksempel konfigurasjon, farge, størrelse og stil. Produkter kan også defineres til å bruke lagerdimensjoner, for eksempel område, lager, og pall og sporingsdimensjon, for eksempel bunkenumre og serienumre. Når disse dimensjonene er tilordnet, må du velge verdier for disse dimensjonene på ordrelinjen. Hvis du vil forbedre effektiviteten for ordreregistrering, kan du legge til de respektive dimensjonsfeltene i rutenettet for ordren.  
1. Klikk Salgsordrelinje.
2. Klikk Dimensjoner.
    * Velg farge-, område- og lagerdimensjonene i dette eksemplet. Dimensjonene du velger her, vises i rutenettet for salgsordren. Hvis du vil at valgene skal beholdes, kan du angi alternativet Lagre oppsett til Ja.   
3. Klikk OK.
4. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
5. I dette eksemplet velger du varenummer T0004.
6. Klikk koblingen i den valgte raden i listen.
    * Hvis varen er en del av en salgskategori, vises varenavnet automatisk i Salgskategori-feltet.  
    * Hvis produktdimensjonsfelt allerede inneholder en verdi, skyldes dette at verdien ble kopiert fra produktposten der den er definert som en standard produktdimensjon. Du kan når som helst endre standardverdien.   
7. Klikk rullegardinknappen i Farge-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
9. Klikk koblingen i den valgte raden i listen.
10. Angi et tall i feltet Antall.
    * Hvis varen selges i andre enheter enn når den kjøpes, produseres og lagres, og en salgsenhet er angitt i produktposten, vises denne verdien i Enhet-feltet. Du kan når som helst endre verdien.   
    * Hvis områdefeltet allerede inneholder en verdi, ble verdien kopiert fra ordrehodet eller fra ordreinnstillingene som er tilknyttet produktet. Du kan når som helst endre verdien. Hvis feltet er tomt, velger du en verdi.   
    * Hvis Enhetspris-feltet allerede inneholder en verdi, ble verdien kopiert fra en gyldig forretningsavtale eller fra produktposten. (Enhetsprisen kan også stamme fra en salgsavtale, men prosessen med å opprette salgsordrer fra salgsavtaler er ulik den som vises her.) Hvis feltet er tomt, kan du angi en verdi.   
    * Rabatt-feltet inneholder et rabattbeløp per produktenhet. For å beregne det totale linjerabattbeløpet multipliseres rabattverdien med linjeantall.    Hvis Rabatt-feltet allerede inneholder en verdi, ble verdien kopiert fra en gyldig forretningsavtale. Hvis feltet er tomt, og du ønsker å gi kunden en linjerabatt, kan du angi en verdi.  
    * Rabattprosent-feltet inneholder en prosentverdi som det totale linjebruttobeløpet skal reduseres med.  Hvis Rabattprosent-feltet allerede inneholder en verdi, ble den kopiert fra en gyldig forretningsavtale. Hvis feltet er tomt, og du ønsker å gi kunden en linjerabatt, kan du angi en verdi.  
    * Nettobeløp-feltet inneholder en verdi som er beregnet basert på linjens vareantall og enhetspris justert etter rabatter.  Du kan overstyre den beregnede verdien til en annen.  

## <a name="review-the-order-totals"></a>Se gjennom ordretotalene
1. Klikk Salgsordre i handlingsruten.
2. Klikk Totaler.
    * Totaler-siden viser detaljer om hele ordren. Dette inkluderer delsumbeløpet, som er summen av alle linjenettobeløp justert for eventuelle linjerabatter, det totale fakturabeløpet, som er en delsum som er justert for eventuell rabatt på ordrenivå, tillegg, merverdiavgift, kundens kredittgrense og mer.  Fakturabeløpet er beløpet som skal vises på kundens fakturadokument.  
3. Klikk OK.

