---
title: Plasser til vegg – plasser til butikk
description: Dette emnet inneholder informasjon om funksjonen for Plasser til vegg – plasser til butikk. Med denne funksjonaliteten kan du håndtere scenarier der du må konsolidere et produkt i et oppsamlingsområde for forhåndspakker basert på konfigurerbare kriterier. Det bidrar til å redusere plukktiden fordi det tillater plukking til et enkelt målnummerskilt og kan bruke flere plasseringsposisjoner enn klyngeplukking.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434743"
---
# <a name="put-to-wall---put-to-store"></a>Plasser til vegg – plasser til butikk

[!include [banner](../includes/banner.md)]

Funksjonen for *Plasser til vegg – plasser til butikk* kan håndtere scenarier der du må konsolidere et produkt i et oppsamlingsområde for forhåndspakker basert på konfigurerbare kriterier. Fordi denne funksjonaliteten gjør det mulig å plukke til et enkelt målnummerskilt og bruke flere plasseringsstillinger enn klyngeplukking, vil firmaer som leverer til butikker eller behandler små varer, dra nytte av å redusere plukktiden.

Arbeidsflyten for denne funksjonaliteten dirigerer plukket produkt til en sorteringslokasjon for distribusjon til forskjellige typer containere. Vanligvis inneholder hver sorteringslokasjon flere sorteringsposisjoner. Hver sorteringsposisjon tilordnes i henhold til kriteriene som er angitt av forretningsprosessen. Vanlige kriterier er det endelige målet, forsendelsen eller lasten. Når et produkt mottas, distribueres det til hver sorteringsposisjon basert på antallet som er knyttet til ordren, målet, forsendelsen eller lasten. Når en container er full eller ferdig, flyttes den til en oppsamlingslokasjon eller en forsendelseslokasjon for videre behandling, avhengig av forretningsprosessen.

Denne lagerfunksjonaliteten refereres også til med andre navn.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivere Utgående sortering-funksjonen

Før du kan bruke funksjonen for *Plasser til vegg – plasser til butikk*, må funksjonen *Utgående sortering* aktiveres på systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Utgående sortering*

Funksjonen *Utgående sortering* kan brukes sammen med funksjonen *Organisasjonsomfattende bølgetrinnkode* hvis den er slått på. Du må også aktivere denne funksjonen hvis du vil bruke forhåndsdefinerte koder som er definert i bølgetrinnkoder. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Organisasjonsomfattende bølgetrinnkode*

## <a name="setup"></a>Installasjon

For denne demoen brukes standard Contoso-data og -lager *62*. Noen tillegg som er nevnt senere, brukes også.

### <a name="location-type"></a>Plasseringstype

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonstyper**.
1. Velg **Ny** i handlingsruten for å opprette en lokasjonstype for sortering.
1. Angi følgende verdier:

    - **Lokasjonstype:** *SORTER*
    - **Beskrivelse:** *Sorter*

1. Velg **Lagre**.

### <a name="warehouse-management-parameters"></a>Lagerstyringsparametere

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I kategorien **Generelt** i hurtigfanen **Lokasjonstyper** setter du feltet for **sorteringslokasjonstype** til *SORTER*.
1. Velg **Lagre**.

### <a name="location-profile"></a>Lokasjonsprofil

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **Ny** i handlingsruten for å opprette en lokasjonsprofil for sorteringslokasjon.
1. I hodet angir du følgende verdier:

    - **Lokasjonsprofil-ID:** *Sorter*
    - **Navn:** *Sorter*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Lokasjonsformat:** *PAKKE*
    - **Lokasjonstype:** *SORTER*
    - **Bruk sporing av nummerskilt:** *Ja*
    - **Tillat kombinerte varer:** *Ja*
    - Velg **Ja** i *Tillat kombinerte lagerstatuser*

1. Velg **Lagre**.

### <a name="locations"></a>Lokasjoner

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.
1. Fjern merket for **Generer kontrollsifre for lokasjon**.
1. Velg **Ny** i handlingsruten, og angi deretter følgende verdier:

    - **Lager:** *62*
    - **Lokasjon:** *Sorter*
    - **Lokasjonsprofil-ID:** *Sorter*

1. Velg **Lagre**.

### <a name="packing-profiles"></a>Emballasjeprofil-ID

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.
1. Velg **Ny** i handlingsruten, og angi deretter følgende verdier:

    - **Pakkeprofil-ID:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Policy for containerpakking:** La dette feltet stå tomt.
    - **Modus for container-ID:** *Automatisk*
    - **Containertype:** *PALL 48X48*
    - **Opprett container automatisk ved containerlukking:** La dette feltet stå tomt.

