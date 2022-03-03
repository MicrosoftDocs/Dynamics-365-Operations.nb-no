---
title: Lagerverdirapporter
description: Dette emnet forklarer hvordan du konfigurerer, genererer og bruker lagerverdirapporter. Disse rapportene inneholder informasjon om fysisk og finansielle antall og beløp for beholdningen.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3da92c384d3074335067433120eccc97d11b6b81
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103946"
---
# <a name="inventory-value-reports"></a>Lagerverdirapporter

[!include [banner](../includes/banner.md)]

Lagerverdirapporter inneholder informasjon om fysisk og finansielle antall og beløp for beholdningen. Du kan vise rapportene på mange forskjellige måter. Du kan for eksempel vise totaler eller transaksjoner, eller filtrere etter varer eller et tidsintervall. Du kan vise verdier for solgte varers kost (vareforbruk) eller verdier for varer i arbeid (VIA) og angi andre alternativer.

Ved hjelp av lagerverdirapporter kan du utføre følgende oppgaver:

- Utføre avstemming mellom økonomimodul og beholdning.
- Konsultere lagerbeholdning og verdier for en bestemt periode.
- Opprette rapportkonfigurasjoner som er tilpasset til et bestemt formål.
- Lagre rapportkonfigurasjoner slik at de kan brukes flere ganger.
- Legge til områder for å filtrere data når du kjører en rapport.

## <a name="types-of-inventory-value-report"></a>Typer lagerverdirapport

Det finnes to typer lagerverdirapport: **Lagerverdi** (standardrapporten) og **Lagring av lagerverdirapport**.

### <a name="standard-inventory-value-report"></a>Standard lagerverdirapport

Standard **lagerverdirapport** er en enkel rapport som lar deg velge informasjonen som er inkludert, og deretter viser denne informasjonen på skjermen. Resultatene lagres ikke. Den inneholder heller ikke interaktive funksjoner for filtrering, drilling, blaing eller eksport. Av disse årsakene anbefaler vi at du bruker rapporten for **oppbevaring av lagerverdi** i stedet i de fleste tilfeller.

### <a name="inventory-value-report-storage-report"></a>Rapport for oppbevaring av lagerverdi

Rapporten for **oppbevaring av lagerverdi** gjør utdataene tilgjengelig digitalt, enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksportert dokument i et av flere formater.

Når du viser rapporten i nettleseren, justeres kolonner og aggregatsaldoer dynamisk, avhengig av det konfigurerte oppsettet. Du kan sortere resultatene, filtrere dem, drille ned til dataene og mye mer.

Rapportresultater lagres i **Lagerverdi**-dataenheten. Derfor kan du filtrere og eksportere resultatene til et format som for eksempel kommadelte verdier (CSV) eller Microsoft Excel-format.

Rapporten for **oppbevaring av lagerverdi** er nyttig når utdataene inneholder mange linjer. Du har for eksempel 50 000 varer, og 300 butikker er opprettet som lagre. Hvis du i så fall ber om sluttsaldoer for beholdning etter vare, område og lager, vil utdataene inneholde mange linjer.

> [!NOTE]
> Rapporten for **oppbevaring av lagerverdi** inkluderer ikke delsummer som er definert i rapportoppsettet. Den inkluderer heller ikke saldoer i økonomimodulen, selv om disse saldoene er definert i rapportoppsettet. Avstemming til økonomimodulen må gjøres ved hjelp av råbalanser. Standard **Lagerverdi**-rapport inneholder imidlertid disse delsummene og saldoene.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Lagring av lagerverdirapport

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Lagring av lagerverdirapport* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Definer konfigurasjoner for lagerverdirapporten

Bruk siden **Lagerverdirapporter** til å definere innholdet som inngår i de ulike typene lagerverdirapport. Du kan definere et hvilket som helst antall rapporttyper. Hver gang du genererer en type lagerverdirapport, velger du en rapporttype.

1. Gå til **Kostnadsstyring \> Oppsett for regnskapspolicyer for beholdning \> Lagerverdirapporter**.
1. Følg ett av disse trinnene:

    - Hvis du vil redigere en eksisterende rapport, velger du den i listeruten, og deretter velger du **Rediger** i handlingsruten.
    - Hvis du vil opprette en ny rapport, velger du **Ny** i handlingsruten .

