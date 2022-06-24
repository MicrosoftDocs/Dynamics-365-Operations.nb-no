---
title: Overplukking for salgs- og overføringsordrer
description: Denne artikkelen forklarer hvordan du aktiverer overplukking for salgsordrer og overføringsordrer.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b8bbc7d532f910edfb442831d6c906f253dee06c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897291"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Overplukking for salgs- og overføringsordrer

[!include [banner](../includes/banner.md)]

Denne artikkelen presenterer et scenario som viser hvordan du gjør det mulig for en bestemt arbeider eller alle arbeidere å overplukke. Overplukkingsprosessen gjør det mulig å kontrollere overplukking under plukkarbeidet.

Lageroverplukking er et enkelt konsept. Systemet gjør det mulig for arbeidere å plukke flere varer enn det som er angitt for en ordre. Den vurderer imidlertid fortsatt overleveringsgrensen som er angitt på linjenivå for overføringsordren eller salgsordren. Hvis denne grensen overskrides, varsler LWarehouse Management-appen arbeiderne om at de overskrider grensen for overlevering.

Overplukkfunksjonen bidrar til å minimere vedlikehold og hjelper også oppsettet med å forbli fleksibelt. Du kan definere et eller flere menyelementer for mobilenheter og aktivere overplukking bare for noen av dem. Du kan også hindre utvalgte arbeidere i å overplukke salgsordrer eller overføringsordrer uten å måtte endre menyelementene. I stedet kan du deaktivere en eller begge disse funksjonene i de relevante arbeideroppsettene.

Overplukkfunksjonen kan hjelpe arbeidere med å spare tid og krefter når de plukker og leverer varer. Funksjonen gjør det for eksempel mulig for arbeidere å utføre disse oppgavene:

- Kompenser for krymping under plukking eller forsendelse.
- Unngå å måtte pakke ut noe emballasjemateriale under plukkprosessen.
- Kompenser for vareskade under transport.
- Levere et antalls- eller enhetsavvik.
- Minimer brudd på antall på nummerskilter.
- Unngå materialavfall og mangel på dyre materialer.
- Mål det plukkede antallet etter plukking (for eksempel gjennom lastebilvekting).

> [!IMPORTANT]
> Overplukkfunksjonen gjelder bare for salgsordre- og overføringsordreplukking og -behandling. Etterfylling støtter ikke overplukking. Når etterfyllingsarbeid kjøres, tillater ikke systemet brukere å overplukke.

Dette scenarioet i denne artikkelen viser hvordan du definerer og bruker overplukkfunksjonen.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Forutsetning for scenario: Gjør demodata tilgjengelige

Scenarioet i denne artikkelen refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til *USMF* før du begynner.

## <a name="scenario-setup"></a>Scenariooppsett

Før du arbeider deg gjennom eksempelscenarioet, må du aktivere overplukking for både den aktuelle arbeideren og det aktuelle menyelementet.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Definer en arbeider slik at den tillater overplukking

Her er den generelle fremgangsmåten for å konfigurere en arbeider til å aktivere overplukking for salgsordrer og overføringsordrer separat. Denne konfigurasjonen kontrollerer hvilken plukkarbeider som kan utføre overplukkingen, og om denne arbeideren kan utføre overplukking for både overføringsordrer og salgsordrer.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. Velg **Julia Funderburk** i listeruten.
1. På hurtigfanen **Brukere** velger du raden som har følgende verdier. Hvis ingen eksisterende rad har disse verdiene, oppretter du den.

    - **Bruker-ID:** *24*
    - **Brukernavn:** *WH 24*
    - **Standardlager:** *24*
    - **Menynavn:** *Hoved*

1. På hurtigfanen **Arbeid** angir du følgende verdier for bruker *24* hvis de ikke allerede er angitt:

    - **Tillat salgsoverplukking:** *Ja*
    - **Tillat overføringsordreoverplukking:** *Ja*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Definere et menyelement for mobilenhet for å tillate overplukking

Her er den generelle fremgangsmåten for å konfigurere et menyelement for mobilenhet for å aktivere overplukking. Avhengig av forretningskravene dine for tillatelsesnivået til arbeideren som skal bruke menyen på den mobile enheten, kan noen parametere være aktivert eller deaktivert.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg posten som heter *Salgsplukking*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft eller angi følgende verdier for posten:

    - **Navn på menyelement:** *Salgsplukking*
    - **Tittel:** *Salgsplukking*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*
    - **Styrt av:** *Brukerstyrt*
    - **Overstyr målnummerskilt:** *Ja*
    - **Overstyr nummerskiltet under plassering:** *Ja*
    - **Hold arbeidet låst av brukeren:** *Ja*
    - **Tillat overplukking:** *Ja*

