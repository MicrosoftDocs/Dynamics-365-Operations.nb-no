---
title: Brukerkontoer for mobilenhet
description: Dette emnet beskriver hvordan du definerer og administrerer brukerkontoer som gjør det mulig for ansatte å logge seg på og bruke lagerappen.
author: MarkusFogelberg
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 9ff6752f303adab6c4c52f2f09eea1c0ae2e8e0a
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647844"
---
# <a name="mobile-device-user-accounts"></a>Brukerkontoer for mobilenhet

[!include [banner](../includes/banner.md)]

Hver gang en arbeider begynner å bruke lagerappen, må de logge seg på ved hjelp av et brukernavn og passord. Et hvilket som helst antall lagerappbrukere kan knyttes til hver arbeider i systemet, og lagre er vanligvis knyttet til hver av lagerappbrukerne. Ulike alternativer konfigureres også for hver arbeider for å opprette standardinnstillinger og andre innstillinger som er relevante for bruk av lagerappen.

## <a name="set-up-the-required-worker-and-employee-records"></a>Definere de nødvendige ansatt- og ansattpostene

Før du kan opprette lagerappbrukere, må hver arbeider allerede eksistere som en ansatt eller arbeider i Supply Chain Management i **Personale**-modulen.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Konfigurere brukerkontoer for mobilenhet

Når de påkrevde arbeiderne og de ansatte er definert i Personale, kan du tilordne lagerappbrukere til hver av dem og definere andre alternativer som påvirker hvordan de kan bruke appen.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. Hvis du vil redigere en eksisterende arbeider, velger du vedkommende i listeruten. For å legge til en ny oppføring velger du **Ny** i handlingsruten.
1. Følg denne fremgangsmåten hvis du skal opprette en ny arbeider:

    1. I **Arbeider**-feltet velger du målbrukeren i listen over ansatte.
    1. Velg **Velg**.
    1. Velg **Lagre** i handlingsruten.

