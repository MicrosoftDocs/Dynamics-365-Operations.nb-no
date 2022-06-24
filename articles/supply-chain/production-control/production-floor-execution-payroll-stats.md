---
title: Vis feriesaldoer i grensesnittet for produksjonsutførelse
description: Denne artikkelen inneholder et eksempelscenario som viser hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management slik at den bruker lønnsstatistikk til å gi arbeidere en oversikt over feriesaldoen for inneværende år.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852280"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Vis feriesaldoer i grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder et eksempelscenario som viser hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management slik at den bruker lønnsstatistikk til å gi hver arbeider en oversikt over feriesaldoen for inneværende år. Arbeidere kan se feriesaldoen i dialogboksen **Min dag** i grensesnittet for produksjonsutførelse.

Dette scenarioet bruker den danske helligdagslovgivningen, der ferieåret går fra 1. september til 31. august. I dette scenarioet har firmaet ansatt en ny arbeider og vil gi den ansatte en saldo på ti feriedager for resten av det nåværende ferieåret.

## <a name="turn-on-the-required-features"></a>Aktivere de nødvendige funksjonene

Hvis du vil kjøre dette scenarioet, må du aktivere *Min dag*-visningen for grensesnittet for produksjonsutførelse i [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Hvis du vil ha informasjon om hvordan du aktiverer denne og andre funksjoner for grensesnittet for produksjonsutførelse, kan du se [Konfigurer grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

## <a name="create-a-new-pay-type"></a>Opprett en ny lønnstype

Start med å opprette en ny *lønnstype* som sporer arbeiderens opptjente feriedager (kalles også *feriesaldoen*). Vanligvis brukes lønnstyper til å beregne arbeidernes lønn. Lønnstypen du oppretter her, blir imidlertid brukt til å beregne en saldo.

1. Gå til **Timeregistrering \> Oppsett \> Lønn \> Lønnstyper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. På den nye raden angir du følgende verdier:

    - **Lønnstype:** *5151-1*
    - **Beskrivelse:** *Teller for feriedager til arbeideren*
    - **Inkluder i eksport:** *Nei*

## <a name="update-the-pay-agreement"></a>Oppdater lønnsavtalen

I denne delen kan du redigere en eksisterende *lønnsavtale* ved å legge til den nye lønnstypen og angi reglene som definerer hvordan feriesaldoen til hver arbeider justeres når feriedager registreres.

1. Gå til **Timeregistrering \> Oppsett \> Lønn \> Lønnsavtaler**.
1. Velg lønnsavtalen der du vil definere feriepolicyen. (Hvis du jobber med standard USMS-eksempeldata, finnes det bare én lønnsavtale. *Man*.)
1. Kontroller at den valgte lønnsavtalen er gyldig for nåværende dato. Hvis du jobber med standard USMS-eksempeldata, kan **Til dato**-feltet i *Man*-lønnsavtalen settes til en dato som er i fortiden. Endre verdien slik at det er et år eller to i fremtiden etter behov.
1. Velg **Avtalelinjer** i handlingsruten.
1. Angi følgende verdier på verktøylinjen på siden **Lønnsavtalelinjer** i hurtigfanen **Oversikt**:

    - I den første rullegardinlisten velger du **Mandag**.
    - I den andre rullegardinlisten velger du **Fravær**.

1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. På den nye raden angir du feltet **Lønnstype** til lønnstypen du opprettet for dette scenarioet (*5151-1*). La alle andre felter stå med standardverdiene.
1. Mens den nye raden fremdeles er merket, angir du følgende verdier i hurtigfanen **Generelt**:

    - **Fraværskode:** *Ferie*
    - **Bruk fast antall:** *Ja*
    - **Konstant:** *–1*

1. I handlingsruten velger du **Kopier dag**.
1. Angi følgende verdier i dialogboksen **Kopier dag**:

    - **Tirsdag**, **Onsdag**, **Torsdag** og **Fredag:** *Ja*
    - **Overskriv:** *Ja*
    - **Fravær:** *Ja*

1. Velg **OK**.

## <a name="create-a-payroll-statistic-group"></a>Opprette en lønnsstatistikkgruppe

*Lønnsstatistikkgrupper* brukes til å definere statistikk for arbeiderregistreringer i en periode. I dette scenarioet bruker du en lønnsstatistikkgruppe til å beregne antallet feriedager arbeiderne får i løpet av en ferieperiode. I Danmark går ferieperioden fra 1. september til 31. august.

1. Gå til **Timeregistrering \> Oppsett \> Lønn \> Lønnsstatistikkgrupper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. På den nye raden angir du følgende verdier:

    - **Lønnsstatistikkgruppe:** *VAC*
    - **Beskrivelse:** *Feriesaldo*
    - **Overfør:** *Nei*

1. Mens den nye raden fremdeles er valgt, velger du **Oppsett** i handlingsruten.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet på siden **Oppsett**.
1. På den nye raden setter du **Lønsstype**-feltet til *5151-1*.
1. Velg og hold (eller høyreklikk) i feltet **Periodekode** og velg **Vis detaljer**. Du kan nå definere periodekoden som du vil tildele dette feltet senere.
1. Velg **Ny** i handlingsruten på siden **Periodetyper** for å legge til en rad i rutenettet.
1. På den nye raden angir du følgende verdier:

    - **Periodetyper:** *VacYear*
    - **Beskrivelse:** *Ferieår*
    - **Frekvens:** *År*

1. Mens den nye raden fremdeles er valgt, velger du **Generer perioder** i handlingsruten.
1. Angi følgende verdier i dialogboksen **Generer perioder**:

    - **Angi periodens startdato:** *1. september 2021*
    - **Periodelengde:** *5*

1. Velg **OK**.
1. Lukk siden **Periodetyper** for å gå tilbake til siden **Lønnsstatistikkgrupper**.
1. Angi **Periodekode**-feltettil periodetypen du akkurat opprettet (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Opprett et statistisk saldooppsett

I denne delen oppretter du et *statistisk saldooppsett* som er koblet til lønnsstatistikkgruppen du opprettet i den forrige delen. Senere kobler du dette statistiske balanseoppsettet til **Min dag**-visningen i grensesnittet for produksjonsutførelse. **Min dag**-visningen kan da vise feriesaldoene for lønnstypen som er tildelt den tilknyttede lønnsstatistikkgruppen.

1. Gå til **Timeregistrering \> Oppsett \> Lønn \> Statistisk saldooppsett**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. På den nye raden angir du følgende verdier:

    - **Lønnsstatistikkgruppe:** *VAC*
    - **Eksternt navn:** *Feriesaldo*
    - **Fleksi:** *Nei*

## <a name="create-a-manual-premium"></a>Opprett en manuell bonus

*Manuelle bonuser* brukes vanligvis til å gi arbeidere ekstra lønn for ekstra arbeid. I dette scenarioet oppretter du en manuell bonus som du kan bruke til å definere den innledende feriesaldoen for hver arbeider.

1. Gå til **Timeregistrering \> Oppsett \> Lønn \> Manuelle bonuser**.
1. I handlingsruten velger du **Ny** for legge til en oppføring.
1. I den nye oppføringen angir du følgende verdier:

    - **Bonuser:** *VAC*
    - **Beskrivelse:** *Justeringer av arbeideres feriesaldo*
    - **Lønnstype:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Angi den første feriesaldoen til en arbeider og juster den med én dag

Lønnsadministratorer bruker siden **Godkjenn** til å gå gjennom og godkjenne arbeideres daglige registreringer. I dette scenarioet tar du på deg rollen som administrator slik at du kan angi den innledende feriesaldoen for en arbeider og registrere feriedager som arbeideren tar.

1. Gå til **Timeregistrering \> Gjennomgå og godkjenn \> Godkjenn**.
1. I **Godkjenn**-dialogboksen angir du følgende felter:

    - **Godkjenningsgruppe** – Velg godkjenningsgruppen du tilhører. (Hvis du jobber med standard USMS-eksempeldata, finnes det bare én godkjenningsgruppe. *AdmMan*.)
    - **Vis hele gruppen, 1 dag** – Velg alternativet, og sett deretter feltet til nåværende dato.

1. Velg **OK**.
1. **Godkjenn**-siden viser en liste med oppføringer som samsvarer med kriteriene. Velg arbeideren du vil godkjenne. Hvis du arbeider med standard USMF-eksempeldata, velger du *000496* (*Christina Portra*).
1. Gi den valgte arbeideren ti dager med ferie:

    1. Mens arbeideren fremdeles er valgt, velger du **Bonuslinjer** i handlingsruten.
    1. Velg **Ny** i handlingsruten på siden **Bonuslinjer** for å legge til en rad i rutenettet.
    1. På den nye raden angir du følgende verdier:

        - **Bonuser:** *VAC*
        - **Antall:** *10*

    1. Lukk **Bonuslinjer**-siden.

1. Registrer at arbeideren brukte én av feriedagene på nåværende dato på **Godkjenn**-siden:

    1. Mens arbeideren fremdeles er valgt i den nedre delen av siden, i fanen **Oversikt**, velger du **Ny** på verktøylinjen for å legge til en ny rad i rutenettet.
    1. På den nye raden angir du følgende verdier:

        - **Journalregistreringstype:** *Fravær*
        - **Referanse:** *Ferie*

    1. I den øvre delen av siden velger du **Overfør** på verktøylinjen for å bruke feriesaldoen og beregne fradraget.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigurer grensesnittet for produksjonsutførelse slik at det inkluderer dialogboksen Min dag

I denne delen legger du til en **Min dag**-knapp i grensesnittet for produksjonsutførelse. Arbeidere kan deretter bruke denne knappen til å åpne dialogboksen **Min dag**.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.
1. Velg en konfigurasjon, for eksempel *Standard*.
1. I handlingsruten velger du **Utformingsfaner**.
1. Velg **Alle jobber** i listeruten på siden *Utformingsfaner* for å vise innstillingene for den fanen. **Hovedvisning**-feltet skal nå vise en verdi for *Alle jobber*.
1. I handlingsruten velger du **Rediger**.
1. Velg **Min dag** i kolonnen **Tilgjengelige handlinger** i hurtigfanen **Sekundærverktøy**. Velg deretter pil høyre-knapp for å flytte den til kolonnen **Valgte handlinger**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Sjekk saldoen i grensesnittet for produksjonsutførelse

I denne delen logger du deg på grensesnittet for produksjonsutførelse som arbeideren du definerte ferietid for tidligere. Deretter åpner du dialogboksen **Min dag** for å vise feriesaldoen.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Produksjonsutførelse**.
1. Hvis du blir bedt om å velge en konfigurasjon, velger du konfigurasjonen du konfigurerte tidligere i dette scenarioet (*Standard*).
1. Logg deg på som brukeren du konfigurerte tidligere i dette scenarioet. Hvis du jobber med standard USMS-eksempeldata, skal du kunne logge deg på ved å angi *123* i **Kort-ID**-feltet. Denne kort-ID-en tilsvarer Christina Portra.
1. Velg **Min dag** på venstre verktøylinje.
1. Undersøk **Saldoer**-delen i dialogboksen. Nå skal denne delen vise at du har en saldo på ni feriedager.