> [!IMPORTANT]
> Når de relevante parameterne for både arbeideren og menyelementet for den mobile enheten er aktivert, kan overplukking bare behandles via den mobile enheten.

## <a name="example-scenario"></a>Eksempelscenario

Når forutsetningene, arbeideroppsettet og menyelementoppsettet er på plass, er du klar til å arbeide med funksjonen.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Opprette en salgsordre som tillater overlevering

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en ny salgsordre.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *24*

1. Velg **OK**.
1. Den nye salgsordren åpnes. På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:

    - **Varenummer:** *A0001*
    - **Antall:** *10*

1. På hurtigfanen **Linjedetaljer**, i fanen **Levering**, setter du feltet **Overlevering** til *10*.
1. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
1. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
1. Lukk **Reservasjon**-siden.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

Når frigivelsen er fullført, mottar du informasjonsmeldinger som viser bølge- og last-ID-er som ble opprettet.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Få arbeids-ID og nummerskiltet for den nye ordren

Da du frigjorde ordren til lageret, skulle systemet ha opprettet en ny arbeids-ID som har én plukklinje. Følg denne fremgangsmåten for å finne arbeids-ID-en og nummerskilttilordningen.

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. I rutenettet **Oversikt** søker du i kolonnen **Ordrenummer** etter de salgsordren du nettopp opprettet. For den salgsordren noterer du den tilsvarende arbeids-ID-en.
1. Velg raden for den nye salgsordren for å vise relatert informasjon i rutenettet **Linjer**. Noter deg hvor varen blir plukket fra.
1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.
1. Klikk på **Dimensjoner** i handlingsruten.
1. I **Dimensjonsvisning**-dialogboksen må du kontrollere at det er merket av for **Nummerskilt**, **Lager** og **Varenummer**, og velg deretter **OK**.
1. Angi følgende filtre i ruten **Filter**:

    - **Varenummer** – **er en av** – *A0001*
    - **Lager** – **starter med** – *24*

1. Velg **Bruk**.
1. Noter deg verdiene for **Nummerskilt** som vises.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Overplukk bestillingen ved hjelp av Warehouse Management-mobilappen

1. Logg på mobilappen Lagerstyring som en bruker som er aktivert i lager *24*.
1. Gå til **Utgående \> Salgsplukking**.
1. I feltet **Skann arbeids-ID eller nummerskilt** angir du arbeids-ID-en som ble opprettet for salgsordren.
1. Velg **OK** (hakesymbol).
1. Velg **Overplukking**.
1. Angi **Plukkantall**-feltet til *14*.
1. Velg **OK** (hakesymbol).

    På **Overplukk**-siden får du følgende melding: Overlevering av linje er 40,00 prosent, men den tillatte overleveringen er bare 10,00 prosent. Denne meldingen angir at plukkantallet du angav, overskrider grensen for overlevering. Overleveringsgrensen for salgsordrelinjen er 10 prosent. For et angitt antall på 10 kan du derfor overplukke med bare 1 for et totalt plukkantall på 11.

1. Angi **Plukkantall**-feltet til *11*.
1. Velg **OK** (hakesymbol).
1. I **Nummerskilt**-feltet angir du nummerskiltet du noterte deg i forrige del.
1. I **Målnummerskilt**-feltet angir du målnummerskiltet. Legg merke til at plukklokasjon (*GULV-001*), vare (*A0001*) og antall (*11 stk*) vises.
1. Velg **OK** (hakesymbol).
1. Se gjennom informasjonen på siden **Salgsordrer - Plasser**. **Lok**-feltet bør angi at de plukkede varene skal overføres til *RAMPEDØR*-lokasjonen.
1. Velg **OK** (hakesymbol).

På siden **Skann en arbeids-ID/nummerskilt-ID** mottar du en "Arbeid fullført"-meldingen. Denne meldingen angir at arbeids-ID-en for salgsordren er fullført, og at antallet som er overplukket, ikke overskrider grensen for overlevering på 10 prosent.