1. Velg **Lagre**.

### <a name="wave-step-codes"></a>Bølgetrinnkoder

Hvis du aktiverte *Organisasjonsomfattende bølgetrinnkode*, definerer du følgende kode.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**.
1. Velg **Ny** i handlingsruten, og angi deretter følgende verdier:

    - **Bølgetrinnkode:** *Sorter*
    - **Bølgetrinnbeskrivelse:** *Sorter*
    - **Bølgetrinntype:** *Sorter mal*

1. Velg **Lagre**.

### <a name="outbound-sorting-template"></a>Mal for utgående sortering

Sorteringsmalen styrer om sorteringsposisjoner opprettes, hvilke kriterier som brukes, og andre attributter for sorteringsprosessen.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Utgående sorteringsmal**.
1. I handlingsruten velger du **Ny** for å opprette en sorteringsmal.
1. I toppteksten på den nye malen angir du følgende verdier:

    - **ID for utgående sorteringsmal:** *Bølgesortering*
    - **Beskrivelse:** *Bølgesortering*
    - **Sorteringsmaltype:** *Bølgebehov*

        Dette feltet definerer prosessen som sorteringsmalen brukes til. Følgende verdier er tilgjengelige:

        - **Bølgebehov** – Sorteringsmalen brukes til prosessen *Plasser til vegg*. Denne maltypen brukes til å omgå pakkestasjonen og behandle lageret direkte utenfor bølgen. Du kan bare bruke denne typen hvis **sortering**-bølgeprosessmetoden er inkludert i bølgemalen.
        - **Container** – Sorteringsmalen brukes til prosessen for *Pallbyggingen etter pakking*. Denne maltypen brukes til å behandle containere som er lukket på pakkestasjonen og må sorteres på paller.

    - **Lager:** *62*
    - **Lokasjon:** *Sorter*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Sorteringsbekreftelse:** *Posisjonsskanning*

        Dette feltet definerer bekreftelsen som kreves ved sortering. Følgende verdier er tilgjengelige:

        - None
        - Nummerskiltskanning
        - Posisjonsskanning

    - **Opprett arbeid ved posisjonslukking:** *Ja*

        Hvis dette valget settes til *Ja* når posisjonen er lukket, opprettes arbeid for å flytte lageret til den endelige leveringslokasjonen. Hvis det settes til *Nei*, plukkes lageret umiddelbart til ordren når posisjonen lukkes.

    - **Stillingstilordning:** *Manuell*

        Dette feltet definerer typen stillingstilordning. Følgende verdier er tilgjengelige:

        - **Manuell** – Brukeren må alltid angi hvilken posisjon lageret skal sorteres til.
        - **Automatisk** – Systemet sender automatisk lageret til en posisjon når det er mulig, basert på inndelingene i sorteringsmalen.

    - **Tilordne kriterier for sorteringsposisjon:** *Bruk bare tom plassering*

        Dette feltet styrer om lageret som allerede finnes på sorteringsposisjoner, skal tas hensyn til når en posisjon tilordnes for behovet. Følgende verdier er tilgjengelige:

        - **Bruk bare tom plassering** – Stillinger som allerede har tilknyttet lager, vil bli tatt med i betraktningen
        - **Anta tom plassering** – Et lager som allerede finnes på plasseringen, ignoreres under tilordningen. Alle tilgjengelige plasseringer vil bli brukt.

    - **Bølgetrinnkode:** *Sorter*

        Hvis funksjonen *Organisasjonsomfattende bølgetrinnkode* er aktivert, må *Sorter*-bølgetrinnkoden også konfigureres i bølgetrinnkodene.

    - **Automatisk lukking av sorteringsposisjon:** *Ja*

        Hvis dette alternativet er satt til *Ja*, vil sorteringsposisjonen automatisk lukkes når alt arbeid som kommer til posisjonen, er fullført.

    - **Antall sorteringsposisjoner:** *3*

        Dette feltet angir maksimalt antall sorteringsposisjoner som systemet vil opprette.

    - **Prefiks for sorteringsposisjon:** *SP-*

        Dette feltet definerer prefikset som systemet tilordner før posisjonsnummeret.

    - **Automatisk pakking av sorteringsposisjon:** *Ja*

        Hvis dette alternativet er satt til *Ja*, vil lageret på sorteringsposisjonen pakkes i en container når posisjonen lukkes.

    - **Pakkeprofil-ID:** *Sorter*

        Dette feltet definerer pakkeprofilen som vil bli brukt når sorteringsposisjonen pakkes i en container.

