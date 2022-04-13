---
title: Oppsett av behovsprognose
description: Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b52b970a8040dcba5a1fc59d297dc9ce1a3c53
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470016"
---
# <a name="demand-forecasting-setup"></a>Oppsett av behovsprognose

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du setter opp behovsprognose.  

## <a name="item-allocation-keys"></a>Varefordelingsnøkler

Varetilordningsnøkler oppretter grupper av varer. En behovsprognose beregnes for en vare og dimensjonene bare hvis varen er en del av en varefordelingsnøkkel. Denne regelen brukes for å gruppere et stort antall varer, slik at behovsprognoser kan opprettes raskere. Prognoser opprettes basert på bare historiske data.

En vare og dimensjonene må være en del av bare én varefordelingsnøkkel hvis varefordelingsnøkkelen brukes under oppretting av prognose.

Følg denne fremgangsmåten for å opprette varetildelingsnøkler og legge til en lagerenhet.

1. Gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Varefordelingsnøkler**.
1. Velg en varefordelingsnøkkel i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny. I toppteksten for den nye eller valgte nøkkelen angir du følgende felter:

    - **Varetilordningsnøkkel** – Angi et unikt navn på nøkkelen.
    - **Navn** – Angi et beskrivende navn for nøkkelen.

1. Følg ett av disse trinnene for å legge til varer i den valgte varetildelingsnøkkelen eller fjerne varer:

    - På hurtigfanen **Varefordeling** bruker du knappene **Ny** og **Slett** på verktøylinjen for å legge til eller fjerne elementer etter behov. Velg varenummeret for hver rad, og tilordne deretter dimensjonsverdier i de andre kolonnene etter behov. Velg **Vis dimensjoner** på verktøylinjen for å endre settet med dimensjonskolonner som vises i rutenettet. (Verdien i kolonnen **Prosent** ignoreres når behovsprognoser genereres.)
    - Hvis du vil legge til et stort antall elementer i nøkkelen, velger du **Tilordne varer** i handlingsruten for å åpne en side der du kan finne og tilordne flere varer til den valgte nøkkelen.

> [!IMPORTANT]
> Vær forsiktig så du bare tar med relevante varer i hver varetildelingsnøkkel. Unødvendige varer kan føre til økte kostnader når du bruker Microsoft Azure Machine Learning.

## <a name="intercompany-planning-groups"></a>Grupper for konsernintern planlegging

Behovsprognose kan generere prognoser på tvers av firmaer. I Dynamics 365 Supply Chain Management grupperes firmaer som er planlagt sammen, i samme konsernintern planleggingsgruppe. Hvis du vil angi hvilke varetildelingsnøkler som skal vurderes for etterspørselsprognoser, knytter du en varetildelingsnøkkel til det konserninterne planleggingsgruppemedlemmet.

> [!IMPORTANT]
> Planleggingsoptimalisering støtter for øyeblikket ikke konserninterne planleggingsgrupper. Hvis du vil utføre konsernintern planlegging som bruker planleggingsoptimalisering, må du definere satsvise jobber for hovedplanlegging som inkluderer hovedplaner for alle de relevante firmaene.

Hvis du vil konfigurere konserninterne planleggingsgrupper, følger du denne fremgangsmåten.

1. Gå til **Hovedplanlegging \> Oppsett \> Konserninterne planleggingsgrupper**.
1. Velg en planleggingsgruppe i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny. I toppteksten for den nye eller valgte gruppen angir du følgende felter:

    - **Navn** – Angi et unikt navn for planleggingsgruppen.
    - **Beskrivelse** – Angi en kort beskrivelse av planleggingsgruppen.

1. I hurtiggruppen **Gruppemedlemmer for konsernintern planleggingsgruppe** bruker du knappene på verktøylinjen til å legge til en rad for hvert firma (juridisk enhet) som skal være en del av gruppen. For hver rad angir du feltene nedenfor:

    - **Juridisk enhet** – Velg navnet på et firma (juridisk enhet) som er medlem av den valgte gruppen.
    - **Planleggingssekvens** – Tilordne ordren som firmaet skal behandles i, i forhold til andre firmaer. Lave verdier behandles først. Denne ordren kan være viktig når etterspørselen etter ett firma påvirker andre firmaer. I disse tilfellene bør firmaet som leverer etterspørselen, behandles sist.
    - **Hovedplan** – Velg hovedplanen som skal utløses for det gjeldende firmaet.
    - **Automatisk kopiering til statisk plan** – Merk av for dette alternativet for å kopiere resultatet av planen til den statiske planen.
    - **Automatisk kopiering til dynamisk plan** – Merk av for dette alternativet for å kopiere resultatet av planen til den dynamiske planen.

