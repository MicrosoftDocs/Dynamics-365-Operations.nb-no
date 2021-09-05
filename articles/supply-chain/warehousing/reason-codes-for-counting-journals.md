---
title: Årsakskoder for lagertelling
description: Dette emnet beskriver hvordan du konfigurerer og bruker årsakskoder for tellingsoppgaver.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 95f7ceb39d2afef1871f395ed562632865022b39
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345272"
---
# <a name="reason-codes-for-inventory-counting"></a>Årsakskoder for lagertelling

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Med årsakskoder kan du analysere resultatene av tellingen og eventuelle avvik som oppstår under denne prosessen. Du kan angi årsaken for å gjøre tellingen, for eksempel en skadet pall eller en lagerjustering som er basert på lagereksempler. Samtidig kan du bruke justeringsfunksjonaliteten til å postere verdien av lagerbeholdningsjusteringer til den aktuelle motkontoen, basert på årsaken til hver lagerjustering.

## <a name="recommendation"></a>Anbefaling

Før du definerer systemet, anbefaler vi at du definerer en strategi for å arbeide med årsakskoder. Du kan for eksempel prøve å svare på følgende spørsmål:

- Skal årsakskoder være obligatoriske på lagre?
- Skal årsakskoder være obligatoriske eller valgfrie for noen varer?
- Hvor mange årsakskoder trenger du?
- Må du forhåndsvelge en begrenset liste over årsakskoder for justeringer?
- Hvordan skal brukerne av strekkodeskannere bruke årsakskoder? Skal årsakskodene være forhåndsvalgt, være obligatoriske eller ikke redigerbare?
- Trenger lagermedarbeidere annen årsakskodevirkemåte på mobile skannere? Hvis svaret er Ja, kan du opprette flere menyelementer og tilordne dem til forskjellige personer.
- Bør årsakskodene drive økonomisk motkontopostering?

## <a name="turn-on-reason-code-features-in-your-system"></a>Aktiver årsakskodefunksjoner i systemet

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Hvis du ikke ser alle funksjonene som er beskrevet i dette emnet i systemet, må du sannsynligvis aktivere funksjonen *Justeringer av poster i lagerbeholdning ved hjelp av konfigurerbare årsakskoder som er koblet til motkonto*. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Poster lagerbeholdninger ved hjelp av konfigurerbare årsakskoder som er koblet til motkontoer*

## <a name="set-up-reason-codes"></a>Definer årsakskoder

### <a name="set-up-reason-code-policies"></a>Definere policyer for årsakskoder

Du kan opprette flere policyer for årsakskoder for å bestemme når og hvordan opptellingsårsakskoder brukes. Hver årsakskodepolicy kan ha én av to kodetyper for opptellingsårsak (*Valgfritt* eller *Obligatorisk*). Policyene for årsakskoder for telling kan brukes på lagernivå eller varenivå.

Hvis du vil opprette en policy for årsakskode, følger du fremgangsmåten nedenfor.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Policyene for årsakskoder for telling**.
1. I handlingsruten velger du **Ny** for å legge til en policy i rutenettet.
1. Angi **Navn**-feltet for den nye policyen.
1. I feltet **Årsakskodetype for telling** velger du *Obligatorisk* eller *Valgfritt* for å angi om valg av en årsakskode skal være en valgfri eller obligatorisk handling i én av følgende lagerjusteringsprosesser:

    - Syklustelling (mobilenhet)
    - Spottelling (mobilenhet)
    - Terskeltelling (mobilenhet)
    - Justering inn (mobil enhet)
    - Justering ut (mobil enhet)
    - Opptellingsjournal (rik klient)
    - Antallsjustering/Online-opptelling (rik klient)

Du kan også definere årsakskodepolicyer for individuelle lagre og for produkter. Årsakskodeoppsettet for et produkt kan overstyre oppsettet for produktets lager.

> [!NOTE]
> For lagre og varer der feltet **Policy for årsakskoder for telling** er angitt til *Obligatorisk*, kan ikke opptellingsjournalen fullføres og lukkes før en årsakskode er angitt. Hvis du vil ha mer informasjon, kan du se neste del.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Tilordne årsakskodepolicyer for telling til lagre

Følg denne fremgangsmåten for å tilordne en årsakskodepolicy for telling til et lager.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lageroppdeling** \> **Lagre**.
1. Velg et lager i listeruten.
1. I handlingsruten i fanen **Lager** i gruppen **Konfigurer** velger du **Policy for årsakskoder for telling**. Følg deretter et av disse trinnene i rullegardinlisten **Tilordne policy for årsakskoder for telling**:

    - Hvis du vil bruke policyoppsettet for hver vare til å bestemme om opptellingsjournaler er obligatoriske for den, angir du ingen verdi (eller sletter den eksisterende verdien).
    - Hvis du vil kreve en årsakskode på opptellingsjournaler for lageret, velger du en årsakspolicy der feltet **Årsakskodetype for telling** er satt til *Obligatorisk*.
    - Hvis en årsakskode er valgfri på opptellingsjournaler for lageret, velger du en årsakspolicy der feltet **Årsakskodetype for telling** er satt til *Valgfritt*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Tilordne årsakskodepolicyer for telling til produkter

