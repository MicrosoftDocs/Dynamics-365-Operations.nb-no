---
title: Inntektsdelingsmaler i Abonnementsfakturering
description: Dette emnet beskriver hvordan du konfigurerer maler for inntektsdeling for varer som selges som bunter.
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
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660458"
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
