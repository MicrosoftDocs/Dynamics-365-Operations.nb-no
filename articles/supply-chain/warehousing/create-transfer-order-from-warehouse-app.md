---
title: Opprette overføringsordrer fra lagerappen
description: Dette emnet beskriver hvordan du oppretter og behandler overføringsordrer fra mobilappen Lagerstyring
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d8bab58727a7031f122864cb7465d9bc5983b467
ms.sourcegitcommit: 1f2394be857afaefa8749f607cda62dfa00ba2c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/02/2021
ms.locfileid: "6164852"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Opprette overføringsordrer fra lagerappen

[!include [banner](../includes/banner.md)]

Denne funksjonen lar lagerarbeidere opprette og behandle overføringsordrer direkte fra mobilappen Lagerstyring. Arbeideren begynner ved å velge destinasjonslageret, og deretter kan de skanne én eller flere nummerskilt ved hjelp av appen for å legge til nummerskilt i overføringsordren. Når lagerarbeideren velger **Fullfør ordre**, vil en satsvis jobb opprette den nødvendige overføringsordren og ordrelinjene basert på lagerbeholdningen som er registrert for disse nummerskiltene.

## <a name="enable-the-create-transfer-orders-from-the-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Aktiver overføringsordrene fra lagerappfunksjonen

Før du kan bruke denne funksjonen, må den og forutsetningene være aktivert i systemet. Administratorer kan bruke siden for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig.

1. Først aktiverer du funksjonen [Behandle lagerapphendelser](warehouse-app-events.md), som er oppført i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) som:
    - **Modul** – lagerstyring
    - **Funksjonsnavn** – Behandle lagerapphendelser
1. Deretter aktiverer du funksjonen *Opprett overføringsordrer fra lagerappen*, som er oppført som:
    - **Modul** – lagerstyring
    - **Funksjonsnavn** – Opprette og behandle overføringsordre fra lagerappen
1. Hvis du vil automatisere behandlingen av de utgående forsendelsene, må du også aktivere funksjonen [Bekreft utgående forsendelser fra satsvise jobber](confirm-outbound-shipments-from-batch-jobs.md). Denne funksjonen er oppført som:
    - **Modul** – lagerstyring
    - **Funksjonsnavn** – Bekreft utgående forsendelser fra satsvise jobber

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Definere et menyelement for mobilenhet for å opprette overføringsordrer

Her er generelle retningslinjer for hvordan du oppretter menyelement for mobilenheter for å opprette en overføringsordre. Avhengig av forretningsbehovene dine for at automatiseringsnivået skal angis når brukere oppretter overføringsordrer fra lageret, blir forskjellige konfigurasjoner aktivert. Scenariet i dette dokumentet beskriver en slik konfigurasjon.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** for å legge til et nytt menyelement. Deretter kan du utføre følgende innstillinger for å komme i gang:

    - **Navn på menyelement** – Tilordne et navn slik det skal vises i Supply Chain Management.
    - **Tittel** – Tilordne et menynavn slik det skal vises for arbeidere i mobilappen Lagerstyring.
    - **Modus** – Satt til *Indirekte* (dette menyelementet vil ikke opprette arbeid).
    - **Aktivitetskode** – Satt til *Opprett overføringsordre fra nummerskilt* for å gjøre det mulig for lagerarbeidere å opprette en overføringsordre basert på én eller flere skannede nummerskilt.

1. Bruk innstillingen **Policy for opprettelse av overføringsordrelinje** til å kontrollere hvordan overføringsordrelinjene opprettes av dette menyelementet. Linjene opprettes/oppdateres basert på lagerbeholdningen som er registrert for de skannede nummerskiltene. Velg én av følgende verdier:

    - **Ingen reservasjon** – Overføringsordrelinjene vil ikke bli reservert.
    - **Nummerskilt veiledet med linjereservasjon** – Overføringsordrelinjene blir reservert og bruker nummerskiltveiledet strategi, som lagrer de aktuelle nummerskilt-ID-ene som er tilknyttet ordrelinjene. Du kan derfor bruke verdier for nummerskilt-ID som en del av arbeidsopprettelsesprosessen for overføringsordrelinjene.