Følg denne fremgangsmåten for å tilordne en årsakskodepolicy for telling til et produkt.

1. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
1. Velg et produkt i rutenettet.
1. I handlingsruten i fanen **Produkt** i gruppen **Konfigurer** velger du **Policy for årsakskoder for telling**. Følg deretter et av disse trinnene i rullegardinlisten **Tilordne policy for årsakskoder for telling**:

    - Hvis du vil bruke policyoppsettet for lageret til å bestemme om opptellingsjournaler er obligatoriske for produktet, angir du ingen verdi (eller sletter den eksisterende verdien).
    - Hvis du vil kreve en årsakskode på opptellingsjournaler for produktet, velger du en årsakspolicy der feltet **Årsakskodetype for telling** er satt til *Obligatorisk*. Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.
    - Hvis en årsakskode er valgfri på opptellingsjournaler for produktet, velger du en årsakspolicy der feltet **Årsakskodetype for telling** er satt til *Valgfritt*. Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.

### <a name="set-up-counting-reason-codes"></a>Definere årsakskoder for telling

Gjør følgende for å konfigurere årsakskoder for telling.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Årsakskoder for telling**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. Angi feltene **Årsakskode for telling** og **Beskrivelse** for den nye raden.
1. Hvis du vil tilordne en motkonto, angir eller velger du en verdi i **Motkonto**-feltet.

    > [!NOTE]
    > Hvis en motkonto er tilordnet en årsakskode for telling, og hvis du posterer en opptellingsjournal bruker denne årsakskoden for telling, blir verdien postert mot den tilordnede motkontoen i stedet for standard lagerposteringsprofilkonto.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Definer årsakskodegrupper for telling

