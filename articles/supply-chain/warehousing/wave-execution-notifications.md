---
title: Varslinger for bølgekjøring
description: Denne artikkelen beskriver varslinger under bølgekjøring og forklarer hvordan du konfigurerer dem.
author: Mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 5c8fa259e51f024d19c1f2f7e84ed7edd0ddb7e1
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069036"
---
# <a name="wave-execution-notifications"></a>Varslinger for bølgekjøring

[!include [banner](../includes/banner.md)]

Funksjonen *Varslinger for bølgekjøring* bruker forretningshendelser og handlingssenteret til å levere varslinger som er knyttet til bølgekjøring. Det lar deg angi hendelsestypene som genererer meldinger, lagrene som genererer dem og brukerne som mottar dem.

Knappen **Vis meldinger** (klokkesymbolet) til høyre på navigasjonslinjen viser når en handlingssentermelding er tilgjengelig for den gjeldende brukeren. Brukeren kan velge **Vis meldinger**-knappen for å åpne handlingssenteret og se gjennom meldingene.

Forretningshendelser forekommer når forretningsprosesser kjøres. Forretningsprosesser består av oppgaver. Under en forretningsprosess utfører brukerne som deltar i den, forretningshandlinger for å fullføre disse oppgavene. Forretningshendelser inneholder en mekanisme som gjør at eksterne systemer kan motta varslinger fra økonomi- og driftsapper. På denne måten kan systemene utføre forretningshandlinger som svar på forretningshendelsene. Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningshendelser](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Varslinger for bølgekjøring

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Varslinger for bølgekjøring* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scenario: Send varslinger om satsvis bølgekjøring til handlingssenteret

Dette scenariet viser slutt-til-slutt-flyten for sending av meldinger om utførelsesfeil for bølgebunke til en bestemt rolle via handlingssenteret.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Kontroller at bølger kjøres i satsvis modus

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. På hurtigfanen **Bølgebehandling** setter du alternativet **Behandle bølger satsvis** til *Ja*.

> [!NOTE]
> Hvis du vil deaktivere varslinger for satsvis bølgekjøring, setter du alternativet **Deaktiver varslinger om satsvis bølgebehandling** til *Ja*.

### <a name="configure-a-wave-notification-policy"></a>Konfigurer en bølgevarslingspolicy

Policyer for bølgevarsling definerer varslingstypene som sendes og brukerne som blir varslet.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Policyer for bølgevarsling**.
1. Opprett en post som har følgende innstillinger:

    - **Policy for bølgevarsling:** *24BatchError*
    - **Beskrivelse:** *Lager 24-bølgebunkefeil*
    - **Send melding ved:** *Bare feil*
    - **Til rolle:** *Systemansvarling*

        > [!NOTE]
        > Fordi dette scenariet bruker demodata, velges *Systemadministrator*-rollen av hensyn til forenkling. Derfor vil du motta meldingene fordi du er logget på som en systemadministratorbruker. I praksis bør du imidlertid vanligvis velge en mer spesifikk rolle for å varsle om feil under utføring av bølgeparti, for eksempel *Lagersjef*.

1. Velg **Lagre** i handlingsruten.

### <a name="configure-a-wave-template"></a>Konfigurere en bølgemal

Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til tilsvarende bølgeetikettmaler.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I listeruten setter du feltet **Bølgemaltype** til *Forsendelse*, og deretter velger du bølgemalen *24 Standardforsendelse* for lager 24.
1. I hurtigfanen **Generelt** angir du feltet **Policy for bølgevarsling**-feltet til *24BatchError*.

### <a name="configure-a-work-template"></a>Konfigurere en arbeidsmal

Arbeidsmaler brukes under bølgekjøring for å generere arbeid. I dette scenariet skal bølgekjøring utløse en feil. Hvis du angir at arbeidsmalspørringen skal bruke et lager som ikke finnes, vil du sikre at bølgeutførelsen mislykkes og derfor sender et varsel.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. I listeruten setter du feltet **Arbeidsmaltype** til *Salgsordrer*, og deretter velger du arbeidsmalen *24 SO stadium* for lager 24.
1. I handlingsruten velger du **Rediger spørring**.
1. I dialogboksen i redigeringsprogrammet for spørringen, på fanen **Område**, redigerer du følgende rad (eller legger den til hvis den ikke finnes):

    - **Tabell:** *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
    - **Felt:** *Lager*
    - **Kriterier:** Endre verdien fra *24* til *Feil*.

1. Velg **OK**, og bekreft endringen.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Opprette en salgsordre og frigi den til lageret

1. Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.
1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Lager:** *24*

1. I hurtigfanen **Salgsordrelinjer** legger du til en salgsordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001*
    - **Antall:** *10*

    > [!NOTE]
    > Disse varene og antallene er bare eksempler. Det angitte lageret må ha nok varer på lager.

1. Mens den nye ordrelinjen fremdeles er valgt på hurtigfanen **Salgsordrelinjer**, velger du **Beholdning \> Reservasjon** på verktøylinjen.
1. På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**. Lukk deretter siden.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

### <a name="notifications-from-wave-batch-job-execution"></a>Varslinger fra utføring av satsvis bølgjobb

Avhengig av oppsettet av forretningshendelsene vil du til slutt få et varsel om mislykket bølgeutførelse. Handlingssentermeldingen vil ligne på følgende eksempel, og vil inneholde en kobling til bølgen som mislyktes.

> **Feil under bølgekjøring**  
> Det oppstod en feil under utføring av bølgen USMF-000000001.  
> Siste meldinger: Intet arbeid ble opprettet for bølgen USMF-000000001.
>
> **STATUS**  
> Aktivt
>
> Åpne bølgedetaljer

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

