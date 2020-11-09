---
title: Opprette en bestilling
description: Dette emnet viser hvordan du oppretter en bestilling manuelt.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec91174f291bcfa7027a93ca344823561cc29e3f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018166"
---
# <a name="create-a-purchase-order"></a>Opprette en bestilling

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter en bestilling manuelt. Det er mer vanlig at bestillinger opprettes automatisk som et resultat av hovedplanleggingen, direkte levering og andre prosesser. Bestillinger opprettes vanligvis av en innkjøpsagent. Dette eksemplet kan brukes i USMF-demodatafirmaet med verdiene som blir foreslått i notatene for de forskjellige trinnene.


## <a name="create-the-purchase-order-header"></a>Opprette bestillingshode
1. Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**.
2. Velg **Ny**.
3. Velg leverandørkonto **US-101**. Når du velger en leverandør, kopieres detaljer fra leverandørposten, for eksempel, adresse, fakturakonto, leveringsbetingelser og leveringsmåte, som standardverdier til ordrehodet. Du kan når som helst endre disse verdiene.  
4. Utvid delen **Generelt**.

    - **Område** - og **Lager** -feltet angir hvor de innkjøpte varene eller tjenestene skal leveres til. Standard leveringsadressen er området. Begge feltene kan fylles ut med verdier som er definert for den valgte leverandøren, eller du kan angi dem manuelt.  
    - **Leveringsdato** -feltet brukes til å angi når innkjøpte varer og tjenester skal leveres. Du kan angi en enkelt leveringsdato for ordren, eller de enkelte ordrelinjene kan gis unike leveringsdatoer. Hvis leveringsdatoen som er angitt her, ikke kan oppfylles for bestemte produkter eller tjenester fordi de har lengre leveringstider, opprettes linjene med en senere leveringsdato for å legge til rette for dette.  

5. Vis delen **Administrasjon**. **Bestiller** -feltet kan brukes til å angi hvem som bestiller. Dette kan være nyttig å dele med leverandøren i tilfelle de må kontakte vedkommende. Feltet kan tilordnes en verdi automatisk hvis gjeldende brukerkonto er knyttet til et navn på **Brukere** -siden.  
6. Velg **OK**. Ordreoverskriften er nå opprettet. Når du arbeider med bestillingslinjer, vises bare et sammendrag av informasjonen i overskriften. Hvis du vil vise resten av informasjonen, klikker du **Overskrift**.  

## <a name="add-a-purchase-order-line"></a>Legge til en bestillingslinje
1. Velg **Bestillingslinje**.
2. Velg **Dimensjoner**. Produkter kan være i varianter som skilles av dimensjoner, for eksempel farge, størrelse eller stil. Produkter kan også defineres til å bruke lagerdimensjoner, for eksempel område og lager. Det er også valgfrie sporingsdimensjoner, for eksempel parti- og serienumre. Hvis du vil forbedre effektiviteten for ordreregistrering, kan du legge til dimensjonsfeltene som du vanligvis bruker, direkte i rutenettet for ordren.  
3. Merk av for **Farge**. Valgfritt: Hvis du velger feltet **Lagre oppsett** , vil de valgte dimensjonene også vises i rutenettet for ordren neste gang du åpner bestillingssiden.  
4. Velg **OK**.
5. Velg **T0004** i feltet **Varenummer**.

    - Ordrelinjer opprettes for produkter og tjenester ved å angi et varenummer, eller som utgifter ved å angi en innkjøpskategori. 
    - Feltet **Innkjøpskategori** brukes til å legge til linjer der innkjøpte varer er utgiftsført direkte, i stedet for å gå til lager. Dette betyr at hvis du vil utgiftsføre et innkjøp, kan du gjøre dette ved å opprette en bestillingslinje som angir en innkjøpskategori, i stedet for å opprette en linje med et varenummer. Varer kan også knyttes til en innkjøpskategori, og i dette tilfellet vises innkjøpskategorien bare som informasjon.  

6. Angi eller velg en verdi i **Farge** -feltet. **Område** - og **Lager** -feltet fylles vanligvis ut med verdier fra ordreoverskriften, men det er mulig å overstyre feltene hvis noen av linjene skal leveres til ulike steder.  
7. Angi et tall i **Antall** -feltet.

    - Velg antallet du vil kjøpe inn. **Antall** -feltet fylles ut automatisk med minimum ordreantall for produktet hvis dette er definert, eller med verdien 1.  
    - **Enhet** -feltet angir måleenheten for det bestilte antallet. Vanligvis angis enheten automatisk fra innkjøpsenheten på hoveddata for produktet, men du kan endre dette.  
    - **Enhetspris** -feltet inneholder vanligvis en verdi fra en kjøpsavtale eller en forretningsavtale. Det er mulig å endre enhetsprisen på enkelte ordrelinjer, for eksempel hvis en unik pris forhandles med leverandøren.  
    - **Rabatt** -feltet representerer et rabattbeløp per enhet. Denne rabatten reduserer derfor enhetsprisen med rabatten. Denne rabatten angis vanligvis automatisk fra innkjøpsavtaler eller forretningsavtaler, men det er mulig å overstyre på de enkelte linjene hvis unike rabatter er forhandlet med leverandøren.  
    - Det kan angis en rabattprosent som reduserer nettobeløpet for linjen i henhold til dette. Rabattprosenten angis ofte automatisk fra innkjøpsavtaler eller forretningsavtaler, men det er mulig å overstyre på de enkelte linjene hvis en unik rabattprosent er forhandlet med leverandøren.  
    - Verdien i feltet **Nettobeløp** beregnes fra andre felt på linjen, inkludert antall, enhetspris, rabatt og rabattprosent. Det er mulig å endre nettobeløpet, men da vil feltene **Enhetspris** , **Rabatt** og **Rabattprosent** være tomme, og når du posterer mot linjen, vil det posterte beløpet være proporsjonalt med nettobeløpet. Feltet **Nettobeløp** brukes vanligvis bare til å vise nettobeløpet for linjen.  

8. Vis delen **Linjedetaljer**.
9. Velg **Levering** -fanen. En unik leveringsdato kan tilordnes til hver linje. Datoen hentes fra feltet i bestillingsoverskriften, men du kan endre dette.  

## <a name="review-order-totals"></a>Se gjennom ordretotaler
1. Velg **Totaler**.

    - Hvis du ikke ser handlingen **Totaler** , klikker du kategorien **Bestilling** i handlingsruten.  
    - Denne dialogboksen viser totaler for hele ordren.  
    -  **Valg** -feltet lar deg endre grunnlaget for hvordan totaler beregnes. Du kan for eksempel velge **Produktkvitteringsantall** for å vise totalsummer som er knyttet til produktantallet som er mottatt, eller **Bestilt antall** for å vise produktantallet som ble bestilt.  

2. Velg **OK**.

