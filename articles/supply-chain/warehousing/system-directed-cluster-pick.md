---
title: Systemstyrt gruppeplukking
description: Dette emnet gir en oversikt over systemstyrt gruppeplukking i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b7ac243a04309a41ab0e06c1b2d4843ae8ac0e22
ms.sourcegitcommit: 7c32e4739c07d825a8562564ea9e78922db2ce38
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406387"
---
# <a name="system-directed-cluster-picking"></a>Systemstyrt gruppeplukking

[!include [banner](../includes/banner.md)]

Gruppeplukking er en stykkplukkingsprosess som lar deg plukke varer for flere ordrer samtidig ved å gruppere dem i plukkgrupper. Du må da gå til plukkstedet bare én gang. Denne funksjonaliteten brukes vanligvis med små ordreplukking eller antall som er mindre enn små kvanta.

Når systemstyrt gruppeplukking er definert, kan du gruppeplukke arbeidshoder, basert på en systemgenerert gruppe. Systemet gruppeplukker ordrer opp til antall stillinger som er angitt i gruppeprofilen. Derfor kan du plukke flere ordrer samtidig uten å måtte opprette en gruppe manuelt.

Systemstyrt gruppeplukking tilbyr et alternativ til manuell gruppebygging, der en gruppeprofil brukes til å opprette en gruppe. Flere oppsettsrelaterte linjer må defineres i gruppeprofilen før den brukes:

- **Antall stillinger** tilsvarer antall ordrer som skal plasseres i en gruppe. Derfor tilsvarer det antall seff.
- **Bryt gruppe** bestemmer når gruppen skal brytes.
- **Generer gruppe-ID** kontrollerer om gruppe-IDen skal genereres av systemet eller angis av brukeren.
- **Sorteringsbekreftelsestype** avgjør om posisjonsverifisering er nødvendig.

Et nytt menyelement for mobilenhet brukes til systemstyrt gruppeplukking. **Gruppeprofil-ID-en** må angis for det valgte **Styrt av**-alternativet. I tillegg kan de systemstyrte spørringene om arbeidssekvens gruppere ordrer basert på firmaspesifikke kriterier. Derfor kan du ytterligere optimalisere tildelingen av arbeidsordrer ved å angi tilpassede sorteringskriterier ved hjelp av en systemstyrte spørringene om arbeidssekvens.

Når systemstyrt gruppeplukking aktiveres, presenteres lagerarbeidere med en gruppe der plukkordrer er forhåndstildelte til gruppestillinger. Arbeidere kan derfor begynne å plukke en vare for flere arbeidsordrer ved å gå til plukkstedet bare én gang. Plukkprosessen for systemstyrt gruppeplukking er den samme som prosessen for brukerstyrt gruppeplukking.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Aktivere funksjonen for systemstyrt gruppeplukking

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke siden for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. Her vises funksjonen som:

- **Modul** – lagerstyring
- **Funksjonsnavn** – systemstyrt gruppeplukking

Denne funksjonen krever også aktivering av en avhengig funksjon. Den avhengige funksjonen er:

- **Modul** – lagerstyring
- **Funksjonsnavn** – systemstyrt arbeidssekvensering i hele organisasjonen

## <a name="set-up-system-directed-cluster-picking"></a>Konfigurere systemstyrt gruppeplukking

### <a name="create-cluster-profiles"></a>Opprette gruppeprofiler

Gruppeprofiler kontrollerer hvordan systemet oppretter hver gruppe. Hvis det kreves forskjellige grupper, bør det opprettes en annen gruppeprofil for hvert menyelement for mobilenhet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.
2. Velg **Ny**.
3. Angi **2 posisjon** i **Gruppeprofil-ID**-feltet.
4. Angi **2 posisjon** i **Navn**-feltet.
5. På **Generelt**-hurtigfanen angir du informasjonen nedenfor:

    - **Generer gruppe-ID** – velg **Ja**. Dette alternativet bestemmer om gruppe-IDen opprettes automatisk av systemet, eller om brukeren skal opprette den på begynnelsen av plukkingen. 
    - **Aktiver stillinger** – velg **Ja**. Dette alternativet bestemmer om stillingsnavnene genereres automatisk basert på oppsettet for stillingsnavnet. Hvis dette alternativet settes til **Nei**, brukes nummerskilt-ID-en for stillingen.
    - **Maksimalt antall stillinger** – velg **2**. Dette feltet fastsetter det maksimale antallet stillinger som gruppen kan ha (det vil si maksimalt antall esker, seff og så videre).
    - **Stillingsnavn** – velg **Numerisk** slik at stillingene navngis ved hjelp av kontinuerlige tall. Hvis du velger **Alfabetisk**, navngis stillingene i alfabetisk rekkefølge.
    - **Bryt opp gruppe ved** – velg **Plasser**. Dette feltet bestemmer når gruppen brytes. 
    - **Sorteringsbekreftelsestype** – velg **Posisjonsskanning**. Dette feltet angir om plasser-til-stilling-trinnet er bekreftet.
        
