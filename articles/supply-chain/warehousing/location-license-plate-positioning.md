---
title: Nummerskiltposisjonering for lokasjon
description: Ved å plassering av nummerskiltlokasjon kan du se hvor et nummerskilt befinner seg på en lokasjon med flere paller, for eksempel en lokasjon som bruker pallestabling med dobbel dybde.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cfab8c36adb08f799305a153589926bfc1ae31fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217107"
---
# <a name="location-license-plate-positioning"></a>Nummerskiltposisjonering for lokasjon

[!include [banner](../includes/banner.md)]

Ved å plassering av nummerskiltlokasjon kan du se hvor et nummerskilt befinner seg på en lokasjon med flere paller, for eksempel en lokasjon som bruker pallestabling med dobbel dybde.

Funksjonen legger til et sekvensnummer for hvert nummerskilt som settes inn i en lagerlokasjon. Dette sekvensnummeret brukes til å bestille nummerskilt i lagerlokasjonen. Derfor støtter funksjonen intelligente scenarioer der kunder bruker et gravitasjonssporingssystem, og må kjenne til, for plukkfomål, hvilket nummerskilt som er vendt forover.

Dette emnet inneholder et scenario som viser hvordan du definerer og bruker funksjonen.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Aktiver Nummerskiltplassering på lokasjon-funksjonen

Før du kan bruke plassering av nummerskiltlokasjon, må funksjonen aktiveres i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Nummerskiltplassering på lokasjon*

## <a name="example-scenario"></a>Eksempelscenario

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke verdiene som foreslås her, må du arbeide på et system der standard eksempeldata er installert. Du må også velge den juridiske enheten **USMF** før du starter.

### <a name="set-up-the-feature-for-this-scenario"></a>Konfigurer funksjonen for dette scenariet

Fullfør fremgangsmåtene nedenfor for å konfigurere *Nummerskiltplassering på lokasjon*-funksjonen for scenariet som presenteres i dette emnet.

#### <a name="location-profiles"></a>Lokasjonsprofiler

Funksjonen må aktiveres i lokasjonsprofilen for hver lokasjon den skal brukes på.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. I listen over lokasjonsprofiler i venstre rute velger du **BULK-06**.
1. På **Generelt**-hurtigfanen er det lagt til to nye alternativer av denne funksjonen. Angi følgende verdier:

    - **Aktiver plassering av nummerskilt:** *Ja*

        Når dette alternativet er satt til *Ja*, opprettholdes nummerskiltplasseringen for nummerskilt på lokasjonen.

    - **Vis LP-plassering for mobil enhet:** *Ja*

        Når dette alternativet er angitt til *Ja*, vises nummerskiltplasseringen for brukere av mobil enhet under justering og opptelling. Du kan endre innstillingen for dette alternativet bare når funksjonen er aktivert.

1. Velg **Lagre**.

#### <a name="location-directives"></a>Lokasjonsdirektiver

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten kontrollerer du at **Arbeidsordretype**-feltet er satt til *Salgsordrer*.
1. I listen over lokasjonsdirektiver velger du **61 SO plukkordre**.
1. I handlingsruten velger du **Rediger**.
1. På **Linjer**-hurtigfanen velger du linjen som har en verdi for **sekvensnummer** på *2*.
1. På **Lokasjonsdirektivhandlinger**-hurtigfanen velger du linjen som har **Navn**-verdien *Plukk for mindre enn pall* (det skal være den eneste linjen), og endrer verdien for **sekvensnummer** til *2*.
1. Velg **Ny** ovenfor rutenettet for å legge til en linje for en ny handling for lokasjonsdirektiv.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** *1*
    - **Navn:** *Plukkplassering 1*

1. Mens den nye linjen fremdeles er valgt, velger du **Rediger spørring** over rutenettet.
1. I redigeringsprogrammet for spørringer velger du **Sammenkoblinger**-fanen.
1. Utvid **Lokasjoner**-tabellsammenkoblingen for å vise sammenkoblingen til **Lagerdimensjoner**-tabellen.
1. Utvid **Lagerdimensjoner**-tabellsammenkoblingen for å vise sammenkoblingen til **Lagerbeholdning**-tabellen.
1. Velg **Lagerdimensjoner** og velg deretter **Legg til tabellsammenkobling**.
1. I listen over tabeller som vises i **Relasjon**-kolonnen, velger du **Nummerskilt (nummerskilt)**. Velg deretter **Velg** for å legge til **Nummerskilt** i **Lagerdimensjoner**-tabellsammenkoblingen.
1. Mens **Nummerskilt** fremdeles er valgt, velger du **Legg til tabellsammenkobling**.
1. I listen over tabeller som vises i **Relasjon**-kolonnen, velger du **Nummerskiltplassering på lokasjon (nummerskilt)**. Velg deretter **Velg** for å legge til **Nummerskiltplassering på lokasjon** i **Lagerdimensjoner**-tabellsammekoblingen.

    ![Tabellsammenkoblinger](media/LpTableJoin.png "Tabellsammenkoblinger")

