---
title: Oppdelt arbeid
description: Dette emnet gir informasjon om funksjonen for oppdelt arbeid. Med denne funksjonen kan du dele opp store arbeidsordrer i flere mindre arbeidsordrer som deretter kan tilordnes til flere lagerarbeidere. På denne måten kan det samme arbeidet plukkes samtidig av flere lagerarbeidere.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6fa8955b935f22a0c4ae7311e871fa64afcd2bcdde48c70bf772a3cb7abd772a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781812"
---
# <a name="work-split"></a>Oppdelt arbeid

Med funksjonen for oppdelt arbeid kan du dele opp store arbeids-ID-er (det vil si arbeidsordrer som har flere linjer) i flere mindre arbeids-ID- som deretter kan tilordnes til flere lagerarbeidere. På denne måten kan det samme arbeidsopprettelsesnummeret plukkes samtidig av flere lagerarbeidere.

> [!IMPORTANT]
> Du kan bare dele opp arbeidsordrer som har statusen *Åpen* eller *Pågår*.

## <a name="turn-on-the-work-split-functionality"></a>Aktivere funksjonen for oppdelt arbeid

Før du kan bruke funksjonen for oppdelt arbeid, må du aktivere funksjonen og den nødvendige funksjonen i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonene og aktivere dem hvis den kreves.

Først aktiverer du den nødvendige funksjonen *Organisasjonsomfattende arbeidsblokkering* hvis den ikke allerede er aktivert. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Organisasjonsomfattende arbeidsblokkering*

> [!NOTE]
> Når denne funksjonen er aktivert, blir dataoppgradering automatisk brukt etter at funksjonen er aktivert på tvers av alle juridiske enheter.

Deretter aktiverer du *Oppdelt arbeid*-funksjonen, som er oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Oppdelt arbeid*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Forbedringer av sidene Arbeidsdetaljer og Alt arbeid

Funksjonen *Oppdelt arbeid* legger til følgende to knapper i fanen **Arbeid** i handlingsruten på sidene **Arbeidsdetaljer** og **Alt arbeid**:

- **Del arbeid** – Del opp gjeldende arbeids-ID i flere mindre arbeids-ID-er som kan behandles av individuelle arbeidere.
- **Avbryt arbeidsoppdelingsøkt** – Avbryt arbeidsoppdelingsøkten, og gjør arbeidet tilgjengelig for behandling.

![Knappene Del opp Arbeid og Avbryt arbeidsoppdelingsøkt.](media/Work_split_buttons.png "Knappene Del opp Arbeid og Avbryt arbeidsoppdelingsøkt")

> [!IMPORTANT]
> Knappen **Del arbeid** er ikke tilgjengelig hvis noen av følgende betingelser er oppfylt:
>
> - Arbeidsstatusen er noe annet enn *Åpen* eller *Pågår*.
> - En container-ID er knyttet til arbeids-ID-en. (En container kan ikke deles systematisk, fordi den krever fysiske handlinger.)
> - Arbeidet er knyttet til en gruppe.
> - Arbeidsordretypen er noe annet enn en av følgende typer:
>
>    - Salgsordre
>    - Råvareplukking
>    - Utstedelse for overføring
>
> - Arbeidet deles for øyeblikket av en annen bruker. Hvis du prøver å åpne delingssiden for arbeid som allerede deles av en annen bruker, får du følgende feilmelding: Arbeidet med ID \#\#\#\# deles for øyeblikket. Prøv på nytt om noen minutter. Hvis du fortsatt får denne meldingen, kontakter du en overordnet.

En ny arbeidsblokkeringsårsak, *Del arbeid*, angir når arbeids-ID-en er i ferd med å deles opp. Det vises både på siden **Del arbeid** og i mobilappen Lagerstyring hvis en bruker prøver å kjøre arbeidet. Når det brukes blokkeringsårsaker, endres navnet på det **Blokkert bølge**-feltet fra arbeids-ID-en til **Blokkert**.

## <a name="initiate-a-work-split"></a>Starte en arbeidsoppdeling

Funksjonen legger til en ny **Del arbeid**-side som gjør det mulig for brukere å dele arbeidslinjer fra arbeids-ID-en. Når siden åpnes for første gang, viser den linjer som har arbeidsstatusen *Åpen* og som kan deles. I handlingsruten velger **Del arbeid** for å behandle det valgte arbeidet.

Følg denne fremgangsmåten for å dele arbeid.

1. Åpne en av følgende sider:

    - **Arbeidsdetaljer** (**Lagerstyring \> Arbeid \> Arbeidsdetaljer**)
    - **Alt arbeid** (**Lagerstyring \> Arbeid \> Alt arbeid**)

1. Velg en arbeids-ID som skal deles, i rutenettet. Feltet **Arbeidsordretype** må være satt til en av følgende verdier:

    - Salgsordre
    - Råvareplukking
    - Utstedelse for overføring

1. Velg **Del arbeid** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.

    Siden **Del arbeid** vises og viser arbeidslinjene som er åpne og som kan deles. Som standard vises bare tilgjengelige arbeidslinjer. Hvis du vil vise alle linjene for arbeids-ID-en (for eksempel linjer med arbeidstypen *Plasser*), merker du av for **Vis alle linjer** over rutenettet.

    Følgende melding vises: Brukere kan ikke behandle linjer for arbeidet før du er ferdig med oppdelingen og lukker denne siden.

    Feltet **Arbeidsblokkeringsårsak** for gjeldende arbeid vil bli satt til *Delt arbeid*, og arbeidet blir blokkert.

    ![Blokkeringsårsak.](media/Blocking_reason.png "Blokkeringsårsak")

