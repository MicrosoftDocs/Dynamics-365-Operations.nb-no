---
title: Faktureringsparametere for regelmessig kontrakt
description: Denne artikkelen beskriver hvordan du definerer standardverdiene for fakturaplaner som er opprettet i Regelmessig kontraktfakturering. Den forklarer også hvordan du oppretter faktureringsplangrupper.
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
ms.openlocfilehash: cb60253f3cbb8c991ef2e106abdb1c685bf22171
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903341"
---
# <a name="recurring-contract-billing-parameters"></a>Faktureringsparametere for regelmessig kontrakt

Bruk siden **Parametere for regelmessig kontraktfakturering** til å definere standardverdiene for fakturaplaner som opprettes i Regelmessig kontraktfakturering. Alle faktureringsplaner du oppretter, vil i utgangspunktet bruke disse standardverdiene. Du kan imidlertid endre verdiene for hver faktureringsplan etter behov.

## <a name="general-tab"></a>Fanen Generelt

1. Velg en faktureringsplangruppe i feltet **Faktureringsplangruppe** på siden **Parametere for regelmessig kontraktfakturering** på fanen **Generelt**. Hvis du vil ha mer informasjon om hvordan du definerer faktureringsplangrupper, kan du se delen [Faktureringsplangrupper](#set-up-billing-schedule-groups) senere i denne artikkelen.
2. I feltet **Oppsigelsestype** velger du hvordan sluttfakturaen skal beregnes når en faktureringsplan avsluttes:

    - **Juster plan** – Avslutt fakturaplanen på avslutningsdatoen, endre statusen for planen til **Siste fakturering** og juster den tilknyttede utsettelsesplanen ved å tilbakeføre beløpet som ikke lenger må gjenkjennes. Hvis startdatoen for fakturering er etter avslutningsdatoen, fjernes de gjenværende faktureringsperiodene.
    - **Fakturer gjenstående** – Legg til et eventuelt restbeløp i faktureringsplanen i avslutningsperioden, og endre statusen for planen til **Siste fakturering**, og oppdater utsettelsesplan. Hvis startdatoen for fakturering er etter avslutningsdatoen, blir totalbeløpet for alle gjenværende faktureringsperioder lagt til i faktureringsperioden, og de gjenværende faktureringsperiodene blir fjernet.
    - **Ingen justering** – Avslutt faktureringsplanen for linjen på avslutningsdatoen. Det gjøres ingen justeringer i faktureringsplanen.

3. I feltet **Unik planleggingstype** velger du **Ingen** for å angi at kunder er begrenset til én enkelt faktureringsplan. Velg **Per kunde** eller **Per sluttbruker** for å angi at kunder er begrenset til en unik plan.
4. Angi **Tilpass til måned** til **Ja** hvis du vil tilpasse detaljlinjene for faktureringsplan til slutten av en måned når en faktureringsplan opprettes eller oppdateres. Sett den til **Nei** hvis du vil bruke trinnvise datoer.
5. Angi alternativet **Fordeling av delvise perioder** til **Ja** for å tildele fakturabeløp basert på antall dager i perioden. Sett det til **Nei** hvis du vil ha et likt beløp i hver faktureringsperiode, uavhengig av antall dager.
6. Hvis du setter alternativet **Fordeling av delvise perioder** til **Ja**, angir du **Fordelingsmetode**-feltettil **Daglig** for å distribuere beløpene basert på antall dager i perioden. Sett den til **Månedlig** for å ha et likt beløp hver måned.
7. Angi om nyopprettede faktureringsplaner skal være satt på vent som standard.

    > [!NOTE]
    > Hvis du vil fjerne betalingen for en faktureringsplan, må brukeren være en del av en brukergruppe. Velg **Fjern overstyring av sperre for brukergruppe** for å definere en brukergruppe der alternativet **Tillat fjerning av sperre** er aktivert.

8. Velg standard fakturatransaksjonstype for nye fakturaplaner i feltet **Fakturatransaksjonstype**.
9. Angi alternativet **Juster utsettelse til fakturering** til **Ja** for å samkjøre den tilsvarende utsatte planen, slik at den bruker de samme datoene som faktureringsplanen. Sett den til **Nei** for å bruke ulike datoer.
10. Hvis du bruker funksjonen for omsetningsdeling, setter du alternativet **Opprett inntektsdeling automatisk** til **Ja** når varer legges til i en faktureringsplan. Avmerkingsboksen **Inntektsdeling** blir automatisk merket av på faktureringsplanlinjen hvis varen er definert som en inntektsdelingsvare. Sett alternativet til **Nei** hvis du vil merke av for **Inntektsdeling** manuelt.
11. Angi feltene for oppretting av salgsordrer:

    - Fakturaer kan konsolideres etter periode, kunde eller vare. En hvilken som helst kombinasjon av **Ja**- og **Nei**-verdier kan angis. Fakturaer kan også deles etter varegruppe.
    - Følgende posteringsalternativer er tilgjengelige for fakturaer:

        - **Opprett salgsordre** – Opprett bare salgsordren.
        - **Vis posteringsfaktura** – Fakturer salgsordren, og åpne en side der du kan postere fakturaen manuelt.
        - **Opprett fritekstfaktura** – Velg dette alternativet hvis du bruker fritekstfakturaer.
        - **Poster faktura automatisk** – Fakturer salgsordren og poster den automatisk.

    - Angi alternativet **Legg til faktureringsdatoer i varebeskrivelsen** til **Ja** for å legge til en beskrivelse som inkluderer startdatoen og sluttdatoen for fakturering.
    - Angi alternativet **Utelukk nullforbruk** til **Ja** for å utelate faktureringsplanlinjer som ikke har forbruk. Sett den til **Nei** hvis du vil inkludere disse linjene i salgsordren.
    - Angi **Ikke skriv ut underordnede varer** til **Ja** hvis du ikke vil skrive ut de underordnede varene for en inntekt som er delt på salgsordren. Bare den overordnede varen vises på fakturaen. Hvis nettobeløpet til de (skjulte) underordnede varene er en sum som ikke er null, viser nettobeløpet til den overordnede linjen et sammendrag av de underordnede linjene. Velg **Nei** hvis du vil skrive ut alle underordnede varer under den overordnede varen på salgsfakturaen.

12. Angi feltene for støtte og fornyelse:

    - Sett alternativet **Aktiver støtte og fornying automatisk** til **Ja** for å bruke støtte- og fornyingsfunksjonen automatisk på en salgsordre.
    - Velg standard støtte- og fornyelsesnivå i feltet **Støtte- og fornyingsnivå**.
    - Angi støtte- og fornyingsantall i feltet **Støtte- og fornyingsantall**.
    - I feltet **Standard startdato for støtte og fornying** angir du datoen som skal brukes som standard startdato for støtte og fornying:

        - **Transaksjonsdato** – Bruk transaksjonsdatoen som startdato:
        - **Starten av gjeldende måned** – Bruk den første i gjeldende måned som startdato.
        - **Starten av neste måned** – Bruk den første i neste måned som startdato. Hvis transaksjonsdatoen er den første, brukes den første for nåværende måned.
        - **Regel på 15** – Bruk den første i gjeldende måned som startdato hvis transaksjonsdatoen er mellom den første og den femtende i måneden. Hvis transaksjonsdatoen er den sekstende eller senere, brukes den første i neste måned som startdato.

    - Angi alternativet **Inkluder rabatt i beregning** til **Ja** for å inkludere rabattbeløpet i støtte- eller fornyingsbeløpet. Sett det til **Nei** for å utelate rabattbeløpet.
    - I feltene **Støttehyppighet** og **Fornyingshyppighet** velger du hyppigheten som skal brukes når støtte- og fornyingsvarer legges til i en faktureringsplan: **Daglig**, **Månedlig**, **Kvartalsvis**, **Halvårlig** eller **Årlig**.
    - Sett alternativet **Juster etter varegruppe** til **Ja** for å samkjøre start- og sluttdatoene for nye varer til eksisterende varer, basert på varegruppen.
    - Sett alternativet **Juster til neste ufakturerte periode** til **Ja** for å angi justeringsdatoen for en fornyingsvare basert på datoen for den neste perioden som ikke er falt etter at fornying har startet.
    - Sett alternativet **Kopier serienummer** til **Ja** for å kopiere vareserienummeret fra den innledende salgsordrelinjen til den tilsvarende faktureringsplanlinjen.

13. Hvis du bruker eskalering på faktureringsplanen, velger du metoden som skal brukes for beregningen av konsumprisindeksen.
14. Angi alternativet **Spor prisendring** til **Ja** hvis du vil ha en post med prisendringer på faktureringsplanlinjer. Hvis en faktureringsplanlinje endres manuelt fra standard til flat, og en ny pris som angis, spores revisjonsinformasjonen på faktureringsplanlinjen. Angi alternativet til **Nei** hvis du ikke vil spore disse endringene.
15. Angi om poster skal filtreres etter startdato eller sluttdato som standard på siden **Generer faktura**.
16. Hvis du bruker funksjonen **Ufakturert inntekt**, angir du alternativene som brukes:

    - Sett alternativet **Poster økonomijournal automatisk** til **Ja** hvis du vil at økonomijournalen skal opprettes og posteres samtidig. Angi det til **Nei** hvis du vil opprette økonomijournalen og deretter postere den manuelt.
    - Velg standard journalnavn som skal brukes når økonomijournalen opprettes, i feltet **Standard journalnavn**.
    - I feltet **Kortsiktig ufakturert metode** velger du den kortsiktige ufakturerte metoden hvis du bruker en. Hvis du velger **Ingen**, vil ikke den kortsiktige funksjonaliteten brukes med inntekter som ikke er fakturert. Velg **Rullende perioder** hvis du alltid vil bruke 12 måneder eller **fast år** for å bruke det gjenstående regnskapsåret.

17. Angi alternativene som skal brukes når en faktureringsplan og linjene i den avsluttes:

    - **Utsted kreditt** – Opprett en kreditnota når en faktureringsplan eller faktureringsplanlinje avsluttes.
    - **Kredittjustering** – Opprett en kredittjustering for en faktureringsplan når en linje avsluttes. Kredittjusteringen vises i en fremtidig faktureringsperiode for faktureringsplanen. Kreditjusteringen oppdaterer fakturabeløpet for den neste faktureringsperioden til kreditten er ferdig brukt på faktureringsplanen.
    - **Ingen kreditt** – Ikke opprett en kreditnota når en faktureringsplan eller faktureringsplanlinje avsluttes. Dette alternativet er bare tilgjengelig når alternativet **Ingen justering** brukes til å avslutte en faktureringsplan.

## <a name="sequence-number-tab"></a>Fanen Serienummer

Bruk fanen **Serienummer** på siden **Parametere for regelmessig kontraktfakturering** til å angi standardverdien for faktureringsplannumre. Standardverdiene defineres på siden **Nummerserie** (**Organisasjonsadministrasjon \> Nummerserier \> Nummerserier**).

## <a name="set-up-billing-schedule-groups"></a>Definer faktureringsplangrupper

Bruk siden **Faktureringsplangruppe** til å opprette en faktureringsplangruppe for Regelmessig kontraktfakturering. Når en ny faktureringsplan blir opprettet og det brukes en faktureringsplangruppe på den, blir verdiene som er definert på siden **Faktureringsplangruppe**, angitt som standardverdier for faktureringsplanen. Du kan endre en hvilken som helst av standardverdiene for den bestemte faktureringsplanen du oppretter. Du kan definere flere faktureringsplangrupper og deretter tildele en av dem som standard fakturaplangruppe på siden **Parametere for regelmessig kontraktfakturering**.

Følg denne fremgangsmåten for å opprette en faktureringsplangruppe for regelmessig kontraktfakturering.

1. På siden **Faktureringsplangruppe** velger du **Ny** for å opprette en faktureringsplangruppe.
2. I **Faktureringsplangruppe**-feltet angir du en unik identifikator.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Angi hvor ofte faktureringsplanen skal faktureres en kunde i feltet **Faktureringshyppighet**: **Én gang**, **Daglig**, **Månedlig**, **Kvartalsvis**, **Halvårig** eller **Årlig**.
5. Angi et faktureringsintervall i feltet **Faktureringsintervall**. Du kan for eksempel sette feltet **Faktureringshyppighet** til **Månedlig** og feltet **Faktureringsintervall** til **2** for fakturering annenhver måned.
6. Velg prissettingsmetoden for varer på faktureringsplanen i feltet **Prissettingsmetode**:

    - **Standard** – Beregn enhetsprisen basert på det totale antallet som er angitt, og bruk standardprissetting fra **Frigitte produkter**-siden i Produktinformasjonsbehandling.
    - **Flat** – Bruk en flat pris som er angitt på faktureringsplanlinjen.
    - **Lag** – Beregn enhetsprisen ved hjelp av et fast antall til ulike prisbraketter. Hvert lag må fylles ut før du kan gå til den neste prisbrakett.
    - **Flatt lag** – Beregn enhetsprisen ved hjelp av et fast antall og utvidede prisbeløp til ulike prisbraketter. Prisen som belastes i en faktureringsperiode, bruker den utvidede prisen som tilsvarer nivået der faktureringsantallet eksisterer.

7. Velg varetypen for faktureringsgruppen i **Varetype**-feltet:

    - **Standard** – Velg denne verdien hvis antallet er statisk.
    - **Bruk** – Velg denne verdien for varer av typen forbruksmålt eller forbruk. Hvis du velger denne verdien, setter du feltet **Bruksavlesingsalternativ** til **Avlesing** for å angi verdien (avlesing) for en faktureringsperiode på en måler eller enhet. Den brukte verdien beregnes basert på den forrige faktureringsperioden og den nåværende avlesningen du angir.
    - **Milepæl** – Velg denne verdien for å bruke funksjonen Milepælfakturering. Hvis du velger denne verdien, velger du milepælmalen hvis du bruker en, i **Milepælmal**-feltet.
    - **Forbruk** – Velg denne verdien hvis du vil angi verdien som forbrukes i en faktureringsperiode.

8. Sett alternativet **Faktura separat** til **Ja** for å opprette en kombinasjon av samlefakturaer og separate fakturaer for den samme kunden. En kunde har for eksempel fem faktureringsplaner. Tre av dem blir konsolidert på én enkelt faktura, men hver av de to andre krever en egen faktura. Sett alternativet til **Nei** hvis du bare vil opprette én samlefaktura for kunden.
9. Angi **Forny automatisk**-alternativet til **Ja** for å fornye regelmessig faktureringsplan automatisk for neste faktureringsperiode når fakturaen opprettes. Angi det til **Nei** for å fornye faktureringsplanen manuelt. Angi hvor mange linjer som skal legges til for hver fornying, i feltet **Linjer som skal legges til per fornying**.
10. Angi alternativet **Eskalering** til **Ja** for å bruke *eskaleringer* (prisøkninger) på faktureringsplanene som er knyttet til denne faktureringsplangruppen.