1. Velg **OK** for å bekrefte de oppdaterte, sammenkoblede tabellene og lukke redigeringsprogrammet for spørring.
1. I hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Rediger spørring** på nytt for å åpne dialogboksen for redigeringsprogram for spørring igjen.
1. På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Nummerskiltplassering på lokasjon*
    - **Avledet tabell:** *Nummerskiltplassering på lokasjon*
    - **Felt:** *LP-plassering*
    - **Kriterier:** *1*

    ![Nytt område](media/LpPositionCriteria.png "Nytt område")

1. Velg **OK** for å bekrefte endringene og lukke redigeringsprogrammet for spørring.

### <a name="set-up-sample-data-for-this-scenario"></a>Konfigurer eksempeldata for dette scenariet

For dette scenariet må brukeren logge seg på lagermobilappen ved hjelp av en arbeider som er satt opp for lager *61* for å utføre arbeid. Brukeren må også fullføre transaksjoner.

Siden *Nummerskiltplassering på lokasjon*-funksjonen legger til en ny identifikator for plassering av nummerskilt på en lokasjon, må du først opprette noen data for å støtte scenariet.

#### <a name="spot-count-the-first-location"></a>Spottelling på første lokasjon

1. Åpne lagermobilappen og logg på lager *61*.
1. Gå til **Beholdning \> Spottelling**.
1. På **Spottelling**-siden setter du **Lokasjon**-feltet til *01A01R1S1B*.
1. Velg **OK**.

    Siden viser lokasjonen du har angitt. Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"

1. Velg **Oppdater** for å legge til en telling på lokasjonen.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0001*.
1. Velg **OK**.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1001* (eller et annet skiltnummer).

    **Syklustelling: Legg til ny LP eller vare**-siden viser **Nummerskiltplassering 1**.

1. Velg **OK**.

    Du må nå angi antallet for varen som telles på nummerskiltet.

1. Angi **Antall**-feltet til *10*.
1. Velg **OK**.

    Siden viser lokasjonen du har angitt. Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"

1. Velg **Oppdater** for å legge til en ny telling på lokasjonen.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0002*.
1. Velg **OK**.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1002* (eller eventuelle andre skiltnumre du velger, forutsatt at det er forskjellig fra skiltnummeret du angav tidligere).
1. Endre nummerskiltplasseringen ved å sette feltet **LP-plassering** til *2*.
1. Velg **OK**.
1. Angi antallet av varen som telles, på nummerskiltet ved å sette **Antall**-feltet til *10*.
1. Velg **OK**.

    Siden viser lokasjonen du har angitt. Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"

1. Velg **OK**.

Arbeidet er nå fullført.

#### <a name="spot-count-the-second-location"></a>Spottelling på andre lokasjon

1. På **Spottelling**-siden setter du **Lokasjon**-feltet til *01A01R1S2B*.
1. Velg **OK**.

    Siden viser lokasjonen du har angitt. Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"

1. Velg **Oppdater** for å legge til en telling på lokasjonen.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0002*.
1. Velg **OK**.
1. På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1003* (eller eventuelle andre skiltnumre du velger, forutsatt at det er forskjellig fra begge skiltnumrene du angav i den forrige prosedyren).

    **Syklustelling: Legg til ny LP eller vare**-siden viser **Nummerskiltplassering 1**.

1. Velg **OK**.
1. Angi antallet av varen som telles, på nummerskiltet ved å sette **Antall**-feltet til *10*.
1. Velg **OK**.

    Siden viser lokasjonen du har angitt. Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"

1. Velg **OK**.

Arbeidet er nå fullført.

#### <a name="work-details"></a>Arbeidsdetaljer

> [!NOTE]
> Spottellinger fra den mobile appen syklustellingsarbeid i Microsoft Dynamics 365. Arbeidet krever at tellingene godtas før de posteres til beholdningen.

1. Logg på Dynamics 365 Supply Chain Management.
1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. I **Oversikt**-fanen kan du se etter linjene som har følgende verdier:

    - **Arbeidsordretype:** *Syklustelling*
    - **Lager:** *61*
    - **Arbeidsstatus:** *Venter på gjennomgang*

    To arbeids-ID-er skal ha blitt opprettet for disse linjene. Tellingene for begge disse arbeids-ID-ene må godtas.