6. På hurtigfanen **Gruppesortering** kan du definere sorteringskriterier ved å opprette en ny linje og angi følgende informasjon:

    - **Sekvensnummer** – velg **1**. Dette feltet bestemmer rekkefølgen systemet sorterer etter. En verdi angis automatisk, men du kan endre den etter behov.
    - **Feltnavn** – angi **WMSLocationId**. Dette feltet bestemmer feltet som linjen bruker til sorteringskriterier.
    - **Sortering** – velg **Stigende**. Dette feltet angir om sorteringen utføres i stigende eller synkende rekkefølge.

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

Hvis du vil opprette et nytt menyelement for mobilenhet for systemstyrt gruppeplukking og koble gruppeprofil-IDen til menyelementet for mobilenhet, følger du denne fremgangsmåten.

1. Gå til **Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten**.
1. Velg **Ny**.
1. Angi følgende informasjon i overskriftdelen:
    - **Menyelementnavn** – SD-gruppe
    - **Tittel** – SD-gruppe
    - **Modus** – Arbeid
    - **Bruke eksisterende arbeid** – Ja

1. På **Generelt**-hurtigfanen angir du informasjonen nedenfor:
    - **Styrt av** – Systemstyrt gruppeplukking
    - **Generer nummerskilt** – Ja
    - **Gruppeprofil-ID** – 2. posisjon

1. I hurtigfanen **Arbeidsklasser** konfigurerer du den gyldige arbeidsklassen for dette menyelementet for mobilenhet ved å angi følgende felt:
    - **Arbeidsklasse-ID** – Salg
    - **Arbeidsordretype** – Salgsordrer

1. I **Menyelementer på mobilenheten**-handlingsruten velger du **Systemstyrte spørringer om arbeidssekvens**, og følger denne fremgangsmåten for å angi en ny systemstyrt arbeidssekvensspørring:
    - Velg **Ny** i handlingsruten.
    - **Sekvensnummer** – 1
    - **Beskrivelse** – Arbeidsprioritet – Arbeids-ID

1. I handlingsruten velger du **Rediger spørring**
1. Velg kategorien **Sortering**
1. Velg **Legg til** for å legge til en ny linje, og angi deretter følgende:
    - **Tabell** – Arbeid
    - **Avledet tabell** – Arbeid
    - **Felt** – Arbeidsprioritet
    - **Søkeretning** – Stigende
1. Velg **Legg til** for å legge til en ekstra linje, og angi deretter følgende:
    - **Tabell** – Arbeid
    - **Avledet tabell** – Arbeid
    - **Felt** – Arbeids-ID
    - **Søkeretning** – Stigende

1. Systemet vil nå sortere arbeids-IDer i gruppen, først etter arbeidsprioritet og deretter etter arbeids-ID.

### <a name="set-up-a-mobile-device-menu"></a>Definere en mobilenhetsmeny

1. Gå til **Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.
1. Legg til menyelementet for **SD-gruppen** som du nettopp opprettet i en mobilenhetsmeny.
1. Velg **Utgående**-menyen.
1. Velg **Rediger** i handlingsruten.
1. Bla til du finner **SD-gruppe**.
1. Velg **SD-gruppe**, så aktiveres pilen som peker til **Menystruktur**-listen.
1. Velg **pil**-knappen for å flytte **SD-gruppe**-menyelementet til **Utgående**-menystrukturen.
1. Velg **SD-gruppe** fra **Menystruktur**-listen, og velg deretter pil **OPP** eller **NED** for å flytte menyelementet til ønsket plassering på mobilenhetsmenyen.

## <a name="scenario"></a>Scenario

### <a name="create-picking-work"></a>Opprett plukkarbeid

Før du kan definere systemstyrt gruppeplukking, må du opprette kvalifisert utgående arbeid. Gruppeprofilen du opprettet tidligere, angir to gruppestillinger. Derfor må du opprette minst to arbeids-IDer. I dette scenariet skal du opprette to salgsordrer, reserverebeholdning, frigi salgsordrene til lageret, og deretter behandle bølgen manuelt.

1. Gå til **Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
1. Velg **Ny** i handlingsruten for å opprette den første salgsordren.
    - I **Opprett salgsordre**-menyen som åpnes, angir du følgende informasjon:
        - I **Kunde**-hurtigkategorien angir du **Kundekonto** - **US-004**.
        - I **Generelt**-hurtigkategorien angir du **Lager** - **62**.
        - Velg **OK** for å lukke menyen og opprette salgsordren.
    - I **Salgsordrelinjer**-hurtigkategorien velger du **Legg til linje** dersom en ny linje ikke automatisk legges til, og deretter angir du følgende:
        - **Varenummer** – A0001
        - **Antall** – 1
        - Velg **Legg til linje** for å legge til en ny linje.
        - **Varenummer** – A0002
        - **Antall** – 3
    - Reserver beholdning for begge linjene du nettopp opprettet.
        - Velg **Linje 1**.
        - På **Salgsordrelinjer**-handlingsruten velger du **Beholdning** og deretter **Reservasjon** fra listen.
        - I **Reservasjon**-skjemaet velger du **Reserver parti** for å reservere beholdningen.
        - Lukk **Reservasjon**-skjemaet når reservasjonen er fullført.
        - Gjenta disse trinnene for å reservere beholdning for **Linje 2**.