1. Bruk innstillingen **Utgående forsendelsespolicy** til å legge til mer automatisering for forsendelsesprosessen for utgående overføringsordre etter behov. Når en arbeider velger **Fullfør ordre**-knappen, oppretter appen den *Fullfør ordre*-lagerapphendelsen, som vil lagre verdien du velger her i **Utgående forsendelsespolicy** for alle linjene i gjeldende overføringsordre. Senere, når hendelseskøen behandles av en satsvis jobb for å opprette overføringsordren, kan verdien som er lagret i dette feltet, leses av den satsvise jobben, og kan derfor kontrollere hvordan denne jobben behandler hver linje. Velg ett av følgende:

    - **Ingen** – Ingen automatisert behandling utføres.
    - **Frigi til lager** – Automatiserer prosessen for frigi til lager.
    - **Forsendelsesbekreftelse** – Automatiserer prosessen for forsendelsesbekreftelse.
    - **Frigivelses- og forsendelsesbekreftelse** – Automatiserer prosessene frigi til lager og forsendelsesbekreftelse.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Legge til menyelementet på en meny for mobilenhet

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Rediger**.
1. Velg en eksisterende meny etter valg av det nye menyelementet under **Tilgjengelige menyer og menyelementer**. Legg til menyelementet ved å velge pil høyre-knappen.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Opprette en overføringsordre basert på nummerskilt

Mobilappen Lagerstyring har en enkel prosess for oppretting av overføringsordrer basert på nummerskilt. Hvis du vil gjøre dette, gjør arbeideren følgende ved hjelp av mobilappen Lagerstyring:

1. Opprett overføringsordren, og Identifiser destinasjonslageret.
1. Identifiser hvert nummerskilt som skal leveres.
1. Velg **Fullfør ordre**.

