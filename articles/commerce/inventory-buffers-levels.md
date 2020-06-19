---
title: Konfigurere beholdningsbuffere og beholdningsnivåer
description: Dette emnet beskriver hvordan du konfigurerer beholdningsbuffere og beholdningsnivåer som bestemmer tilgjengelighetsmeldinger for beholdning på Microsoft Dynamics 365 Commerce-nettsteder.
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: cbc1f5f6fb2c35b009d65b03ffcaffc75a73f188
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417513"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Konfigurere beholdningsbuffere og beholdningsnivåer

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan du konfigurerer beholdningsbuffere og beholdningsnivåer som bestemmer meldinger om tilgjengelighet av beholdning på Microsoft Dynamics 365 Commerce-nettsteder.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce-hovedkontorer inneholder beholdningsdata og ulike kanaler som for eksempel POS-programmer, butikkfronter for e-handel og andre egendefinerte, integrerte programmer som sender og henter beholdning på en asynkron måte. Derfor er ikke de tilgjengelige beholdningsverdiene som hentes gjennom tilgjengelig beholdning-siden i Commerce Headquarters, via POS-grensesnittet (UI), samt via API-er for beholdningstilgjengelighet for e-handel, alltid 100 prosent nøyaktige i sanntid.

I stedet for å vise faktiske beholdningverdier i e-handelsbutikker, foretrekker mange forhandlere å bare vise meldinger om lagertilgjengelighet (for eksempel "Tilgjengelig" eller "Tomt på lager") for å informere kunder om en vare er tilgjengelig for kjøp eller potensielt ikke på lager. For denne fremgangsmåten må beholdningsbuffere og beholdningsnivåer som bestemmer tilgjengelighetsmeldinger, gjøres tilgjengelige og konfigureres.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Forutsetning: Slå på funksjonen for beholdningsbuffere og beholdningsnivåer

Funksjonen for beholdningsbuffere og beholdningsnivåer kontrolleres via Funksjonsbehandling i Commerce Headquarters. Følg denne fremgangsmåten for å aktivere denne funksjonen.

1. Gå til **Systemadministrasjon** \> **Arbeidsområder** \> **Funksjonsbehandling**.
1. Søk etter **Aktiver beholdningsbuffere og beholdningsnivåer**-funksjonen, merk raden, og velg deretter **Aktiver nå**.

Når funksjonen er aktivert, kan du finne beholdningsnivåer på **Detaljhandel og handel \> Lagerstyring**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Opprette og konfigurere en beholdningsnivåprofil

En *beholdningsnivåprofil* bestemmer om en gitt produktantallstatus anses som tilgjengelig på lager, tomt på lager eller en annen egendefinert status. Du kan opprette og konfigurere flere beholdningsnivåprofiler for hver juridisk enhet. Hver profil består av et sett med beholdningsnivåer, og hvert nivå defineres av et *område*, en *kode* og en *etikett*.

- **Område** – hvert område er definert av et *startantall* og et *sluttantall*. En antallsverdi er innenfor et godkjent område hvis verdien er større enn startantallet for det gitte området, og samtidig ikke større enn sluttantallet.
- **Kode** – en kode er en intern forkortelse som representerer nivået. Kunder som direkte integrerer med beholdnings-API-ene, kan bruke koder til å bygge ekstra logikk for et gitt beholdningsnivå. De kan for eksempel slå av kjøpsfunksjonen for et produkt når beholdningsnivåkoden er **OOS** ("Out of stock" / "Ikke på lager").
- **Etikett** – en etikett er en forståelig melding til kundene som formidler et beholdningsnivå til kunder på et e-handelsnettsted.

### <a name="create-an-inventory-level-profile"></a>Opprette en beholdningsnivåprofil

For å opprette en beholdningsnivåprofil følger du disse trinnene.