1. En standardprofil kan brukes til å veilede lagerarbeideren ved pakkestasjonen gjennom prosessen som kreves der. Standardprofilen kan eventuelt brukes til å lagre innstillingene for den foretrukne profilen for arbeideren. Angi følgende felt i hurtigfanen **Profil**.

    - **Policy for containerpakking** – Velg en policy for containerpakke som definerer hvordan containere ved pakkestasjonen skal behandles. Policyen for containerpakke som velges her, forhåndsdefineres for arbeideren når de åpner pakkestasjonen. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Forbedret pakkefunksjonalitet](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkeprofil-ID** – Velg en pakkeprofil-ID som definerer emballasjepolicyen og containerinnstillingene som brukes. Hvis den valgte pakkeprofil-IDen er knyttet til en policy for containerpakke, kan du ikke endre innstillingen for **Policy for containerpakking** på denne siden.

1. Angi følgende felt i fanen **Standard pakkestasjon** for å definere standard pakkestasjon som gjelder når arbeideren logger på. Arbeideren kan fremdeles velge en annen pakkestasjon etter behov.

    - **Sted** – Velg stedet der standard pakkestasjon finnes.
    - **Lager** – Velg lageret der standard pakkestasjon finnes.
    - **Lokasjon** – Velg lokasjonen for standard pakkestasjon.

1. Med hurtigfanen **Brukere** kan du opprette et hvilket som helst antall lagerappbrukerkontoer for den valgte arbeideren. Hver konto er knyttet til et bestemt lager eller lagre. Bruk verktøylinjen til å legge til eller fjerne brukerkontoer, tilbakestille passordet for en valgt konto eller tilordne lagre til en valgt konto. For hver brukerkonto kan du angi du følgende felt:

    - **Bruker-ID** – Angi en unik ID.
    - **Brukernavn** – Angi et navn på ID-en.
    - **Standardlager** – Angi standardlageret der arbeideren vanligvis jobber. Du kan bruke verktøylinjen til å tilordne flere lagre, og arbeideren kan bytte mellom lagre ved å bruke den indirekte aktiviteten **Endre lager** for menyelementet for mobilenheten.
    - **Menynavn** – Velg rotmenyen som blir startsiden for arbeideren. Muligheten til å sette opp en rotmeny for hver arbeider er nyttig fordi det lar deg styre menystrukturen som hver arbeider kan bruke. For eksempel kan menyen for arbeidere som er aktive bare i det utgående området, tilpasses for oppgaver som er knyttet til utgående operasjoner for dette området.
    - **Inaktiv** – En merket avmerkingsboks angir at brukerkontoen er inaktiv. Brukerkontoen deaktiveres automatisk hvis en arbeider angir feil passord fem ganger på rad i lagerappen. Du kan imidlertid også merke av i boksen manuelt. Fjern merket for å gjøre brukeren aktiv igjen.

1. Angi følgende felter i hurtigfanen **Arbeid**:

    - **Tillat overstyring av plukkplassering** – Sett dette alternativet til *Ja* for å tillate at arbeideren kan overstyre lokasjonen for plukktrinn. Denne funksjonen kan være nyttig hvis den fysiske beholdningen ikke samsvarer med den systemforeslåtte lokasjonen.
    - **Tillat overstyring av plukkplassering** – Sett dette alternativet til *Ja* for å tillate at arbeideren kan overstyre lokasjonen for plasseringstrinn. Denne funksjonen kan være nyttig hvis den foreslåtte plasseringslokasjonen for øyeblikket er full eller ikke tilgjengelig, eller hvis oppsamlingslokasjoner endres.
    - **Tillat salgsoverplukking** – Sett dette alternativet til *Ja* for å tillate at arbeideren overplukker når salgsordrer plukkes. Hvis du vil ha mer informasjon, kan du se [Overplukking for salgs- og overføringsordrer](over-picking-for-sales-and-transfer-orders.md).
    - **Tillat overføringsordreoverplukking** – Sett dette alternativet til *Ja* for å tillate at arbeideren overplukker når overføringsordrer plukkes. Hvis du vil ha mer informasjon, kan du se [Overplukking for salgs- og overføringsordrer](over-picking-for-sales-and-transfer-orders.md).
    - **Tillat bevegelse av beholdning med tilhørende arbeid** – Sett dette alternativet til *Ja* for å tillate at arbeideren kan flytte lager som allerede er reservert eller allerede er knyttet til annet arbeid. Hvis du vil ha mer informasjon, kan du se [Flytting av beholdning med tilknyttet arbeid i Warehouse management](move-inventory-associated-work.md).
    - **Tillat manuell ny tildeling av vare** – Sett dette alternativet til *Ja* for å aktivere manuell omplassering for arbeideren under kort plukking. Med Ny fordeling av vare får arbeidere veiledning i å plukke lager fra en annen lokasjon. Selv om automatisk omfordeling er tilgjengelig for alle arbeidere, krever manuell omplassering eksplisitt oppsett for en arbeider. Muligheten til å kontrollere manuell ny tildeling for hver arbeider kan være nyttig fordi det gir deg muligheten til å kontrollere synligheten som hver arbeider har, for eksempel når varplukking fra karantene- eller partiområdet er begrenset til klarerte arbeidere. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Automatisk og manuell omplassering av varer under kort plukking](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Er en syklustellingsansvarlig** – Angi dette alternativet til *Ja* for å gjøre arbeideren til en syklustellingsleder. I dette tilfellet vil alle syklustellinger som arbeideren utfører i lagerappen, bli godkjent umiddelbart. **Grense for største prosent**, **Grense for største antall** og **Grense for største verdi**-felt vurderes ikke for arbeidere som dette alternativet er satt til *Ja* for.
    - **Grense for største prosent:** – Angi den høyeste prosentgrensen som en syklustelling kan variere fra det forventede antallet, uten å kreve godkjenning av en syklustellingsansvarlig.
    - **Grense for største antall** – Angi det totale antallet som det angitte antallet kan være forskjellig fra det forventede antallet (i enheter) uten at det kreves godkjenning av en arbeidsleder for syklustelling.
    - **Grense for største verdi** – Angi det maksimale beløpet beholdningens kostnad kan avvike fra den forventede kostnaden, uten å kreve godkjenning av en syklustellingsansvarlig.

1. Velg **Lagre** i handlingsruten.
1. Hvis du la til en ny brukerkonto, vil dialogboksen **Angi passord** vises, der du kan opprette et enkelt passord som brukeren kan bruke til å logge på mobilappen. Angi det enkle passordet to ganger, og velg deretter **Lagre passord** for å fortsette.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Angi språket, nummerformater og tidssone for hver lagerappbruker

Når en arbeider logger seg på mobilappen Warehouse Management, endres språket, nummerformatet og tidssonen, slik at den samsvarer med arbeiderens innstillinger. Kontoinnstillingene for arbeideren som ble valgt i trinn 3 i delen [Konfigurere brukerkontoer for mobilenhet](#set-wma-users), bestemmer hvilke innstillinger som skal brukes. Hvis du trenger separate innstillinger for hver bruker, kan du bruke forskjellige arbeiderkontoer. Følgende fremgangsmåte viser hvordan du endrer språk, nummerformater og tidssone for hver lagerappbruker.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. Finn navnet på arbeideren du vil definere. Kontroller at arbeideren har alle de nødvendige lagerappbrukerkontoene som er oppført i hurtigfanen **Brukere**. Opprett en ny arbeider og/eller legg til lagerappbrukerkontoer etter behov, ved å følge trinnene i delen [Konfigurere brukerkontoer for mobilenhet](#set-wma-users).
1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
1. Velg brukerkontoen der **Person**-kolonnen viser navnet på arbeideren som du fant i trinn 2.

    > [!IMPORTANT]
    > **Bruker-ID**-verdiene som vises på **Brukere**-siden, er *ikke* knyttet til verdien som vises på hurtigfanen **Brukere** på siden **Arbeider** som du åpnet i trinn 1.

1. Velg **Brukeralternativer** i handlingsruten.
1. Angi følgende felt i fanen **Innstillinger**:

    - **Språk** – Velg språket som arbeideren foretrekker. Dette feltet styrer også datoformatet som vises i lagerappen.
    - **Dato, klokkeslett og nummerformat** – Velg språket som bestemmer nummerformatene som vises i lagerappen. Legg merke til at dato- og klokkeslettformatene som vises i lagerappen, faktisk bestemmes av **Språk**-feltet, ikke av dette feltet.
    - **Tidssone** – Velg tidssonen der arbeideren arbeider. Dette feltet påvirker tidsangivelsen for alle registreringer som arbeideren gjør ved hjelp av appen.

> [!NOTE]
> I noen tilfeller kan ikke lagerappen finne bestemte arbeidsinnstillinger som fastsetter språket, nummerformatene og tidssonen. Følgende regler gjelder:
>
> - Hvis appen ikke er koblet til et Supply Chain Management-miljø (for eksempel første gang appen startes etter at den er installert), brukes språket for den lokale enheten. Når enhetsspråket endres, endres også språket i appen. Hvis du vil ha mer informasjon om hvordan du konfigurerer språket for den lokale enheten, kan du se dokumentasjonen for enheten og/eller operativsystemet.
> - Hvis appen er koblet til et Supply Chain Management-miljø, men ingen innstillinger er angitt for den signerte arbeideren, velges språket, nummerformatene og tidssonen basert på kontoen som er knyttet til klient-IDen som enheten bruker til å koble til Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Opprette og konfigurere en brukerkonto i Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Hvis du legger merke til at feil tidsangivelser vises for registreringer som gjøres ved hjelp av lagerappen, må du kanskje justere tidssonen som er angitt for brukerkontoen som arbeidere bruker til å logge seg på og/eller godkjenne med Supply Chain Management. Som tidligere ble nevnt, kan tidssoneinnstillingen komme fra brukerkontoen som brukes til å logge seg på lagerappen, slik den er angitt på **Arbeider**-siden. Hvis brukerkontoen ikke er definert på **Arbeider**-siden, kommer tidssonen fra brukerkontoen som er knyttet til klient-IDen som brukes til godkjenning, slik den er angitt på **[Azure Active Directory-programmer](install-configure-warehouse-management-app.md)**-siden.