1. I toppteksten i den nye eller valgte rapporten angir du følgende felter:

    - **ID** – Angi en kort ID for rapporten. Denne verdien må være unik blant alle konfigurasjoner for lagerverdirapporter. Den kan ikke redigeres etter at du har lagret en ny konfigurasjon.
    - **Navn** – Angi et beskrivende navn for rapporten.

1. Hvis du oppretter en ny rapportkonfigurasjon, velger du **Lagre** i handlingsruten for å gjøre resten av feltene tilgjengelige.
1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Datointervall** – Velg et forhåndsdefinert datointervall. Du kan overstyre dette datointervallet når du kjører rapporten.
    - **Område** – Velg enten *Posteringsdato* eller *Transaksjonstidspunkt*, avhengig av datoen og klokkeslettet som skal brukes når poster hentes for rapporten.
    - **Dimensjonssett** – Velg settet med dimensjoner som dataene skal kjøres for. (Dimensjonene er definert i økonomimodulen.) Du kan for eksempel kjøre dataene for *hovedkonto* eller *hovedkonto + forretningsenhet*. Dimensjonssettet du velger, kan ikke ha flere enn to dimensjoner. Hvis du vil ha mer informasjon, kan du se [Finansdimensjonssett](../../finance/general-ledger/financial-dimension-sets.md).

