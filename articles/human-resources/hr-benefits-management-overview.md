---
title: Oversikt over fordelsbehandling
description: Dette emnet gir en oversikt over funksjonen Fordelsbehandling i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc06fd2ef4992b4ef2e20ace4f5c6bcc0bffb9d2
ms.sourcegitcommit: e06b7d4de6d5ee7ae491d437d6c0365608a5380b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2021
ms.locfileid: "7892508"
---
# <a name="benefits-management-overview"></a>Oversikt over fordelsbehandling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte. I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær. Med Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer. Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.

- Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag. Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.
- Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.
- Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.
- Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.
- Behandling av kvalifisert levetidshendelse støtter fremtidige levetidshendelser.

Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.

> [!NOTE]
> Du kan nå tilpasse sider i Fordelsbehandling. Egendefinerte felter relatert til dekningssatser kan legges til på siden **Dekningsalternativ** for fordelsplaner. Hvis du vil ha mer informasjon om å arbeide med egendefinerte felt, kan du se [Egendefinerte felt](hr-developer-custom-fields.md).
>
> ![Egendefinerte felt for fordelsbehandling](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Aktivere Fordelsbehandling

Dette emnet beskriver hvordan du aktiverer funksjoner i Human Resources. Den forklarer også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, og som deaktiveres når du aktiverer Fordelsbehandling.

> [!IMPORTANT]
> Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det. Det anbefales at du aktiverer og tester Fordelsbehandling i et **Sandkasse**-miljø før du aktiverer det i et **Produksjon**-miljø. Det er store forskjeller mellom den eldre Fordel-funksjonaliteten og den nye Fordelsbehandling-funksjonaliteten, som krever ekstra oppsett, og som bør testes før den blir satt i produksjon.

Hvis du vil ha mer informasjon, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

## <a name="process-overview"></a>Prosessoversikt

Prosessen med å konfigurere fordeler omfatter følgende oppgaver:

1.  Definere nødvendig fordelsinformasjon.
2.  Definere valgfri fordelsinformasjon.
3.  Definere fordelsplaner.
4.  Definere fleksible kredittprogrammer (valgfritt).
5.  Konfigurere nødvendig ansattinformasjon.
6.  Konfigurere valgfri ansattinformasjon.
7.  Behandle ansatte for å fastslå rettigheten.
8.  Ansatte velger planer via ansattselvbetjening (valgfritt).
9.  Bekreft valg av ansattplan.
10. Behandling av levetidshendelse (valgfritt).
11. Vurdere oppdateringer (valgfritt).

## <a name="set-up-required-benefit-information"></a>Definere nødvendig fordelsinformasjon

Før ansatte kan registreres i planene, må flere komponenter defineres:

- **Fordelsstyringsparametere** – Disse innstillingene deles på tvers av firmaer. Du kan definere standard årsakskoder, aktivere alternativet **Årlig fordelslønn**, angi en standard betalingsfrekvens for nye ansettelser og aktivere livshendelser. Hvis du vil ha mer informasjon, kan du se [Angi parametere for fordelsbehandling](hr-benefits-setup-parameters.md).
- **Alternativer for rettighet for personlig kontakt** – Personlige kontakter er personene som enten er avhengige av eller mottakere av planene som er definert. Vanligvis er de barn, ektefeller eller tillitsorganisasjoner. Hvis du vil ha mer informasjon, kan du se [Konfigurere alternativer for personlige kontaktrettigheter](hr-benefits-setup-contact-eligibility-options.md).
- **Dekningsalternativer** – Definer dekningstypene som skal være tilgjengelige for en plan. Mer bestemt definerer du hvem som skal dekkes, eller hvor mye dekning som er tilgjengelig. Hvis du vil ha mer informasjon, se [Opprette dekningsalternativer](hr-benefits-setup-coverage-options.md).
- **Plantyper** – Definer plantypene som skal være tilgjengelige når du oppretter en fordelsplan. Eksempler på plantyper er **Tannforsikring**, **Syn** og **Sparing**. Noen viktige innstillinger for plantypen bestemmer hvilke innstillinger som er tilgjengelige i fordelsplanen. Hvis du vil ha mer informasjon, se [Opprett plantyper](hr-benefits-setup-plan-types.md).
- **Rettighetsregler** – Rettighetsregler brukes til å fastslå om ansatte er kvalifisert for en plan. Minst én rettighetsregel må knyttes til hver fordelsplan. Hvis du vil ha mer informasjon, kan du se [Konfigurere rettighetsregler og -alternativer](hr-benefits-setup-eligibility-rules.md).
- **Betalingsfrekvenser** – Betalingsfrekvenser er nødvendige når fordelssatser er konfigurert. Betalingsfrekvensen som brukes til en sats, er med på å identifisere beløpet den ansatte og/eller arbeidsgiveren skylder ukentlig, månedlig eller årlig. Hvis du vil ha mer informasjon, kan du se [Definere betalingshyppigheter](hr-benefits-setup-payment-frequencies.md).
- **Satser** – Satser definerer hvor mye en fordel vil koste enten den ansatte eller arbeidsgiveren. Hvis penger skal tildeles tilbake til en ansatt (for eksempel en kreditt for et medlemskap på treningssenter), angis det en negativ sats. Hvis du vil ha mer informasjon, kan du se [Konfigurere satser](hr-benefits-setup-rates.md).
- **Lagsatser** – Lagsatser brukes når en sats må endres på grunnlag av enkelte kriterier. Den vanligste lagsatsen er et enkelt lag som er basert på alder. Det kan imidlertid også defineres dobbeltlagssatser, der satsen kan endres basert på kjønn, alder eller andre kriterier.
- **Fradrag** - Fradragene er egentlig hodeinformasjon/-koder som vil bli sendt videre til lønnssystemet for å identifisere fradraget for fordelen. Du må definere disse fradragene fordi de kreves i fordelsplanen. Hvis du vil ha mer informasjon, kan du se [Konfigurere fradrag](hr-benefits-setup-deductions.md).
- **Fordelsperioder** – En fordelsperiode er perioden når de ansatte skal ha fordelsdekning. Det er også kjent som et planår. De åpne registreringsperiodene defineres også her.

## <a name="set-up-optional-benefit-information"></a>Definere valgfri fordelsinformasjon

Følgende komponenter må ikke konfigureres for å opprette en fordelsplan:

- **Programmer** – Et program er et sett med fordeler som styres av de samme rettighetsreglene. Alle i salgsavdelingen kan for eksempel få en mobiltelefon.
- **Bunter** – En bunt er en gruppe av fordeler, der én plan må velges før alternativet for å velge flere planer er tilgjengelig. En medisinsk plan med høy fradragsberettiget kan for eksempel være buntet med en HSA-plan.
- **Livshendelsestyper** – Livshendelser er hendelser som gjør det mulig å endre en ansatts dekning. Typer livshendelser er koblet til en plantype. For eksempel kan en medisinsk plantype tillate endringer i planer på grunn av fødsel eller adopsjon, eller på grunn av en endring i sivilstatus. Det kan imidlertid hende at en forsikringsplantype ikke tillater endringer på grunn av livshendelser. Hvis du vil ha mer informasjon, kan du se [Konfigurere hendelsestyper for levetid](hr-benefits-setup-life-event-types.md).
- **Ventedager og venteperioder** – En venteperiode for dekning kan defineres for en fordelsplan. En nyansatt kan for eksempel registrere seg i en 401(k) bare etter tre måneders ansettelse. I dette tilfellet er venteperioden tre måneder. Ventedager brukes i venteperioden hvis nye registreringer kan behandles og sendes til leverandøren bare på en bestemt dag i måneden. Hvis for eksempel 401(k) registreringer bare kan behandles den 15. i måneden, etter tre måneders ansettelse, er venteperioden som er definert, tre måneder, og ventedagen er den 15. Hvis du vil ha mer informasjon, kan du se [Konfigurere ventedager](hr-benefits-setup-waiting-days.md) og [Konfigurere venteperioder](hr-benefits-setup-waiting-periods.md).
- **Årsakskoder** – Årsakskoder brukes til å forklare hvorfor en fordel kan endres for en ansatt. Hvis du vil ha mer informasjon, kan du se [Definere årsakskoder](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Definere fordelsplaner

Når du definerer en fordelsplan, må du fullføre følgende trinn før ansatte kan registreres:

- Tilordne en fordelsperiode.
- Tilknytte dekningsalternativer.
- Angi en gyldig fra-dato og en gyldig til-dato i kategorien **Generelt**.
- Tilordne minst én rettighetsregel.
- Angi feltet **Tillat/fortsett registrering** i kategorien **Oppsett**.

Hvis du vil ha mer informasjon om hvordan du definerer fordelsplaner, kan du se [Definere fordelsplaner](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Definere fleksible kredittprogrammer (valgfritt)

Du kan bruke fleksible kredittprogrammer til å registrere ansatte i fordeler i henhold til et forhåndsdefinert antall fleksible kreditter. Ansatte kan velge hvordan de skal fordele den fleksible kreditten. Hvis ansatte for eksempel allerede er dekket under ektefellens helseforsikringsplan, trenger de ikke å bruke kreditten til helsedekningen. Derfor kan de i stedet bruke dem til andre fordeler. Hvis du vil ha mer informasjon om programmer for fleksikreditt, kan du se [Definere fleksible kredittprogrammer](hr-benefits-plans-flex-credit-programs.md)

## <a name="configure-required-employee-information"></a>Konfigurere nødvendig ansattinformasjon

Før du kan registrere ansatte i fordeler, må du angi nødvendig informasjon for dem. 

Den ansatte må ha tilordnet en **Stilling**. En **Stilling** kan tilordnes den ansatte på sidene **Arbeider** eller **Stilling** ved å oppdatere **Arbeidertilordning**. 

Deretter må ansatte registreres i en fast kompensasjonsplan på startdatoen eller ha en et **Årlig lønnsbeløp for fordeler**. Før du tilordner **Fast kompensasjon** til en ansatt, må en **Stilling** tilordnes. 

> [!NOTE] 
> Startdatoen for **Startdato for fast kompensasjon** kan ikke komme før **Dato for stillingstilordning**.

Alternativt, hvis du har en ansatt som får tilleggskompensasjon som provisjon, kan du legge til en **Årlig fordelslønn** fra ansattposten. Personaladministrasjon bruker **Årlig fordelslønn** til å fastsette dekningsbeløp i stedet for **Fast kompensasjon**. **Årlig lønnsbeløp for fordeler** må være gyldig per den ansattes startdato eller starte av fordelsperioden, avhengig av hva som er sist. Det er imidlertid ikke påkrevd å tilordne **Årlig fordelslønn** til en stilling. Hvis du vil aktivere funksjonen **Årlig fordelslønn**, går du til siden **Delte parametere for Human Resources** i fanen **Fordelsbehandling**. Denne funksjonen er slått av som standard.

> [!IMPORTANT]
> Hvis både **Fast kompensasjon** og **Årlig fordelslønn** er registrert for en ansatt, blir **Årlig fordelslønn** brukt til å bestemme dekningsbeløp. I delen **Ansattdetaljer** på **Arbeider**-siden må du velge en verdi i feltet **Frekvens for fordelsbetaling**.

## <a name="configure-optional-employee-information"></a>Konfigurere valgfri ansattinformasjon
Når du oppretter en fordelsplan som bruker satser som er basert på kjønn eller alder, må du angi en fødselsdato og et kjønn for den ansatte for å beregne fordelskostnaden.

## <a name="process-employees-to-determine-eligibility"></a>Behandle ansatte for å fastslå rettigheten
Før ansatte kan registreres i planer, kjøres rettighetsbehandling for å bestemme hvilke planer de er kvalifisert for. Du kan vise resultatene av rettighetsprosessen i **visningsprogrammet for prosessresultater**. Hvis du vil ha mer informasjon, kan du se [Behandle registreringsberettigelse](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Ansatte velger planer ved å bruke **Ansattselvbetjening** (valgfritt)

Når en åpen registrering forekommer, ansettes de ansatte nylig, eller når en livshendelse forekommer, kan ansatte velge eller oppdatere fordeler ved hjelp av **Ansattselvbetjening**. Hvis du vil ha mer informasjon, kan du se [Konfigurere selvbetjening for ansatte](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Bekreft valg av ansattplan

Fordelene som den ansatte velger, må bekreftes før den ansatte regnes som registrert. Fordeler kan også velges på vegne av en ansatt. Hvis du vil velge eller bekrefte fordeler, går du til **Ansatt**-siden i kategorien **Fordeler** og velger **Planer for arbeidsfordeler**. Hvis du vil velge eller bekrefte fordeler for flere ansatte, kan du bruke siden for **masseoppdatering av fordeler for fordelsplaner**.

## <a name="life-event-processing-optional"></a>Behandling av levetidshendelse (valgfritt)

I løpet av den ansattes livssyklus kan hver ansatt oppleve ulike livshendelser, for eksempel endring i ansettelse eller endringer i avhengige eller mottakere. Hvis du vil bruke livshendelser, må du aktivere dem på siden **Delte parametere for Human Resources**. Definer alternativer for livshendelser og alternativer for livshendelse for plantyper.

Før du kan behandle livshendelser, må du allerede kjøre åpen registrering minst én gang i løpet av en tidsramme for ansettelsen. I USA blir det vanligvis åpen registrering én gang per år. Utenfor USA kan åpen registrering kjøres på ansettelsestidspunktet. Behandling av livshendelser krever ikke at arbeidere velger en fordelsplan. Arbeiderne må imidlertid ha blitt inkludert i åpen innmeldingsbehandling. Hvis du vil ha mer informasjon, kan du se følgende emner:

- [Behandle levetidshendelser](hr-benefits-process-life-events.md)
- [Behandle endringer i levetidshendelse](hr-benefits-process-life-event-changes.md)
- [Behandle rettighet for levetidshendelse](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Vurdere oppdateringer (valgfritt)

Av og til endres fordelsraten i løpet av planperioden. Hvis du vil oppdatere satsene for ansatte som allerede er registrert i planen, må du behandle satsendringene. Hvis du vil ha mer informasjon, se [Behandle satsendringer](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
