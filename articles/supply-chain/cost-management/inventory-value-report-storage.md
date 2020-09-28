---
title: Rapport for oppbevaring av lagerverdi
description: Dette emnet forklarer hvordan du kjører en rapport for oppbevaring av lagerverdi og gjør utdataene tilgjengelig digitalt, enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksportert dokument i et av flere formater.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759574"
---
# <a name="inventory-value-storage-report"></a>Rapport for oppbevaring av lagerverdi

Dette emnet forklarer hvordan du kjører en rapport for **oppbevaring av lagerverdi** og gjør utdataene tilgjengelig digitalt, enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksportert dokument i et av flere formater.

Når du viser rapporten i nettleseren, justeres kolonner og aggregatsaldoer dynamisk, avhengig av det konfigurerte oppsettet. Du kan sortere resultatene, filtrere dem, drille ned til dataene og mye mer.

Rapportresultater lagres i **Lagerverdi**-dataenheten. Derfor kan du filtrere og eksportere resultatene til et format som for eksempel kommadelte verdier (CSV) eller Microsoft Excel-format.

Rapporten for **oppbevaring av lagerverdi** er nyttig når utdataene inneholder mange linjer. Du har for eksempel 50 000 varer, og 300 butikker er opprettet som lagre. Hvis du i så fall ber om sluttsaldoer for beholdning etter vare, område og lager, vil utdataene inneholde mange linjer.

> [!NOTE]
> Rapporten inkluderer ikke delsummer som er definert i rapportoppsettet. Den inkluderer heller ikke saldoer i økonomimodulen, selv når de er definert i rapportoppsettet. Avstemming til økonomimodulen må gjøres ved hjelp av råbalanser.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Aktiver funksjonen for oppbevaring av lagerverdi

Før du kan generere en rapport for **oppbevaring av lagerverdi**, må du aktivere funksjonen i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul** – Kostnadsstyring
- **Funksjonsnavn** – oppbevaring av lagerverdi

## <a name="generate-an-inventory-value-storage-report"></a>Generere en rapport for oppbevaring av lagerverdi

Følg denne fremgangsmåten for å generere og lagre en rapport for **oppbevaring av lagerverdi**:

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Rapport for oppbevaring av lagerverdi**.
1. Velg **Ny**.
1. I dialogboksen **Lagerverdi** som vises, angir du følgende verdier for å definere hvilke poster som skal tas med i rapporten:

    - I hurtigfanen **Parametere** angir du et unikt navn på rapporten, og bruker feltene i **Datointervall**-delen til å definere hvilke poster som skal tas med i rapporten. Hvis du vil definere datointervallet, kan du enten velge et forhåndsdefinert område (i forhold til rapportgenereringsdatoen) i feltet **Datointervallkode**, eller velge bestemte datoer i feltene **Fra-dato** og **Til-dato**.
    - I hurtigfanen **Poster som skal inkluderes** definerer du filtre og betingelser for å definere hvilke data som skal tas med i rapporten.
    - Angi hvordan, når og hvor ofte rapporten skal genereres, i hurtigfanen **Kjør i bakgrunnen**.

    > [!NOTE]
    > Denne rapporten blir alltid kjørt som en del av en satsvis jobb.

1. Velg **OK** for å bruke innstillingene og lukke dialogboksen.

Når den satsvise jobben er fullført, vises rapporten på siden **Rapport for oppbevaring av lagerverdi**. Du må kanskje oppdatere siden for å kunne se rapporten.

## <a name="explore-an-inventory-value-storage-report"></a>Utforske en rapport for oppbevaring av lagerverdi

Når du har generert en rapport, kan du vise og utforske den når som helst på følgende måte:

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Rapport for oppbevaring av lagerverdi**.
1. Velg en rapport i listen.
1. Velg **Vis detaljer** for å vise rapportinnholdet.
1. Utforsk rapporten ved å følge et av disse trinnene:

    - Du kan velge nesten hvilken som helst kolonneoverskrift for å sortere eller filtrere rutenettet etter verdier i denne kolonnen, på samme måte som med de fleste standardsidene i Supply Chain Management.
    - Bruk **Filter**-feltet til å filtrere rapporten ved hjelp av en hvilken som helst verdi i en av flere tilgjengelige kolonner.
    - Bruk Vis-menyen (over **Filter**-feltet) til å lagre og laste inn dine favorittkombinasjoner av sorterings- og filteralternativer.

## <a name="export-an-inventory-value-storage-report"></a>Eksportere en rapport for oppbevaring av lagerverdi

Hver rapport du genererer, lagres i dataenheten **Lagerverdi**. Du kan bruke standardfunksjonene i Supply Chain Management til å eksportere data fra denne enheten til alle støttede dataformater, inkludert CSV eller Excel-format.

Følgende eksempel viser hvordan du eksporterer en rapport for **oppbevaring av lagerverdi**.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Databehandling**.
1. I delen **Import/eksport** velger du **Eksport**-flisen. 
1. På **Eksport**-siden som vises, vil du konfigurere eksportjobben. Skriv først inn et gruppenavn for jobben.
1. I **Valgte enheter**-delen velger du **Legg til enhet**.
1. I dialogboksen som vises, angir du følgende felt:

    - **Enhetsnavn** – Velg **Lagerverdi**.
    - **Måldataformat** – Velg formatet du vil eksportere data til.

1. Velg **Legg til** for å legge til en ny rad, og velg deretter **Lukk** for å lukke dialogboksen.
1. Vanligvis eksporterer du én rapport om gangen. Hvis du vil eksportere en enkelt rapport, definerer du et filter for raden du nettopp la til, i **Forespørsel**-dialogboksen. På denne måten kan du definere hvilken rapport fra **Lagerverdi**-enheten som skal tas med i eksporten. Følg denne fremgangsmåten for å angi følgende filteralternativer for å eksportere en enkelt rapport:

    1. I kategorien **Område** velger du **Legg til** for å legge til en rad.
    2. Angi **Tabell**-feltet til **Lagerverdi**.
    3. Angi **Avledet tabell**-feltet til **Lagerverdi**.
    4. Sett **Felt**-felten til feltet som du vil filtrere etter. Vanligvis bruker du feltet **Kjørenavn** og/eller feltet **Kjøretid**.
    5. Sett **Vilkår**-feltet til verdien du vil søke etter i det valgte feltet. (Hvis du valgte feltet **Kjørenavn** i det forrige trinnet, vil denne verdien være navnet på rapporten. Hvis du valgte feltet **Kjøretid**, vil det være tidspunktet da rapporten ble generert.)
    6. Legg til flere rader i **Område**-kategorien etter behov, til du har unikt angitt hvilken rapport du vil søke etter.

1. Velg **OK** for å lagre innstillingene og lukke dialogboksen.
1. Velg **Lagre** for å lagre eksportoppsettet.
1. I kategorien **Eksportalternativer** velger du **Eksporter nå** for å generere eksportfilen.
1. På siden **Kjøringssammendrag** som vises, kan du se statusen for eksportjobben og en liste over enheter som ble eksportert. Velg **Lagerverdi**-enheten i delen **Behandlingsstatus for enhet**, og velg deretter **Last ned fil** for å laste ned dataene som er eksportert fra denne enheten.

Hvis du vil ha mer informasjon om hvordan du bruker databehandling til å eksportere data, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