1. Angi følgende felter på hurtigfanen **Kolonner**. Disse feltene styrer kolonnene som rapporten inkluderer, og typene data som disse kolonnene inneholder.

    - **Beholdning** – Sett dette alternativet til *Ja* for å vise lagerverdiene. Du kan deretter avstemme disse verdiene med kontosaldoene i økonomimodulen.
    - **VIA** – Sett dette alternativet til *Ja* for å vise VIA-verdiene. Du kan deretter avstemme disse verdiene med VIA-kontosaldoene i økonomimodulen. Når du velger *Ja*, viser rapporten bare de fysiske antallene og beløpene for beholdningen som har VIA-status. Produksjonsordrer som har VIA-status, er plukket eller ferdigmeldt, men de har ikke blitt avsluttet.
    - **Utsatt vareforbruk** – Angi dette alternativet til *Ja* hvis du vil vise en kolonne som viser de fysiske antallene og lagerbeløpene for utsatt vareforbruk. Utsatt vareforbruk vises ved hjelp av fysiske antall og beløp, fordi det motposterer følgeseddelantall og -beløp.
    - **Vareforbruk** – Angi dette alternativet til *Ja* hvis du vil vise en kolonne som viser de øonomiske antallene og beløpene for vareforbruket. Vareforbruk vises ved hjelp av økonomiske antall og beløp, fordi det motposterer fakturaantall og -beløp.
    - **Resultat** – Sett dette alternativet til *Ja* hvis du vil vise en kolonne som viser det økonomiske beløpet som ble postert til resultatkontoene for beholdningen.
    - **Skriv ut kumulative kontoverdier for sammenligning** – Sett dette alternativet til *Ja* for å vise en kolonne som viser finanskontosaldoen. På denne måten trenger du ikke kontrollere råbalansen. Dette alternativet fungerer bare med standard **Lagerverdi**-rapport, ikke med rapporten for **oppbevaring av lagerverdi**. Når du har angitt dette alternativet til *Ja*, må du bruke følgende felter til å angi hver konto i økonomimodulen du vil vise, avhengig av alternativene for **Finansell stilling** du har aktivert.

        > [!NOTE]
        > Hvis du velger en *totalkonto* for noen av disse feltene, vises både beløpet i hver beholdningskonto som er inkludert i totalkontoen, og beløpet i totalkontoen.

        - **Beholdningskonto** – Angi kontoen i økonomimodulen du vil vise beholdningsinformasjon for. (Både **Beholdning** og **Skriv ut kumulative kontoverdier for sammenligning** må være angitt til *Ja*.)
        - **VIA-konto** – Angi kontoen i økonomimodulen du vil vise VIA-informasjon for. (Både **VIA** og **Skriv ut kumulative kontoverdier for sammenligning** må være angitt til *Ja*.)
        - **Konto for utsatt vareforbruk** – Angi kontoen i økonomimodulen du vil vise informasjon om utsatt vareforbruk for. (Både **Utsatt vareforbruk** og **Skriv ut kumulative kontoverdier for sammenligning** må være angitt til *Ja*.)
        - **Konto for vareforbruk** – Angi kontoen i økonomimodulen du vil vise informasjon om vareforbruk for. (Både **Vareforbruk** og **Skriv ut kumulative kontoverdier for sammenligning** må være angitt til *Ja*.)

    - **Oppsummer fysiske og økonomiske verdier** – Sett dette alternativet til *Ja* for å vise en kolonne som viser totalt beholdningsantall og beholdningsbeløp (et sammendrag av både fysiske og økonomiske beholdningsverdier). Hvis dette alternativet er satt til *Nei*, viser rapporten både fysiske og økonomiske beholdningsverdier.
    - **Inkluder ikke postert til økonomimodul** – Sett dette alternativet til *Ja* hvis du vil vise en kolonne som viser transaksjonene som aldri ble postert til økonomimodulen. Det kan hende at transaksjoner for følgende varetyper ikke posteres i økonomimodulen:

        - Mottatte og ennå ikke fakturerte varer når alternativet **Poster aktuell beholdning** er fjernet for den relevante varemodellgruppen.
        - Mottatte og ennå ikke fakturerte varer når alternativet **Poster produktkvittering i finans** er fjernet på hurtigfanen **Produktkvittering** på **Generelt**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**).

    - **Beregn gjennomsnittlig enhetskostnad** – Sett dette alternativet til *Ja* for å vise en kolonne som viser gjennomsnittlig enhetskostnad. Den gjennomsnittlige enhetskostnaden er det totale antallet delt på totalbeløpet.
    - **Totalt antall og verdi** – Sett dette alternativet til *Ja* for å vise kolonner som viser totalt antall fysisk beholdning (og økonomisk antall) og totalbeløp for fysisk beholdning (og finansbeløp). Du kan bare sette dette alternativet til *Ja* hvis **Oppsummer fysiske og økonomiske verdier** er satt til *Nei*.
    - **Lagerdimensjoner** – I dette rutenettet merker du av for **Vis** for hver dimensjon du vil vise i rapporten. Bare dimensjoner der alternativet **Økonomisk lager** er aktivert, vil vise verdier i rapporten. Andre dimensjoner viser bare tomme kolonner. For de dimensjonene du velger å vise, kan du merke av for **Totalt** for å inkludere totaler.
    - **Ressurs-ID** – Sett **Vis**-alternativet til *Ja* for å vise en kolonne som identifiserer varen for hver rad. Sett **Totalt**-alternativet til *Ja* for også å inkludere totaler. Kolonnen viser en av følgende typer informasjon, avhengig av varetypen som vises i hver rad:

        - **Materiale** – Kolonnen viser `ItemID`-feltverdien for den relevante materialposten.
        - **Arbeid** – Kolonnen viser `WorkCenterID`-feltverdien for den relevante arbeidsposten.
        - **Indirekte kostnad** – Kolonnen viser `CodeID`-feltverdien for den relevante kostnadsposten.

        Hvis **Vis**-alternativet er satt til *Nei* både for feltet **Ressurs-ID** og **Ressursgruppe**, vises bare en total lagerverdi som er basert på lagerdimensjonene du har valgt.

    - **Ressursgruppe** – Sett **Vis**-alternativet til *Ja* for å vise en kolonne som identifiserer ressursgruppen for hver rad. Sett **Totalt**-alternativet til *Ja* for også å inkludere totaler. Kolonnen viser en av følgende typer informasjon, avhengig av varetypen som vises i hver rad:

        - **Materiale** – Kolonnen viser `ItemGroup`-feltverdien for den relevante materialposten.
        - **Arbeid** – Kolonnen viser `WorkcenterGroup`-feltverdien for den relevante arbeidsposten.
        - **Indirekte kostnad** – Kolonnen viser `CostGroup`-feltverdien for den relevante kostnadsposten. (Verdien for `CostGroupType` må være *Indirekte*.)

        Hvis **Vis**-alternativet er satt til *Nei* både for feltet **Ressurs-ID** og **Ressursgruppe**, vises bare en total lagerverdi som er basert på lagerdimensjonene du har valgt.