1. Velg **Rediger spørring** i handlingsruten for å angi kriteriene som brukes for denne sorteringsmalen.
1. I spørringsdialogboksen i kategorien **Sortering** velger du **Ny** for å legge til en linje, og angi deretter følgende verdier:

    - **Tabell:** *Lastdetaljer*
    - **Avledet tabell:** *Lastdetaljer*
    - **Felt:** *Leverings-ID*
    - **Søkeretning:** *Stigende*

1. Velg **OK**.
1. Du kan få følgende melding: "Gruppering vil bli tilbakestilt, vil du fortsette?" Velg **Ja**.

    Knappen for **Inndelinger for utgående sortereringmal** i handlingsruten blir tilgjengelig.

1. Velg alternativet for **Inndelinger for utgående sortereringmal** i handlingsruten.
1. Merk av for **Grupper etter-feltet** for å gruppere etter forsendelses-ID.

    Denne innstillingen vil opprette én sorteringsposisjon per forsendelse som er en container i bølgen.

1. Velg **OK**.

### <a name="wave-process-methods"></a>Bølgebehandlingsmetoder

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Velg **Regenerer metoder** i handlingsruten.

    **Sortering**-metoden legges til i listen over tilgjengelige metoder, og bølgemaltypen *Forsendelse* velges for den.

### <a name="wave-templates"></a>Bølgemaler

Rediger bølgemalen som brukes for bølgebehovsortering.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I feltet *Bølgemaltype* velger du **Forsendelse**.
1. Velg den eksisterende malen **62 Standardforsendelse**.
1. I handlingsruten velger du **Rediger**.
1. Gjør følgende endringer i hurtigfanen **Generelt**:

    - Sett alternativet **Behandle bølge ved frigivelse til lager** til *Nei*.
    - Sett alternativet **Tilordne til åpne bølger** til *Ja*.

1. I hurtigfanen **Metoder** angir du metoden **Sortering**:

    1. I rutenettet **Gjenværende metoder** velger du **Sortering**.
    2. Velg høyre pil for å flytte **sortering** til **Valgte metoder**-rutenettet.
    3. I rutenettet **Valgte metoder** velger du **Sortering**.
    4. Angi feltet **Bølgetrinnkode** til *Sorter*.

1. Velg **Lagre**.

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Menyelementnavn:** *Sorter*
    - **Tittel:** *Sorter*
    - **Modus:** *Indirekte*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktivitetskode:** *Utgående sortering*
    - **Bruk prosessveiledning:** *Ja* (standardverdi)
    - **ID for utgående sorteringsmal:** *Bølgesortering*

1. Velg **Lagre**.

### <a name="mobile-device-menu"></a>Meny på mobilenheten

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Utgående** i listen over menyer.
1. I handlingsruten velger du **Rediger**.
1. I rutenettet **Tilgjengelige menyer og menyelementer** finner og velger du **Sorter**-menyelementet du nettopp opprettet.
1. Velg høyre pil-knappen for å flytte **Sorter** til rutenettet **Menystruktur**. På denne måten legger du til menyelementet på menyen **Utgående**.
1. Velg **Lagre**.

### <a name="location-directives"></a>Lokasjonsdirektiver

Du må opprette lokasjonsdirektiver for å veilede arbeidet som opprettes etter at sorteringen er fullført.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Velg *Sortert lagerplukking* i feltet **Arbeidsordretype**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Sekvens:** *1*
    - **Navn:** *Sett til rampedør*

1. Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:

    - **Arbeidstype:** *Plasser*
    - **Område:** *6*
    - **Lager:** *62*
    - **Direktivkoden:** La dette feltet stå tomt.
    - **Flere SKUer:** *Nei*

1. Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier. Godta standardverdiene for alle de andre feltene.

    - **Sekvensnummer:** *1*
    - **Fra-antall:** *0*
    - **Til-antall:** *1000000*

1. Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier. Godta standardverdiene for alle de andre feltene.

    - **Sekvensnummer:** *1*
    - **Navn:** *Rampedør*

1. Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.
1. I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.
1. I dialogboksen for spørring, i kategorien **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*. Sett **Vilkår**-feltet for denne raden til *Rampedør*.
1. Velg **OK** for å bekrefte redigeringen.

