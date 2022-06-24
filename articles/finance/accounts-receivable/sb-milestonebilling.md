---
title: Milepælmaler
description: Denne artikkelen forklarer hvordan du setter opp funksjonaliteten for milepælfakturering i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856777"
---
# <a name="milestone-billing"></a>Milepælfakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du definerer maler for funksjonaliteten for milepælfakturering i Abonnementsfakturering. For hver linje i milepælmalen kan du definere tildelingsprosenten eller beløpet. Du kan deretter tilordne milepælmalen til faktureringsplanelementer som bruker funksjonaliteten for milepælfakturering.

## <a name="add-a-template"></a>Legg til en mal

Hvis du vil legge til en milepælmal, gjør du følgende.

1. Gå til **Abonnementsfakturering \> Gjentakende kontraktfakturering \> Oppsett \> Milepælmaler**.
2. Velg **Ny**.
3. I feltet **Milepælmal** angir du en unik ID for den nye malen.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg en tildelingsmetode i feltet **Tildelingsmetode**.
6. Valgfritt: I **Totalbeløp**-feltet angir du totalbeløpet for malen.
7. Velg **Legg til** for å legge til en linje. I **Varenummer**-feltet velger du deretter varenummeret for den nye linjen.
8. Følg ett av disse trinnene, avhengig av verdien du valgte i feltet **Tildelingsmetode**-feltet:

    - Hvis du valgte **Prosent** som tildelingsmetode, angir du tildelingsprosenten for hver linje i **Prosent**-feltet. Hvis du angir prosenter, må summen av prosenter som vises feltet **Total prosent**, være lik **100**.
    - Hvis du valgte **Variabelt beløp** som tildelingsmetode, angir du beløpet for hver linje i **Beløp**-feltet.
    - Hvis du valgte **Likt beløp** som tildelingsmetode, trenger du ikke å angi et beløp. Hver linje blir oppdatert med riktig prosent og beløp, basert på antall varer som blir lagt til malen.

9. Velg **Lagre**.

## <a name="delete-a-template"></a>Slett en mal

Hvis du vil slette en milepælmal, gjør du følgende.

1. Velg til én eller flere linjer som skal slettes, og velg deretter **Slett**.
2. Når du blir bedt om å bekrefte handlingen, velger du **Ja**.

## <a name="milestone-template-fields"></a>Felter i milepælmaler

Siden **Milepælmal** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------| 
| Milepælmal | Den unike ID-en for milepælmalen. |
| Beskrivelse | Beskrivelsen av milepælmalen. |
| Tildelingsmetode | <p>Velg tildelingsmetoden:</p><ul><li>**Fullføringsprosent** – En akkumulert fullføringsverdi brukes for hver linje.</li><li>**Prosent** – Det kan angis et prosentbeløp for tildelingen. Summen av alle prosenter må være lik 100.</li><li>**Variabelt beløp** – Det kan angis et beløp for tildelingen. Tildelingsbeløpet angis på transaksjonsnivå.</li><li>**Likt beløp** – Tildelingsprosentene beregnes automatisk og fordeles likt mellom varene i malen.</li></ul> |
| Totalt fravær | Angi milepælbeløpet for malen. |
| **Linjer** | |
| Varenummer | Velg varenummeret for milepælmalen. |
| Produktnavn | Navnet på varen. |
| Prosent | <p>Angi tildelingsprosenten for linjen:</p><ul><li>Hvis feltet **Tildelingsmetode** er satt til **Prosent**, angir du prosenten for linjen.</li><li>Hvis feltet **Tildelingsmetode** er satt til **Likt beløp**, deles prosenten automatisk opp i like prosentverdier, basert på antallet varer i malen.</li></ul><p>Summen av alle prosentene må være lik 100.</p><p>Hvis en verdi for **Totalbeløp** er angitt i hodet og du endrer **Prosent**-verdien for linjen, blir **Beløp**-verdien oppdatert. Og hvis du endrer **Beløp**-verdien, blir **Prosent**-verdien oppdatert.</p> |
| Beløp | <p>Tildelingsbeløpet for linjen:</p><ul><li>Hvis feltet **Tildelingsmetode** er satt til **Variabelt beløp**, angir du beløpet for linjen.</li><li>Hvis feltet **Tildelingsmetode** er angitt til **Likt beløp**, deles beløpet automatisk inn i like beløp, basert på antallet varer i malen og verdien for **Totalbeløp** som er spesifisert i hodet.</li></ul><p>Summen av alle beløpene må være lik verdien for **Totalbeløp** som er angitt i hodet.</p><p>Hvis en verdi for **Totalbeløp** er angitt i hodet og du endrer **Beløp**-verdien for linjen, blir **Prosent**-verdien oppdatert. Og hvis du endrer **Prosent**-verdien, blir **Beløp**-verdien oppdatert.</p> |
| **Totaler** | |
| Total prosentandel | Summen av prosenter. Summen av alle prosenter må være lik 100. |
| Totalt fravær | Summen av **Beløp**-verdier for alle linjer. Denne summen må være lik verdien for **Totalbeløp** som er angitt i hodet. |
| Restbeløp | Gjenstående beløp. Verdien blir beregnet som verdien for **Totalbeløp** fra hodet minus summen av **Beløp**-verdier for alle linjer.|

## <a name="milestone-allocation"></a>Milepæltildeling

