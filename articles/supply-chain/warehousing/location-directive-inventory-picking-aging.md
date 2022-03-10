---
title: Aldersfordeling for lagerplukking for lokasjonsdirektiv
description: Dette emnet forklarer hvordan du bruker først-inn-først-ut (FIFO) og sist-inn-først-ut (LIFO) lokasjonsdirektivstrategier under plukking.
author: mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 83f73052d1d9d8a29a80ce3cf1035a259cd92c17
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578590"
---
# <a name="location-directive-inventory-picking-aging"></a>Aldersfordeling for lagerplukking for lokasjonsdirektiv

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker først-inn-først-ut (FIFO) og sist-inn-først-ut (LIFO) lokasjonsdirektivstrategier under plukking. Disse strategiene fungerer sammen med aldersfordelingsdatoene som registreres for lokasjoner som skal spores når beholdningen først ankom lageret. Funksjonen *Aldersfordeling for lagerplukking for lokasjonsdirektiv* bruker datoen for lokasjonen for å bestemme aldersfordeling. Funksjonen *Status for lagerlokasjon* oppdaterer datoen på lokasjonen basert på datoen fra nummerskiltet.

Du kan bruke FIFO- og LIFO-strategier til å levere både partisporingsvarer og ikke-partisporingsvarer, basert på datoen da beholdningen ble registrerte på lageret. Denne funksjonen kan være spesielt nyttig for ikke-partisporinglageret, der en utløpsdato ikke er tilgjengelig for sortering.

Når beholdning mottas eller opprettes i lageret, oppdaterer systemet det aktuelle nummerskiltet, slik at gjeldende dato vises som aldersfordelingsdato. Denne datoen brukes deretter av lokasjonsdirektivstrategiene til å identifisere den eldste eller nyeste beholdningen i lageret. Hvis lager flyttes til en lokasjon som ikke er sporet av lisensnummeret, oppdateres selve lokasjonen med aldersfordelingsinformasjon, og denne informasjonen brukes deretter av strategiene.

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) i denne rekkefølgen:

1. Status for lagerlokasjon
1. Aldersfordeling for lagerplukking for lokasjonsdirektiv

## <a name="feature-requirements"></a>Funksjonskrav

Hvis du vil bruke denne funksjonen, må du angi alternativet **Aktiver lokasjonsstatus** til *Ja* for hver [lokasjonsprofil](tasks/create-location-profile.md) som brukes til å lagre lager. Hvis du vil angi dette alternativet for en lokasjonsprofil, kan du gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**, og velg deretter lokasjonsprofilen. Du finner alternativet i hurtigfanen **Generelt**.

## <a name="feature-scenarios"></a>Funksjonsscenarier

Denne delen inneholder eksempler som viser hvordan du definerer og bruker FIFO- og LIFO-strategier.

> [!TIP]
> Denne delen inneholder to scenarier, én for FIFO og én for LIFO. Fremgangsmåtene som oppgis, antar at du utfører begge scenariene, i rekkefølge. Det anbefales at du gjør begge scenariene, slik at du kan oppleve forskjellene mellom de to strategiene.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom disse scenariene ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke disse scenariene som en veiledning for å bruke funksjonen i et produksjonssystem. I så fall må du imidlertid bytte dine egne verdier for hver innstilling som beskrives her.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Definere scenarioene

Demonstrasjonsdataene krever oppsett- og lagerjusteringer for å støtte scenariene. Følg denne fremgangsmåten for å opprette lagerdataene som kreves for å jobbe gjennom FIFO- og LIFO-scenariene.

1. Logg på et system der demodata er installert, og velg den juridiske enheten **USMF**.
1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. I handlingsruten velger du **Rediger**.
1. Velg **ETASJE-05** i listen over lokasjonsprofiler.
1. På **Generelt**-hurtigfanen angir du **Aktiver lokasjonsstatus**-alternativet til *Ja*.
1. Velg **Lagre**.
1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I listen over lokasjonsdirektiver velger du **63 plukk containerbruk**.
1. Velg **Rediger** for å legge siden inn i redigeringsmodus.
1. På hurtigfanen **Lokasjonsdirektivhandlinger** finner du linjen der feltet **Sekvensnummer** er satt til *1*, og følg et av disse trinnene:

    - Hvis du definerer et FIFO-scenario, endrer du verdien for **Strategi**-feltet til *Lokasjon med aldersfordelt FIFO*.
    - Hvis du definerer et LIFO-scenario, endrer du verdien for **Strategi**-feltet til *Lokasjon med aldersfordelt FIFO*.

1. I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.
1. I spørringsdialogboksen i fanen **Område** velger du **Legg til** for å legge til en linje, og angi deretter følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *Sone-ID*
    - **Vilkår:** *Etasje*