### <a name="work-classes"></a>Arbeidsklasser

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Arbeidsklasse-ID:** *Sortering*
    - **Beskrivelse:** *Sortering*
    - **Arbeidsordretype:** *Sortert lagerplukking*

1. Velg **Lagre**.

### <a name="work-templates"></a>Arbeidsmaler

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsmaler**.
1. Velg *Salgsordrer* i feltet **Arbeidsordretype**.
1. Velg **62 Plukk til pakke**-arbeidsmalen i rutenettet.
1. Velg **Arbeidshodeskift** i handlingsruten.
1. I handlingsruten velger du **Rediger**.
1. I linjen der **Feltnavn**-feltet er satt til *Forsendelses-ID*, fjerner du merket i avmerkings boksen **Grupper etter dette feltet** .
1. Velg **Lagre**, og lukk deretter dialogboksen **Arbeidshodeskift**.
1. Velg *Sortert lagerplukking* i feltet **Arbeidsordretype**.
1. Velg **Ny** for å opprette en arbeidsmal.
1. Angi følgende verdier i delen **Oversikt**. Godta standardverdiene for alle de andre feltene.

    - **Arbeidsmal:** *Sortert plukking*
    - **Beskrivelse av arbeidsmal:** *Sortert plukking*

1. Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-delen tilgjengelig.
1. I delen **Arbeidsmaldetaljer** oppretter du to linjer. Velg **Ny**, og angi deretter følgende verdier for linje 1:

    - **Arbeidstype:** *Plukk*
    - **Obligatorisk:** Valgt (= *Ja*)
    - **Arbeidsklasse-ID:** *Sortering*

1. Velg **Ny** på nytt, og angi deretter følgende verdier for linje 2:

    - **Arbeidstype:** *Plasser*
    - **Obligatorisk:** Valgt (= *Ja*)
    - **Arbeidsklasse-ID:** *Sortering*

1. Velg **Lagre**.

## <a name="example-scenario"></a>Eksempelscenario

Dette scenariet simulerer en situasjon der lageret lagrer små varer på lokasjoner og må pakke dem i bokser før de leveres, og der pakkestasjonsfunksjonaliteten ikke passer. Arbeidere plukker bestillinger for flere kunder og forskjellige adresser samtidig for å øke plukkehastigheten. Når plukkingen er fullført, kommer arbeidere til sorteringslokasjonen, der de plukkede varene kan sorteres til riktig boks basert på nødvendige kriterier. I dette eksemplet vil forsendelses-IDen bli brukt til å fastslå den riktige boksen, fordi hver forsendelse har en annen adresse. Etter at alle varer fra lasten er pakket og sortert etter forsendelse, flyttes boksene til oppsamlingsområdet, og til slutt lastes de på en lastebil.

Før du starter scenariet må du kontrollere at alle standard lagerfunksjoner er definert riktig for lageret. Standard Contoso-lager *62* brukes til dette formålet. Standardkonfigurasjoner er ikke endret, bortsett fra det som er beskrevet i oppsettet.

### <a name="create-demand"></a>Opprette behov

Før funksjonaliteten kan demonstreres, må du opprette behov. I dette scenariet skal du opprette tre salgsordrer for at tre ulike kunder skal simulere forskjellige leveringsadresser. På denne måten skal du opprette tre separate forsendelser.

Før du oppretter salgsordrer og forsendelser må du kontrollere at plukklokasjonene har nok lager for alle varene på ordrene. Se gjennom lokasjonsdirektivinnstillingene for å bekrefte plukklokasjonene som skal brukes for plukking av salgsordre. Hvis du må justere beholdninge, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt. Reserver deretter lageret.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en ny salgsordre for ordre 1.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kunde:** *US-001*
    - **Lager:** *62*

1. Velg **OK**.
1. Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. Angi følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *5*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *10*

1. Gjenta følgende trinn for hver salgslinje i ordren for å reservere lager for den:

    1. På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.
    1. På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.
    1. Velg **Lagre**.

1. Velg **Ny** for å opprette en ny salgsordre for ordre 2.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kunde:** *US-004*
    - **Lager:** *62*

1. Velg **OK**.
1. Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. Angi følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *7*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *3*

1. Gjenta følgende trinn for hver salgslinje i ordren for å reservere lager for den:

    1. På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.
    1. På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.
    1. Velg **Lagre**.

1. Velg **Ny** for å opprette en ny salgsordre for ordre 3.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kunde:** *US-007*
    - **Lager:** *62*

1. Velg **OK**.
1. Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. Angi følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *8*

