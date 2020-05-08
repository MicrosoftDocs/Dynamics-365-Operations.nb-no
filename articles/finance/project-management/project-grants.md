---
title: Prosjekttilskudd
description: Dette emnet forklarer hvordan du endrer et tilskudd.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282842"
---
# <a name="project-grants"></a>Prosjekttilskudd

[!include [banner](../includes/banner.md)]

Et tilskudd er en pengegave for et bestemt formål eller prosjekt. Vanligvis er det begrensninger på hvordan et tilskudd kan brukes. I Prosjektstyring og regnskap kan du angi og spore tilskudd og definere relasjonene deres til prosjekter og prosjektkontrakter. Du kan for eksempel utføre følgende oppgaver:

- Knytt tilskudd til prosjekter og finansieringskilder ved hjelp av sidene **Prosjekt** og **Detaljer for prosjektkontrakt**.
- Angi og spor endringer av et tilskudd mens det går fra én status til en annen.
- Angi og spor kostnader, forespurte beløp og tildelte beløp.
- Opprett hovedtilskudd, og knytt undertilskudd til dem.

Du kan opprette et tilskudd ved å angi alle detaljene i en ny post, eller du kan kopiere detaljene fra et eksisterende tilskudd og deretter oppdatere dem.

## <a name="create-a-new-grant"></a>Opprett et nytt tilskudd

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg **Ny** \> **Tilskudd**.
3. Angi en alfanumerisk ID for tilskuddet i **Tilskudds-ID**-feltet på hurtigfanen **Generelt** på siden for tilskuddsdetaljer.
4. I feltet **Tilskuddsnavn** angir du et navn for tilskuddet.
5. I **Beskrivelse**-feltet legger du til detaljer om det nye tilskuddet.

    De fleste av de andre feltene på siden er valgfrie, og du kan angi så lite eller mye informasjon du vil.

    Følgende liste beskriver informasjonen som er angitt i hver hurtigfane på tilskuddsdetaljer-siden:

    - **Generelt** – Angi navn, status, beskrivelse, formål og beløp for tilskuddet.
    - **Kontaktinformasjon** – Angi detaljer om stabsmedlemmer, avdelingen som administrerer tilskuddet, og om tilskuddskunden eller organisasjonenskilden til tilskuddet. Du kan også angi om organisasjonen din er en videreføringsenhet som mottar tilskuddet og deretter sender det videre til en annen mottaker. Velg **Legg til** for å legge til kontaktinformasjon, for eksempel telefonnumre og e-postadresser for organisasjonen som gir tilskuddet.
    - **Datoer og tidsfrister** – Angi datoer som er relatert til tilskuddet og tilskuddssøknaden. Eksempler inkluderer søknadens forfallsdato, innsendingsdato og dato for når tilskuddet er godkjent eller avvist.
    - **Tilknyttede prosjekter og prosjektkontrakter** – Du kan bare angi informasjon på denne hurtigfanen hvis **Tilskuddsstatus**-feltet på hurtigfanen **Generelt** er satt til **Aktiv** eller **Tildelt**. Velg blant følgende alternativer for å fullføre den tilknyttede oppgaven:

        - **Legg til finansieringskilde** – Legg til en ny finansieringskilde for tilskuddet. Du kan angi alle detaljene nå eller bruke standardinformasjon og oppdatere den senere.
        - **Legg til prosjektkontrakt** – Legg til eller oppdater informasjon om prosjektkontrakt.
        - **Legg til prosjekt** – Legg til eller oppdater prosjektdetaljer.

    - **Oppsett** – Angi detaljer om samsvarende midler hvis denne informasjonen er nødvendig. Mange organisasjoner som tildeler tilskudd, krever at mottakerer bruker et visst beløp av sine egne penger eller ressurser til å matche det som tildeles i tilskuddet. I feltet **Lokalt prosjekt eller sporings-ID** kan du angi en ID som er forskjellig fra prosjekt-IDen.

        > [!NOTE]
        > Sett alternativet **Undertilskuddsgiver** til **Ja** hvis en del av tilskuddet skal tildeles til en annen organisasjon. Når det gjelder tilskudd som tildeles i USA, kan du angi om et tilskudd skal tildeles under et delstatsmandat eller føderalt mandat.

    - **Nedtrekkingsdetaljer** – Legg til eller oppdater informasjon om hvor ofte tilskuddsmidler kan tas ut, faktureres for eller brukes.

## <a name="create-a-new-grant-from-a-copy"></a>Opprette et nytt tilskudd fra en kopi

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg **Ny** \> **Kopier fra tilskudd**.
3. Skriv inn en alfanumerisk identifikator og et navn for det nye tilskuddet, og klikk deretter **OK**.
4. På tilskuddsdetaljer-siden kan du se detaljene for det kopierte tilskuddet, og foreta eventuelle endringer som kreves. De fleste feltene på siden er valgfrie.

## <a name="view-or-modify-grant-details"></a>Vise eller endre tilskuddsdetaljer

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg tilskuddet du vil endre.
3. I handlingsruten, i kategorien **Tilskudd**, i **Oppretthold**-gruppen, velger du **Rediger**.
4. Se gjennom tilskuddsdetaljene, og foreta eventuelle endringer som kreves.