1. Velg **OK** for å bruke innstillingene og lukke spørringsdialogboksen.
1. Velg **Lagre** for å lagre endringene i lokasjonsdirektivet.
1. På en mobilenhet eller i appen *Dynamics 365 for Finance and Operations – Lager* på PCen følger du denne fremgangsmåten for å fjerne et eksisterende lager fra lagerlokasjonen for å støtte scenariene:

    1. Logg på lager *63* ved å bruke riktig bruker-ID og passord.
    1. I hovedmenyen velger du **Kvalitet**.
    1. I menyen **Kvalitetsstyring** velger du **Svinn**.
    1. På siden **Svinn** velger du feltet **LOC/LP**, og deretter angir du *63\_1*.
    1. Velg **Angi** eller **OK**.
    1. Bekreft **Svinn**-detaljene for **Justering ut** ved å velge **Enter** eller **OK**.

    Når lisensnummerlageret justeres ut, får du en "Arbeid fullført"-melding.

    Disse trinnene lar lageret være på to steder i demodataene. Hver lokasjon har en annen aldersfordelingsdato. Lokasjonen *FL-001* har en aldersfordelingsdato på 15. april 2017, og lokasjonen *FL-002* har en aldersfordelingsdato på 29. januar 2017. Begge lokasjonene inneholder vare *A0001*.

    Hvis du vil vise disse dataene, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste** og deretter filtrere på lager *63* og vare *A0001*. I radene der **Lokasjon**-feltet er satt til *FL-001* eller *FL-002*, velger du en linje som har en positiv **Aktuell beholdning**-verdi, og deretter velger du **Transaksjoner** i handlingsruten. Feltet **Fysisk dato** vil vise en dato som samsvarer med en av de tidligere angitte aldersfordelingsdatoene.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Scenario 1: Definere og bruke FIFO aldersfordeling for lokasjon

FIFO-strategien finner lokasjonen som inneholder den eldste aldersfordelingsdatoen, og den tildeler plukking basert på den aldersfordelingsdatoen.

1. Hvis du ikke allerede har gjort det, kan du [forberede eksempeldataene](#demo-set-up) som kreves for dette scenariet.
1. Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.
1. Velg **Ny**.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-001*.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *63*.

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Det inneholder en ny, tom rad i rutenettet på **Salgsordrelinjer**-hurtigfanen. For denne ordrelinjen setter du feltet **Varenummer** til *A0001* og **Antall**-feltet til *1*.
1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere det bestilte antallet av denne varen fra det bestemte lageret.
1. Lukk **Reservasjon**-siden.
1. På siden **Salgsordre**, i handlingsruten i fanen **Lager** i gruppen **Handlinger**, velger du **Frigi til lager**. Du mottar informasjonsmeldinger. Systemet oppretter en forsendelse, legger den til en ny last, og oppretter det nødvendige arbeidet.
1. I hurtigfanen **Salgsordrelinjer** på menyen **Lager** velger du **Arbeidsdetaljer** for å åpne arbeidet som ble opprettet for denne salgsordren. Legg merke til at linjen der **Arbeidstype**-verdien er *Plukk*, viser en **Lokasjon**-verdi på *FL-002*. Denne lokasjonen inneholder nummerskiltet som har den eldste aldersfordelingsdatoen (FIFO).
1. Velg **Lager \> Forsendelsesdetaljer**.
1. På hurtigfanen **Generelt** noterer du bølge-ID-en, slik at du kan bruke den i scenario 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Scenario 2: Definere og bruke LIFO aldersfordeling for lokasjon

LIFO-strategien finner lokasjonen som inneholder den nyeste aldersfordelingsdatoen, og den tildeler plukking basert på den aldersfordelingsdatoen. I scenario 2 skal du redigere oppsettet for scenario 1 (FIFO), og bruke salgsordren og bølgen som ble opprettet i løpet av scenariet.

1. Før du starter dette scenariet konfigurerer og fullfører du det fullstendige FIFO-scenariet som beskrevet i [forrige del](#fifo-demo). I dette scenariet skal du bruke bølgen på nytt og det meste av oppsettet som ble opprettet for det scenariet.
1. Rediger **63 plukk containerbruk**-lokasjonsdirektivet, slik at det bruker *Lokasjon med aldersfordelt LIFO*-strategien, som beskrevet i den første delen av prosedyren [Definere scenarioene](#demo-set-up).

    Deretter endrer du bølgen som ble opprettet for salgsordren i scenario 1, slik at den bruker strategien *Lokasjon med aldersfordelt LIFO*.

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg og åpne lyden som inneholder ordren du opprettet for FIFO-scenariet.
1. I handlingsruten, i fanen **Arbeid**, velger du **Avbryt** for å avbryte arbeidet du opprettet for FIFO-scenarioet.
1. I handlingsruten, i fanen **Bølge**, i **Bølge**-gruppen, velger du **Behandle**.
1. Når behandlingen er fullført, velger du **Arbeid** for å åpne arbeidet som ble opprettet for denne bølgen, i handlingsruten i fanen **Bølge** i gruppen **Relatert informasjon**.
1. På **Arbeid**-siden, i fanen **Oversikt**, skal det være to linjer. Velg linjen der **Arbeidsstatus**-feltet er satt til *Åpen*.
1. Legg merke til at linjen der **Arbeidstype**-verdien er *Plukk*, viser en **Lokasjon**-verdi på *FL-001*. Denne lokasjonen inneholder nummerskiltet som har den nyeste aldersfordelingsdatoen (LIFO).

I disse scenariene har du sett hvordan strategien for aldersfordeling for lokasjon fungerer for lagerlokasjonen som enten har det eldste lageret eller den nyeste lageret, avhengig av den valgte strategien.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]