1. Følg disse trinnene for reservere lager for salgslinjen:

    1. På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.
    1. På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.
    1. Velg **Lagre**.

Fullfør følgende fremgangsmåte for å frigi hver salgsordre til lageret. Det opprettes tre forskjellige forsendelser. Deretter legger du til alle de tre leveringer i én ny bølge.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. I rutenettet velger du første salgsordre du opprettet.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.

    Du mottar en informasjonsmelding som viser bølge-ID og forsendelses-ID som er opprettet.

1. Gjenta de forrige trinnene for å frigi salgsordre 2 og 3 til lageret. Legg merke til at informasjonsmeldingen du mottar, angir at det er lagt til en forsendelse til bølgen som ble opprettet da du frigav salgsordre 1.
1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølge-IDen som ble opprettet fra frigivelsen av salgsordrene for å åpne **Bølger**-siden. Denne siden viser bølgeinformasjon. Hurtigfanen **Bølgelinjer** viser forsendelsene som ble opprettet.

    Du må nå opprette arbeid for å hente varer fra plukklokasjonene til sorteringslokasjonen.

1. Klikk på **Prosess** i handlingsruten.

    Under bølgebehandling vil sorteringsmetoden bruke sorteringsmalen til å tilordne lageret for å sortere posisjoner. Når bølgebehandling er fullført, mottar du en informasjonsmeling som angir at bølgen er postert og arbeidet er opprettet.

1. I handlingsruten i kategorien **Bølge** i gruppen **Relatert informasjon** velger du **Arbeid** for å vise arbeidet som ble opprettet. Noter arbeids-ID-en.
1. Gå til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.
1. I den venstre kolonnen kan du vise den utgående sorteringsposisjonen som ble opprettet for hver forsendelse.
1. I hurtigfanen **Kriterier for sorteringsposisjon** kan du vise forsendelses-ID for posisjonen.

Én arbeids-ID er opprettet for å hente lager fra plukklokasjonene til sorteringslokasjonen. For å fullføre arbeidet trenger du arbeids-IDen som ble opprettet under bølgebehandlingen.

### <a name="sales-order-picking-to-the-sorting-location"></a>Salgsordreplukking til sorteringslokasjonen

1. Logg på mobilappen som en arbeider i lageret *62*.
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Salgsplukking**.
1. Velg **ID**-feltet, og angi deretter arbeids-IDen fra bølgebehandlingen.
1. Bekreft oppføringen.

    Deretter blir du bedt om å angi et målnummerskilt (LP). Legg merke til at linje 1 fra salgsordre 1 må plukkes og legges til målnummerskiltet. Varenummeret, antallet, varebeskrivelsen og plukklokasjonen vises.

1. I feltet for **målnummerskilt** angir du målnummerskilt.

    Du vil plukke alle linjer som ble opprettet fra den behandlede bølgen, til samme mållisensplate.

1. Bekreft oppføringen.

    Mobilappen presenterer nå en serie med **Plukk**-sider som peker deg til plukklokasjonen og til varen og antallet som må plukkes. Når den plukkede varen er lagt til i nummerskiltet, bekrefter du plukkarbeidet. Den siste siden vil være arbeidet med å sette de plukkede varene inn i sorteringslokasjonen.

1. Bekreft det første plukkarbeidet.
1. Det neste plukkarbeidet vises. Bekreft plukket.
1. Fortsett med å bekrefte det gjenstående plukkarbeidet.
1. Det siste trinnet er å fullføre plasseringsarbeidet. Bekreft plasseringen til sorteringslokasjonen.

    Du mottar en Arbeid fullført-melding.

1. Avslutt **Salgsplukking** på mobilappen.

### <a name="sortingput-to-wall"></a>Sortering/plassering til vegg

Nå som alt lager er plassert til sorteringslokasjonen, må den sorteres til den riktige sorteringsposisjonen.

1. Logge på mobilappen.
1. I hovedmenyen velger du **Utgående**.
1. På menyen **Utgående** velger du **Sortering** for å starte sorteringen av varene.
1. I **LP/CON**-feltet angir du mållisensplaten for det plukkede salgsordrearbeidet.
1. Bekreft oppføringen.
1. Angi varenummeret som skal sorteres først.
1. Systemet bestemmer den første sorteringsposisjonen som skal vises. Bekreft sorteringsposisjonen.
1. Du blir bedt om å tilordne en lisensplate til sorteringsposisjonen. Velg **LP**-feltet, angi et lisensplatenummer, og bekreft deretter oppføringen.

    Siden sorteringsposisjonen er knyttet til forsendelses-IDen, skal du sortere de plukkede varene til et nummerskilt som er spesifikt for den utgående forsendelsen og salgsordren.

    Den neste siden viser vare-IDen, antallet, sorteringsposisjons-IDen og "fra"- (plukk) og "til"-nummerskilt-IDene (sortering). Informasjonen på denne siden instruerer deg om å sortere den angitte varen og mengdene fra plukkingens nummerskilt til sorteringsnummerskiltet.