1. Angi følgende felter i hurtigfanen **Rader**. Ved bruk av disse feltene kan du legge til tilsvarende VIA-relaterte underseksjoner i rapporten eller fjerne dem.

    - **Materiale** – Sett dette alternativet til *Ja* for å vise informasjon om materialer. *Materiale* er en standard ressurstype, fordi materialer må inkluderes i alle rapportkonfigurasjoner for å opprette pålitelige utdata.
    - **Arbeid** – Sett dette alternativet til *Ja* for å vise arbeidskostnader for VIA.
    - **Indirekte kostnad** – Sett dette alternativet til *Ja* for å vise indirekte kostnader for VIA.
    - **Direkte utsetting** – Sett dette alternativet til *Ja* for å kostnader for direkte utsetting for VIA. Denne informasjonen er nyttig for utsetting.
    - **Detaljnivå** – Velg et visningsalternativ for rapporten:

        - *Transaksjoner* – Vis alle relevante transaksjoner i rapporten. Vær oppmerksom på at du kan oppleve ytelsesproblemer når du viser rapporter som inneholder et stort transaksjonsvolum. Hvis du vil bruke dette visningsalternativet, anbefaler vi derfor at du bruker rapporten for **oppbevaring av lagerverdi**.
        - *Totaler* – Vis det totale resultatet.

    - **Inkluder startsaldo** – Sett dette alternativet til *Ja* for å vise startsaldoen. Dette alternativet bare tilgjengelig når feltet **Detaljnivå** er satt til *Transaksjoner*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Generer en rapport for oppbevaring av lagerverdi

