---
title: Eksempelscenarier for syklustelling
description: Denne artikkelen inneholder en samling scenarier som utforsker funksjonene for syklustelling i Microsoft Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 91a18b6deade6d67fce6b90308671910a4196104
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335743"
---
# <a name="cycle-counting-example-scenarios"></a>Eksempelscenarier for syklustelling

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder en samling scenarier som utforsker funksjonene for syklustelling i Microsoft Dynamics 365 Supply Chain Management. Den beskriver først kravene for ditt eksisterende Supply Chain Management-miljø. Deretter forklarer den hvordan du konfigurerer syklustelling og beskriver alle syklustellingsstadiene. Når du er ferdig, har du en god forståelse av syklustelling, inkludert veiledet syklustelling, blind syklustelling, spotsyklustelling, syklustellingsterskler og syklustellingsplaner.

## <a name="prerequisites"></a>Forutsetninger

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Hvert scenario i denne artikkelen refererer til verdier og poster som er inkludert i standard demodata som leveres for Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du går gjennom scenarioene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten (firma) til **USMF** før du begynner.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Aktivere støtte for mobilappen Warehouse Management

Du må aktivere funksjonen *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen* for systemet for å kunne bruke mobilappen Warehouse Management. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Klargjøre demodata for scenariene

Følg disse trinnene for å bekrefte at alle demodata som kreves for scenariene, er tilgjengelige i USMF-firmaet i systemet. Opprett eventuelle poster eller verdier som mangler.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. Velg **Julia Funderburk** i listeruten.
1. På hurtigfanen **Brukere** velger du raden som har følgende verdier. Hvis ingen eksisterende rad har disse verdiene, oppretter du den.

    - **Bruker-ID:** *61*
    - **Brukernavn:** *WH61*
    - **Standardlager:** *61*
    - **Menynavn:** *Hoved*

1. På hurtigfanen **Arbeid** angir du følgende verdier for bruker *61* hvis de ikke allerede er angitt:

    - **Er en syklustellingsansvarlig** *Nei*
    - **Grense for største prosent:** *0*
    - **Grense for største antall:** *0*
    - **Grense for største verdi:** *0*

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsutvalg**.
1. Arbeidsutvalg brukes til å skille lagerarbeidet basert på typen arbeid (i dette tilfellet syklusopptellingsarbeid). Kontroller at det finnes en post som har følgende innstillinger:

    - **ID for arbeidsutvalg:** *CycleCount*
    - **Beskrivelse:** *Syklustelling*

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg posten som heter *Syklustelling*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft eller angi følgende verdier for posten:

    - **Navn på menyelementet:** *Syklustelling*
    - **Tittel:** *Syklustelling-ledet*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*
    - **Styrt av:** *Systemstyrt* (Denne verdien angir at Supply Chain Management vil tilordne en arbeids-ID for syklusopptelling til arbeideren.)
    - **Vis beholdningsstatus:** *Ja*

1. Klikk på **Syklustelling** i handlingsruten.
1. Bekreft eller angi følgende verdier i dialogboksen **Syklustelling for mobilenhet**:

    - **Vis varenummer:** *Ja*
    - **Vis nummerskilt:** *Ja*
    - **Antall forsøk:** *1*

1. Velg **OK** for å lukke dialogboksen.
1. Velg posten som heter *Blind syklustelling*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft eller angi følgende verdier for posten:

    - **Navn på menyelementet:** *Blind syklustelling*
    - **Tittel:** *Blind syklustelling*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*
    - **Styrt av** *Gruppering av syklustelling* – (Denne verdien angir at arbeideren kan gruppere ID-er for syklustellingsarbeid som er spesifikke for en bestemt lokasjon, sone eller arbeidspulje.)

1. Klikk på **Syklustelling** i handlingsruten.
1. Bekreft eller angi følgende verdier i dialogboksen **Syklustelling for mobilenhet**:

    - **Vis varenummer:** *Nei*
    - **Vis nummerskilt:** *Nei*
    - **Antall forsøk:** *0*