1. Velg linjene som skal fjernes fra den gjeldende arbeids-ID-en, og legg til en ny arbeids-ID. Følgende hendelser skjer:

    - Når du deler arbeidet, annulleres de valgte linjene eller linjene fra den opprinnelige arbeids-ID-en og kopieres til en ny arbeids-ID.
    - Den eksisterende arbeidsmalstrukturen og lokasjonen til plasseringen (og også fremtidige plukk/plasser-par) beholdes. Verdiene for følgende arbeids-ID-felter kopieres fra det opprinnelige arbeidet til det nye arbeidet:

        - Last-ID
        - Forsendelses-ID
        - Arbeidsordretype
        - Ordrenummer
        - Site
        - Lager
        - Arbeidsprioritet
        - ID for arbeidsutvalg
        - Bølge-ID
        - Arbeidsopprettingsnummer

    - Følgende felter kopieres ikke til den nye arbeids-ID-en:

        - **Arbeids-ID** – En ny arbeids-ID genereres fra den riktige nummerserien.
        - **Arbeidsstatus** – Dette feltet er satt til *Åpen*.
        - **Låst av** – Dette feltet er opprinnelig satt til tomt.
        - **ID for målnummerskilt** – Dette feltet blir stående tomt.
        - **Opprettingsdato og -klokkeslett** – Dette feltet blir satt til gjeldende dato og klokkeslett.
        - **Blokkert bølge / låst** – Dette feltet omberegnes for den opprinnelige arbeids-ID-en og den nye arbeids-ID-en.

1. Velg **Del arbeid** i handlingsruten.

Mens arbeidet deles, vises følgende melding: Behandler operasjon – del arbeid. Når denne meldingen er synlig, kan du avbryte operasjonen ved å velge **Avbryt** i meldingsboksen.

Hvis avmerkingsboksen **Vis alle linjer** ikke vises, vil ikke linjen som ble oppdelt og avbrutt, lenger vises i rutenettet. Hvis avmerkingsboksen er valgt, skal du se at verdien i **Arbeidsstatus**-feltet for den linjen er endret til *Avbrutt*.

Følgende varsel vises for å angi at den nye arbeids-ID-en er opprettet: Arbeid \#\#\#\#e r opprettet ved deling av opprinnelig arbeid \#\#\#\#.

Andre arbeidslinjer fra den opprinnelige arbeids-ID-en (for eksempel *Plasser*-linjer) blir justert som påkrevd for å gjenspeile arbeidslinjene som er avbrutt. Hvis for eksempel den opprinnelige arbeids-ID-en hadde en *Plasser*-linje for et antall på 15, og *Plukk*-linjer som har et totalt antall på 10, ble avbrutt, vil det nye *plasseringsantallet* på den opprinnelige Arbeids-ID-en nå være 5.

Det nye arbeidet vil ikke umiddelbart være tilordnet til noen brukere. Du kan imidlertid tilordne det til en bruker nå, hvis det er nødvendig, ved å bruke standardfunksjonaliteten på siden **Arbeidsdetaljer**.

> [!IMPORTANT]
> Du kan bare dele arbeids-ID-er som inneholder to eller flere tilgjengelige arbeidslinjer. Hvis du velger **Del arbeid** når det bare er én arbeidslinje, vil du få følgende feilmelding: Minst én arbeidslinje må forbli på innledende arbeid. I dette tilfellet vil ingen oppdeling skje.

## <a name="finish-a-work-split"></a>Fullfør en arbeidsoppdeling

Hvis du vil fullføre deling av arbeidet, må du fjerne blokkeringsårsaken *Del arbeid*. Det er to måter å fullføre dette trinnet på:

- Brukeren som deler arbeidet, lukker siden **Del arbeid** ved å velge **Lukk**-knappen (**X**) øverst til høyre. Når siden er lukket, fjernes blokkeringsårsaken *Del arbeid*. *Blokkert*-statusen for dette arbeidet blir omberegnet, og hvis det ikke er noen gjenstående blokkeringsårsaker for dette arbeidet, oppheves blokkeringen av arbeidet.
- Alle brukere som åpner arbeids-ID-en og velger knappen **Avbryt arbeidsoppdelingsøkt** i handlingsruten. Blokkeringsårsaken *Del arbeid* blir fjernet, og *Blokkert*-statusen for dette arbeidet blir omberegnet, akkurat som når siden **Del arbeid** lukkes.

Når blokkeringsårsaken *Delt arbeid* er fjernet, kan arbeidet kjøres på mobilenheten, forutsatt at statusen **Blokkert** er satt til *Nei* på arbeids-ID-en.

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a>Brukerblokkering i mobilappen Lagerstyring

Hvis du prøver å bruke mobilappen Lagerstyring til å kjøre plukkarbeid mot en arbeids-ID som deles, får du følgende feilmelding: Arbeidet med ID \#\#\#\# deles for øyeblikket. Hvis du får denne meldingen, velger du **Avbryt**. Deretter kan du fortsette å behandle annet arbeid.

## <a name="other-blocked-operations"></a>Andre blokkerte operasjoner

Alle operasjoner som endrer arbeidslinjer, arbeidslagertransaksjoner eller etterfyllingskoblinger som er relatert til arbeid som deles, vil mislykkes, og følgende feilmelding vises: Arbeidet med ID \#\#\#\# deles nå.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]