1. Gå til **Detaljhandel og handel** \> **Beholdningsstyring** \> **Beholdningsnivåer**.
1. Velg **Ny** i handlings ruten, og angi deretter verdier i feltene **Profil-ID** og **Beskrivelse**.
1. I **Områder**-hurtigkategorien velger du **Legg til** for å legge til et nytt nivå, og angir deretter verdier i kolonnene **Startantall**, **Sluttantall**, **Kode** og **etikett** for dette nivået. Gjenta dette trinnet for å legge til flere nivåer. Ved behov kan du redigere verdiene i datarutenettet, eller du kan velge **Slett** for å fjerne et nivå.
1. Velg **Lagre** i handlingsruten.

Når en ny profil opprettes, iverksettes to beholdningsnivåer automatisk:

- **OOS** – Nivået "out of stock" (ikke på lager), hvor den nedre grensen for området er negativ uendelighet. Startantallet og -koden kan ikke redigeres for dette nivået.
- **AVAIL** – Nivået "available" (tilgjengelig), hvor den øvre grensen for området er uendelig. Sluttantallet og -koden kan ikke redigeres for dette nivået.

> [!NOTE]
> Det kan ikke være gap eller overlapping mellom områder i profildefinisjonen.

Du kan bruke **Oversettelser**-knappen i handlingsruten til å konfigurere lokaliserte strenger for etikettmeldingen. Deretter må du kjøre **1110** (**global konfigurasjon**)-distribusjonsplanjobben for å synkronisere de lokaliserte strengene til kanaler.

### <a name="configure-an-inventory-level-profile"></a>Konfigurere en beholdningsnivåprofil

Du kan konfigurere en beholdningsnivåprofil enten på produktkategorinivå eller på enkeltproduktnivå. Når en beholdningsnivåprofil konfigureres for et produkt, bestemmes beholdningsnivået basert på områdene som er definert i den tilknyttede profilen. Ellers bestemmes beholdningsnivåene "tilgjengelig" eller "tomt på lager" basert på om produktet har et positivt beholdningsantall.

For å konfigurere en beholdningsnivåprofil for en kategori følger du disse trinnene.

1. Gå til **Detaljhandel og handel** \> **Produkter og kategorier** \> **Handelsprodukthierarki**.
1. Velg kategorien du vil konfigurere en beholdningsnivåprofil for.
1. I **Selg produktegenskaper**-hurtigkategorien velger du en juridisk enhet.
1. I **Handelsbeholdning**-delen i **Beholdningsnivåprofil**-feltet velger du én av de forhåndsdefinerte beholdningsnivåprofilene.

Du kan bruke **Oppdater produkter**-knappen i handlingsruten til å overføre verdien av profilen på kategorinivå til kategoriens underliggende produkter. For mer informasjon, se [Administrere produktkategorier og produkter](category-management-product-creation.md).

For å konfigurere en beholdningsnivåprofil for et lansert produkt følger du disse trinnene.

1. Gå til **Detaljhandel og handel** \> **Produkter og kategorier** \> **Utgitte produkter etter kategori**.
1. Velg et produkt, og åpne deretter siden med produktinformasjon.
1. I **Selg**-hurtigkategorien, i **Handelsbeholdning**-delen i **Beholdningsnivåprofil**-feltet, velger du én av de forhåndsdefinerte beholdningsnivåprofilene.

Når et nytt produkt opprettes, blir feltet **Beholdningsnivåprofil**, som mange andre attributter på produktnivå, satt til verdien som er konfigurert for kategorien som produktet er knyttet til.

> [!NOTE]
> Beholdningsnivåprofilen er en juridisk enhet-spesifikk attributt. Beholdningsnivåprofilens verdi kan variere på tvers av juridiske enheter for samme kategori eller produkt.

For å synkronisere konfigurasjonene av beholdningsnivåprofiler med kanaler følger du denne fremgangsmåten.

1. Gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**.
1. Kjør distribusjonsplanen **1040** (**Produkt**).

## <a name="configure-an-inventory-buffer"></a>Konfigurere en beholdningsbuffer

