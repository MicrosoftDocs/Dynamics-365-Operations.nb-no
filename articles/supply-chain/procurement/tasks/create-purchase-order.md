--- 
title: Opprette en bestilling
description: "Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt."
author: FrankDahl
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Opprette en bestilling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt. Det er mer vanlig at bestillinger opprettes automatisk som et resultat av hovedplanleggingen, direkte levering og andre prosesser. Bestillinger opprettes vanligvis av en innkjøpsagent. Dette eksemplet kan brukes i USMF-demodatafirmaet med verdiene som blir foreslått i notatene for de forskjellige trinnene.


## <a name="create-the-purchase-order-header"></a>Opprette bestillingshode
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Velg leverandørkonto US-101.
    * Når du velger en leverandør, kopieres detaljer fra leverandørposten, for eksempel, adresse, fakturakonto, leveringsbetingelser og leveringsmåte, som standardverdier til ordrehodet. Du kan når som helst endre disse verdiene.  
4. Utvid seksjonen Generelt.
    * Område- og Lager-feltet angir hvor de innkjøpte varene eller tjenestene skal leveres til. Standard leveringsadressen er området. Begge feltene kan fylles ut med verdier som er definert for den valgte leverandøren, eller du kan angi dem manuelt.  
    * Leveringsdato-feltet brukes til å angi når innkjøpte varer og tjenester skal leveres. Du kan angi en enkelt leveringsdato for ordren, eller de enkelte ordrelinjene kan gis unike leveringsdatoer. Hvis leveringsdatoen som er angitt her, ikke kan oppfylles for bestemte produkter eller tjenester fordi de har lengre leveringstider, opprettes linjene med en senere leveringsdato for å legge til rette for dette.  
5. Skjul delen Generelt.
6. Vis delen Administrasjon.
    * Bestiller-feltet kan brukes til å angi hvem som bestiller. Dette kan være nyttig å dele med leverandøren i tilfelle de må kontakte vedkommende. Feltet kan tilordnes en verdi automatisk hvis gjeldende brukerkonto er knyttet til et navn på Brukere-siden.  
7. Skjul delen Administrasjon.
8. Klikk OK.
    * Ordreoverskriften er nå opprettet. Når du arbeider med bestillingslinjer, vises bare et sammendrag av informasjonen i overskriften. Hvis du vil vise resten av informasjonen, klikker du overskriften.  

## <a name="add-a-purchase-order-line"></a>Legge til en bestillingslinje
1. Klikk Bestillingslinje.
2. Klikk Dimensjoner.
    * Produkter kan være i varianter som skilles av dimensjoner, for eksempel farge, størrelse eller stil. Produkter kan også defineres til å bruke lagerdimensjoner, for eksempel område og lager. Det er også valgfrie sporingsdimensjoner, for eksempel parti- og serienumre. Hvis du vil forbedre effektiviteten for ordreregistrering, kan du legge til dimensjonsfeltene som du vanligvis bruker, direkte i rutenettet for ordren.  
3. Merk av for Farge.
    * Valgfritt: Hvis du velger feltet Lagre oppsett, vil de valgte dimensjonene også vises i rutenettet for ordren neste gang du åpner bestillingssiden.  
4. Klikk OK.
5. Velg T0004 i feltet Varenummer.
    * Ordrelinjer opprettes for produkter og tjenester ved å angi et varenummer, eller som utgifter ved å angi en innkjøpskategori.  
    * Feltet Innkjøpskategori brukes til å legge til linjer der innkjøpte varer er utgiftsført direkte, i stedet for å gå til lager. Dette betyr at hvis du vil utgiftsføre et innkjøp, kan du gjøre dette ved å opprette en bestillingslinje som angir en innkjøpskategori, i stedet for å opprette en linje med et varenummer. Varer kan også knyttes til en innkjøpskategori, og i dette tilfellet vises innkjøpskategorien bare som informasjon.  
6. Angi eller velg en verdi i feltet Farge.
    * Område- og Lager-feltet fylles vanligvis ut med verdier fra ordreoverskriften, men det er mulig å overstyre feltene hvis noen av linjene skal leveres til ulike steder.  
7. Angi et tall i feltet Antall.
    * Velg antallet du vil kjøpe inn. Antall-feltet fylles ut automatisk med minimum ordreantall for produktet hvis dette er definert, eller med verdien 1.  
    * Enhet-feltet angir måleenheten for det bestilte antallet. Vanligvis angis enheten automatisk fra innkjøpsenheten på hoveddata for produktet, men du kan endre dette.  
    * Enhetspris-feltet inneholder vanligvis en verdi fra en kjøpsavtale eller en forretningsavtale. Det er mulig å endre enhetsprisen på enkelte ordrelinjene, for eksempel hvis en unik pris forhandles med leverandøren.  
    * Rabatt-feltet representerer et rabattbeløp per enhet. Denne rabatten reduserer derfor enhetsprisen med rabatten. Denne rabatten angis vanligvis automatisk fra innkjøpsavtaler eller forretningsavtaler, men det er mulig å overstyre på de enkelte linjene hvis unike rabatter er forhandlet med leverandøren.  
    * Det kan angis en rabattprosent som reduserer nettobeløpet for linjen i henhold til dette. Rabattprosenten angis ofte automatisk fra innkjøpsavtaler eller forretningsavtaler, men det er mulig å overstyre på de enkelte linjene hvis en unik rabattprosent er forhandlet med leverandøren.  
    * Verdien i feltet Nettobeløp beregnes fra andre felt på linjen, inkludert antall, enhetspris, rabatt og rabattprosent. Det er mulig å endre nettobeløpet, men da vil feltene Enhetspris, Rabatt, og Rabattprosent være tomme, og når du posterer mot linjen, vil det posterte beløpet være proporsjonalt med nettobeløpet. Feltet Nettobeløp brukes vanligvis bare til å vise nettobeløpet for linjen.  
8. Vis seksjonen Linjedetaljer.
9. Velg kategorien Levering.
    * En unik leveringsdato kan tilordnes til hver ordrelinje. Datoen hentes fra feltet i bestillingsoverskriften, men du kan endre dette.  
10. Skjul Linjedetaljer-delen.

## <a name="review-order-totals"></a>Se gjennom ordretotaler
1. Klikk Totaler.
    * Hvis du ikke ser handlingen Totaler, klikker du kategorien Bestilling på handlingslinjen.  
    * Denne dialogboksen viser totaler for hele ordren.  
    * Valg-feltet lar deg endre grunnlaget for hvordan totaler beregnes. Du kan for eksempel velge Produktkvitteringsantall for å vise totalsummer som er knyttet til produktantallet som er mottatt, eller Bestilt antall for å vise produktantallet som ble bestilt.  
2. Klikk OK.