>[!NOTE]
> Det er mulig for flere arbeidere å tilordne nummerskilt som er beregnet på den samme overføringsordren ved å bruke knappen **Velg overføringsordre** til å velge et eksisterende, ubehandlet ordrenummer fra hendelseskøen for lagerappen. Hvis du vil ha mer informasjon om hvordan du finner nummerverdier for overføringsordrer, kan du se [Spørring til lagereapphendelser](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Eksempelscenario

Dette scenariet gir en oversikt over prosessen for å hente overføringsordrer som er opprettet og automatisk behandlet basert på lagerbeholdningen som er registrert på de valgte nummerskiltene.

Hvis du vil omgå dette scenariet ved hjelp av verdiene som foreslås, må du arbeide på et system med demonstrasjonsdata installert og velge den juridiske enheten *USMF* før du begynner.

I dette scenariet forutsettes det at du allerede har aktivert funksjonen [Opprette og behandle overføringsordre fra lagerappen](#enable-create-transfer-order-from-warehouse-app) og [Behandling av lagerapphendelse](warehouse-app-events.md).

I tillegg til å konfigurere Opprett overføringsordre i menyelementene for mobilenhet, må tilleggsmaler, lokasjonsdirektiver og satsvise jobber også konfigureres og aktiveres.

### <a name="example-scenario-blueprint"></a>Eksempelscenario

Du er forhandler og har flere nummerskilt som hver inneholder en blanding av varer på en bestemt lokasjon i ett av lagrene (*lager 51*). Du vil aktivere prosessen som gjør at arbeidere kan opprette en overføringsordre til et annet lager (*lager 61*) for en samling av skannede nummerskilt. Du vil automatisk oppdatere overføringsordren så snart det siste nummerskiltet for ordren er identifisert.

![Eksempel på prosess for automatisk overføring av ordre](media/create-transfer-order-from-app-example.png "Eksempel på prosess for automatisk overføring av ordre")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Opprette et menyelement for mobilenhet for å opprette overføringsordrer

Denne delen beskriver hvordan du oppretter et nytt menyelement for mobilenhet for oppretting av overføringsordrer. Sett **Modus** til *Indirekte* og **Aktivitetskode** til *Opprett overføringsordre fra nummerskilt*.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny**.
1. I feltet **Menyelementnavn** angir du navnet *Opprett TIL*.
1. I **Tittel**-feltet angir du beskrivelsen *Opprett TIL*.
1. Velg *Indirekte* i feltet **Modus**.
1. I **Aktivitetskode** velger du *Opprett overføringsordre fra nummerskilt*
1. I **Policy for oppretting av ordrelinje** velger du *Nummerskilt veiledet med linjereservasjon*.
1. I **Utgående forsendelsespolicy** velger du *Frigivelses- og forsendelsesbekreftelse*.
1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Rediger**.
1. Velg den eksisterende **Lager**-menyen, og velg deretter det nye menyelementet under **Tilgjengelige menyer og menyelementer**. Legg til menyelementet i **Lager**-menyen ved å velge pil høyre-knappen.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Konfigurere arbeidsmaler for automatisk behandling og pausearbeid ved å finne nummerskiltet

Denne delen beskriver hvordan du kan aktivere en arbeidsmal for automatisk behandling av arbeidet som opprettes av malen når en bølge frigis.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Velg *Utstedelse for overføring* i feltet **Arbeidsordretype**.
1. Velg **Ny** for å opprette en ny arbeidsmal.
1. I **Arbeidsmal**-feltet angir du *51 Automatisk behandling LP*.
1. I feltet **Beskrivelse av arbeidsmal** angir du *51 Automatisk behandling LP*.
1. Merk av for **Automatisk behandling**. Dette må velges for at det skal utføres automatiseringstrinn.
1. I demonstrasjonsdataene finnes allerede arbeidsmalen *51 Overfør*. Rediger **Serienummer**-feltet, slik at den nye arbeidsmalen har et lavere serienummer enn den eksisterende arbeidsmalen *51 Overfør*.
1. Velg **Lagre** på verktøylinjen for å aktivere hurtigfanen **Arbeidsmaldetaljer**.
1. Velg **Ny** på verktøylinjen i hurtigfanen **Arbeidsmaldetaljer**. Du skal legge til to linjer.
1. Velg *Plukk* i **Arbeidstype**-feltet.
1. I feltet **Arbeidsklasse-ID** velger du *TransfOut*.
1. Velg **Ny** på verktøylinjen **Arbeidsmaldetaljer**.
1. Velg *Plasser* i **Arbeidstype**-feltet.
1. I feltet **Arbeidsklasse-ID** velger du *TransfOut*.
1. Velg **Lagre** for å aktivere feltet **Direktivkode**.
1. På linjen **Arbeidstype** *Plasser* velger du **Direktivkode** *Rampedør*. Kontroller at denne nye arbeidsmalen får det laveste **serienummeret**.
1. På verktøylinjen velger du **Rediger spørring** for å åpne redigeringsprogrammet for spørring.
1. Velg **Legg til** i fanen **Område**.
1. På linjen som legges til velger du *Lager* i **Felt**.
1. Velg *51* i feltet **Vilkår**.
1. Velg fanen **Sortering**.
1. Velg **Legg til** og sett **Felt** til *ID for nummerskilt*. Hvis du velger dette feltet, aktiveres verktøylinjeknappen **Arbeidshodeskift**.
1. Velg **OK** etterfulgt av **Ja** for å tilbakestille grupperingen og gå tilbake til siden **Arbeidsmaler**.
1. Velg **Arbeidshodeskift**, og Aktiver **Grupper etter dette feltet** for **ID for nummerskilt** og lukk.

> [!NOTE]
> Ikke alle oppsett kan behandles automatisk, for eksempel faktisk vekt-varer og bruk av blandede sporingsdimensjoner.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Konfigurere lokasjonsdirektiver for nummerskiltledet strategi

Denne delen forklarer hvordan du konfigurerer en plukkprosess for lokasjonsdirektiv for å bruke **nummerskiltledet** strategi.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Velg **Rediger**.
1. I overskriften for navigasjonslisten velger du **Arbeidsordretype** *Utstedelse for overføring*.
1. I navigasjonslisten velger du det eksisterende lokasjonsdirektivet **51 Å plukke**.
1. I hurtigfanen **Linjer** merker du av for **Tillat deling**.
1. I hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en ny handlingslinje.
1. Angi *LP-ledet* i **Navn**-feltet.
1. I **Strategi**-feltet velger du *Nummerskiltledet*. Denne handlingen må ha det laveste serienummeret.
1. Velg **Lagre** på verktøylinjen.
1. Velg **Oppdater**-sideikonet fra verktøylinjen.
1. I hurtigfanen **Handlinger for lokasjonsdirektiv** velger du linjen for *Å plukke*.
1. Velg **Flytt ned** på verktøylinjen **Handlinger for lokasjonsdirektiv** for å endre serienummeret, slik at det er større enn serienummeret for den nylig opprettede handlingen *LP-ledet*.

> [!NOTE]
> Strategien for nummerskiltledet vil prøve å reservere og opprette plukkarbeid mot lokasjonene som inneholder de forespurte nummerskiltene som er knyttet til overføringsordrelinjene. Hvis dette ikke er mulig og du fortsatt vil opprette plukkarbeid, må du imidlertid gå tilbake til en annen strategi for lokasjonsdirektivhandling, og kanskje også søke etter beholdning i et annet område av lageret, avhengig av behovet til forretningsprosessen.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere en satsvis jobb for å behandle lagerapphendelser

Denne delen beskriver hvordan du konfigurerer en planlagt satsvis jobb for å behandle lagerapphendelser.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle lagerapphendelser**.
2. I dialogboksen aktiverer du **Satsvis behandling** under delen **Kjør i bakgrunnen**.
3. Velg **Regelmessighet**, og konfigurer den satsvise jobben som skal behandles, basert på intervallet som kreves for din virksomhet.
4. Velg **OK** for å gå tilbake til hoveddialogboksen.
5. Velg **OK** i hoveddialogboksen for å legge til jobben i den satsvise køen.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Konfigurere en satsvis jobb for å frigi overføringsordrer automatisk

Denne delen beskriver hvordan du konfigurerer en planlagt satsvis jobb for å frigi overføringsordrene som er merket som "klar til frigivelse".

1. Gå til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse av overføringsordrer**.
1. I dialogboksen viser du delen **Poster som skal inkluderes**.
1. Velg **Filtrer** under delen **Poster som skal inkluderes**.
1. På spørringssiden **WHSTransferAutoRTWQuery**, i fanen **Område**, velger du **Legg til** for å legge til en ny linje i spørringen.
1. I den nye linjen **Tabell**-felt velger du rullegardinmenyen og deretter tabellen **Frigjør overføringslinje til lager**.
1. I rullegardinmenyen **Felt** velger du **Utgående forsendelsespolicy**.
1. I **Vilkår**-feltet velger du **Frigivelses- og forsendelsesbekreftelse**.
1. I linjen der **Felt** er satt til *Fra lager*, i feltet **Vilkår**, velger du *51*.
1. Velg **OK** for å gå tilbake til hoveddialogboksen.
1. Vis delen **Kjør i bakgrunnen** for å konfigurere satsvis behandling.
1. Aktiver **Satsvis behandling** under delen **Kjør i bakgrunnen**.
1. Velg **Regelmessighet**, og konfigurer den satsvise jobben som skal behandles, basert på intervallet som kreves for din virksomhet.
1. Velg **OK** for å gå tilbake til hoveddialogboksen.
1. Velg **OK** i hoveddialogboksen for å legge til den satsvise jobben i den satsvise køen.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Konfigurere den satsvise jobben Behandle utgående forsendelser

Denne delen beskriver hvordan du konfigurerer en planlagt satsvis jobb for å kjøre den utgående forsendelsesbekreftelsen for last klare til forsendelse, som er knyttet til overføringsordrelinjer som er klare til forsendelse.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle utgående forsendelser**.
1. Utvid delen **Poster som skal inkluderes**.
1. Velg **Filter**.
1. I spørringen **WHSLoadShipConfirm** velger du fanen **Sammenkoblinger**.
1. Vis tabellhierarkiet slik at **Laster** og **Lastdetaljer** vises.
1. Velg tabellen **Lastdetaljer**.
1. Velg knappen **Legg til tabellsammenkobling**.
1. Filtrer eller søk på **Relasjon**-kolonnen for *Overføringsordrelinjer (referanse)* i listen over tabellrelasjoner.
1. Fokuser på tabellrelasjonen i listen, og trykk deretter på **Velg**-knappen.
1. Velg tabellen **Overføringsordrelinjer**.
1. Velg knappen **Legg til tabellsammenkobling**.
1. Filtrer eller søk på **Relasjon**-kolonnen for *Tilleggsfelt for lageroverføring (post-ID)* i listen over tabellrelasjoner.
1. Fokuser på tabellrelasjonen i listen, og trykk deretter på **Velg**-knappen.
1. Velg **Område**-fanen.
1. I spørringstabellene **Område** konfigurerer du tre områder for spørringskriterier. Velg **Legg til**-knappen for å legge til en linje.
1. Legg til et område for tabellen **Laster**. Sett **Felt** til *Laststatus*, og sett **Vilkår** til *Lastet*.
1. Legg til et nytt område for tabellen **Tilleggsfelt for lageroverføring**. Sett **Felt** til *utgående forsendelsespolicy*, og sett **Vilkår** til *Frigivelses- og forsendelsesbekreftelse*.
1. Legg til et nytt område for tabellen **Lastdetaljer**. Sett **Felt** til *Referanse*, og sett **Vilkår** til *Overføringsordreforsendelse*.
1. Velg **OK** for å gå tilbake til hoveddialogboksen.
1. Vis delen **Kjør i bakgrunnen**.
1. Aktiver **Satsvis behandling**.
1. Velg **Regelmessighet**, og konfigurer den satsvise jobben som skal behandles, basert på intervallet som kreves for din virksomhet.
1. Velg **OK** for å gå tilbake til hoveddialogboksen.
1. Velg **OK** i hoveddialogboksen for å legge til den satsvise jobben i den satsvise køen.

> [!NOTE]
> Hvis du vil ha mer informasjon, kan du se [Bekreft utgående forsendelser fra satsvise jobber](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Behandle eksemplet for Opprette overføringsordre fra lagerappen

### <a name="add-on-hand-on-a-license-plate"></a>Legge til beholdning på et nummerskilt

Som et utgangspunkt for dette scenariet må du ha et nummerskilt som inneholder aktuell tilgjengelig lagerbeholdning.

| Artikkel | Lager | Beholdningsstatus | Lokasjon | Nummerskilt | Antall |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Tilgjengelig | LP-010 | LP10 | 1 |
| A0002 | 51 | Tilgjengelig | LP-010 | LP10 | 2 |

Legg til aktuell lagerbeholdning ved hjelp av følgende verdier:

> [!NOTE]
> Du må opprette et nummerskilt og bruke lokasjoner som lar deg overføre kombinerte varer, for eksempel LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Opprett og behandle overføringsordrer fra lagerappen

1. Åpne appen, og logg på som bruker *51*. Gjeldende brukerlager vil være 51.
1. Velg menyelementet **Opprett TIL** fra menyplasseringen der du la det til under konfigurasjonen.
1. Starte opprettelsen av en overføringsordre ved å angi mållageret (Til-lager) i **Lager**-feltet, og angi *61*. Den nye overføringsordren vil gå fra gjeldende lager 51 (Fra-lager) til mållageret *61*.
1. Velg **OK**.
1. Skanne en nummerskilt-ID i **Nummerskilt**-feltet. Angi nummerskiltet for lageret som ble lagt til i et tidligere trinn, *LP10*.
1. Velg **OK**.
1. Velg menyknappen, og velg deretter **Fullfør ordre** for å fullføre opprettingen av overføringsordre for lagerapp.

I det nevnte eksemplet brukes to **lagerapphendelser** ( *Opprett overføringsordre* og *Fullfør overføringsordre*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Spørring til lagerapphendelser

Du kan vise hendelseskøen og hendelsesmeldingene som genereres av mobilappen Lagerstyring, ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Logger for mobilenheter \> Lagerapphendelser**.

Hendelsesmeldingene *Opprett overføringsordre* vil motta statusen *Venter*, som betyr at den satsvise jobben **Behandle lagerapphendelser** ikke henter inn og behandler hendelsesmeldinger. Så snart hendelsesmeldingen blir oppdatert til statusen *I kø*, behandler den satsvise jobben hendelsene. Dette skjer samtidig som opprettelsen av hendelsen *Fullfør overføringsordre* (når en arbeider velger **Fullfør ordre**-knappen i mobilappen Lagerstyring). Når hendelsesmeldingene *Opprett overføringsordre* er behandlet, oppdateres statusen til *Fullført* eller *Mislyktes*. Når statusen *Fullfør overføringsordre* oppdateres til *Fullført*, slettes alle relaterte hendelser fra køen.

Fordi **lagerapphendelsene** for opprettingen av data for overføringsordre ikke vil bli behandlet av den satsvise jobben før meldingene oppdateres til statusen *I kø*, må du slå opp de forespurte numrene for overføringsordre som en del av **Identifikator**-feltet. **Identifikator**-feltet er i overskriften på siden **Lagerapphendelser**.

Som en del av behandling av lagerhendelser kan det hende at opprettingen av overføringsordrelinjen mislykkes. I slike tilfeller blir tilstanden til hendelsesmeldingen oppdatert til *Mislyktes*, og du kan bruke informasjonen om den **satsvise loggen** til å finne ut hvorfor og iverksette tiltak for å løse eventuelle problemer.

Vanlige problemer kan være knyttet til manglende oppsett for prosessen, for eksempel et manglende transittlager for hendelsen *Opprett overføringsordre*. I et eksempel som dette, kan du legge til et transittlager i forsendelseslageret og bruke alternativet **Tilbakestill** til å endre statusen for alle meldinger for lagerapphendelse fra *Mislyktes* til *I kø*, noe som betyr at den satsvise jobben vil behandle hendelsesmeldingene på nytt etter rettelsen av konfigurasjonsdataene.

I produksjonsmiljøer vil unntakene være mer prosessrelatert, for eksempel å ha en forespurt et nummerskilt, som ved behandling av den satsvise jobben er tom, slik at ingen overføringsordrelinjer opprettes. Hendelsesmeldingen som mislyktes kan fjernes ved hjelp av alternativet **Slett**, eller du kan legge til den nødvendige fysiske lagerbeholdningen på nummerskiltet og bruke alternativet **Tilbakestill** for alle relaterte hendelsesmeldinger.

Hvis du vil ha mer informasjon, kan du se [Behandling av hendelse for lagerappen](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Følge opp behandling av eksempelscenario

Følgende oppstod i dette scenariet:

1. Ved hjelp av mobilappen Lagerstyring valgte du et menyelement som bruker aktivitetskoden **Opprett overføringsordre fra nummerskilt**.
1. Appen ba deg om å velge mållageret for overføringsordren. Kildelageret er alltid det du er logget på som arbeider.
1. Ved valg av mållageret reserverte systemet et ID-nummer for den kommende overføringsordren (basert på nummerserien for overføringsorden som er definert i systemet), men oppretter ikke overføringsordren ennå.
1. Da du skannet nummerskiltet *LP10* som inneholder lagerbeholdningen som skal flyttes til det nye lageret, ble det lagt til en **lagerapphendelse** i hendelseskøen for å behandle dem senere. Lagerhendelsen inneholdt meldingsdetaljer om skanningen, inkludert det tiltenkte nummeret for overføringsordren.
1. Når **Fullfør ordre**-knappen velges i mobilappen Lagerstyring, opprettes en ny lagerapphendelse, **Fullfør overføringsordre**, og den relaterte eksisterende hendelsen, **Opprett overføringsordre**, endret status til **I kø**.
1. I serverdelen hentet den **satsvise jobben Behandle lagerapphendelser** hendelsen **I kø**, og samlet inn beholdningen relatert til det skannede nummerskiltet. Basert på beholdningen ble den faktiske posten for overføringsordre og tilknyttede linjer opprettet. Jobben fylte også ut feltet **Utgående forsendelsespolicy** for overføringsordren med verdien basert på den konfigurerte *Frigivelses- og forsendelsesbekreftelsen* og koblet nummerskilt mot linjene for strategien **Nummerskiltledet**.
1. Basert på overføringsordrelinjen **Utgående forsendelsespolicy** vil feltverdien for spørringen **Satsvis jobb for automatisk frigivelse av overføringsordrer** nå føre til frigivelse av overføringsordren til leveringslageret. På grunn av oppsettet for den brukte **bølgemalen**, **arbeidsmalen** og **lokasjonsdirektivene**, fikk arbeidet resultat av automatiske prosesser på **Laststatus** oppdatert til *Lastet*.
1. **Satsvise jobb for Behandle utgående forsendelse** utføres for lasten, noe som fører til at overføringsordren blir levert og det blir generert et forhåndsvarsel for forsendelse (ASN).
1. Tidsberegningen for alle disse hendelsene er avhengig av innstillingene for **Regelmessighet** for de satsvise jobbene som er opprettet.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="mobile-device-menu-item-setup"></a>Konfigurere et menyelement på mobilenhet

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Hvorfor kan jeg ikke se Opprett overføringsordre fra nummerskilt i rullegardinlisten for menyelementet for arbeidsaktivitet?

Funksjonen *Opprette og behandle overføringsordre fra lagerappen* må være aktivert. Hvis du vil ha mer informasjon, kan du se [Aktivere overføringsordrene fra lagerappfunksjonen](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Prosesser i mobilappen Lagerstyring

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Hvorfor kan jeg ikke se menyknappen Fullfør ordre?

Du må ha minst ett nummerskilt tilordnet overføringsordren.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Kan flere brukere i mobilappen Lagerstyring legge til nummerskilt i samme overføringsordre samtidig?

Ja, flere lagerarbeidere kan skanne nummerskilt inn i samme overføringsordre.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Kan det samme nummerskiltet legges til forskjellige overføringsordrer?

Nei, et nummerskilt kan bare legges til én overføringsordre om gangen.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Når jeg har valgt Fullfør ordre-knappen, kan jeg legge til flere nummerskilt for denne overføringsordren?

Nei, du kan ikke legge til flere nummerskilt i en overføringsordre som har lagerapphendelsen **Fullfør overføringsordre**.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Hvordan kan jeg finne eksisterende overføringsordrer som skal brukes via knappen Velg overføringsordre i mobilappen Lagerstyring, hvis ordren ennå ikke er opprettet i serverdelsystemet?

Du kan for øyeblikket ikke slå opp overføringsordrer i appen, men du kan finne numrene for overføringsordrer på siden **Lagerapphendelser**. Hvis du vil ha mer informasjon, kan du se [Spørring til lagerapphendelser](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Kan jeg velge manuelt nummeret for overføringsordre som skal brukes fra mobilappen Lagerstyring?

Bare numre for overføringsordrer som genereres automatisk via nummerserier, støttes.

### <a name="background-processing"></a>Bakgrunnsbehandling

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Hvordan bør jeg rydde opp i poster i meldingstabellene for køen for lagerapphendelser?

Du kan vise og vedlikeholde dette på siden **Lagerapphendelser**. Hvis du vil ha mer informasjon, kan du se [Spørring til lagerapphendelser](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Hvorfor oppdateres ikke overføringsordrens mottaksdato i henhold til oppsettet for leveringsdatokontroll?

Overføringsordrene opprettes uten bruk av funksjonene for **leveringsdatokontroll**.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Kan jeg bruke et nummerskilt med fysisk negativ lagerbeholdning?

Funksjonen støtter bare positive fysiske lagerbeholdningsantall på nummerskiltnivået, men du kan ha fysisk negative lagerbeholdningsantall på høyere lager- og lagerstatusnivåer når du tilordner nummerskilt til overføringsordrer.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]