*Beholdningsbuffer* er en brukerdefinert verdi som trekker det ekstra antallet av en vare fra det opprinnelige antallet for å beregne det estimerte antallet. Dette estimerte antallet gir forhandlere en sikker buffer slik at de ikke overselger et produkt ved å selge mer enn den faktiske beholdningen. Du kan konfigurere beholdningsbufferen enten på produktkategorinivå eller på enkeltproduktnivå. Hvis du ikke spesifiserer en beholdningsbuffer, brukes standardverdien **0** (null).

For å konfigurere en beholdningsbufferen for en kategori følger du disse trinnene.

1. Gå til **Detaljhandel og handel** \> **Produkter og kategorier** \> **Handelsprodukthierarki**.
1. Velg kategorien du vil konfigurere beholdningsbufferen for.
1. I **Selg produktegenskaper**-hurtigkategorien velger du en juridisk enhet.
1. I **Handelsbeholdning**-delen i **Beholdningsbuffer**-feltet angir du en positiv verdi.

Du kan bruke **Oppdater produkter**-knappen i handlingsruten til å overføre verdien av bufferen på kategorinivå til kategoriens underliggende produkter. For mer informasjon, se [Administrere produktkategorier og produkter](category-management-product-creation.md).

For å konfigurere beholdningsbufferen for et frigitt produkt følger du disse trinnene.

1. Gå til **Detaljhandel og handel** \> **Produkter og kategorier** \> **Utgitte produkter etter kategori**.
1. Velg et produkt, og åpne deretter siden med produktinformasjon.
1. I **Selg**-hurtigkategorien i **Handelsbeholdning**-delen i **Beholdningsbuffer**-feltet, angir du en positiv verdi.

Når et nytt produkt opprettes, blir feltet **Beholdningsbuffer** satt til verdien som er konfigurert for kategorien som produktet er knyttet til.

> [!NOTE]
> Hvis både beholdningsbufferen og beholdningsnivåprofilene er konfigurert for et produkt, brukes det estimerte antallet for produktet (det vil si det opprinnelige antallet minus bufferverdien) for områdeberegning for å bestemme beholdningsnivået.

For å synkronisere konfigurasjonene av beholdningsbuffere med kanaler følger du denne fremgangsmåten.

1. Gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**.
1. Kjør distribusjonsplanen **1040** (**Produkt**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Bruke beholdningsbuffere og beholdningsnivåer i et e-handelsscenario

Områdebygger for handel bruker funksjonene for beholdningsbuffer og beholdningsnivå i Commerce Headquarters til å bestemme tilgjengelighetsmeldinger for beholdning på e-handelsnettsteder. For mer informasjon, se [Bruke beholdningsinnstillinger](inventory-settings.md).

Hvis du integrerer med en e-handelsløsning fra en tredjepart, kan du også bruke **GetEstimatedAvailability**- og **GetEstimatedProductWarehouseAvailability-**-API-ene til å vise lagertilgjengelighet for et produkt i e-handelsscenariet ditt. Hvis du vil ha mer informasjon om disse API-ene, kan du se [Beregne beholdningstilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).

Innføringen av beholdningsbuffere og -nivåer gjør at disse API-ene kan returnere beholdningsnivåkoder og etikettmeldinger som bestemmes basert på verdiene "Totalt antall tilgjengelige" og "Fysisk tilgjengelige". API-ene kan konfigureres ytterligere for å avgjøre om lagerantallet skal returneres sammen med meldingen, og om det tilgjengelige antallet reduseres av lagerbufferverdien.

Følg denne fremgangsmåten for å konfigurere responsen fra API-ene for produkttilgjengelighet.

1. Gå til **Detaljhandel og handel** \> **Hovedkvarteroppsett** \> **Parametere** \> **Handelsparametere**.
1. I **Butikklager**-delen, i **Beholdning**-kategorien i **API-er for produkttilgjengelighet for e-handel**-feltet, velger du en verdi.
1. For å bruke innstillingene i kanaler kjører du distribusjonsplanjobben **1110** (**Global konfigurasjon**).

## <a name="additional-resources"></a>Tilleggsressurser

[Administrere produktkategorier og produkter](category-management-product-creation.md)

[Ta i bruk innstillinger for beholdning](inventory-settings.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)