1. I rutenettet velger du den første arbeids-ID-en for *Syklustelling*-arbeidsordretypen.
1. Velg **Syklustelling** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.

    To linjer vises, én for hver vare og hvert nummerskilt. Verdiene i feltene **Opptalt antall**, **Lokasjon**, **Nummerskilt** og **Vare** må være i samsvar med opptellingsoppføringene du opprettet på den mobile enheten. Hvis noen av disse feltene ikke er synlige, velger du **Vis dimensjoner** i handlingsruten for å legge dem til i rutenettet.

1. Velg begge linjene.
1. Klikk på **Godta telling** i handlingsruten.
1. Du får meldingen Postering – journal. Velg **Meldingsdetaljer** for å vise det posterte journalnummeret.
1. Lukk meldingsdetaljene.
1. Oppdater **Arbeid**-siden.

    Den første arbeids-ID-en er lukket og vises ikke lenger.

    > [!TIP]
    > Hvis du vil vise lukket arbeid, merker du av for **Vis lukket** over rutenettet.

    Du vil nå godta arbeidet for nummerskiltet i *01A01R1S2B*-lokasjonen.

1. I rutenettet velger du den andre arbeids-ID-en for *Syklustelling*-arbeidsordretypen på **Oversikt**-fanen.
1. Velg **Syklustelling** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.

    Det vises en linje for varen og nummerskiltet. Verdiene i feltene **Opptalt antall**, **Lokasjon**, **Nummerskilt** og **Vare** må være i samsvar med opptellingsoppføringene du opprettet på den mobile enheten.

1. Velg linjen.
1. Klikk på **Godta telling** i handlingsruten.
1. Du får meldingen Postering – journal. Velg **Meldingsdetaljer** for å vise det posterte journalnummeret.
1. Lukk meldingsdetaljene.
1. Oppdater **Arbeid**-siden.

    Den andre arbeids-ID-en er lukket og vises ikke lenger.

    > [!TIP]
    > Hvis du vil vise lukket arbeid, merker du av for **Vis lukket** over rutenettet.

#### <a name="on-hand-by-location"></a>Beholdning etter lokasjon

1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdning etter lokasjon**.
1. Angi følgende verdier:

    - **Område:** *6*
    - **Lager:** *61*
    - **Oppdater på tvers av lokasjoner:** *Ja*

1. Merk at lokasjonen *01A01R1S1B* har to nummerskilt:

    - **A0001**, der **LP-posisjon**-feltet er satt til *1*
    - **A0002**, der **LP-posisjon**-feltet er satt til *2*

1. Merk at lokasjonen *01A01R1S2B* har ett nummerskilt:

    - **A0002**, der **LP-posisjon**-feltet er satt til *1*

### <a name="sales-order-scenario"></a>Salgsordrescenario

Nå når funksjonen *Nummerskiltplassering på lokasjon* er konfigurert, og beholdningen er klargjort, må du opprette en salgsordre for å generere plukking av arbeid som vil styre lagerarbeideren for å plukke vare *A0002* fra lagerlokasjonen der pall-ID-en er i posisjon *1*.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-004*
    - **Lager:** *61*

1. Velg **OK**.
1. Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. På denne nye linjen angir du følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *1*

1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere beholdning for ordrelinjen.
1. Lukk **Reservasjon**-siden.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.

    Du mottar en informasjonsmelding som viser bølge-ID og forsendelses-ID-er som er opprettet for ordren.

1. I **Salgsordrelinjer**-hurtigfanen, på **Lager**-menyen over rutenettet, velger du **Arbeidsdetaljer**.
1. **Arbeid**-siden vises og viser arbeidet som ble opprettet for salgslinjen. Noter deg arbeids-ID-en som vises.

### <a name="sales-picking-scenario"></a>Salgsplukkscenario

1. Åpne mobilappen og logg på lager *61*.
1. Gå til **Utgående \> Salgsplukking**.
1. På **Skann en arbeids-ID/nummerskilt-ID**-siden velger du **ID**-feltet og angir deretter arbeids-ID-en fra salgslinjen.
1. Legg merke til at plukkarbeidet leder deg til å plukke vare *A0002* fra lokasjon *01A01R1S2B*. Du får denne instruksjonen fordi vare *A0002* er på et nummerskilt som er på plassering *1* på den lokasjonen.

    ![Plassering 1-lokasjon](media/LocationLicensePlatePositioning.png "Plassering 1-lokasjon")

1. Angi nummerskilt-ID-en du opprettet for lokasjonen, og følg deretter instruksjonene for å velge salgsordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]