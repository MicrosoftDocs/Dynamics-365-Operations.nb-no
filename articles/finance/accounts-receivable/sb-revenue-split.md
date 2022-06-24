---
title: Inntektsdelingsmaler i Abonnementsfakturering
description: Denne artikkelen beskriver hvordan du konfigurerer maler for inntektsdeling for varer som selges som bunter.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904766"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Inntektsdelingsmaler i Abonnementsfakturering

Bruk siden **Inntektsdelingsmal** til å opprette maler for inntektsoppdeling. Inntektsdeling består av en overordnet vare som har underordnede varer. Denne typen vare selges ofte til kunder som en enkeltvare eller bunt.

En datamaskinvare kan for eksempel opprettes på følgende måte:

- **Overordnet vare:** Abonnement Sølv
- **Linjevarer (underordnede):**

    - Kundestøtte
    - Vedlikehold
    - Lisens

Når du oppretter en overordnet vare, må du huske på følgende begrensninger:

- En vare kan bare angis som en overordnet vare én gang.
- Den overordnede varen kan velges som en underordnet vare i samme mal.
- En gyldig mal krever minst én underordnet vare.
- En vare kan angis som en underordnet vare for mer enn én buntvare.
- Hver overordnet-underordnet-relasjon må være unik.

## <a name="create-a-parent-item-that-has-child-items"></a>Opprett en overordnet vare som har underordnede varer

Følg denne fremgangsmåten for å opprette en overordnet vare som har underordnede varer.

1. Velg **Ny** på siden **Inntektsdelingsmal**.
1. Velg en overordnet vare i feltet **Overordnet vare**. **Variantnummer**-feltet oppdateres automatisk. Du kan endre verdien etter behov.
1. Velg en tildelingsmetode i feltet **Tildelingsmetode**.
1. Velg **Legg til** for å legge til underordnede varer i **Komponentvarer**-listen.
1. Hvis du valgte **Prosent** i feltet **Tildelingsmetode**, angir du en prosent i **Prosent**-feltet.

    - Hvis du valgte **Like beløp** i **Tildelingsmetode**-feltet, oppdateres **Prosent**-feltet automatisk slik at hver vare har lik prosent.
    - Hvis du valgte **Variabelt beløp**, **Null overordnet beløp** eller **Nullbeløp** i **Tildelingsmetode**-feltet,blir verdien i **Prosent**-feltet **0** (null) og kan ikke endres.

1. Velg **Lagre**.

## <a name="fields"></a>Felt

Siden **Inntektdelingsmal** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Overordnet vare | Velg et varenummer. Denne varen blir den overordnede varen for buntvaren du oppretter. |
| Produktnavn | Produktnavnet. |
| Tildelingsmetode | <p>Velg tildelingsmetoden:</p><ul><li>**Likt beløp** – Tildelingsprosentene beregnes automatisk og fordeles likt mellom alle varene i malen.</li><li>**Prosent** – Du kan angi et prosentbeløp for tildelingen. Summen av alle prosenter må være lik 100.</li><li>**Variabelt beløp** – Underordnede varer som legges til, har nettobeløp på 0 (null). Prisen på de underordnede varene må angis på transaksjonsnivå.</li><li>**Nullbeløp** – Den overordnede varen beholder enhetsprisen og nettobeløpet. Alle underordnede varer har et nettobeløp på 0 (null).</li><li>**Null overordnet beløp** – Den overordnede varen har et fast nettobeløp på 0 (null). Alle underordnede varer behandles som standardvarer. Det utføres ingen validering for å kontrollere at summen av underordnede varebeløp er lik det overordnede varebeløpet.</li></ul> |
| **Komponentvarer** | |
| Komponentvare | Velg et varenummer. Denne varen er en underordnet vare. |
| Variantnummer | Velg variantnummer for varen. |
| Produktnavn | Produktnavnet. |
| Prosent | <p>Tildelingsprosenten for milepælen:</p><ul><li>Hvis feltet **Tildelingsmetode** er satt til **Prosent**, kan du angi prosenten.</li><li>Hvis feltet **Tildelingsmetode** er satt til **Likt beløp**, beregnes prosenten automatisk slik at hver vare i malen har lik prosent.</li><li>Hvis **Tildelingsmetode**-feltet er satt til **Variabelt beløp**, **Null overordnet beløp** eller **Nullbeløp**, er prosenten 0 (null) og kan ikke redigeres.</li></ul><p>Verdien i dette feltet kan være et hvilket som helst positivt tall mellom 0 (null) og 100. Summen av alle prosentene må være lik 100.</p> |
| Total prosentandel | <p>Summen av verdier i **Prosent**-kolonnen.</p><ul><li>Hvis feltet **Tildelingsmetode** er satt til **Like beløp** eller **Prosent**, må summen av alle prosentverdiene være lik 100.</li><li>Hvis **Tildelingsmetode**-feltet er satt til **Variabelt beløp**, **Null overordnet beløp** eller **Nullbeløp**, er total prosent 0 (null).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Inntektsdeling på en salgsordre