1. Velg **OK** for å lukke dialogboksen.
1. Velg posten som heter *Spottelling*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft eller angi følgende verdier for posten:

    - **Menyelementnavn:** *Spottelling*
    - **Tittel:** *Spottelling*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Nei*
    - **Arbeidsopprettelsesprosess:** *Spotsyklustelling* (Denne verdien angir at arbeideren kan telle varer på en lagerlokasjon når som helst, uten å opprette syklustellingsarbeid. For å utføre spotsyklustelling på en lokasjon, må arbeideren angi steds-ID.)

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg posten som heter *Lager*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft at følgende menyelementer for syklusopptelling vises i **Menystruktur**-kolonnen:

    - Syklustelling
    - Blind syklustelling
    - Spottelling

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. Angi følgende verdier i fanen **Syklustelling**:

    - **Standard type syklusopptellingsjustering:** *Syklustelling* (Dette feltet angir journaltypen som posteres når syklusopptelling er utført.)
    - **Standard arbeidsklasse-ID for syklusopptelling:** *CCount* (Dette feltet angir arbeidsklassen som brukes til syklustelling.)
    - **Standard arbeidsprioritet for syklustelling** *50* (Dette feltet angir prioriteten som syklustellingsarbeid har i forhold til andre typer arbeid på lageret. Ved å skrive inn et tall som er lavere enn tallet som angis for andre typer arbeid, kan du øke prioriteten for syklustellingsarbeidet.)

1. Gå til **Warehouse Management \> Oppsett \> Lager \> Justeringstyper**.
1. På **Justeringstyper**-siden kan du opprette koder for forskjellige inn- og utjusteringer som kan forekomme. Bekreft at det finnes en post som har følgende innstillinger:

    - **Lagerjusteringstype:** *Syklustelling*
    - **Beskrivelse:** *Syklustelling*
    - **Navn:** *ICnt*

1. Gå til **Warehouse Management \> Oppsett \> Lageroppsett \> Lagre**.
1. I listen velger du lager *61*. Hvis ingen eksisterende poster har dette navnet, oppretter du det.
1. Angi følgende verdier i hurtigfanen **Lager**:

    - **Bruk Warehouse Management-prosess:** *Ja* (Denne verdien aktiverer lageret for Warehouse Management-prosesser (WMS).)
    - **Tillat at nummerskilt flyttes under syklustelling:** *Ja* (Denne verdien gjør det mulig for ansatte å flytte nummerskilt under en syklustelling.)

## <a name="scenario-1-guided-cycle-counting"></a>Scenario 1: Veiledet syklustelling

Før veiledet syklustelling kan forekomme, må du opprette arbeid. Dette arbeidet fører den tilordnede personen gjennom lageret, fra lokasjon til lokasjon, for å fullføre opptellingene som er satt opp i arbeidet.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Opprette syklustellingsarbeid for scenario 1

Følg denne fremgangsmåten når du skal opprette syklustellingsarbeid for varelokasjon *01A02R2S2B* (BULK-06) i lager *61*.

1. Gå til **Warehouse Management \> Syklustelling \> Syklustellingsarbeid etter lokasjon**.
1. I dialogboksen **Opprett syklustellingsarbeid etter lokasjon** angir du feltet **Arbeidspulje-ID** til *CycleCount*.
1. Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .
1. I dialogboksen for Power Query-redigering i fanen **Område** følger du disse trinnene:

    - For raden der **Felt**-feltet er satt til *Lager*, setter du **Kriterier**-feltet til *61*.
    - For raden der **Felt**-feltet er satt til *Lokasjon*, setter du **Kriterier**-feltet til *01A02R2S2B*.

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. Velg **OK** for å lukke dialogboksen **Opprett syklustellingsarbeid etter lokasjon**.

    Når arbeidsopprettingsprosessen er fullført, vises en melding i handlingssenteret.

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Finn det nyopprettede arbeidet ved å sette et filter i kolonnen **Arbeidspulje-ID** for å finne poster som har verdien *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Utføre syklustellingsarbeid for scenario 1