Følg denne fremgangsmåten for å generere og lagre en rapport for **oppbevaring av lagerverdi**:

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Rapport for oppbevaring av lagerverdi**.
1. Velg **Ny** i handlingsruten.
1. I dialogboksen **Lagerverdi** angir du følgende felter på hurtigfanen **Parametere**:

    - **Navn** – Angi et unikt navn for rapporten.
    - **ID** – Velg [konfigurasjonen for lagerverdirapporten](#report-configuration) som skal brukes for rapporten. Konfigurasjonen fastsetter alternativer for kolonnene og radene som skal tas med i rapporten.
    - **Datointervall** – Bruk feltene i denne delen til å definere hvilke poster som skal tas med i rapporten. Hvis du vil definere datointervallet, kan du enten velge et forhåndsdefinert område (i forhold til rapportgenereringsdatoen) i feltet **Datointervallkode**, eller velge bestemte datoer i feltene **Fra-dato** og **Til-dato**.

1. I hurtigfanen **Poster som skal inkluderes** definerer du filtre og betingelser for å definere hvilke data som skal tas med i rapporten. Velg **Filter** for å åpne en standard dialogboks for Power Query-redigering der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Supply Chain Management. Alle disse filtrene brukes på lagertransaksjonene, men ikke på økonomimodulsaldoen. Tenk på denne virkemåten når du definerer filtrene. Ellers vil du kanskje se et avvik mellom lageret og økonomimodulen.
1. Angi hvordan, når og hvor ofte rapporten skal genereres, i hurtigfanen **Kjør i bakgrunnen**. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.

    > [!NOTE]
    > Denne rapporten blir alltid kjørt som en del av en satsvis jobb.

1. Velg **OK** for å bruke innstillingene og lukke dialogboksen.

Når den satsvise jobben er fullført, vises rapporten på siden **Rapport for oppbevaring av lagerverdi**. Du må kanskje oppdatere siden for å kunne se rapporten.

> [!IMPORTANT]
> I den valgte konfigurasjonen for lagerverdirapporten kan det hende du får en feil startsaldo hvis du velger samme dato både i **Fra dato**-feltet og **Til dato**-feltet, og også hvis du angir alternativet **Inkluder startsaldo** til *Ja*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Utforsk en rapport for oppbevaring av lagerverdi

Når du har generert en rapport, kan du vise og utforske den når som helst på følgende måte:

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Rapport for oppbevaring av lagerverdi**.
1. Velg en rapport i listen. Siden viser detaljene i [konfigurasjonen for lagerverdirapporten](#report-configuration) som ble brukt til å generere den valgte rapporten.
1. I handlingsruten velger du **Vis detaljer** for å vise rapportinnholdet.
1. Utforsk rapporten ved å følge et av disse trinnene:

    - Du kan velge nesten hvilken som helst kolonneoverskrift for å sortere eller filtrere rutenettet etter verdier i denne kolonnen, på samme måte som med de fleste standardsidene i Supply Chain Management.
    - Bruk **Filter**-feltet til å filtrere rapporten ved hjelp av en hvilken som helst verdi i en av flere tilgjengelige kolonner.
    - Bruk Vis-menyen (over **Filter**-feltet) til å lagre og laste inn dine favorittkombinasjoner av sorterings- og filteralternativer.

## <a name="export-an-inventory-value-report-storage-report"></a>Eksporter en rapport for oppbevaring av lagerverdi

Hver rapport du genererer, lagres i dataenheten **Lagerverdi**. Du kan bruke standardfunksjonene i Supply Chain Management til å eksportere data fra denne enheten til alle støttede dataformater, inkludert CSV eller Excel-format.

Følgende eksempel viser hvordan du eksporterer en rapport for **oppbevaring av lagerverdi**.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Dataadministrasjon**.
1. I delen **Import/eksport** velger du **Eksport**-flisen.
1. På **Eksport**-siden som vises, vil du konfigurere eksportjobben. Skriv først inn et gruppenavn for jobben.
1. I **Valgte enheter**-delen velger du **Legg til enhet**.
1. I dialogboksen som vises, angir du følgende felt:

    - **Enhetsnavn** – Velg *Lagerverdi*.
    - **Måldataformat** – Velg formatet du vil eksportere data til.

1. Velg **Legg til** for å legge til en ny rad, og velg deretter **Lukk** for å lukke dialogboksen.
1. Vanligvis eksporterer du én rapport om gangen. Hvis du vil eksportere en enkelt rapport, definerer du et filter for raden du nettopp la til, i **Forespørsel**-dialogboksen. På denne måten kan du definere hvilken rapport fra **Lagerverdi**-enheten som skal tas med i eksporten. Følg denne fremgangsmåten for å angi følgende filteralternativer for å eksportere en enkelt rapport:

    1. I fanen **Område** velger du **Legg til** for å legge til en rad.
    2. Angi **Tabell**-feltet til *Lagerverdi*.
    3. Angi **Avledet tabell**-feltet til *Lagerverdi*.
    4. Sett **Felt**-felten til feltet som du vil filtrere etter. Vanligvis bruker du feltet **Kjørenavn** og/eller feltet **Kjøretid**.
    5. Sett **Vilkår**-feltet til verdien du vil søke etter i det valgte feltet. (Hvis du valgte feltet **Kjørenavn** i det forrige trinnet, vil denne verdien være navnet på rapporten. Hvis du valgte feltet **Kjøretid**, vil det være tidspunktet da rapporten ble generert.)
    6. Legg til flere rader i **Område**-fanen etter behov, til du har unikt angitt hvilken rapport du vil søke etter.

1. Velg **OK** for å lagre innstillingene og lukke dialogboksen.
1. Velg **Lagre** for å lagre eksportoppsettet.
1. I fanen **Eksportalternativer** velger du **Eksporter nå** for å generere eksportfilen.
1. På siden **Kjøringssammendrag** som vises, kan du se statusen for eksportjobben og en liste over enheter som ble eksportert. Velg **Lagerverdi**-enheten i delen **Behandlingsstatus for enhet**, og velg deretter **Last ned fil** for å laste ned dataene som er eksportert fra denne enheten.

Hvis du vil ha mer informasjon om hvordan du bruker databehandling til å eksportere data, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Generer en standard lagerverdirapport

Bruk fremgangsmåten nedenfor til å generere en standard **Lagerverdi**-rapport.

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagerregnskap – Statusrapporter \> Lagerverdi**.
1. I dialogboksen **Lagerverdirapport** angir du følgende felter på hurtigfanen **Parametere**:

    - **Navn** – Angi et unikt navn for rapporten.
    - **ID** – Velg [konfigurasjonen for lagerverdirapporten](#report-configuration) som skal brukes for rapporten. Konfigurasjonen fastsetter alternativer for kolonnene og radene som skal tas med i rapporten.
    - **Datointervall** – Bruk feltene i denne delen til å definere hvilke poster som skal tas med i rapporten. Hvis du vil definere datointervallet, kan du enten velge et forhåndsdefinert område (i forhold til rapportgenereringsdatoen) i feltet **Datointervallkode**, eller velge bestemte datoer i feltene **Fra-dato** og **Til-dato**.

1. I hurtigfanen **Poster som skal inkluderes** definerer du filtre og betingelser for å definere hvilke data som skal tas med i rapporten. Velg **Filter** for å åpne en standard dialogboks for Power Query-redigering der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Supply Chain Management.
1. Angi hvordan, når og hvor ofte rapporten skal genereres, i hurtigfanen **Kjør i bakgrunnen**. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og lukke dialogboksen. Rapporten vises.

## <a name="reading-inventory-value-reports"></a>Lesing av lagerverdirapporter

Denne delen gir litt veiledning om hvordan du leser og forstår en lagerverdirapport.

Supply Chain Management støtter følgende to viktige begreper som er knyttet til lagerstatus:

- **Økonomisk oppdatert** – Dette konseptet angir at lagertransaksjonene allerede er fakturert. For produksjonsordrer angir det slutten på en produksjonsordre.
- **Fysisk oppdatert** – Dette konseptet angir at lagertransaksjonene ikke har blitt fakturert ennå, men de er mottatt eller sendt. For produksjonsordrer angir det at materiale er plukket eller at produksjonsordren er ferdigmeldt.

Når du forstår disse to begrepene, bør det være enkelt å forstå følgende kolonner i rapportutdataene:

- **Beholdning: Økonomisk antall** – Antallet som er økonomisk oppdatert.
- **Beholdning: Økonomisk beløp** – Antallsverdien for beholdningen for antallet som er økonomisk oppdatert.
- **Beholdning: Fysisk antall postert** – Antallet som er fysisk oppdatert.
- **Beholdning: Fysisk beløp postert** – Beløpsverdien for beholdningen for antallet som er fysisk oppdatert.
- **Beholdning: Fysisk antall ikke postert** – Antallet som har lagertransaksjoner, men som ikke er postert i økonomimodulen. Du har for eksempel en varemodellgruppe der det ikke er merket av for **Poster aktuell beholdning** og **Poster økonomisk lager**, og du har en vare som er knyttet til denne gruppen. Deretter oppretter du en bestilling, mottar den og fakturerer den. Hvis du ser gjennom lagerverdirapporten for varen på dette tidspunktet, vil du se at antallet og verdien på bestillingen vises i kolonnene **Beholdning: Fysisk antall ikke postert** og **Beholdning: Fysisk beløp ikke postert**.
- **Beholdning: Fysisk beløp ikke postert** – Du kan definere rapportene slik at de viser uposterte beløp. Hvis du imidlertid bruker rapporten for beholdningsavstemming, må du ikke bruke denne verdien. Ellers posteres beløpet som ikke er postert, til økonomimodulen.
- **Beholdning: Antall** – Det totale antallet for alle antallkolonnene i rapporten.
- **Beholdning: Beløp** – Det totale antallet for alle beløpskolonnene i rapporten. Når du gjør beholdningsavstemming, må du ikke bruke denne kolonnen hvis rapporten inneholder kolonnen **Beholdning: Fysisk beløp ikke postert**. I dette tilfellet må du utelate beløpet i **Beholdning: Fysisk beløp ikke postert** fra totalbeløpet.
- **Gjennomsnittlig enhetskostnad** – Totalbeløpet dividert på totalt antall.

Vanligvis bruker du en lagerverdirapport til å vise lagerverdi og -antall. Noen ganger vil imidlertid ikke rapporten vise alle relevante lagerdimensjoner. Hvis du ikke ser dimensjonene du forventer, validerer du følgende innstillinger:

- Se gjennom gruppene for varelager og sporingsdimensjoner. Bare dimensjoner der alternativet **Økonomisk lager** er aktivert, kan vises i rapporten.
- Gå til **Kostnadsstyring \> Oppsett for regnskapspolicyer for beholdning \> Lagerverdirapporter**, velg rapportkonfigurasjonen som du brukte til å generere rapporten, og kontroller at de nødvendige lagerdimensjonene er valgt i **Vis**-kolonnen.

Du har for eksempel en vare med varenummeret *A0001*. I lagringsdimensjonsgruppen er det bare området som er aktivert for økonomisk lager. Både området og lageret er aktivert for fysisk lager. I sporingsdimensjonsgruppen er partinummeret aktivert for fysisk lager, men ikke for økonomisk lager. Deretter bruker du en rapportkonfigurasjon der område, lager og partinummer er valgt. Når du viser rapporten, vises en verdi bare for området. Kolonnene for lageret og partinummeret er tomme. Som dette eksemplet viser, kan lagerverdirapporter bare vise lagerdimensjoner som er aktivert for økonomisk lager.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
