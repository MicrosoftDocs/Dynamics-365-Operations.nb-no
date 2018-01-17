---
title: Konfigurere RFM-analyse
description: Dette emnet forklarer hvordan du setter opp en recency-, frekvens- og pengeanalyse (RFM) av kundene dine.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: e66208ccceb4c248c2704bb7358d77447e032205
ms.openlocfilehash: c59d12c54563b883ae6d8ea8594f423f02797f4f
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-rfm-analysis"></a>Konfigurere RFM-analyse

[!include[banner](includes/banner.md)]


Dette emnet forklarer hvordan du setter opp en recency-, frekvens- og pengeanalyse (RFM) av kundene dine.

Recency-, frekvens- og pengeanalyse (RFM) er et markedsføringsverktøy organisasjonen kan bruke til å evaluere dataene som genereres av kundebestillinger. Når du har definert RFM-analyse, tilordnes kunder en beregnet RFM-poengsum når de gjør innkjøp. Poengsummen for tilbudsforespørselen kan være en tresifret vurdering eller et samlet tall, avhengig av hvordan organisasjonen har konfigurert analyse av tilbudsforespørsler. Slik fungerer vurderingen hvis organisasjonen bruker en tresifret vurdering for poengsummen:

- Det første sifferet er kundens recency-vurderingen, som er hvor nylig kunden har gjort et kjøpt fra din organisasjon. 
- Det andre sifferet er kundens frekvensrangering, som er hvor ofte kunden kjøper fra organisasjonen. 
- Det tredje sifferet er kundens pengerangering, som er hvor mye kundene bruker når de foretar kjøp fra organisasjonen. 

Organisasjonen har for eksempel satt vurderingene på en skala fra 1 til 5, der 5 er den høyeste klassifiseringen. I dette tilfellet forteller en kunde vurdering på 535 deg følgende informasjon om kunden:

-   **Recency-rangering på 5** – Kunden har handlet nylig.
-   **Frekvensrangering på 3** – Kunden kjøper produkter fra organisasjonen med moderat hyppighet.
-   **Pengerangering på 5** – når kundene kjøper noe, bruker de et betydelig pengebeløp.

Hvis organisasjonen bruker en sum av tallene, legges de individuelle rangeringene sammen. For det samme eksemplet har kunden en rangering på 13 (5 + 3 + 5).

## <a name="to-set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Slik konfigurerer du RFM-analyse for kundene i organisasjonen.

1.  Gå til **Telefonsenter** > **Periodisk** > **RFM-analyse**.

2.  På siden **RFM-analyse** velger du **Ny**. I feltet **RFM-definisjon** angir du et beskrivende navn på RFM-definisjonen. Du kan for eksempel kalle definisjonen RFM-A.

3.  Angi en startdato og en sluttdato for denne RFM-definisjonen.

4.  På hurtigfanen **Generelt** gjør du følgende: 
    - Hvis hver del av RFM-poengsummen må inneholde et likt antall kunder, merker du av for **Jevn fordeling**. 
    - Merk av for **Legg til poengummer** for å legge sammen de tre poengsummene. Dette vil for eksempel gi en kunde en RFM-poengsum på 13 i stedet for 535. 
    - Merk av for **Lagre historikk** hvis du vil at systemet skal lagre statistiske data for kunder, slik at dataene kan brukes til å beregne RFM-poengsum.
  
5.  På hurtigfanen **Recency** gjør du følgende: 
    - I **Inndelinger**-feltet angir du hvor mange inndelinger, eller grupper, som skal brukes til å beregne recency-poengsummen for kunder. Hvis du for eksempel har 100 kunder, betyr en inndeling på 5 at det er 20 kunder for hvert resultat. De 20 kundene som har foretatt de siste kjøpene, har en recency-poengsum på 5. De neste 20 kundene har en recency-poengsum på 4 og så videre. Hvis du har 50 kunder, har 10 kunder recency-poengsummen 5, 10 har recency-poengsummen 4 og så videre. 
    - I **Prioritet**-feltet velger du hvor stor vekt du vil legge på recency-parameteren i forhold til de andre parameterne, når RFM-poengsummen beregnes for en kunde. Du kan for eksempel legge mer vekt på recency-poengsummen enn pengepoengsummen. 
    - I **Multiplikator**-feltet angir du verdien som recency-poengsummen skal multipliseres med. Hvis du ikke angir en verdi, blir ikke poengsummen multiplisert. 
    - I **Periode**-feltet velger du hvilken tidsperiode beregningen av recency-poengsummen skal baseres på. For eksempel etter uke eller måned.
   
6.  På hurtigfanen **Frekvens** gjør du følgende: 
    - I **Inndelinger**-feltet angir du hvor mange inndelinger, eller grupper, som skal brukes til å beregne frekvenspoengsummen for kunder. 
    - I **Prioritet**-feltet velger du hvor stor vekt du vil legge på frekvensparameteren i forhold til de andre, når RFM-poengsummen beregnes for en kunde. 
    - I **Multiplikator**-feltet angir du verdien som frekvenspoengsummen skal multipliseres med. Hvis du ikke angir en verdi, blir ikke poengsummen multiplisert.
   
7.  På hurtigfanen **Monetær** gjør du følgende: 
    - I **Inndelinger**-feltet angir du hvor mange inndelinger, eller grupper, som skal brukes til å beregne pengepoengsummen for kunder. 
    - I **Prioritet**-feltet velger du hvor stor vekt du vil legge på pengeparameteren i forhold til de andre, når RFM-poengsummen beregnes for en kunde. 
    - I **Multiplikator**-feltet angir du verdien som pengepoengsummen skal multipliseres med. Hvis du ikke angir en verdi, blir ikke poengsummen multiplisert. 
    - I feltet **Brutto/netto** velger du om kundens pengepoengsum skal beregnes ved hjelp av brutto eller netto fakturabeløp. 
    - Hvis en kundes returbeløp skal trekkes fra beregningen av fakturatotalen for kunden, merker du av for **Trekk fra returer**. 
 
## <a name="view-a-customers-rfm-score"></a>Vise RFM-poengsum for en kunde
Bruk denne fremgangsmåten for å vise RFM-poengsum for en kunde. 

1.  Gå til **Telefonsenter** > **Journaler** > **Kundeservice**. 

2.  Velg nøkkelordtypen du vil søke etter, i søkefeltene i ruten **Kundeservice** på siden **Kundeservice**, og skriv inn søketeksten.

3.  Velg **Søk**.

4.  På siden **Kundesøk** velger du kundeposten du vil bruke, og klikker deretter på **Velg kunde**. 

Tilbudsforespørselens poengsum vises i gruppen **Ordrehistorikk** til høyre på siden **Kundeservice**. 

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Vise eller tømme loggen for en RFM-analysepost
Bruk denne fremgangsmåten for å vise eller tømme loggen for en RFM-analysepost. 

1.  Gå til **Telefonsenter** > **Periodisk** > **RFM-analyse**.

2.  Velg posten du vil vise, på siden **RFM-analyse**.

3.  Hvis du vil vise posthistorikken, velger du hurtigfanen **Historikk**.

4.  Hvis du vil slette historikken for posten, velger du **Tøm historikk**.