1. Hvis ingen varefordelingsnøkler er tilordnet til medlemmer av konsernintern planleggingsgruppe, beregnes en behovsprognose som standard for alle varer som er tilordnet til alle varefordelingsnøkler fra alle firmaer. Flere filtreringsalternativer for firmaer og varetildelingsnøkler er tilgjengelige i dialogboksen **Generer statistisk basislinjeprognose** (**Hovedplanlegging \> Prognose \> Behovsprognose \> Generer statistisk basislinjeprognose basislinjeprognose**). Hvis du vil tilordne varetildelingsnøkler til et firma i den valgte konserninterne planleggingsgruppen, velger du firmaet, og i hurtigfanen **Gruppemedlemmer for konsernintern planleggingsgruppe** velger du **Varetildelingsnøkler** på verktøylinjen.

> [!IMPORTANT]
> Vær forsiktig så du bare tar med relevante varetildelingsnøkler i hver konsernintern planleggingsgruppe. Unødvendige varer kan føre til økte kostnader når du bruker Azure Machine Learning.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Definere parametere for behovsprognose

Bruk siden **Parametere for behovsprognose** til å konfigurere flere alternativer som kontrollerer hvordan etterspørselsprognoser vil fungere i systemet.

### <a name="open-the-demand-forecasting-parameters-page"></a>Åpne siden Parametere for behovsprognose

Hvis du vil definere parametere for behovsprognose, kan du gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Parametere for behovsprognose**. Fordi behovsprognose kjører mellom firmaer er oppsettet globalt. Det brukes med andre ord for alle juridiske enheter (selskaper).

### <a name="general-settings"></a>Generelle innstillinger

Bruk kategorien **Generelt** på siden **Parametere for behovsprognose** for å definere generelle innstillinger for behovsprognose.

#### <a name="demand-forecast-unit"></a>Behovsprognoseenhet

Behovsprognose genererer prognosen i antall. Enheten som antallet som skal uttrykkes i, må derfor angis i feltet **Behovsprognoseenhet**. Dette feltet definerer enheten som skal brukes for alle behovsprognoser, uavhengig av de vanlige lagerenhetene for hvert produkt. Ved å bruke en konsekvent prognoseenhet sørger du for at aggregering og prosentvis fordeling gir mening. Hvis du vil ha mer informasjon om aggregering og prosentvis fordeling, se [Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md).