1. Velg **Ny** i handlingsruten for å opprette den andre salgsordren
    - I **Opprett salgsordre**-menyen som åpnes, angir du følgende informasjon:
        - I **Kunde**-hurtigkategorien angir du **Kundekonto** - **US-005**.
        - I **Generelt**-hurtigkategorien angir du **Lager** - **62**.
        - Velg **OK** for å lukke menyen og opprette salgsordren
    - I **Salgsordrelinjer**-hurtigkategorien velger du **Legg til linje** dersom en ny linje ikke automatisk legges til, og deretter angir du følgende informasjon:
        - **Varenummer** – A0001
        - **Antall** – 4
        - Velg **Legg til linje** for å legge til en ny linje.
        - **Varenummer** – A0002
        - **Antall** – 2
    - Reserver beholdning for begge linjene du nettopp opprettet.
        - Velg **Linje 1**.
        - På **Salgsordrelinjer**-handlingsruten velger du **Beholdning** og deretter **Reservasjon** fra listen.
        - I **Reservasjon**-skjemaet velger du **Reserver parti** for å reservere beholdningen.
        - Lukk **Reservasjon**-skjemaet når reservasjonen er fullført.
        - Gjenta disse trinnene for å reservere beholdning for **Linje 2**.
    - Lukk salgsordren og gå tilbake til **Alle salgsordrer**-listesiden.
1. Finn de to salgsordrene du nettopp opprettet (du må kanskje oppdatere siden). I tabellen velger du begge salgsordrene ved hjelp av avkrysningsmerket for delen.
    - I **Alle salgsordre**-hurtigkategorien velger du **Lager**-fanen.
    - I **Handlinger**-gruppen velger du **Frigi til lager** for å frigi begge salgsordrene til lageret.
1. Når prosessen med å frigi til lager er fullført, vises en infomelding.
    - Forsendelser blir opprettet for hver salgsordre.
    - Det opprettes en bølge, og begge forsendelsene tilordnes til bølgen. Noter **bølge-ID-en**.
1. Gå til **Lagerstyring > Utgående bølger > Forsendelsesbølger > Alle bølger**.
    - I **Alle bølger**-listen finner og velger du **bølge-ID-en** du opprettet i det forrige trinnet.
    - Velg **Bølge**-kategorien i handlingsruten.
    - I **Bølge**-gruppen velger du **Behandle** for å prosessere bølgen og opprette **Arbeid**.
    - Informasjonsmeldinger blir generert når behandlingen er fullført, og angir at arbeidet er opprettet og at bølgen er postert.
1. **Valgfritt**: Gå til **Lagerstyring > Arbeid > Arbeidsdetaljer** for å se arbeidet som ble opprettet. To forskjellige arbeids-IDer opprettes. Hver arbeids-ID har to plukklinjer.

### <a name="run-the-mobile-device-flow"></a>Kjør flyten for mobilenhet

1. Logg på mobilenheten for en bruker i lageret **62**.
1. I **hovedmenyen** velger du **Utgående**.
1. På **Utgående**-menyen velger du **SD-gruppe** for å iverksette plukkingen.
    - Det opprettes en gruppe, og de to arbeids-ID-ene som du opprettet tidligere, er tilknyttet. Hvis du har opprettet mer enn to arbeids-IDer, legges bare de to første til i gruppen. Legg merke til at arbeids-IDene legges til gruppen i stigende rekkefølge, som du angav i spørringsoppsettet.

    > [!NOTE]
    > Den nye gruppen opprettes automatisk bare hvis nok ekstra arbeids-IDer ble opprettet tidligere. Ellers vises følgende melding: "Finner ikke nok arbeid for gruppen."

    - Når du har valgt menyen, vises det første plukkskjermbildet. Systemet samler alle samsvarende plukklinjer fra de to arbeids-IDene, og dirigerer deg til å gå til plukkstedet én gang, slik at du kan oppfylle begge ordrene ved hjelp av én plukking. Denne prosessen utføres på samme måte som prosess for brukerstyrt gruppeplukking.

1. Bekreft den første plukkelokasjonen og varen ved å velge **OK**.
    - Antallet i plukkingen blir totalantallet for varen som vises i salgsordrene i gruppen.
1. Angi posisjonsnavnet (numerisk eller alfabetisk) for å bekrefte at vareantallet som ble plukket for posisjonen, ble satt i riktig posisjon.
1. Gjenta denne prosessen til alle vareantallene er plukket og satt til riktig posisjon.
1. Det siste trinnet på mobilenheten er å **Plassere** gruppen i den endelige plasseringen. Velg **OK**
    - Når plasseringsoperasjonen er bekreftet, lukkes og brytes gruppen, basert på verdien som du angir for **Pausegruppe ved** -feltet i gruppeprofilen. Arbeids-IDer lukkes også.
1. En "Gruppe fullført"-melding vises på mobilenheten.