*Årsakskodegrupper for telling* kan brukes som en del av menyelementene *Justering inn* og *Justering ut* i Warehouse Management-mobilappen til å begrense listen over opptellingsårsakskoder. (Hvis du vil ha mer informasjon om årsakskodegrupper for telling, kan du se [Definer menyelementer for mobilenheter for justering inn og justering ut](#setup-adjustment-in-out) senere i dette emnet.)

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Årsakskodegrupper for telling**.
1. I handlingsruten velger du **Ny** for legge til en gruppe.
1. Angi feltene **Årsaksgruppe for telling** og **Gruppebeskrivelse** for den nye gruppen.
1. Velg **Lagre** i handlingsruten.
1. I delen **Detaljer** velger du **Ny** på verktøylinjen for å legge til en rad i rutenettet. Angi feltet **Årsakskode for telling** for den nye raden. 
1. Gjenta det forrige trinnet for å tilordne flere koder etter behov. Hvis du må fjerne en kode fra gruppen, velger du den og velger deretter **Slett** på verktøylinjen.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Konfigurer årsakskoder for menyelementer i mobilenheter

Du kan konfigurere årsakskoder for følgende justeringstyper for lagerbeholdning:

- Syklustelling
- Spottelling
- Terskeltelling
- Justering inn
- Justering ut

I de fleste tilfeller kan du definere følgende informasjon for hvert relevant menyelement for mobilenhet:

- Om årsakskoden vises for mobilenhetsmedarbeideren under opptelling.
- Standard årsakskode som vises på et menyelement for mobilenhet.
- Om brukeren kan redigere årsakskoden.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Konfigurer menyelementer i mobilenheter for en tellingsprosess

Følg disse trinnene for å definere et menyelement for en mobilenhet for en tellingsprosess.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.
1. Velg det relevante menyelementet i listeruten, eller opprett et nytt menyelement.
1. Klikk på **Syklustelling** i handlingsruten.
1. I feltet **Standard årsakskode for telling** angir du standard årsakskode som skal registreres når menyelementet på mobilenheten brukes til telling.
1. I feltet **Vis årsakskode for telling** velger du en av følgende verdier:

    - *Linje* – Vis årsakskoden etter at hvert avvik er registrert.
    - *Skjul* – Ikke vis årsakskoden.

1. Angi **Rediger årsakskode for telling** til *Ja* for å tillate at medarbeideren kan redigere årsakskoden når den vises på mobilenheten under opptelling. Sett den til *Nei* for å hindre at arbeideren kan redigere koden.

> [!NOTE]
> **Syklustelling**-knappen kan aktiveres på et menyelement for mobilenhet der telling kan utføres. Eksempler omfatter menyelementene for spottelling, brukerstyrt arbeid og systemstyrt arbeid.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Definer menyelementer for mobilenheter for justering inn og justering ut

Følg disse trinnene for å definere et menyelement for en mobilenhet for justering inn eller justering ut.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.
1. I handlingsruten velger du **Ny** for å opprette et menyelement.
1. Angi feltene for **navnet på mobilelementet** og **tittel** for det nye menyelementet.
1. Sett **Modus**-feltet til *Arbeid*.
1. Sett alternativet **Bruk eksisterende arbeid** til *Ja*.
1. Velg **Justering inn** eller *Justering ut* i feltet *Arbeidsopprettelsesprosess*.
1. Angi følgende felt i hurtigfanen **Generelt**. (Alle disse feltene blir lagt til når du velger *Justeringer inn* eller *Justering ut* i feltet **Arbeidsopprettelsesprosess**.)

    - **Bruk prosesshåndbok** – Hvis du oppretter en *Justering ut*-prosess, må du passe på at du setter dette alternativet til *Ja*. Hvis du oppretter en *Justering ut*-prosess, er dette alternativet alltid satt til *Ja*.
    - **Standard årsakskode for telling** – Angi standard årsakskode som skal registreres når menyelementet på mobilenheten brukes til telling.
    - **Vis årsakskode for telling** – Velg en av følgende verdier:

        - *Linje* – Vis årsakskoden etter at hvert avvik er registrert.
        - *Skjul* – Ikke vis årsakskoden.

    - **Rediger årsakskode for telling** – Angi dette alternativet til *Ja* for å tillate at medarbeideren kan redigere årsakskoden når den vises på mobilenheten under opptelling. Sett den til *Nei* for å hindre at arbeideren kan redigere koden.
    - **Årsakskodegruppe for telling** – Velg en årsakskodegruppe hvis du vil begrense listen over alternativer som presenteres for arbeidere. Hvis du vil ha mer informasjon om hvordan du definerer årsakskodegrupper, kan du se delen [Definer årsakskodegrupper for telling](#reason-groups) tidligere i dette emnet. 

> [!NOTE]
> Når du tilordner en årsakskodegruppe for telling til menyelementene *Justering inn* og *Justering ut* der alternativet **Bruk prosesshåndbok** er angitt til *Ja*, kan du få en begrenset liste over opptellingsårsakskodene som en del av behandling i Warehouse Management-mobilappen.
>
> Alternativet **Bruk prosesshåndbok** kan også forhindre at store justeringsantall oppstår ved en feil. (En arbeider kan for eksempel skanne en strekkode med et varenummer ved et uhell i stedet for en mengdeverdi.) Hvis du vil sette opp denne funksjonaliteten, setter du alternativet **Bruk prosesshåndbok** til *Ja* for hvert relevante menyelement. Deretter går du til **Lagerstyring \> Oppsett \> Arbeider**, og angir **Grense for justeringsantall**-feltet for hver relevante lagerarbeider for å angi det maksimale justeringsantallet som arbeideren kan registrere.

## <a name="processing-that-uses-counting-reason-codes"></a>Behandling som bruker opptellingsårsakskoder

Når ansatte bruker Warehouse Management-mobilappen, registreres årsakskodene. Med mindre en opptellingsgodkjenningsprosess er definert, brukes de registrerte årsakskodene umiddelbart som en del av opptellingsjournalposteringen som følger.

### <a name="cycle-count-approvals"></a>Godkjenninger av syklustelling

Før en telling er godkjent, kan arbeideren endre årsakskoden som er knyttet til opptellingen. Når tellingen er godkjent, oppføres årsakskoden på opptellingsjournallinjene.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Endre årsakskoder for godkjenninger av syklustelling

Følg disse trinnene for å endre en syklustellingsgodkjenning.

1. Gå til **Lagerstyring** \> **Syklustelling** \> **Syklustellingsarbeid venter på gjennomgang**.
1. Velg en syklustelling i rutenettet.
1. Velg **Syklustelling** i **Arbeid**-fanen i handlingsruten. Velg en ny årsakskode i feltet **Årsakskode**.

Årsakskoder legges til i journallinjene i opptellingsjournaler av typen *Opptellingsjournal*.

1. Gå til **Lagerstyring** \> **Loggoppføringer** \> **Vareopptelling** \> **Opptelling**.
2. I opptellingsjournalens linjedetaljer velger du årsakskoden som samsvarer med den gjeldende situasjonen, i feltet **Åårsakskode for telling**.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Vis årsakskodene som er registrert, i opptellingshistorikken

Følg denne fremgangsmåten for å vise årsakskodene som er registrert, i opptellingshistorikken.

1. Gå til **Lagerstyring** \> **Forespørsler og rapporter** \> **Opptellingshistorikk**.
1. Velg en vareopptellingspost i listeruten.
1. Vis opptellingshistorikken som er registrert, ved hjelp av en årsakskode, i feltet **Årsakskode for telling**.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Bruk årsakskoder for antallsjustering eller online-opptelling

Følg denne fremgangsmåten for å bruke en årsakskode for en antallsjustering eller online-opptelling.

1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.
1. Velg **Antallsjustering** i handlingsruten.
1. Velg **Antallsjustering**, og deretter i **Årsakskode for telling**, velger en årsakskode.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
