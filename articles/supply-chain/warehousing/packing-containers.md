---
title: Pakkebeholdere til forsendelse
description: Denne artikkelen beskriver pakkeprosessen som lar deg validere lagervarer og pakke dem i beholdere.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708790"
---
# <a name="pack-containers-for-shipment"></a>Pakkebeholdere til forsendelse

[!include [banner](../../includes/banner.md)]

Beholderpakkeprosessen lar deg validere lagervarer og pakke dem i beholdere. I løpet av denne prosessen plukker lagerarbeidere vanligvis lagervarer fra masselagringsområder og flytter dem til et pakkeområde. Der kontrollerer flere lagerarbeidere vareantallene og -typene, og tildeler dem til riktige beholderstørrelser. Når en beholder er fullstendig pakket, lukkes den og flyttes til utleveringsområdet der den gjøres klar til forsendelse.

Beholdere representerer fysiske strukturer som varer er pakket i, og du kan spore beholderinformasjon i systemet. Denne informasjonen kan være nyttig under transportplanlegging, spesielt hvis du beregner forsendelseskostnader basert på beholdere. Før du sender, kan du se antall beholdere som brukes i en forsendelse, hvilke typer beholdere som brukes og de fysiske dimensjonene til hver beholder (for eksempel totalt volum og vekt).

Flere relaterte utgående lagerfunksjoner kan brukes med beholdere. Hvis du vil ha mer informasjon, kan du se følgende artikler:

- [Bølgecontainerbruk](wave-containerization.md)
- [Utgående sortering](outbound-sorting.md)
- [Forsendelse av småpakker](small-parcel-shipping.md)
- [Bekreft og overfør](confirm-and-transfer.md)
- [Angi ulike dimensjoner for pakking og lagring](packing-vs-storage-dimensions.md)
- [Pakkearbeid for pakking av utgående beholdere og behandling av forsendelser](packing-work.md)
- [Pakke containere med mobilappen Warehouse Management](warehouse-app-packing-containers.md)
- [Eksempelscenario - Pakke containere med mobilappen Warehouse Management](warehouse-app-pack-containers-scenario.md)
- [Skriv ut containeretiketter](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Definer lageret for å bruke manuelle pakkeoperasjoner

Det er to grunnleggende måter å organisere utgående operasjoner på:

- **Bølgeoppretting og - behandling** – Arbeidere plukker varer basert på utgående lagerarbeid. Deretter plasserte de varene direkte i en utgående forsendelseslokasjon, der de er klare for umiddelbar forsendelse. Hvis du vil ha informasjon om hvordan du konfigurerer og bruker denne prosessen, kan du se [Bølgeoppretting og -behandling](wave-processing.md).
- **Manuell pakking ved pakkestasjoner –** Denne prosessen har en tilleggsoperasjon mellom plukk- og forsendelsesoperasjonene. I stedet for å plassere lagerbeholdningen i en *forsendelseslokasjon*, plasserte arbeiderne det på en *pakkelokasjon*. Deretter administrerer de pakkeprosessen ved pakkestasjonen ved å bruke siden **Pakk** i nettklienten. Først må du konfigurere systemet som beskrevet i denne delen for å aktivere denne prosessen.

### <a name="set-up-warehouse-locations-for-packing"></a>Konfigurer lagerlokasjoner for pakking

Du må ha minst én pakkelokasjon der arbeidere skal plassere lagervarer slik at de kan pakkes inn i beholdere. Hvis du vil ha mer informasjon om hvordan du oppretter lagerlokasjoner, kan du se [Konfigurer lokasjoner i et WMS-aktivert lager](tasks\configure-locations-wms-enabled-warehouse.md). Underdelene nedenfor beskriver hvordan du oppretter og konfigurerer pakkelokasjoner.

#### <a name="set-up-location-types-for-packing"></a>Konfigurer lokasjonstyper for pakking

Du må definere en *lokasjonstype* for pakkelokasjonene. Lokasjonstyper kan brukes som filtreringsalternativer for å styre de ulike lagerstyringsprosessene. Navnet på hver lokasjonstype beskriver vanligvis noe om hvordan denne lokasjonstypen skal brukes. Lokasjonstypen du definerer her, må være tilknyttet hver lokasjon som brukes til pakkeoperasjoner.

Følg denne fremgangsmåten for å konfigurere en lokasjonstype.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonstyper**.
1. I handlingsruten velger du **Ny** for å legge til en lokasjonstype i rutenettet.
1. Angi følgende felter for den nye lokasjonstypen:

    - **Lokasjonstype** – Angi et navn på lokasjonstypen. Hvert navn må være unikt og bør beskrive noe om hvordan lokasjonstypen skal brukes.
    - **Beskrivelse** – Angi en kort beskrivelse av lokasjonstypen.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Informer systemet om pakkelokasjonstypen

Når du har opprettet en lokasjonstype, må du konfigurere systemet til å gjenkjenne den som lokasjonstypen som skal brukes for pakkeoperasjoner.

Følg denne fremgangsmåten for å angi lokasjonstypen som brukes til pakkeoperasjoner.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**
2. Sett feltet **Pakkelokasjonstype** til lokasjonstypen du vil bruke til å identifisere pakkestasjoner, i fanen **Generelt** på hurtigfanen **Lokasjonstyper**.

> [!NOTE]
> Hvis du oppgraderer fra en versjon av Microsoft Dynamics AX, er statusen *Pakkes* fjernet fra forsendelser og belastninger, fordi den ikke fungerte konsekvent og utløste overflødige data. Derfor er listesidene **I forsendelser** og **Belastninger i pakking** avskrevet. Beholdersom som må pakkes, spores på lokasjonsnivå.
>
> I tidligere versjoner definerte du pakkelokasjonen ved å bruke **Profil-ID for pakkelokasjon** i fanen **Pakking** på siden **Lagerstyringsparametere** for å angi en *lokasjonsprofil*. I den nåværende versjonen bruker du feltet **Pakkelokasjonstype** i fanen **Generelt** på siden **Lagerstyringsparametere** til å angi en *lokasjonstype*, som beskrevet i denne artikkelen. Det nye feltet er bedre samkjørt med prosessen for identifisering av oppsamlingslokasjoner og endelig forsendelseslokasjoner.
>
> Selv om du kan fortsette å bruke det gamle feltet **Profil-ID til pakkelokasjon**, anbefaler vi at du begynner å bruke det nye feltet **Pakkelokasjonstype** i stedet, fordi det gamle feltet til slutt blir avskrevet.
>
> Hvis du fjerner merket for det gamle feltet **Profil-ID for pakkelokasjon** og deretter lagrer siden, blir feltet permanent deaktivert. For installasjoner der feltet **Profil-ID for pakkelokasjon** aldri har blitt brukt, er den alltid deaktivert. Når du har fjernet innstillingen for feltet **Profil-ID for pakkelokasjon**, bruker du innstillingene som beskrives i denne artikkelen, til å definere og identifisere pakkelokasjonen.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Konfigurer lokasjonsprofiler for pakkelokasjoner

Hver *lokasjonsprofil* oppretter informasjon og regler som gjelder de tilknyttede lokasjonene. Siden du trenger minst én lokasjon for bruk til pakkeoperasjoner, må du opprette en lokasjonsprofil for den i tillegg til en lokasjonstype. Hver profil kan brukes av et hvilket som helst antall lokasjoner. Lokasjoner som brukes til pakking, må være konfigurert til å spore lisensavtaler.

Følg denne fremgangsmåten for å definere en lokasjonsprofil for en pakkelokasjon.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg en eksisterende profil fra listeruten, eller velg **Ny** i handlingsruten for å opprette en ny en.
1. I toppteksten i den nye eller valgte profilen angir du følgende felter:

    - **Lokasjonsprofil-ID** – Angi en unik ID for profilen.
    - **Navn** – Angi et beskrivende navn for profilen.

1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Lokasjonsformat** – Velg lokasjonsformatet som skal brukes for nåværende lokasjon. Lokasjonsformatene er et navngivningssystem som brukes til å opprette unike og konsekvente navn for de ulike lokasjonshylleposisjonene som brukes i et lager. Hvis du ikke allerede har det formatet du trenger, kan du opprette det ved å gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsformater**. Hvis du vil ha mer informasjon, kan du se [Konfigurere lokasjoner i et WMS-aktivert lager](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Lokasjonstype** – Velg lokasjonstypen som er definert som pakkelokasjonstype på siden **Lagerstyringsparametere**, som beskrevet tidligere i denne artikkelen.
    - **Bruk sporing av nummerskilt** – Velg *Ja* for dette alternativet for pakkelokasjoner. Systemet må kunne spore nummerskilt-ID-er ved for lisens på pakkelokasjoner slik at det kan kontrollere pakkeprosessen.
    - **Tillat negativt lager** – Sett dette alternativet til *Nei* for pakkelokasjoner.
    - **Tillat blandede varer** – Sett dette alternativet til *Ja* for pakkelokasjoner. Denne innstillingen er nødvendig fordi mange forskjellige varenumre vanligvis blir hentet til pakkelokasjoner samtidig.
    - **Tillat blandede lagerstatuser** – Sett dette alternativet til *Ja* for pakkelokasjoner. Denne innstillingen er nødvendig fordi varer som har forskjellige lagerstatuser, vanligvis blir hentet til pakkelokasjoner samtidig.
    - **Tillat blandede lagerpartier** – Sett dette alternativet til *Ja* for pakkelokasjoner. Dette alternativet er satt til *Ja* automatisk når **Tillat blandede varer**-alternativet er satt til *Ja*.

#### <a name="set-up-packing-locations"></a>Definer pakkelokasjoner

Du må ha minst én *lokasjon* der arbeidere skal plassere lagervarer som må pakkes inn i beholdere.

Følg denne fremgangsmåten for å legge til en pakkelokasjon.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.
1. I handlingsruten velger du **Ny** for legge til en lokasjon.
1. Angi følgende felter for den nye lokasjonen:

    - **Lager** – Angi lageret der standard pakkelokasjonen må finnes.
    - **Lokasjon** – Angi et navn på den nye lokasjonen.
    - **Lokasjonsprofil-ID** – Pass på at du angir ID-en som du opprettet i den forrige delen.

## <a name="set-up-the-packing-process"></a>Definer pakkeprosessen

Denne delen beskriver hvordan du konfigurerer innstillinger som aktiverer pakkeprosessen, og lar arbeidere pakke lager i beholdere.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Definere policyer for containerpakking

Hver *beholderpakkepolicy* definerer hvordan en beholder skal behandles. Hver gang du oppretter en ny beholder, velger du også en pakkepolicy for beholder som skal brukes for den.

Følg denne fremgangsmåten for å definere en policy for containerpakking.

1. Gå til **Lagerstyring \> Oppsett \> Containere \> Policyer for containerpakking**.
1. Velg en eksisterende policy fra listeruten, eller velg **Ny** i handlingsruten for å opprette en ny en.
1. I toppteksten i den nye eller valgte policyen angir du følgende felter:

    - **Pakkepolicy for beholder** – Angi et unikt navn på policyen.
    - **Beskrivelse** – Skriv inn et beskrivende navn for policyen.

1. Angi følgende felter i fanen **Oversikt**: Ved hjelp av disse feltene kan du angi hvilke handlinger som skal utføres når beholderen er lukket, om den skal fungere med eller uten arbeidsoppretting og når beholderen skal frigis fra pakkestasjonen.

    - **Lager** – Velg lageret der pakkepolicyen gjelder.
    - **Standardlokasjon for sluttforsendelsen** – Angi den foretrukne lokasjonen for beholderen etter at den er lukket. Dette feltet er bare tilgjengelig når feltet **Frigivelsespolicy for beholder** er satt til *Gjør tilgjengelig på endelig leveringslokasjon*.
    - **Standardlokasjon for sortering** – Dette feltet brukes med funksjonen for [utgående sortering](outbound-sorting.md).
    - **Vektenhet** – Velg standard måleenhet som skal brukes når en beholder lukkes og manifesteres. Denne måleenheten vil vanligvis være måleenheten som brukes av en skala ved pakkestasjonen. Dette feltet gjelder policyer med eller uten arbeidsoppretting.
    - **Avslutningspolicy for beholder** – Velg et av de følgende alternativene for å definere hva som skal skje når beholderen lukkes:

        - *Automatisk frigivelse* – Beholderen blir betraktet som frigitt fra pakkestasjonen, og handlingen som er angitt i feltet **Frigivelsespolicy for beholder**, utløses.
        - *Forsinket frigivelse* – Beholderen frigis ikke umiddelbart fra pakkestasjonen. En lagerarbeider må frigi den manuelt senere.
        - *Valgfritt* – Mens en arbeider lukker beholderen, kan de velge om beholderen skal frigis.

        Hvis pakkestasjonen hovedsakelig håndterer enkeltbeholdere som sendes direkte til kundene, er den mest naturlig tilnærmingen å frigi beholdere umiddelbart. Hvis pakkestasjonen håndterer forsendelser som består av flere beholdere eller til og med paller, er det sannsynligvis best å utsette frigivelsen til hele forsendelsen eller pallen er pakket og er klar til plukking.

    - **Frigivelsespolicy for beholder** – Velg et av de følgende alternativene for å definere hva som skal skje når beholderen frigis fra pakkelokasjonen:

        - *Gjør tilgjengelig på det endelige forsendelsesstedet* – Oppdater beholderen til den endelige forsendelseslokasjonen. Hvis du velger dette alternativet bruker du feltet **Standardlokasjon for sluttforsendelsen** til å angi den foretrukne lokasjonen for beholderen etter at den er lukket.
        - *Opprett arbeid for å flytte beholderen fra pakkestasjonen* – Opprett arbeid for å flytte beholderen fra pakkestasjonen til oppsamlingsområdet eller direkte til oppsamlingsområdet. Bruk **Arbeidsmal**-feltet til å angi arbeidsmalen som skal brukes når arbeid opprettes for beholderen.
        - *Tildel beholder til utgående sorteringsposisjon* – Dette alternativet brukes med funksjonen for [utgående sortering](outbound-sorting.md).

        I de fleste tilfeller anbefaler vi at du oppretter arbeid for å flytte beholdere, fordi denne fremgangsmåten representerer de faktiske manuelle prosessene på lageret bedre. For enkle scenarioer eller situasjoner der pakkeforsendelse finner sted direkte i området der pakkestasjonen er plassert, kan det imidlertid være å foretrekke for at beholderen skal være tilgjengelig umiddelbart på det endelige forsendelsesstedet.

    - **Arbeidsmal** – Velg arbeidsmalen som skal brukes når arbeid opprettes for beholderen. Dette feltet er bare tilgjengelig når feltet **Frigivelsespolicy for beholder** er satt til *Opprett arbeid for å flytte beholderen fra pakkestasjonen* og er knyttet til en arbeidsordretype som kalles *Pakket beholderplukking*. Hvis du vil ha mer informasjon om maler, kan du se [Arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).

    I de gjenværende trinnene konfigurerer du innstillinger som er knyttet til tilknytning til *manifestering*. Manifestering er prosessen med å angi vekten til en beholder, beholdergruppe eller forsendelse, sammen med sporings-ID-en som mottas fra en transportleverandør. Dynamics 365 Supply Chain Management integreres ikke med eksterne transportleverandørsystemer. I stedet må lagerarbeidere skrive ut etiketter som mottas fra transportleverandøren, og så skanne et sporingsnummer når de fullfører manifestprosedyren.

    Siden manifestkravene varierer fra kunde til kunde, og til og med fra forsendelse til forsendelse, gir pakkepolicyer en betydelig fleksibilitet i arbeidsflyten. Du kan definere beholdere, beholdergrupper og forsendelser i en hvilken som helst kombinasjon.

    Hvis du bruker en fremgangsmåte for flere nivåer, må arbeidere ta vare på alle beholdere før de finner den tilknyttede beholdergruppen, og de må sørge for at alle beholdergruppene trenger hjelp før de finner den tilknyttede forsendelsen.

1. I hurtigfanen **Beholdermanifest** angir du følgende felter:

    - **Automatisk manifest ved beholderlukking** – Sett dette alternativet til *Ja* for å bruke informasjon om viktig informasjon som en del av beholderlukkingsprosessen. Hvis du ikke bruker transportintegrering, må informasjonen registreres manuelt.
    - **Manifestkrav for beholder** – Velg et av følgende alternativer:

        - *Ingen* – Ingen manifestprosess blir brukt.
        - *Manuell* – Manifestering kreves pakkearbeidsflyten. Systemet tillater ikke at en beholder lukkes eller frigis før lukking er fullført.
        - *Transportstyring* – Manifestering blir utført ved hjelp av TMS-vurderingsmotorer (Transport Management). Fordi dette alternativet krever egendefinert utvikling for å implementere en bestemt motor for transportleverandøren, vil det ikke fungere som standard i nåværende versjon.

    - **Skriv ut beholderinnhold** – Sett dette alternativet til *Ja* for å skrive ut beholderinnholdsrapporten automatisk når en beholder registreres som lukket. Rapporten kan skrives ut på forespørsel.

1. Velg et av følgende alternativer i feltet **Manifestkrav for beholdergruppe** i hurtigfanen **Manifest for beholdergruppe**:

    - *Ingen* – Beholdergruppemanifestet blir ikke inkludert som et krav i pakkearbeidsflyten.
    - *Manuell* – Beholdergruppemanifestet blir inkludert som et krav i pakkearbeidsflyten. Alle beholdere som er inkludert i gruppen, må være lukket før gruppen kan manifesteres. Velg dette alternativet hvis du må fullføre et manifest for hver beholdergruppe som er pakket på pakkestasjonen. Du velger vanligvis dette alternativet hvis beholdere er pakket på en pall og hele pallen kan manifesteres.

    > [!NOTE]
    > Den nåværende versjonen støtter ikke manifestrapporter for beholdergrupper, og det er ingen TMS-motorstøtte for beholdergrupper.

1. I hurtigfanen **Forsendelsesmanifest** angir du følgende felter:

    - **Manifestkrav for forsendelse** – Velg et av følgende alternativer:

        - *Ingen* – Forsendelsesmanifestet blir ikke inkludert som et krav i pakkearbeidsflyten.
        - *Manuell* – Forsendelsesmanifestet blir inkludert som et krav i pakkearbeidsflyten. Ingen beholdere for en forsendelse kan frigis før manifestering er fullført.
        - *Transportstyring* – Manifestering blir utført ved hjelp av TMS-vurderingsmotorer. Fordi dette alternativet krever egendefinert utvikling for å implementere en bestemt motor for transportleverandøren, vil det ikke fungere som standard i nåværende versjon.

        Forsendelsesmanifestering bør aktiveres hvis du må fullføre en utvidelse for hele forsendelsen som pakkes ved pakkestasjonen. Det brukes som regel når det kreves én konsolidert forsendelse selv om forsendelsen består av flere beholdere eller beholdergrupper.

    - **Skriv ut følgeseddel** – Sett dette alternativet til *Ja* for å skrive ut følgeseddelen automatisk som en del av forsendelsesmanifestet. Følgeseddelen kan skrives ut på forespørsel.

### <a name="set-up-container-types"></a>Definere containertyper

Under den manuelle pakkeprosessen må det opprettes beholdere før varer kan pakkes inn i dem. Hver beholder må være basert på en *beholdertype*, som definerer beholderens maksimale fysiske volum og vektkapasitet.

Følg denne fremgangsmåten for å opprette en beholdertype.

1. Gå til **Lagerstyring \> Oppsett \> Beholdere \> Beholdertyper**.
1. I handlingsruten velger du **Ny** for å legge til en beholdertype.
1. Angi følgende felter for den nye beholdertypen:

    - **Beholdertypekode** – Angi en unik ID for beholdertypen.
    - **Beskrivelse** – Angi en beskrivelse av den nye beholdertypen.
    - **Taravekt** – Angi den faktiske eller beregnede vekten til beholderen.
    - **Maksimums nettovekt** – Angi den maksimale vekten som beholderen tåler.

1. Angi de fysiske dimensjonene til selve beholderen i feltene **Lengde**, **Bredde**, **Høyde** og **Volum** i **Beholderdimensjoner**-delen.
1. Angi maksimum fysiske dimensjoner som beholderen kan håndtere, i feltene **Lengde**, **Bredde**, **Høyde** og **Volum** i **Maksimalt**-delen.
1. Du kan definere flere attributter for beholdertyper som er knyttet til andre operasjoner som bruker beholdere. Hvis du vil ha mer informasjon, kan du se [Containerbruk](wave-containerization.md).

> [!NOTE]
> For den manuelle pakkeprosessen bruker systemet bare verdien i feltet **Maksimal nettovekt** og verdien i **Volum**-feltet i **Maksimum**-delen.

### <a name="set-up-packing-profiles"></a>Definere pakkeprofiler

*Pakkeprofiler* er nødvendig for pakkeprosessen. De kan velges eller angis som standard når du starter en pakkeoperasjon på siden **Pakke**.

Følg denne fremgangsmåten for å definere en pakkeprofil.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.
1. Velg en eksisterende profil fra listeruten, eller velg **Ny** i handlingsruten for å opprette en ny en.
1. I toppteksten i den nye eller valgte profilen angir du følgende felter:

    - **Pakkeprofil-ID** – Angi en kort ID for profilen.
    - **Beskrivelse** – Angi en beskrivelse av pakkeprofilen.
    - **Pakkepolicy for beholder** – Velg pakkepolicyen som gjelder profilen. Hvis du vil ha mer informasjon, kan du se delen [Konfigurer pakkepolicyer for beholder](#packing-policy) i denne artikkelen.
    - **Beholder-ID-modus** – Velg om en beholder-ID skal genereres automatisk når det opprettes en beholder, eller om den må opprettes manuelt.
    - **Beholdertyper** – Velg beholdertypen som brukes som standard når det opprettes en ny beholder.
    - **Opprett automatisk beholder ved beholderlukking** – Merk av i denne avmerkingsboksen for å opprette en ny beholder automatisk hvis den forrige beholderen er lukket, og en eller flere linjer blir værende i den nåværende forsendelsen.

### <a name="set-up-warehouse-workers"></a>Definere lagerarbeidere

Hver bruker eller arbeider som pakker beholdere ved hjelp av side **Pakke** i nettklienten eller *Pakking*-aktivitetskoden i Warehouse Management-mobilappen, må ha en brukerkonto som er knyttet til en *arbeider/person*-post som de nødvendige sikkerhetstilgangsrettighetene er tildelt. (Hvis du vil ha informasjon om hvordan du konfigurerer brukere, kan du se [Opprett nye brukere](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Følg denne fremgangsmåten for å definere en *arbeider/person*-post for pakkeprosessen.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. I handlingsruten velger du **Ny** for legge til en arbeidsbruker.
1. Sett **Arbeider**-feltet til den eksisterende arbeiderposten som er definert i **Personale**-modulen for brukeren som skal fullføre pakkeprosessen.
1. Angi følgende felt i hurtigfanen **Profil**.

    - **Policy for containerpakking** – Velg en policy for containerpakke som definerer hvordan containere ved pakkestasjonen skal behandles. Policyen for containerpakke som du velger, forhåndsdefineres for arbeideren når de åpner pakkestasjonen. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Forbedret pakkefunksjonalitet](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkeprofil-ID** – Velg en pakkeprofil-ID som definerer emballasjepolicyen og containerinnstillingene som skal brukes. Hvis den valgte pakkeprofil-ID-en er knyttet til en pakkepolicy for beholder, kan du ikke endre innstillingen for feltet **Pakkepolicy for beholder** på denne siden.

1. Velg standardområdet, lageret og lokasjonen som gjelder arbeideren, i hurtigfanen **Standard pakkestasjon**.
1. Hvis du vil bruke Warehouse Management-mobilappen til å administrere og registrere beholderpakkearbeid, kan du bruke hurtigfanen **Brukere** til å definere en eller flere kontoer som arbeideren kan bruke til å logge seg på appen. Hvis du vil ha mer informasjon, kan du se [Brukerkontoer for mobilenhet](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Eksempelscenario

Denne delen inneholder et eksempelscenario som viser hvordan du oppretter en ordre og pakker varene.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke dette scenarioet som en veiledning for å bruke funksjonen i et produksjonssystem. I så fall må du imidlertid bytte dine egne verdier for hver innstilling som beskrives her.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Logg deg på som en bruker som kan gjøre pakkearbeid

Logg deg på Supply Chain Management ved å bruke en brukerkonto som har de nødvendige tillatelsene for å pakke beholdere. Brukeren *Julia Funderburk* er inkludert som en del av demodataene, og har de nødvendige tillatelsene. Denne brukeren har bruker-ID-en *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Opprett en salgsordre og fullfør arbeidet

Følg denne fremgangsmåten når du skal opprette en salgsordre, og fullfør arbeidet med å flytte de bestilte varene til pakkestasjonen.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du *US-005*.
1. Velg **OK** for å lukke dialogboksen.
1. Den nye salgsordren åpnes, og inkluderer en enkelt, tom linje i hurtigfanen **Salgsordrelinjer**. Angi følgende verdier for den nye ordrelinjen:

    - **Varenummer:** *A0001*
    - **Antall:** *2*
    - **Område:** *6*
    - **Lager:** *62*

1. Mens ordrelinjen fremdeles er valgt, velger du **Lager \> Reservasjon** på verktøylinjen for **Salgsordrelinjer**.
1. På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    En melding viser forsendelsen og bølge-ID-ene for ordren.

1. Mens ordrelinjen fremdeles er valgt, velger du **Lager** \> **Arbeidsdetaljer** på verktøylinjen for **Salgsordrelinjer**. Hvis du bruker satsvis behandling til å kjøre bølgene, må du kanskje vente en kort stund før arbeidet skal opprettes.
1. På siden **Arbeid** på handlingsruten på fanen **Arbeid** velger du **Fullfør arbeid**.
1. Angi feltet **Bruker-ID** til **62** på siden *Arbeidsfullføring*.
1. Velg deretter **Valider arbeid** i handlingsruten.
1. Når du mottar en melding som angir at arbeidet er gyldig, velger du **Fullfør arbeid** for å fullføre prosessen med å plukke lagervarene og legge dem til i *pakkelokasjonen*.
1. Legg merke til verdien for **forsendelses-ID** som vises for arbeidet i det øvre rutenettet.

### <a name="pack-the-ordered-items-into-a-container"></a>Pakk de bestilte varene i en beholder

Lagervarene er nå sendt til pakkeområdet og er klare til pakkes i beholdere. Følg denne fremgangsmåten for å opprette en ny beholder i systemet og pakke den.

1. Gå til **Lagerstyring \> Pakking og containerbruk \> Pakke**.
1. I dialogboksen **Velg pakkstasjon** angir du følgende verdier:

    - **Område:** *6*
    - **Lager:** *62*
    - **Plassering:** *Pakke*
    - **Pakkeprofil-ID**: *WH62*

1. Velg **OK**.
1. På siden **Pakke** i feltet **Nummerskilt eller forsendelse** angir du forsendelses-ID-en du skrev ned tidligere. Nå skal du se de gjenværende utpakkede varene i hurtigfanen **Åpne linjer**.
1. Velg **Ny beholder** i handlingsruten for å opprette en beholder i systemet.
1. I dialogboksen **ID for ny beholder** angir du feltet **Beholdertype** til *SmallBox*.
1. Velg **OK** for å opprette beholderen.
1. Velg **OK** for å gå tilbake til siden **Pakke**. Hurtigfanen **Åpne beholdere** viser nå **beholder-ID-verdien** for beholderen som du opprettet.
1. I dette scenarioet pakker du bare én av de bestilte varene foreløpig. Angi derfor følgende verdier på **Varepakking**-hurtigfanen:

    - **Antall:** *1.00*
    - **Identifikator:** *A0001*

    Rett etter at du har valgt **identifikatorverdien**, oppdaterer siden hurtigfanene **Åpne linjer** og **Alle linjer** for å angi at én vare er pakket. Du skal nå ha pakket én av de to stykkene av varen *A0001*.

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** velger du **Hent systemvekt** for å fylle ut standardverdi for **bruttovekt**.
1. Velg **OK** for å lukke beholderen.

> [!TIP]
> Det er forskjellige måter å vise beholdere på, basert på kontekst. Når du for eksempel pakker en forsendelse, er det ofte nyttig å vise enten beholdere som er en del av forsendelsen eller alle beholdere som er fysisk ved en pakkestasjon. Siden **Pakkestasjon** har knapper som du kan bruke til å vise alle åpne og lukkede beholdere ved en pakkestasjon. Disse visningene er ikke begrenset til en bestemt forsendelse. De kan være svært nyttig i situasjoner der en arbeider pakker en beholder og en annen arbeider manifesterer og frigir beholderen.
>
> En konsolidert visning av alle beholdere er også tilgjengelig. Denne visningen er nyttig for brukere som arbeider utenfor konteksten av én enkelt pakkestasjon. For å se den går du til **Lagerstyring \> Pakking og containerbruk \> Beholdere**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