Følg denne fremgangsmåten for å opprette en salgsordre som har en vare som er definert for inntektsdeling.

1. Opprett en salgsordre på siden **Salgsordrer**.
2. Merk av for **Inntektsdeling** på linjen for hver vare som er definert for inntektsdeling. Denne varen blir den overordnede varen. Hvis malen allerede er definert, vises de underordnede varene automatisk i listen.
3. Hvis du vil legge til flere underordnede varer, velger du **Legg til underordnet inntektsdeling** og velger den underordnede varen du vil legge til.
4. Lagre ordren.

## <a name="revenue-split-with-billing-schedules"></a>Inntektsdeling med faktureringsplaner

Følg denne fremgangsmåten for å opprette en faktureringsplan som har en vare som er definert for inntektsdeling.

1. Opprett en faktureringsplan på siden **Alle/aktive faktureringsplaner**.
2. Merk av for **Inntektsdeling** på linjen for hver vare som er definert for inntektsdeling. Denne varen blir den overordnede varen. Hvis malen allerede er definert, vises de underordnede varene automatisk i listen.
3. Hvis du vil legge til flere underordnede varer, velger du **Legg til underordnet inntektsdeling** og velger den underordnede varen du vil legge til.
4. Fortsett med trinnene for arbeid med faktureringsplanen.

> [!NOTE]
> Hvis alternativet **Opprett inntektsdeling automatisk** er satt til **Ja** på siden **Parametere for regelmessig kontraktfakturering**, skjer følgende handlinger:
>
> - Hvis linjevaren er satt opp som overordnet vare i en inntektsdelingsmal, velges **Inntektsdeling**-avmerkingsboksen automatisk.
> - De underordnede varene angis automatisk på salgsordre- eller faktureringsplanlinjen.
>
> Hvis alternativet **Opprett inntektsdeling automatisk** er satt til **Nei**, er virkemåten som forklart tidligere.

## <a name="additional-revenue-split-information"></a>Ytterligere inntektsdelingsinformasjon

Når du legger til en vare som er del av en omsetningsdeling, noterer du deg følgende informasjon: 

- Det overordnede beløpet kan ikke utsettes.
- Startdatoen, sluttdatoen, antallet, enheten, området og lagerverdiene for underordnede varer er basert på den overordnede varen. Disse verdiene kan ikke endres for de underordnede varene. Alle endringer må foretas i den overordnede varen. 
- Prissettingsmetoden er **Flat** og kan ikke endres.
- Underordnede varer kan legges til eller fjernes.
- Overordnede og underordnede varer må bruke samme varegruppe. 
- Underordnede varer kan ha ett av følgende oppsett:

    - Feltene **Faktureringsfrekvens** og **Faktureringsintervaller** settes til samme verdi som den overordnede varen. 
    - Feltet **Faktureringshyppighet** er satt til **Én gang**. I dette tilfellet er feltet **Fakturaintervaller** automatisk satt til **1**. 

- Summen av nettobeløpene for de underordnede varene er lik det overordnede beløpet. Hvis tildelingsmetoden er **Nullbeløp**, er både summen av de underordnede varebeløpene og det overordnede beløpet 0 (null). 

    > [!NOTE]
    > Hvis tildelingsmetoden er **Null overordnet beløp**, vil (ikke-null)-summen til de underordnede varene være lik det overordnede beløpet, som er 0 (null). Denne tildelingsmetoden brukes til interne formål, slik at ansatte kan se de underordnede varene. Kundene kan imidlertid bare se den overordnede varen.