Når du har opprettet syklustellingsarbeid, utfører du arbeidet ved å telle varene på en lagerlokasjon, og deretter bruker du en mobilenhet til å angi resultatene i Supply Chain Management. Følg denne fremgangsmåten for å bruke syklusopptellingsarbeid i mobilappen Warehouse Management.

1. Logg deg på mobilappen Warehouse Management som arbeidsbrukeren du konfigurerte i delen [Klargjøre demodata for scenarier](#prepare-demo-data) tidligere i denne artikkelen. For eksempel i denne artikkelen heter brukeren *Julia Funderburk* og er definert for lager *61*. (USMF-demodataene bør la deg logge deg på som denne arbeidsbrukeren ved å angi *61* som bruker-ID og *1* som passord.)
1. I hovedmenyen velger du **Lager**.
1. Velg **Veiledet syklustelling** på **Lager**-menyen.
1. Velg **Antall**-feltet, angi *9* ved å bruke talltastaturet, og velg deretter **OK** (hakesymbolknappen).
1. Systemet forventer at du skal angi en telling på 10 stykker for denne varen, lokasjonen og nummerskiltet. Derfor blir du bedt om å utføre opptelling på nytt. Velg **Antall**-feltet, angi *9* på nytt ved å bruke talltastaturet, og velg deretter **OK** (hakesymbolknappen). I det andre forsøket blir opptellingen godtatt.

    > [!NOTE]
    > Da systemet oppdaget en forskjell mellom den forventede lagerbeholdningen og antallet du angav, ble du bedt om å telle en ny gang, fordi feltet for **Antall forsøk** er satt til *1* for menyelementet **Veiledet syklustelling** for mobilenhet. Du ble veiledet til et bestemt varenummer og skiltnummer fordi både alternativet **Vis varenummer** og alternativet **Vis nummerskilt** er angitt til *Ja* for menyelementet for mobilenhet.

1. Velg **OK** (hakesymbolknappen).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Gå gjennom syklusopptellingsdifferansene for scenario 1

Følg denne fremgangsmåten for å se gjennom syklusopptellingsdifferansene.

1. Returner til Supply Chain Management.
1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Finn og velg syklusopptellingsarbeidet du så på tidligere. (Du kan for eksempel definere et filter for kolonnen **ID for arbeidsutvalg** for å finne poster som har verdien *CycleCount*.) Legg merke til at **Arbeidsstatus**-feltet for dette arbeidet nå er satt til *Venter på gjennomgang*.

    > [!NOTE]
    > For arbeidsbrukerkontoen som du brukte til å gjøre opptellingsarbeidet, blir alternativet **Syklustellingsansvarlig** satt til *Nei*, og feltene for **Grense for største prosent**, **Grense for største antall** og **Grense for største verdi** blir alle satt til *0* (null). Derfor må alle opptellingsdifferanser som denne brukeren rapporterer, godkjennes manuelt, og feltet **Arbeidsstatus** for det relaterte arbeidet settes til *Ventende gjennomgang*. Hvis opptellingsverdien var innenfor avviksgrensene (som angitt i feltene for **Grense for største prosent** eller **Grense for største antall** på **Arbeidsbrukere**-siden), eller hvis alternativet **Syklustellingsansvarlig** var satt til *Ja* for brukeren, ville arbeidet automatisk ha blitt lukket.

1. Velg **Syklustelling** i **Arbeid**-fanen i handlingsruten.
1. Klikk på **Godta telling** i handlingsruten.

    Differansen posteres ved hjelp av standard opptellingsjournal, og en ny arbeidsordre opprettes.

1. Velg **Syklustellingstransaksjoner** i handlingsruten, velg **Avledet arbeid** for å finne arbeidet som ble opprettet for den godkjente differansen.

## <a name="scenario-2-blind-cycle-counting"></a>Scenario 2: Blind syklustelling

Dette scenariet krever at scenario 1 allerede er fullført i systemet.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Opprette syklustellingsarbeid for scenario 2

Før blind syklustelling kan forekomme, må du opprette arbeid. Følg denne fremgangsmåten når du skal opprette syklustellingsarbeid for varelokasjon *01A02R2S2B* (BULK-06) i lager *61*.

1. Gå til **Warehouse Management \> Syklustelling \> Syklustellingsarbeid etter vare**.
1. I dialogboksen **Opprett syklustellingsarbeid etter vare** angir du feltet **Arbeidspulje-ID** til *CycleCount*.
1. Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .
1. I dialoglogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til tre rader med følgende innstillinger:

    - Rad 1:

        - **Tabell:** *Varer*
        - **Felt:** *Varenummer*
        - **Vilkår:** *L0101*

    - Rad 2:

        - **Tabell:** *Lagerdimensjoner*
        - **Felt:** *Lager*
        - **Kriterier:** *61*

    - Rad 3:

        - **Tabell:** *Lagerdimensjoner*
        - **Felt:** *Lokasjon*
        - **Vilkår:** *01A02R2S2B*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. Velg **OK** for å lukke dialogboksen **Opprett syklustellingsarbeid etter vare**.

    Når arbeidsopprettingsprosessen er fullført, får du en informasjonsmelding.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Utføre syklustellingsarbeid for scenario 2

Når du hra opprettet syklustellingsarbeider, følger du disse trinnene for å utføre arbeidet i mobilappen Warehouse Management.

1. Logg deg på mobilappen Warehouse Management som arbeidsbrukeren du konfigurerte i delen [Klargjøre demodata for scenarier](#prepare-demo-data) tidligere i denne artikkelen. For eksempel i denne artikkelen heter brukeren *Julia Funderburk* og er definert for lager *61*. (USMF-demodataene bør la deg logge deg på som denne arbeidsbrukeren ved å angi *61* som bruker-ID og *1* som passord.)
1. I hovedmenyen velger du **Lager**.
1. Velg **Blind syklustelling** på **Lager**-menyen.
1. Velg **Sone-ID**-feltet, angi *BULK06*, og velg deretter **OK** (hakesymbolknappen).
1. Velg **Vare**-feltet, angi *L0101*, og velg deretter **OK** (hakesymbolknappen).
1. Velg **Nummerskilt**, angi *LP\_BULK\_06\_01*, og velg deretter **OK** (hakesymbolknappen).
1. Velg **Antall**-feltet, angi *10*, og velg deretter **OK** (hakesymbolknappen).

    > [!NOTE]
    > Selv om systemet oppdaget en forskjell mellom den forventede lagerbeholdningen og antallet du skannet, ble du ikke bedt om å telle en ny gang, fordi feltet for **Antall forsøk** er satt til *0* (null) for menyelementet **Blind syklustelling** for mobilenhet. Du ble bedt om å skanne varenummeret og skiltnummeret fordi både alternativet **Vis varenummer** og alternativet **Vis nummerskilt** er angitt til *Nei* for menyelementet for mobilenhet.

1. Velg **OK** (hakesymbolknappen).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Gå gjennom syklusopptellingsdifferansene for scenario 2

Følg denne fremgangsmåten for å se gjennom syklusopptellingsdifferansene.

1. Returner til Supply Chain Management.
1. Gå til **Warehouse Management \> Felles \> Arbeid \> Syklustellingsarbeid venter på gjennomgang**.
1. Velg **Syklustelling** i **Arbeid**-fanen i handlingsruten.
1. Velg **Avslå antall** i handlingsruten.

    Fordi opptellingsdifferansen ble avvist, er arbeidet lukket.

## <a name="scenario-3-spot-cycle-counting"></a>Scenario 3: Spotsyklustelling

Lagerbeholdningsposten angir at det er et lagerbeholdning av varen *L0101* på lokasjonen *01A02R2S2B*. Lagerarbeideren er på lokasjonen *01A02R2S1B*. Selv om lokasjonen er tom, er den full. Derfor gjør lagerarbeideren umiddelbart spottelling for denne lokasjonen.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Utføre syklustellingsarbeid for scenario 3

Følg denne fremgangsmåten for å bruke syklusopptellingsarbeid i mobilappen Warehouse Management.

1. Logg deg på mobilappen Warehouse Management som arbeidsbrukeren du konfigurerte i delen [Klargjøre demodata for scenarier](#prepare-demo-data) tidligere i denne artikkelen. For eksempel i denne artikkelen heter brukeren *Julia Funderburk* og er definert for lager *61*. (USMF-demodataene bør la deg logge deg på som denne arbeidsbrukeren ved å angi *61* som bruker-ID og *1* som passord.)
1. I hovedmenyen velger du **Lager**.
1. Velg **Spottelling** på **Lager**-menyen.
1. Velg **Lokasjon**-feltet, angi *01A02R2S1B*, og velg deretter **OK** (hakesymbolknappen).

    Systemet oppdager at lokasjonen er tom i Supply Chain Management.

1. Velg **Legg til LP eller vare**.
1. Velg **Vare**-feltet, angi *L0101*, og velg deretter **OK** (hakesymbolknappen).
1. Velg **Nummerskilt**, angi *LP\_BULK\_06\_01*, og velg deretter **OK** (hakesymbolknappen).
1. Velg **Antall**-feltet, angi *9*, og velg deretter **OK** (hakesymbolknappen).

    Fordi systemet oppdager at det angitte nummerskiltet allerede er tilgjengelig på et annet sted i Supply Chain Management, blir lisensen flyttet til det gjeldende stedet. Derfor ber systemet deg om å bekrefte flyttingen.

1. Velg **OK** (hakesymbolknappen).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Gå gjennom syklusopptellingsdifferansene for scenario 3

Følg denne fremgangsmåten for å se gjennom opptellingsresultatene.

1. Returner til Supply Chain Management.
1. Gå til **Warehouse Management \> Felles \> Arbeidsdetaljer**.
1. Merk av for **Vis lukkede** øverst i rutenettet.
1. Sett filteret for kolonnen **Arbeidsordretype** til *Lagerbevegelse*.

    Systemet oppdaget automatisk denne opptellingen som en lagerbevegelse. Denne flyttingen er tillatt fordi alternativet **illat at nummerskilt flyttes under syklustelling** er satt til *Ja* for lager *61* på **Lagre**-siden.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Scenario 4: Definere terskler for syklustelling

Én måte å opprette syklustellingsarbeid på, er å bruke terskler. En syklustellingsterskel angir antall- eller prosentgrensen for lagervarer. Syklustellingsarbeid opprettes automatisk når terskelen er nådd.

Det finnes for eksempel 60 elementer på en lokasjon der terskelverdien for syklustelling er 40. Under en salgsordretransaksjon plukkes 25 varer fra lokasjonen og plasseres i en oppsamlingslokasjon. Siden det nye vareantallet på 35 er mindre enn terskelantallet, opprettes syklustellingsarbeid automatisk for lokasjonen.

Følg disse trinnene for å opprette syklustellingterskler.

1. Gå til **Warehouse Management \> Oppsett \> Syklustelling \> Terskler for syklustelling**.
1. I handlingsruten velger du **Ny** for å opprette en terskel, og deretter angir du følgende verdier for den:

    - **ID for syklustellingsterskel:** *L0101*
    - **Beskrivelse:** *Terskel L0101*
    - **Terskelantall:** *2*
    - **Enhet:** *ea*
    - **Kapasitetsterskel basert på prosentandel:** *0,00*
    - **Terskeltype for syklustelling:** *Antall*
    - **Behandle syklustelling umiddelbart:** *Ja*
    - **Dager mellom syklustelling:** *1*
    - **ID for arbeidsutvalg:** *CycleCount*

1. Velg **Velg varer** i handlingsruten.
1. I dialogboksen for Power Query-redigering, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Varenummer*. Sett **Vilkår**-feltet for denne raden til *0101*.
1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.

    Du har nå definert en syklustellingsterskel for vare *L0101*.

Syklustelling vil nå bli opprettet for vare *L0101* på en lokasjon hvis lagerbeholdning er mindre enn 2, og hvis datoen for den siste syklustellingen for lokasjonen ikke er i dag.

## <a name="scenario-5-define-cycle-count-plans"></a>Scenario 5: Definere planer for syklustelling

Med syklustellingsplaner kan du automatisere opprettelsen av syklustellingsarbeid. Du kan definere hver syklustellingsplan med bestemte vare- og lokasjonsspørringer. Når den satsvise jobben kjøres, vil den opprette syklustellingsarbeid for alle lokasjoner som er i samsvar med vare- og lokasjonskriteriene (opptil det maksimale antallet tellinger som er angitt for planen). Når syklustellingsarbeid opprettes, inneholder tellingsarbeidslinjen informasjon om lokasjonen som må telles. Lagerbeholdningen som er knyttet til denne lokasjonen, er ikke blokkert. Derfor er den tilgjengelig for reservasjon og utgående behandling, selv om det finnes åpent opptellingsarbeid.

Følg disse trinnene for å opprette en syklustellingsplan.

1. Gå til **Warehouse Management \> Oppsett \> Syklustelling \> Planer for syklustelling**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet, og angi deretter følgende verdier:

    - **ID for syklustellingsplan:** *BULK06*
    - **Beskrivelse:** *Telling av lokasjon for BULK06*
    - **ID for arbeidsutvalg:** *CycleCount*
    - **Største antall syklustellinger:** *10*
    - **Dager mellom syklustelling:** *10*
    - **Tomme lokasjoner:** *Utelukk tomme*
    - **Arbeidsmal:** La dette feltet stå tomt.

1. Velg **Velg lokasjoner** i handlingsruten.
1. En standard dialogboks for Power Query-redigering vises. På **Område**-fanen legger du til en rad og angir følgende verdier for den:

    - **Tabell:** *Plasseringer*
    - **Felt:** *Sone-ID*
    - **Vilkår:** *BULK06*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. Velg **Behandle syklustellingsplan** i handlingsruten.
1. I dialogboksen **Planer for syklustelling** i hurtigfanen **Kjør i bakgrunnen** setter du alternativet for **Satsvis behandling** til *Ja*.
1. Velg **Regelmessighet**.
1. I dialogboksen **Definer regelmessighet** definerer du den satsvise jobben, slik at den starter umiddelbart og kjøres én gang hvert minutt, og slik at det ikke er noen sluttdato.
1. Velg **OK** for å lukke dialogboksen **Definer regelmessighet**.
1. Velg **OK** for å lukke dialogboksen **Planer for syklustelling**.

    En melding forteller deg at jobben ble lagt til i den satsvise køen.

1. Gå til **Warehouse Management \> Felles \> Tidsplanlegging av syklustelling**. Planen begynner umiddelbart og oppretter opptellingsarbeid. Fordi opptellingsarbeid ikke er fullført, settes **Status**-feltet til *Pågår*. Etter ett minutt endres verdien i kolonnen for **Total syklusantall** til *1*.

    > [!NOTE]
    > Det opprettes ikke syklustellingsarbeid hvis antall dager siden siste syklusopptelling er mindre enn verdien du angir for feltet **Dager mellom syklustelling** for syklusopptellingsplanen. Hvis for eksempel feltet **Dager mellom syklustellinger** er angitt til *5*, opprettes syklustellingsarbeidet hver femte dag. Hvis syklustellingsarbeid imidlertid behandles på dag tre, opprettes neste syklustellingsarbeid fem dager etter den siste syklustellingen ble behandlet, på dag åtte.

1. Velg **Arbeid** i handlingsruten for å vise opptellingsarbeidet som ble opprettet.