For hver måleenhet som skal brukes for lagerføringsenheter som er inkludert i behovsprognose, kontrollerer du at det er en regel for konvertering for måleenheten og den generelle måleenheten for prognose som du velger her. Når du genererer en prognose, logges listen over varer som ikke har en konvertering av måleenhet. Derfor er det lett å rette oppsettet. Hvis du vil ha mer informasjon måleenheter og hvordan du konverterer dem, kan du se [Administrere måleenheter](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Transaksjonstyper

Bruk feltene i hurtigfanen **Transaksjonstyper** til å velge transaksjonstypene som brukes når den statistiske basislinjeprognosen genereres.

Behovsprognose kan brukes til å beregne både avhengig behov og uavhengig behov. Hvis for eksempel bare alternativet **Salgsordre** er satt til *Ja*, og hvis alle varene som vurderes for behovsprognose, er varer som selges, beregner systemet uavhengig behov. Kritiske delkomponenter kan imidlertid legges til i varefordelingsnøkler og inkluderes i behovsprognose. I så fall, hvis boksen **Produksjonslinje** er satt til *Ja*, beregnes en avhengige prognose.

Du kan overstyre transaksjonstyper for én eller flere bestemte varetildelingsnøkler ved å bruke kategorien **Varetildelingsnøkler**. Denne kategorien inneholder lignende felt.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Velge hvordan basislinjeprognosen skal opprettes

Feltet **Kopier over historisk behov** lar deg velge metoden som skal brukes til å opprette en basislinjeprognose. Tre metoder er tilgjengelige:

- *Kopier over historisk behov* – Opprett prognoser ved bare å kopiere historiske data.
- *Azure Machine Learning Service* – Bruk en prognosemodell som bruker Azure Machine Learning Service. Azure Machine Learning Service er den gjeldende maskinopplæringsløsningen for Azure. Vi anbefaler derfor at du bruker det hvis du vil bruke en prognosemodell.
- *Azure Machine Learning* – Bruk en prognosemodell som bruker Azure Machine Learning Studio (klassisk). Azure Machine Learning Studio (klassisk) er blitt avviklet, og vil snart bli fjernet fra Azure. Derfor anbefaler vi at du velger *Azure Machine Learning Service* hvis du setter opp behovsprognose for første gang. Hvis du for øyeblikket bruker Azure Machine Learning Studio (classic), bør du planlegge å bytte til Azure Machine Learning Service så snart som mulig.

Du kan overstyre prognosegenereringsmetoden for én eller flere bestemte varetildelingsnøkler ved å bruke kategorien **Varetildelingsnøkler**. Denne kategorien inneholder lignende felt.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Overstyre standard prognosealgoritmeparametere globalt

Standard parametere og verdier for prognosealgoritmer tilordnes på siden **Parametere for behovsprognose** (**Hovedplanlegging \> Oppsett \> Behovsprognose \> Parametere for behovsprognose**). Du kan imidlertid overstyre dem globalt ved å bruke hurtigfanen **Prognosealgoritmeparametere** i fanen **Generelt** på siden **Parametere for behovsprognose**. (Du kan også overstyre dem for bestemte tilordningsnøkler ved å bruke fanen **Varefordelingsnøkler** på siden **Parametere for behovsprognose**.)

Bruk knappene **Legg til** og **Fjern** på verktøylinjen for å fastsette den nødvendige samlingen med parameteroverstyringer. For hver parameter i listen velger du en verdi i **Navn**-feltet, og deretter angir du en passende verdi i **Verdi**-feltet. Alle parametere som ikke er oppført her, vil ta verdiene sine fra innstillingene på siden **Parametere for behovsprognose**. Hvis du vil ha mer informasjon om hvordan du bruker standardsettet med parametere og velger verdier for dem, kan du se delen [Standardparametere og verdier for modeller for etterspørselsprognose](#model-parameters).

### <a name="set-forecast-dimensions"></a>Angi prognosedimensjoner

En prognosedimensjon angir detaljnivået som prognosen er definert for. Firma, område og varetildelingsnøkkel er nødvendige prognosedimensjoner. Du kan også generere prognoser på nivåene for lageret, lagerstatus, kundegruppe, kundekonto, land/område, tilstand, og/eller varenivå og på alle varedimensjonsnivåer. Bruke fanen **Prognosedimensjoner** på siden **Parametere for behovsprognose** for å velge settet for prognosedimensjoner som brukes når behovsprognosen genereres.

Du kan legge til prognosedimensjoner i listen over dimensjonene som skal brukes for behovsprognose, når som helst. Du kan også fjerne prognosedimensjoner fra listen. Manuelle justeringer går imidlertid tapt hvis du legger til eller fjerner en prognosedimensjon.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Definere overstyringer for bestemte varetildelingsnøkler

Ikke alle varer fungerer på samme måte fra et behovsprognoseperspektiv. Derfor kan du opprette tilordningsnøkkelspesifikke overstyringer for de fleste innstillingene som er definert i kategorien **Generelt**. Unntaket er behovsprognoseenheten. Følg denne fremgangsmåten for å definere overstyringer for en bestemt varetildelingsnøkkel.

1. På siden **Parametere for behovsprognose** bruker du kategorien **Varetildelingsnøkler** til å legge til varetildelingsnøkler i rutenettet til venstre, eller fjerne dem etter behov. Deretter velger du tildelingsnøkkelen du vil definere overstyringer for.
1. På hurtigfanen **Transaksjonstyper** aktiverer du transaksjonstypene du vil bruke til å generere den statistiske basislinjeprognosen for produkter som tilhører den valgte tilordningsnøkkelen. Innstillingene fungerer på samme som i fanen **Generelt**, men de gjelder bare for den valgte varetildelingsnøkkelen. Alle innstillingene her (både *Ja*-verdier og *Nei*-verdier) overstyrer alle **Transaksjonstype**-innstillinger i fanen **Generelt**.
1. I hurtigfanen **Prognosealgoritmeparametere** velger du strategien for prognosegenerering og prognosealgoritmeparameteren som overstyrer for produkter som tilhører den valgte tilordningsnøkkelen. Disse innstillingene fungerer på samme som i fanen **Generelt**, men de gjelder bare for den valgte varetildelingsnøkkelen. Bruk knappene **Legg til** og **Fjern** på verktøylinjen for å definere den nødvendige samlingen med parameteroverstyringer. For hver parameter i listen velger du en verdi i **Navn**-feltet, og deretter angir du en passende verdi i **Verdi**-feltet. Hvis du vil ha mer informasjon om hvordan du bruker standardsettet med parametere og velger verdier for dem, kan du se delen [Standardparametere og verdier for modeller for etterspørselsprognose](#model-parameters).

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Konfigurere tilkoblingen til Azure Machine Learning Service

Bruk kategorien **Azure Machine Learning Service** til å sette opp forbindelsen til Azure Machine Learning Service. Denne løsningen er ett av alternativene for oppretting av basislinjeprognosen. Disse innstillingene i denne kategorien har bare innvirkning når feltet **Strategi for prognosegenerering** er satt til *Azure Machine Learning Service*.

Hvis du vil ha mer informasjon om hvordan du konfigurerer Azure Machine Learning Service og deretter bruker du innstillingene her for å koble til den, kan du se delen [Konfigurere Azure Machine Learning Service](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Konfigurere tilkoblingen til Azure Machine Learning Studio (classic)

> [!IMPORTANT]
> Azure Machine Learning Studio (classic) er blitt avskrevet. Derfor er det ikke lenger mulig å opprette nye arbeidsområder for det i Azure. Den er erstattet av Azure Machine Learning Service, som gir liknende funksjonalitet og mer. Hvis du ikke allerede har brukt Azure Machine Learning, bør du begynne å bruke Azure Machine Learning Service. Hvis du allerede har et arbeidsområde som er opprettet for Azure Machine Learning Studio (classic), kan du fortsette å bruke det til funksjonen er fullstendig fjernet fra Azure. Vi anbefaler imidlertid at du oppdaterer Azure Machine Learning Service så snart som mulig. Selv om programmet vil fortsette å varsle deg om at Azure Machine Learning Studio (classic) er avskrevet, berøres ikke prognoseresultatet. Hvis du vil ha mer informasjon om den nye Azure Machine Learning Service og hvordan du konfigurerer den, kan du se delen [Konfigurere Azure Machine Learning Service](#setup-amls).
>
> Du kan fritt veksle mellom å bruke de nye og gamle maskinopplæringsløsningene med Supply Chain Management så lenge det gamle arbeidsområdet for Azure Machine Learning Studio (classic) forblir tilgjengelig.

Hvis du allerede har et tilgjengelig arbeidsområde for Azure Machine Learning Studio (classic), kan du bruke det til å generere prognoser ved å koble det til Supply Chain Management. Du kan opprette denne tilkoblingen ved fanen **Azure Machine Learning** på siden **Parametere for behovsprognose**. (Innstillingene i denne kategorien har bare virkning når feltet **Strategi for prognosegenerering** er satt til *Azure Machine Learning*.) Angi følgende detaljer for arbeidsområdet Azure Machine Learning Studio (classic):

- API-nøkkel (application programming interface) for webtjenesten
- URL-adresse til webtjenestesluttpunkt
- Azure-lagringskontonavn
- Azure-lagringskontonøkkel

> [!NOTE]
> Azure-lagringskontonavnet og -nøkkel kreves bare hvis du bruker en egendefinert lagring-konto. Hvis du distribuerer den lokale versjonen, må du ha en konto for egendefinert lagring i Azure, slik at Machine Learning får tilgang til historiske data.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Standardparametere og -verdier for modeller for etterspørselsprognose

Når du bruker maskinopplæring til å generere prognoseplanleggingsmodellene, styrer du maskinopplæringsalternativer ved å angi verdier for *prognosealgoritmeparametere*. Disse verdiene sendes fra Supply Chain Management til Azure Machine Learning. Bruk siden **Prognosealgoritmeparametere** til å bestemme hvilke typer verdier som skal oppgis, og hvilke verdier hver av dem skal ha.

For å konfigurere standardparameterne og verdiene som skal brukes for behovsprognosemodellene, går du til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Prognosealgoritmeparametere**. Det finnes et standardsett med parametere. Hver parameter har følgende felt:

- **Navn** – Navnet på parameteren, slik det brukes av Azure. Vanligvis bør du ikke endre dette navnet med mindre du har tilpasset eksperimentet i Azure Machine Learning.
- **Beskrivelse** – Et fellesnavn for parameteren. Dette navnet brukes til å identifisere parameteren andre steder i systemet (for eksempel på siden **Parametere for behovsprognose**).
- **Verdi** – Standardverdien for parameteren. Verdien du bør angi, avhenger av parameteren du redigerer. 
- **Forklaring** – En kort beskrivelse av parameteren og hvordan den brukes. Denne beskrivelsen inneholder vanligvis anbefalinger om gyldige verdier for **Verdi**-feltet.

Følgende parametere angis som standard. (Hvis du noen gang må gå tilbake til denne standardlisten, velger du **Gjenopprett** i handlingsruten.)

- **Konfidensnivåprosent** – Et konfidensintervall består av et verdiområde som fungerer som gode estimater for behovsprognosen. En konfidensnivåprosent på 95 % angir at det er 5 % risiko for at det fremtidige behovet faller utenfor området for konfidensintervallet.
- **Fremtving sesongavhengighet** – Angir om modellen skal tvinges til å bruke en bestemt type sesongavhengighet. Denne parameteren gjelder bare i ARIMA og ETS. Alternativer: *AUTO (standard)*, *INGEN*, *ADDITIVE*, *MULTIPLIKATIV*.
- **Prognosemodell** – Angir hvilken prognosemodell som skal brukes. Alternativer: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALLE*. Hvis du vil velge best mulig tilpasningsmodell, bruker du *ALLE*.
- **Maksimal prognoseverdi** – Angir den største verdien som kan brukes for prognoser. Format: +1E[n] eller numerisk konstant.
- **Minste prognoseverdi** – Angir den minste verdien som kan brukes for prognoser. Format: -1E[n] eller numerisk konstant.
- **Mangler verdierstatning** – Angir hvordan hull i historiske data fylles. Alternativer: *(numerisk verdi)*, *GJENNOMSNITT*, *FORRIGE*, *INTERPOLERT LINEÆR*, *INTERPOLERT POLYNOMISK*.
- **Mangler verdierstatningsområde** – Angir om verdierstatning bare gjelder for datoområdet for hvert enkelt detaljattributt eller for hele datasettet. Følgende alternativer er tilgjengelige for oppretting av datoområdet som systemet bruker til å fylle ut huller i historiske data:

    - *GLOBAL* – Systemet bruker hele datoområdet for alle detaljattributter.
    - *HISTORY_DATE_RANGE* – Systemet bruker et bestemt datoområde som er definert av feltene **Fra dato** og **Til dato** i **Historisk horisont**-delen i dialogboksen **Generer statistisk basislinjeprognose**.
    - *GRANULARITY_ATTRIBUTE* – Systemet bruker datoområdet til det behandlede detaljattributtet.

    > [!NOTE]
    > Et detaljattributt er en kombinasjon av prognosedimensjoner som prognosen utføres mot. Du kan definere prognosedimensjoner på siden **Parametere for behovsprognose**.

- **Tips om sesongavhengighet** – For sesongbaserte data angir du et tips til prognosemodellen for å forbedre prognosenøyaktigheten. Format: heltall som representerer antallet perioder som et behovsmønster gjentar seg selv etter. Fyll for eksempel inn *6* for data som gjentar seg selv hver sjette måned.
- **Prosentandel testsettstørrelse** – Prosentandel historiske data som skal brukes som et testsett for beregning av prognosenøyaktighet.

Du kan overskrive verdiene for disse parameterne ved å gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Parametere for behovsprognose**. Du kan overskrive disse parameterne på siden **Parametere for behovsprognose** på følgende måter:

- Bruk kategorien **Generelt** til å overstyre parameterne globalt.
- Bruk kategorien **Varetildelingsnøkler** til å overstyre parameterne for spesifikke varetildelingsnøkler. Parametere som overstyres for en spesifikk varefordelingsnøkkel, påvirker bare prognosen for varer som er knyttet til denne varefordelingsnøkkelen.

> [!NOTE]
> På siden **Parametere for prognosealgoritme** kan du bruke knappene i handlingsruten til å legge til parametere i listen eller fjerne parametere fra listen. Vanligvis bør du imidlertid bruke denne fremgangsmåten med mindre du har tilpasset eksperimentet i Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Konfigurere Azure Machine Learning Service

Supply Chain Management beregner behovsprognoser ved hjelp av Azure Machine Learning Service, som du må definere og kjøre på eget Azure-abonnement. I denne delen finner du informasjon om hvordan du konfigurerer Azure Machine Learning Service i Azure og deretter kobler til Supply Chain Management-miljøet.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Aktivere Azure Machine Learning Service i funksjonsbehandling

Før du kan bruke Azure Machine Learning Service for behovsprognose, må du aktivere en funksjon i Supply Chain Management for å aktivere integreringen. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *Azure Machine Learning Service for behovsprognose*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Konfigurere maskinlæring i Azure

Hvis du vil gjøre det mulig for Azure å bruke maskinopplæring for å behandle prognosene, må du sette opp et Azure-arbeidsområde for maskinopplæring til dette formålet. Du har to alternativer:

- Hvis du vil konfigurere arbeidsområdet ved å kjøre et skript som leveres av Microsoft, følger du instruksjonene i [Alternativ 1: Kjør et skript for automatisk konfigurering av arbeidsområdet for maskinopplæring](#ml-workspace-script), og gå deretter videre til delen [Konfigurere Azure Machine Learning Service-tilkoblingsparametere i Supply Chain Management](#demand-forecast-parameters).
- Hvis du vil konfigurere arbeidsområdet manuelt, følger du instruksjonene i delen [Alternativ 2: Manuell konfigurering av arbeidsområdet for maskinopplæring](#ml-workspace-manual), og gå deretter videre til delen [Konfigurere Azure Machine Learning Service-tilkoblingsparametere i Supply Chain Management](#demand-forecast-parameters). Dette alternativet tar mer tid, men det gir mer kontroll.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Alternativ 1: Kjør et skript for å konfigurere arbeidsområdet for maskinopplæring automatisk

Denne delen beskriver hvordan du konfigurerer arbeidsområdet for maskinlæring ved hjelp av et automatisert skript som leveres av Microsoft. Hvis du foretrekker det, kan du manuelt konfigurere alle ressursene ved å følge instruksjonene i delen [Alternativ 2: Konfigurere arbeidsområdet for maskinopplæring](#ml-workspace-manual). Du trenger ikke å fullføre begge alternativene.

1. I GitHub åpner du [Malene for Dynamics 365 Supply Chain Management-etterspørselsprognoser med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-repositoriet, og last ned følgende filer:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Åpne et PowerShell-vindu, og kjør **quick_setup.ps1**-skriptet du lastet ned i forrige trinn. Følg instruksjonene på skjermen. Skriptet vil sette opp det nødvendige arbeidsområdet, lagring, standard datalager og beregne ressurser. Du må imidlertid fremdeles opprette de nødvendige pipelinene ved å følge de gjenværende trinnene i denne fremgangsmåten. (Pipelinene er en metode for å starte prognoseskript fra Supply Chain Management.)
1. I Azure Machine Learning Studio laster du opp filen **sampleInput.csv** som du lastet ned i trinn 1, til containeren som kalles *demplan-azureml*. (Skriptet quick_setup.ps1 opprettet denne containeren.) Denne filen er nødvendig for å publisere en pipeline og generere en testprognose. Hvis du vil ha instruksjoner, kan du se [Laste opp en blokkeringsblokk](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. I Azure Machine Learning Studio velger du **Notatblokk** i navigasjonsvinduet.
1. Finn følgende plassering i strukturen **Filer**: **Brukere/\[gjeldende bruker\]/src**.
1. Last opp de gjenværende fire filene du lastet ned i trinn 1, til stedet du fant i forrige trinn.
1. Velg **api_trigger.py** som du akkurat lastet opp, og kjør den. Det vil opprette en pipeline som kan utløses via API.
1. Arbeidsområdet er nå konfigurert. Gå til delen [Konfigurere Azure Machine Learning Service-tilkoblingsparametere i Supply Chain Management](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Alternativ 2: Konfigurere maskinopplæringsarbeidsområdet manuelt

Denne delen beskriver hvordan du konfigurerer arbeidsområdet for maskinopplæring manuelt. Du må bare fullføre prosedyrene i denne delen hvis du bestemte deg for å ikke kjøre det automatiserte konfigurasjonsskriptet, som beskrevet i delen [Alternativ 1: Kjør et skript for å konfigurere arbeidsområdet for maskinopplæring](#ml-workspace-script).

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Trinn 1: Opprette et nytt arbeidsområde

Bruk fremgangsmåten nedenfor for å opprette et arbeidsområde for maskinopplæring.

1. Logg på Azure-portalen.
1. Åpne tjenesten for **maskinlæring**.
1. Velg **Opprett** på verktøylinjen for å åpne **Opprett**-veiviseren.
1. Fullfør veiviseren ved å følge instruksjonene på skjermen. Husk at følgende punkter er i bakhodet når du arbeider:

    - Bruk standardinnstillingene hvis ikke andre punkt i denne listen anbefaler andre innstillinger.
    - Pass på at du velger det geografiske området som samsvarer med området der forekomsten av Supply Chain Management er distribuert. Hvis ikke kan det hende at noen av dataene dine passerer gjennom områdegrensene. Hvis du vil ha mer informasjon, kan du se delen [personvernerklæring](#privacy) senere i dette emnet.
    - Bruk dedikerte ressurser, for eksempel ressursgrupper, lagringskontoer, containerregistrer, Azure-key vault og nettverksressurser.
    - Du må angi et navn på lagringskonto på siden **Konfigurere Azure Machine Learning Service-tilkoblingsparametere**. Bruk en konto som er dedikert til behovsprognose. Behovsprognose-inndata og -utdata lagres i denne lagringskontoen.

Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyten](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Trinn 2: Konfigurer lagring

Bruk fremgangsmåten nedenfor for å konfigurere lagringen.

1. I GitHub åpner du [Malene for Dynamics 365 Supply Chain Management-etterspørselsprognoser med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-repositoriet, og last ned filen **sampleInput.csv**:
1. Åpne lagringskontoen du opprettet i delen [Trinn 1: Opprett en ny arbeidsområde](#create-workspace).
1. Følg instruksjonene i [Opprett en container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) for å opprette en container som kalles *demplan-azureml*.
1. Last opp filen **sampleInput.csv** som du lastet ned i trinn 1, til beholderen du nettopp opprettet. Denne filen er nødvendig for å publisere en pipeline og generere en testprognose. Hvis du vil ha instruksjoner, kan du se [Laste opp en blokkeringsblokk](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Trinn 3: Konfigurere et standard datalager

Bruk fremgangsmåten nedenfor for å konfigurere datalageret.

1. I Azure Machine Learning Studio velger du **Datalagre** i navigasjonsvinduet.
1. Opprett et nytt datalager av typen *Azure Blob Storage* som peker til blob-lagringscontaineren *demplan-azureml* som du opprettet i delen [Trinn 2: Konfigurere lagring](#config-storage). (Hvis godkjenningstypen for det nye datalageret er *Kontonøkkel*, angir du en kontonøkkel for den opprettede lagringskontoen. Hvis du vil ha instruksjoner, kan du se [Behandle tilgangsnøkler for lagringskonto](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Gjør det nye datalageret til standard datalager ved å åpne detaljene og velge **Angi som standard datalager**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Trinn 4: Konfigurere beregningsressurser

Bruk fremgangsmåten nedenfor til å konfigurere en beregningsressurs i Azure Machine Learning Studio for å kjøre prognosegenereringsskriptene.

1. Åpne detaljsiden for arbeidsområdet for maskinopplæring som du opprettet i delen [Trinn 1: Opprette et nytt arbeidsområde](#create-workspace). Finn verdien **Web-URL-verdi for studio**, og velg koblingen for å åpne den.
1. Velg **Beregn** i navigasjonsruten.
1. I fanen **Beregningsforekomster** velger du **Ny** for å åpne en veiviser som hjelper deg med å opprette en ny beregningsforekomst. Følg instruksjonene på skjermen. Beregningsforekomsten vil bli brukt til å opprette behovsprognosepipelinen (Den kan slettes etter at pipeline er publisert.) Bruk standardinnstillingene.
1. I fanen **Beregningsklynger** velger du **Ny** for å åpne en veiviser som hjelper deg med å opprette en ny beregningsklynge. Følg instruksjonene på skjermen. Beregningsklyngen vil bli brukt til å generere etterspørselsprognoser. Innstillingene påvirker ytelsen og det maksimale parallelliseringsnivået for kjøringen. Angi følgende felt, men bruk standardinnstillingene for alle andre felt:

    - **Navn** – Angi *e2ecpucluster*.
    - **Virtuell maskinstørrelse** – Juster denne innstillingen i henhold til volumet av data som du forventer å bruke som inndata for etterspørselsprognoser. Nodeantallet bør ikke overskride 11, fordi det kreves en node for å utløse generering av behovsprognoser, og maksimalt antall noder som deretter kan brukes til å generere en prognose, er 10. (Du skalo også angi nodeantallet i parameters.py i delen [Trinn 5: Opprette pipeliner](#create-pipelines).) På hver node vil det være flere arbeidsprosesser som kjører prognoseskript parallelt. Det totale antallet arbeidsprosesser i jobben din vil være *Antall kjerner som en node har* × *Nodeantall*. Hvis for eksempel beregningsklyngen har typen *Standard\_D4* (åtte kjerner), og maksimalt 11 noder, og hvis verdien `nodes_count` er satt til *10* i parameters.py-filen, er effektiv parallellitet 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Trinn 5: Opprette pipeliner

Pipelinene er en metode for å starte prognoseskript fra Supply Chain Management. Bruk fremgangsmåten nedenfor for å opprette den nødvendige pipelinene.

1. I GitHub åpner du [Malene for Dynamics 365 Supply Chain Management-etterspørselsprognoser med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-repositoriet, og last ned følgende filer:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. I Azure Machine Learning Studio velger du **Notatblokk** i navigasjonsvinduet.
1. Finn følgende plassering i strukturen **Filer**: **Brukere/\[gjeldende bruker\]/src**.
1. Last opp de fire filene du lastet ned i trinn 1, til stedet du fant i forrige trinn.
1. Åpne og gå gjennom **parameters.py**-filen du akkurat lastet opp, i Azure. Kontroller at verdien `nodes_count` er én mindre enn verdien du konfigurerte for beregningsklyngen i [Trinn 4: Konfigurer beregningsressurser](#config-compute-resources). Hvis verdien `nodes_count` er større enn eller lik antall noder i beregningsklyngen, kan det hende at pipelineutkjøringen kan starte. Det vil imidlertid stoppe å svare mens den venter på de nødvendige ressursene. Hvis du vil ha mer informasjon om nodeopptellingen, kan du se delen [Trinn 4: Konfigurere beregningsressurser](#config-compute-resources).
1. Velg **api_trigger.py** som du akkurat lastet opp, og kjør den. Det vil opprette en pipeline som kan utløses via API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Konfigurere et nytt Active Directory-program

Et Active Directory-program kreves for å godkjenne med ressursene som er dedikerte til etterspørselsprognoser ved hjelp av tjenestekontohaver. Programmet bør derfor ha det laveste privileginivået som kreves for å generere prognosen.

1. Logg på Azure-portalen.
1. Registrere et nytt program i leierens Azure Active Directory (Azure AD). For informasjon kan du se [Bruke portalen til å opprette en Azure AD-app og tjenestekontohaver som har tilgang til ressurser](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Følge instruksjonene på skjermen når du fullfører veiviseren. Bruk standardinnstillingene.
1. Gi det nye Active Directory-programmet tilgang til følgende ressurser som du opprettet i delen [Oppsett av maskinopplæring i Azure](#ml-workspace). Hvis du vil ha instruksjoner, kan du se [Tilordne Azure-rollene ved hjelp av Azure-portalen](/azure/role-based-access-control/role-assignments-portal?tabs=current). Dette trinnet vil gjøre det mulig for systemet å importere og eksportere prognosedata, og utløse en pipeline for maskinopplæring fra Supply Chain Management.

    - Bidragsyterrollen for maskinopplæringsarbeidsområdet
    - Bidragsyterrollen til den dedikerte lagringskontoen
    - Databidragsrollen for Storage Blob for den dedikerte lagringskontoen

1. I delen **Sertifikater og hemmeligheter** i programmet du har opprettet, oppretter du en hemmelighet for programmet. Hvis du vil ha instruksjoner, kan du se [Legge til en klient](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Legg merke til program-IDen og bruken av den. Du trenger detaljene i dette programmet senere, når du konfigurerer siden **Parametere for behovsprognose** i Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Konfigurere Azure Machine Learning Service-tilkoblingsparametere i Supply Chain Management

Bruk den følgende fremgangsmåten for å koble Supply Chain Management-miljøet til maskinlæringstjenesten du nettopp konfigurerte i Azure.

1. Logg på Supply Chain Management.
1. Gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Parametere for behovsprognose**.
1. I kategorien **Generelt** kontrollerer du at feltet **Strategi for prognosegenerering** er satt til *Azure Machine Learning Service*.
1. I kategorien **Varefordelingsnøkler** kontrollerer du at feltet **Strategi for prognosegenerering** er satt til *Azure Machine Learning Service* for hver tilordningsnøkkel som skal bruke Azure Machine Learning Service for behovsprognose.
1. Angi følgende felt i fanen **Azure Machine Learning Service**:

    - **Leier-ID** – Angi IDen for Azure-leieren. Supply Chain Management vil bruke denne IDen til å godkjenne med Azure Machine Learning Service. Du finner leier-IDen på siden **Oversikt** for Azure AD i Azure-portalen.
    - **App-ID for tjenestekontohaver** – Angi program-IDen for programmet du opprettet i delen [Active Directory-program](#aad-app). Denne verdien brukes for å autorisere API-forespørsler til Azure Machine Learning Service.
    - **Tjenestekontohaverhemmelighet** – Angi tjenestekontohaverhemmelighet for programmet du opprettet i delen [Active Directory-program](#aad-app). Denne verdien brukes til å skaffe tilgangstokenet for sikkerhetskontohaver du opprettet for å utføre autoriserte operasjoner mot Azure Storage og Azure Machine Language-arbeidsområdet.
    - **Navn på lagringskonto** – Angi navnet på Azure-lagringskontoen for lagringen som du angav da du kjørte installasjonsveiviseren i Azure-arbeidsområdet. (Hvis du vil ha mer informasjon, kan du se delen [Definere maskinopplæring i Azure](#ml-workspace).)
    - **Pipeline-sluttpunktadressen** – Angi URL-adressen til REST-sluttpunktet for pipeline for Azure Machine Learning Service. Du opprettet denne pipelinen som siste trinn da du [konfigurerte maskinopplæring i Azure](#ml-workspace). Hvis du vil hente URL-adressen for pipeline, logger du deg på Azure-portalen og velger **Pipeliner** i navigasjonen. I fanen **Pipeline** velger du pipelinesluttpunktet som kalles **TriggerDemandForecastGeneration**. Deretter kopierer du REST-endepunktet som vises.

    ![Parametere i fanen Azure Machine Learning Service på siden Parametere for behovsprognose.](media/azure-ml-service-parameters.png "Parametere i fanen Azure Machine Learning Service på siden Parametere for behovsprognose")

## <a name="privacy-notice"></a><a name="privacy"></a>Personvernerklæring

Når du velger *Azure Machine Learning Service* for prognosegenerering, sender Supply Chain Management automatisk kundedata for historisk etterspørsel, for eksempel oppsamlet antall, produktnavn og deres produktdimensjoner, forsendelses- og mottakslokasjoner, kunde-IDer og prognoseparametere, til det geografiske området der maskinopplæringsarbeidsområdet og den koblede lagringskontoen er plassert, i den hensikt å stille prognoser for fremtidige behov. Azure Machine Learning Service kan være i et annet geografisk område enn det geografiske området der Supply Chain Management distribueres. Noen brukere kan styre om denne funksjonaliteten er aktivert, ved å velge strategien for prognosegenerering på siden **Parametere for behovsprognose**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over behovsprognose](introduction-demand-forecasting.md)
- [Generer en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)
- [Foreta manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