- Hvis MEA-typen (multiple element arrangement) for salgsordren er **Enkel**, opprettes den tilsvarende transaksjonslinjen for inntektstildeling for flere varer når de overordnede og underordnede varene legges til. 
- Hvis tildelingsmetoden for en omsetningsdeling er **Like beløp**, og det overordnede beløpet endres, beregnes beløpene på nytt for alle underordnede linjer. 
- For en omsetningsdeling der fordelingsmetoden er **Variabelt beløp**, skjer følgende virkemåte:

    - Nettobeløpet til den overordnede varen vises i **Overordnet beløp**-kolonnen. Denne verdien kan redigeres. Enhetsprisen, nettobeløpet og rabatten er imidlerdig 0 (null) og kan ikke redigeres.
    - Enhetsprisen for underordnede varer er 0 (null). Du kan redigere enhetsprisen eller nettobeløpet. Når du redigerer én verdi, oppdateres den andre verdien automatisk.

- For en omsetningsdeling der fordelingsmetoden er **Prosent**, skjer følgende virkemåte:

    - Nettobeløpet til den overordnede varen vises i **Overordnet beløp**-kolonnen. Denne verdien kan redigeres. Enhetsprisen, nettobeløpet og rabatten er imidlerdig 0 (null) og kan ikke redigeres. 
    - Nettobeløpet for underordnede varer beregnes *Prosent* &times; *Overordnet beløp*.

- For en omsetningsdeling der fordelingsmetoden er **Likt beløp**, skjer følgende virkemåte:

    - Nettobeløpet til den overordnede varen vises i **Overordnet beløp**-kolonnen. Denne verdien kan redigeres. Enhetsprisen, nettobeløpet og rabatten er imidlerdig 0 (null) og kan ikke redigeres. 
    - Nettobeløpet for underordnede varer beregnes ved å dele det overordnede beløpet likt på alle de underordnede varene. 
    - Hvis underordnede varer fjernes eller legges til, beregnes nettobeløpet og enhetsprisene på nytt, slik at alle underordnede linjer har lik beløp. 
    - Hvis det overordnede beløpet ikke kan deles likt, kan nettobeløpet og enhetsprisen for den siste underordnede varen være litt mer eller mindre enn nettobeløpet og enhetsprisen for de andre underordnede varene. 

- For en omsetningsdeling der fordelingsmetoden er **Nullbeløp**, skjer følgende virkemåte:

    - Enhetsprisen, nettobeløpet og rabatten kan redigeres. Det overordnede beløpet er 0 (null) og kan ikke redigeres. 
    - Antallet, enheten, området og lagerverdiene for underordnede varer er basert på den overordnede varen. Du kan ikke endre disse verdiene for de underordnede varene. Alle endringer må foretas i den overordnede varen. 
    - Enhetsprisen og nettoprisen for underordnede varer er 0 (null) og kan ikke redigeres. 

- For en omsetningsdeling der fordelingsmetoden er **Null overordnet beløp**, skjer følgende virkemåte:

    - Enhetsprisen, overordnet beløp og nettobeløp for den overordnede varen er 0 (null).
    - I en faktureringsplan vises de underordnede linjene som om de ble lagt til manuelt, og alle verdiene oppdateres basert på den valgte faktureringsplangruppen. Disse verdiene kan ikke redigeres. For underordnede varer kan du få tilgang til alternativene **Eskalering og rabatt** og **Avansert prissetting** ved hjelp av feltene **Angitt antall**, **Enhetspris**, **Rabatt** og **Nettobeløp** i **Vis faktureringsdetaljer**. 
    - I en salgsordre har de underordnede linjene en rabatt og rabattprosent på 0 (null). 
    - Faktureringsfrekvensen for det overordnede og det underordnede objektet kan endres, og hver linje kan ha ulike frekvenser. Den overordnede varen oppdateres imidlertid automatisk slik at den bruker den kortest frekvensen blant de underordnede linjene. En inntektsdeling har for eksempel to underordnede varer, der én bruker **Månedlig** faktureringsfrekvens, og den andre bruker faktureringsfrekvensen **Årlig**. I dette tilfellet oppdateres faktureringsfrekvensen for den overordnede varen til **Månedlig**.