Før du begynner å bruke milepælfunksjonalitet, må du fullføre disse oppgavene.

1. Legg til en eller flere milepælmaler.
2. Opprett en faktureringsplangruppe. Angi **Milepæl** som varetypen, og velg en mal.
3. På siden **Vareoppsett** (**Abonnementsfakturering \> Gjentakende kontraktfakturering \> Oppsett \> Varer**) velger du en varerelasjon og en milepælmal for vareoppsettet.

Når du har opprettet milepælmalene, faktureringsplangruppene og varene, kan du opprette en faktureringsplan som bruker milepælfunksjonaliteten.

Følg denne fremgangsmåten for å definere en faktureringsplan som bruker milepæler.

1. Fra listen **Alle/Aktive faktureringsplaner** på siden **Faktureringsplaner** velger du **Ny**.
2. Opprett en ny faktureringsplan på siden **Alle faktureringsplaner**, og angi en kundekonto og en startdato.
3. I delen **Faktureringsplanlinjer** velger du **Legg til linje**. Deretter legger du til et varenummer, og setter **Varetype**-feltet til **Milepæl**.

    Hvis en standard milepælmal er definert for varen, legges milepælhendelsene automatisk til i faktureringsplanlinjene. Sluttdatoer er tomme for milepællinjer.

    Hvis ingen milepælmal er definert for varen, velger du **Milepæltildeling**. Deretter velger du en milepælmal på siden **Milepæltildeling** og foretar eventuelle nødvendige oppdateringer. Velg deretter **Lukk** for å gå tilbake til faktureringsplanen, og fullfør opprettelsen av faktureringsplanen.

4. Hvis du vil opprette fakturaer for faktureringsplanen, må du oppdatere sluttdatoen for hver milepælhendelse. For en enkelt faktureringsplan kan du oppdatere sluttdatoen for milepælhendelsen i faktureringsplanlinjene. Hvis du vil oppdatere flere faktureringsplaner, velger du **Prosess for å oppdatere fullføringsdato**.
5. Når sluttdatoen er oppdatert, kan du opprette fakturaen. For en enkelt faktureringsplan velger du **Generer faktura** på siden **Alle faktureringsplaner**. Hvis du vil opprette fakturaer for flere faktureringsplaner, velger du **Generer faktura** eller **Generer satsvis fakturabehandling** under **Periodiske oppgaver**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Rediger milepæltildeling på en faktureringsplanlinje

Hvis du vil redigere milepæltildeling på en faktureringsplanlinje, følger du trinnene nedenfor.

1. På siden **Faktureringsplaner** > **Alle eller aktive faktureringsplaner**, i feltet **Plannummer**, velger du plannummeret til faktureringsplanen.
2. I delen **Faktureringsplanlinjer** angir du en vare, angir **Milepæl** som varen og velger **Milepæltildeling**.
3. Velg en milepælmal i **Milepælmal**-feltet.
4. Velg **Prosess**. Milepælmallinjene legges automatisk til i faktureringsplanlinjene.

## <a name="milestone-allocation-fields"></a>Felter for milepæltildeling

Siden **Milepæltildeling** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Overordnet vare | Varenummeret til den overordnede. |
| Utvidet pris | <p>Den utvidede prisen på varen. Verdien tilsvarer verdien for **Nettobeløp** for faktureringsplanlinjen.</p></p>For en overordnet milepælvare er standardverdien **Totalbeløp**-verdien som er angitt for milepælmalen. Hvis totalbeløpet er 0 (null), er standardverdien **Nettobeløp**-verdien for faktureringsplanlinjen.</p> |
| Milepælmal | Milepælmal-ID-en for linjevaren. |
| Malbeskrivelse | Beskrivelsen av milepælmalen. |
| Tildelingsmetode | Tildelingsmetoden som brukes for milepælmalen. |
| **Linjer** | Standardverdiene for alle linjer er basert på den valgte milepælmalen. Du kan endre dem etter behov. |
| Varenummer | Varenummeret for milepæltildelingsmalen. |
| Produktnavn | Produktnavnet. |
| Prosent | <p>Tildelingsprosenten for linjen. Summen av alle prosentene må være lik 100.</p><p>Hvis du endrer **Prosent**-verdien for linjen, blir **Nettobeløp**-verdien oppdatert. Og hvis du endrer **Nettobeløp**-verdien, blir **Prosent**-verdien oppdatert.</p> |
| Nettobeløp | <p>Tildelingsbeløpet for linjen. Summen av nettobeløp for alle linjer må være lik verdien for **Utvidet pris** som er angitt i hodet.</p><p>Hvis du endrer **Nettobeløp**-verdien for linjen, blir **Prosent**-verdien oppdatert. Og hvis du endrer **Prosent**-verdien, blir **Nettobeløp**-verdien oppdatert.</p> |
| **Totaler** | |
| Total prosent | Summen av **Prosent**-verdier for alle linjer. Denne summen må være lik 100. |
| Totalt fravær | Summen av **Nettobeløp**-verdier for alle linjer. Denne summen må være lik verdien for **Utvidet pris** som er angitt i hodet. |
| Restbeløp | Gjenstående beløp. Verdien blir beregnet som verdien for **Utvidet pris** fra hodet minus summen av **Nettobeløp**-verdier for alle linjer. Sluttbeløpet må være 0 (null). |