1. Bekreft sorteringsposisjonen.
1. Sorter varene i den første sorteringsposisjonen. Når du er ferdig, sender systemet deg til den neste sorteringsposisjonen.
1. Gjenta denne prosessen for alle valgte linjer i arbeidsordren. Du bør også bruke denne prosessen når det er flere plukklinjer med samme varenummer.

    Når du gjentar denne prosessen for alle varer, evaluerer systemet kriteriene fra det neste skannede element (arbeidslinje) og bestemmer hvilken sorteringsposisjon den skal legges til. Du blir automatisk dirigert til å plassere varen til riktig sorteringsposisjon. Avhengig av bekreftelsesoppsettet blir du også dirigert til å bekrefte denne handlingen ved å angi posisjonsnummeret eller nummerskilt-ID-en.

    > [!NOTE]
    > Hvis automatisk sortering er aktivert, er ikke manuell overstyring tilgjengelig.

1. Når du er ferdig, åpner du siden **Posisjonstilordninger for utgående sortering** i Microsoft Dynamics 365 Supply Chain Management for å se gjennom statusen for posisjonene.

    - Hvis stillingene er lukket automatisk, velger du **Vis lukket** for å vise de lukkede posisjonene.
    - Legg merke til at sorteringsposisjonstransaksjoner vises. Varen og antallet som ble behandlet via posisjonen, vises.

    Når du definerer den utgående sorteringsmalen, setter du alternativet **Sorteringsposisjonen automatisk lukking** til *Ja*. Derfor lukkes stillingen automatisk etter at det siste forventede lageret blir lagt til den. Sorteringsposisjonene er i **Lukket**-status, og arbeidet er opprettet for å flytte det sorterte lageret til *Rampedør*-lokasjon.

1. Fullfør det sorterte lagerplukkingsarbeidet for å flytte lageret til forsendelsesstedet. Når lageret er klart, bekrefter du sending.

> [!NOTE]
> For sortert lagerplukkingsarbeid skal behandles på rett måte, må et mobilenhetsmenyelement med arbeidsklasse-ID der feltet **Arbeidsordretype** er satt til *Sortert lagerplukking*, brukes til flyttings- og innlastingsprosessen.

### <a name="manually-close-a-position-optional"></a>Lukke en stilling manuelt (valgfritt)

Hvis sorteringsposisjoner skal lukkes manuelt, må alternativet **Sorteringsposisjonen automatisk lukking** for den utgående sorteringsmalen settes til *Nei*, og det må gjøres en lukking før lageret kan flyttes til rampedøren. Stillinger kan lukkes på forskjellige måter:

- Via lagerappen:

    - Brukeren kan skanne én av varene som allerede finnes på posisjonen, og deretter velge **Lukk** for å lukke posisjonen.
    - Hvis brukeren skanner en container som allerede er sortert container, vises det en feilmelding. Brukeren kan imidlertid fremdeles fortsette å lukke posisjonen.

- Fra Microsoft Dynamics 365 Supply Chain Management siden **Posisjonstilordninger for utgående sortering**:

    - Brukeren kan velge den utgående sorteringsposisjonsposten og deretter velge **Lukk posisjon** i handlingsruten.

## <a name="tips"></a>Tips!

- Varer kan ikke flyttes mellom posisjoner etter at de er tilordnet til en posisjon. Systemet evaluerer hvor mange av hver vare som skal gå til en bestemt posisjon.
- Sorteringsmal kan konfigureres til å opprette containere automatisk når posisjoner er lukket. Denne fremgangsmåten vil opprette en standard container-ID-struktur som er basert på den angitte pakkeprofilen.

> [!IMPORTANT]
> Etter at bevegelsesarbeidet er opprettet fra sorteringslokasjonen, må du ikke avbryte arbeidet. Hvis ikke blir posisjonen og containerne i den slettet fra systemet og vil ikke være tilgjengelig for videre behandling. Beholdningen blir også fjernet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]