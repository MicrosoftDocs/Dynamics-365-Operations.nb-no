---
title: Opprette salgsordrer
description: Denne fremgangsmåten viser hvordan du oppretter en salgsordre.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a52c512d630e560afac998e1a35e71204d98f5d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841365"
---
# <a name="create-sales-orders"></a>Opprette salgsordrer

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en salgsordre. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Salgsordrer opprettes vanligvis av en salgsordrebehandler. 

## <a name="enter-sales-order-header-details"></a>Angi topptekstdetaljer for salgsordre
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
2. Velg **Ny**.
3. Klikk på rullegardinknappen i **Kundekonto**-feltet for å åpne oppslaget.
4. Finn og velg kundeposten i listen.
    - I dette eksemplet kan du velge kundenummer USA-004.  
5. Velg **OK**.

## <a name="enter-sales-order-line-details"></a>Angi detaljer for salgsordrelinje
    
Produktene som selges av organisasjon din, kan leveres i ulike varianter differensiert etter dimensjoner, for eksempel konfigurasjon, farge, størrelse og stil. Produkter kan også defineres slik at de bruker lagerdimensjoner, for eksempel område, lager, og pall og sporingsdimensjoner, for eksempel bunkenumre og serienumre. Når disse dimensjonene er tilordnet, må du velge verdier for disse dimensjonene på ordrelinjen. Hvis du vil forbedre effektiviteten for ordreregistrering, kan du legge til de respektive dimensjonsfeltene i rutenettet for ordren.
    
1. Velg **Salgsordrelinje** i delen **Salgsordrelinjer**.
2. Velg **Dimensjoner**.
    
    Velg farge-, område- og lagerdimensjonene i dette eksemplet. Dimensjonene du velger her, vises i rutenettet for salgsordren. Hvis du vil at valgene skal beholdes, setter du alternativet **Lagre oppsett** til Ja.
    
3. Velg **OK**.
4. Klikk på rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
5. I dette eksemplet velger du varenummer T0004.
    - Hvis varen er en del av en salgskategori, vises varenavnet automatisk i Salgskategori-feltet.  
    - Hvis produktdimensjonsfelt allerede inneholder en verdi, skyldes dette at verdien ble kopiert fra produktposten der den er definert som en standard produktdimensjon. Du kan når som helst endre standardverdien.   
6. Klikk på rullegardinknappen i **Farge**-feltet for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Angi et tall i **Antall**-feltet.
    - Hvis varen selges i andre enheter enn når den kjøpes, produseres og lagres, og en salgsenhet er angitt i produktposten, vises denne verdien i **Enhet**-feltet. Du kan når som helst endre verdien.   
    - Hvis **Område**-feltet allerede inneholder en verdi, ble verdien kopiert fra ordrehodet eller fra ordreinnstillingene som er knyttet til produktet. Du kan når som helst endre verdien. Hvis feltet er tomt, velger du en verdi.   
    - Hvis **Enhetspris**-feltet allerede inneholder en verdi, ble verdien kopiert fra en gyldig forretningsavtale eller fra produktposten. (Enhetsprisen kan også stamme fra en salgsavtale, men prosessen med å opprette salgsordrer fra salgsavtaler er ulik den som vises her.) Hvis feltet er tomt, kan du angi en verdi.   
    - **Rabatt**-feltet inneholder et rabattbeløp per produktenhet. For å beregne det totale linjerabattbeløpet multipliseres rabattverdien med linjeantall. Hvis **Rabatt**-feltet allerede inneholder en verdi, ble verdien kopiert fra en gyldig forretningsavtale. Hvis feltet er tomt, og du ønsker å gi kunden en linjerabatt, kan du angi en verdi.  
    - **Rabattprosent**-feltet inneholder en prosentverdi som det totale linjebruttobeløpet skal reduseres med.  Hvis **Rabattprosent**-feltet allerede inneholder en verdi, ble den kopiert fra en gyldig forretningsavtale. Hvis feltet er tomt, og du ønsker å gi kunden en linjerabatt, kan du angi en verdi. 
    - **Nettobeløp**-feltet inneholder en verdi som er beregnet basert på linjens vareantall og enhetspris justert etter rabatter.  Du kan overstyre den beregnede verdien til en annen.  

## <a name="review-the-order-totals"></a>Se gjennom ordretotalene
1. Velg **Salgsordre** i **Handlingsrute**.
2. Velg **Totaler**.
    
    **Totaler**-siden viser detaljer om hele ordren. Dette inkluderer delsumbeløpet, som er summen av alle linjenettobeløp justert for eventuelle linjerabatter, det totale fakturabeløpet, som er en delsum som er justert for eventuell rabatt på ordrenivå, tillegg, merverdiavgift, kundens kredittgrense og mer. Fakturabeløpet er beløpet som skal vises på kundens fakturadokument.  
    
3. Velg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]