---
title: Bekreft og overfør
description: Dette emnet forklarer hvordan du bruker funksjonen Bekreft og overfør, som gjør at brukere kan levere last fra lageret før de fullfører alt arbeidet som er knyttet til disse lastene.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4c366d2f9091ee46ac3b1b6eff72e178932da18e
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592634"
---
# <a name="confirm-and-transfer"></a>Bekreft og overfør

[!include [banner](../includes/banner.md)]

Med funksjonen *Bekreft og overfør* kan brukere levere last fra lageret før de fullfører alt arbeidet som er knyttet til disse lastene. Når en forsendelse mottas som omfatter lastlinjer som ikke ble plukket ferdig, blir brukeren bedt om å dele det gjenstående antallet på en ny last, eller for å avbryte det ufullstendige antallet.

Systemer som er konfigurert til å tillate laststøttescenarier der planlagte og delvis innlastede lastene må tilpasses på grunn av nye eller skiftende forhold.

Klienten inkluderer logikk som gjør det mulig å lukke en delvis lastet last og bekreftes som sendt. Alle gjenværende leveringer og lastlinjer (inkludert fullstendige eller delvise antall) blir deretter rullet over til en nylig opprettet last og forsendelse, hvis denne overrullingen er nødvendig og oppsettet gjør det. Nye forsendelser og laster opprettes automatisk basert på de opprinnelige kriteriene for forsendelse og lastopprettelse, og hovedattributtene forblir uendret. Det finnes også et alternativ for automatisk annullering av gjenstående antall hvis en arbeidsordre ennå ikke er opprettet, og brukeren anser annulleringen som nødvendig.

Denne funksjonaliteten støtter scenarier der full last ikke passer på en enkelt lastebil, eller der noe av lasten skal beholde lageret før resten av lasten er klar til levering. I disse scenariene kan de gjenværende produktene overføres til en ny last og dermed til en ny lastebil. Fordi denne funksjonen kan brukes med laster som ellers ville kreve fullstendig lastforsendelse, gir den ekstra fleksibilitet slik at transportledere kan løse ikke-standard eller uforutsette scenarier.

Når en last deles, utfører *Bekreft og overfør*-funksjonen følgende handlinger:

- Nye laster og forsendelser opprettes etter hvert som de kreves. Hver last eller forsendelse vil ha de samme attributtene som den opprinnelige lasten eller forsendelsen. Unntaket er laststatusen, som vil bli beregnet på nytt basert på arbeidsstatus.
- Brukeren blir informert om at en ny last er opprettet. Brukeren blir også varslet om ID-en til den nye lasten.
- Lastlinjene, arbeidshodene og arbeidslinjene som ble delt, oppdateres med ny last-og forsendelsesinformasjon.
- Hvis en hel forsendelse deles, vedlikeholdes forsendelsen og bare lastreferansene oppdateres. Hvis forsendelsen må deles, opprettes det en ny forsendelse.

Når gjenstående antall er annullert, fjernes eventuelle lastlinjeantall som ikke er plukket, og som ikke har et annullert arbeid knyttet til seg, fra lasten. Hvis et arbeid pågår, kan brukeren bare dele lasten. Gjenværende antall kan ikke annulleres.

Du kan bare dele last som oppfyller alle disse kriteriene:

- Én eller flere lastlinjer har plukket antall.
- Laststatusen er mindre enn lastet inn.
- Det finnes ingen lastlinjedata. (Disse dataene opprettes via nummerskiltkonsolidering på oppsamlingslokasjonen, og Bekreft og overfør-funksjonen støtter ikke nummerskiltkonsolidering.)
- Ingen beholdning venter på pakking på en pakkelokasjon. (*Bekreft og overfør*-funksjonen støtter ikke lager som er plukket til pakkestasjonen, men er ennå ikke pakket med mindre containere som er pakket, plasseres ved oppsamlingslokasjoner med lastearbeid opprettet.)

> [!NOTE]
> Denne funksjonaliteten er forskjellig fra transportlastfunksjonaliteten, som skal brukes i lagre som aldri kan planlegge og opprette last før plukking, men som i stedet laster inn tilgjengelig transportplass etter at plukkingen er fullført.
>
> Bruk *Bekreft og overfør*-funksjonen i situasjoner der laster vanligvis planlegges og opprettes før, men der det av og til oppstår unntak der lasten ikke passer til den tilgjengelige transporten (for eksempel en lastebil).

## <a name="turn-on-confirm-and-transfer"></a>Aktiver bekreft og overfør

Før du kan bruke funksjonen *Bekreft og overfør*, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Bekreft og overfør*

## <a name="set-up-confirm-and-transfer"></a>Konfigurer bekreft og overfør

Hvis du vil bruke funksjonen *Bekreft og overfør*, må du aktivere den i hver relevante lastmal. I tillegg kan det hende at du vil forberede arbeidsmalene til å støtte funksjonen, avhengig av dine behov. Hvis du vil arbeide med eksempelscenarioet som er oppgitt senere i dette emnet, setter du opp systemet som beskrevet i denne delen. (Det scenarioet er basert på **USMF**-demonstrasjonsdata.)

### <a name="prepare-your-load-templates"></a>Forberede lastmalene

1. Gå til **Lagerstyring \> Oppsett \> Last \> Lastmaler**.
1. I handlingsruten velger du **Rediger** for å legge siden inn i redigeringsmodus.
1. Merk av **Tillat lastdeling under forsendelsesbekreftelse** for hver eksisterende mal der du vil aktivere funksjonen. Du kan også velge **Ny** for å opprette en ny mal, og konfigurere den slik du ønsker. Hver last du oppretter ved hjelp av denne malen, vil arve denne funksjonaliteten. (Hvis du arbeider med **USMF**-demodata, kan du aktivere funksjonen for **20' Beholder**-lastmalen.)

### <a name="prepare-your-work-templates"></a>Forberede arbeidsmalene

Dette oppsettet er ikke nødvendig i alle situasjoner. Eksemplet som vises her, sikrer at arbeidet kan brytes ved hjelp av forsendelse for å støtte eksempelscenarioet som er oppgitt senere i dette emnet. Det finnes også andre måter å oppnå dette resultatet på.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. I rutenettet i den øvre delen av siden velger du en eksisterende arbeidsmal der du vil definere *Bekreft og overfør*-funksjonen. (Hvis du arbeider med **USMF**-demonstrasjonsdata, velger du **51 Plukk til trinn**-arbeidsmalen.) Du kan også opprette en ny arbeidsmal.
1. I handlingsruten velger du **Rediger spørring** for å åpne **Salg**-dialogboksen for spørring.
1. I **Salg**-dialogboksen, på **Sortering**-fanen, velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
    - **Felt:** *Leverings-ID*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lagre innstillingene og lukke **Salg**-dialogboksen.
1. Hvis du får en melding som angir at grupperingen skal tilbakestilles, velger du **Ja** for å fortsette.
1. Velg malen du nettopp redigerte i rutenettet i den øvre delen av **Arbeidsmaler**-siden, og velg deretter **Arbeidshodeskift**.
1. I handlingsruten velger du **Rediger** for å legge siden inn i redigeringsmodus.
1. I rutenettet angir du følgende verdier:

    - **Tabellnavn:** *Midlertidige arbeidstransaksjoner*
    - **Feltnavn:** *Leverings-ID*
    - **Grupper etter dette feltet:** Merk av i denne boksen.

1. Velg **Lagre** i handlingsruten.
1. Lukk siden.

## <a name="scenario"></a>Scenario

Dette scenariet viser et eksempel der plukkprosessen ennå ikke er fullført, men varene som er plukket så langt, må lastes inn i en lastebil og sendes likevel. Derfor kan brukeren dele opp de ikke-plukkede lastlinjene på en ny last. Alle datarelasjonene blir deretter oppdatert automatisk.

> [!NOTE]
> De spesifikke verdiene som beskrives i dette scenariet, er basert på **USMF**-demodataene. Det anbefales at du bruker denne demodataene mens du demonstrerer eller lærer hvordan du bruker funksjonen. Hvis du ikke bruker **USMF**-demodata, må du bytte ut dine egne verdier etter behov.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Trinn 1: Opprette en last som har flere lastlinjer

Før du kan bruke denne funksjonen, må du ha en last som inneholder flere lastlinjer. Du må også kontrollere at plukklokasjonene har nok beholdning for alle varene på salgsordrene du vil opprette. Gå gjennom oppsettet av lokasjonsdirektivet (**Lagerstyring \> Oppsett \> Lokasjonsdirektiver**), og noter plukklokasjonene som brukes ved plukking av salgsordre. Hvis du må justere beholdningen, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt, etter behov.

Hvis du vil opprette en kvalifiserende last, må du først opprette tre salgsordrer ved å følge disse trinnene.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruten velger du **Ny** for å åpne **Opprett salgsordre**-dialogboksen.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier (for et minimum):

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-004* (*Cave Wholesales*).
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *51*.

1. Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.
1. Den nye salgsordren åpnes. I **Salgsordrelinjer**-rutenettet legger du til en linje som har følgende verdier:

    - **Varenummer:** *M9200*
    - **Antall:** *40*
    - **Enhet:** *ea*

1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. Åpne **Reservasjon**-siden ved å velge **Reserver parti** i handlingsruten.
1. Reserver beholdningen på salgslinjen, og lukk deretter **Reservasjon**-siden.
1. Gjenta trinn 1 til og med 4 for å legge til en ny salgsordre for samme kunde og lager.
1. Legg til to salgslinjer som har følgende verdier. Når du har lagt til hver linje, kan du reservere beholdning for den som beskrevet i trinn 6 til og med 8.

    - **Linje 1:** Angi **Varenummer**-feltet til *M9200*, **Antall**-feltet til *30* og **Enhet**-feltet til *ea*.
    - **Linje 2:** Angi **Varenummer**-feltet til *M9201*, **Antall**-feltet til *20* og **Enhet**-feltet til *ea*.

1. Gjenta trinn 1 til og med 4 for å legge til en tredje salgsordre for samme kunde og lager.
1. Legg til to salgslinjer som har følgende verdier. Når du har lagt til hver linje, kan du reservere beholdning for den som beskrevet i trinn 6 til og med 8.

    - **Linje 1:** Angi **Varenummer**-feltet til *M9201*, **Antall**-feltet til *20* og **Enhet**-feltet til *ea*.
    - **Linje 2:** Angi **Varenummer**-feltet til *M9202*, **Antall**-feltet til *60* og **Enhet**-feltet til *ea*.

#### <a name="load-planning-workbench"></a>Arbeidsområde for lastplanlegging

Lastplanleggingsarbeidsområdet bruker lastmal-ID-en til å planlegge forsendelser og frigi salgsordrelinjene til lageret.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I **Lager**-feltet velger du *51*.

    Du vil nå planlegge lasten for salgsordre som du nettopp opprettet.

1. På **Salgslinje**-fanen, i rutenettet, velger du salgslinjene for de nye salgsordrene.
1. I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**.
1. I dialogboksen **Tilordning av lastmal**, i **Lastmal-ID**-feltet, velger du *20' beholder*.
1. Velg **OK**.
1. I **Laster**-delen på **Lastplanleggingsarbeidsområdet**-siden, i rutenettet, finner du den nylig oppretted last-ID-en for lager *51*. Rull mot høyre til du ser **Tillat lastdeling under forsendelse**-kolonne. Avmerkingsboksen bør være merket for lasten.
1. Velg lasten.
1. På **Frigi**-menyen over rutenettet velger du **Frigi til lager** for å opprette arbeid.
1. I **Frigi last til lager**-dialogboksen bekrefter du at **Poster som inkluderer**-hurtigfanen viser last-ID-en.
1. Velg **OK**.

    Du kan få en Behandler operasjon-melding mens systemet oppretter forsendelsene og arbeidet.

1. I **Last**-delen på **Lastplanleggingsarbeidsområdet**-siden bør lasten nå ha laststatusen *Bølget*. Velg lasten og deretter, på **Tilknyttet informasjon**-menyen over rutenettet, velger du **Bølgedetaljer** for å vise forsendelses-ID-ene som ble opprettet. Når du er ferdig, lukker du **Bølger**-siden.
1. I **Laster**-delen på **Lastplanleggingsarbeidsområde**-siden velger du lasten og på **Tilknyttet informasjon**-menyen over rutenettet, velger du **Arbeidsdetaljer** for å vise arbeidet som ble opprettet for salgsordrene.
1. Noter deg arbeids-ID-ene som ble opprettet. Det kan hende du må rulle mot høyre for å se salgsordrenummeret og forsendelses-ID-en som er knyttet til arbeids-ID-en.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Trinn 2: Definere kjøringsflyten for mobile enheter

Oppgaver for mobile enheter krever informasjon fra brukerens inndata, for eksempel arbeids-ID eller nummerskilt-ID. I feltene er denne informasjonen vanligvis oppgitt for lagerbrukere i form av strekkoder som finnes i dokumentasjon, pakking eller sporing. Hvis du vil fullføre trinnene for den mobile enheten for scenarier, må du kontrollere at du har identifisert arbeids-ID-ene for transaksjonene, og nummerskilt-ID-ene til varen og lokasjonen i transaksjonene.

1. Logg på den mobile enheten ved å bruke en bruker-ID og et passord for lager *51*.
1. Velg **Utgående**.
1. Velg **Salgsplukking**.
1. Du kan angi arbeids-ID-en eller nummerskilt-ID-en. Angi arbeids-ID-en for den første salgsordren, og velg deretter **Enter**.
1. I **Loc**-feltet angir du lokasjonen som vises for å bekrefte plukklokasjonen. Velg deretter **Enter**.
1. I **LP**-feltet angir du nummerskilt-ID-en. Nummerskilt-ID-en må være et treff for varen, lageret og lokasjonen til varen som blir plukket fra den valgte lokasjonen. Når du er ferdig, velg **Enter**.
1. I **Vare**-feltet angir du varenummeret som skal bekrefte varen som skal plukkes, og deretter velger du **Enter**.
1. I **Qty**-feltet angir du antallet for varen som skal plukkes, og deretter velger du **Enter**.
1. I **Mål-LP**-feltet angir du målnummerskilt-ID-en. Målnummerskilt er brukerdefinert. Pass på at du angir en nummerskilt-ID som du vil huske. Det anbefales at du bruker gjeldende dato pluss en tosifret sekvens (ÅÅMMDD\#\#) som format, for eksempel *19112301*. Når du er ferdig, velg **Enter**.
1. Se gjennom informasjonen som vises. Denne informasjonen er *Plukk*-informasjonen som nå blir *Plasser*-dataene for Plasser-transaksjonen. Når du er ferdig, velg **Enter**.

    - Du mottar en **Arbeids fullført**-melding.

1. Gjenta trinn 4 til og med 10 for arbeids-ID-en til den andre salgsordren.

Det neste trinnet er å laste de to plukkede nummerskiltene på lastebilen.

1. Logg på den mobile enheten ved å bruke en bruker-ID og et passord for lager *51*.
1. Velg **Utgående**.
1. Velg **Salgslasting**.
1. Angi den brukerdefinerte målnummerskilt-ID-en som du opprettet for den første arbeids-ID-en i den forrige prosedyren. Velg deretter **Enter** for å sette målnummerskiltet i **TRINN**-lokasjonen.
1. Angi målnummerskilt-ID-en på nytt, og velg deretter **Enter** for å sette nummerskiltet inn i **BAYDOOR**-lokasjon.
1. Gjenta trinn 4 til og med 5 for målnummerskilt-ID-en du opprettet for den andre arbeids-ID-en.

De to arbeids-ID-ene blir nå lukket (lastet inn).

### <a name="step-3-confirm-the-outbound-shipment"></a>Trinn 3: Bekreft den utgående forsendelsen

I dette trinnet skal du bekrefte de to salgsordrene og arbeidet som er fullført for lasten, for å sende de plukkede varene av lasten, og opprette en ny last for de varer som ikke er plukket. Utgående forsendelsesbekreftelse må gjøres på **Lastdetaljer**-siden.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I **Laster**-delen i rutenettet velger du raden for last-ID-en du opprettet.
1. Velg last-ID-koblingen for å åpne **Lastdetaljer**-siden.
1. På **Lastdetaljer**-siden, i handlingsruten, på **Send og motta**-fanen, i **Bekreft**-gruppen, velger du **Utgående forsendelse** for starte bekreftelsen.
1. I **Forsendelsesbekreftelse**-dialogboksen, i **Lastdelingsmetode under forsendelsesbekreftelse**-feltet, velger du *Del antall til ny last*.
1. Velg **OK**.

    Du kan få Behandler operasjon-meldingen.

    Du mottar informasjonsmeldinger som angir at forsendelsen for lasten er bekreftet, og at en ny last er opprettet fra det delte antallet.

Oppdater **Lastplanleggingsområde**-siden for å se den nyopprettede lasten.

Du kan også bekrefte at transaksjonsrelasjoner er oppdatert på følgende måter:

- De gjenværende (ubehandlede) forsendelsene og forsendelseslinjene oppdateres med den nye last-ID-en.
- Salgsordren er koblet til den nye last-ID-en.
- Den opprinnelige lasten inkluderer ikke de gjenværende lastlinjene.
- Det gjenstående arbeidet er oppdatert med den nye last-ID-en.
- Bølgen forblir den samme.
- Statusen til den nye lasten er riktig oppdatert. (Hvis arbeidsstatusen er _Pågår_, bør også laststatusen være _Pågår_ .)

## <a name="notes-and-tips"></a>Merknader og tips

- Du kan også aktivere **Tillat lastdeling under forsendelsesbekreftelse**-parameteren etter at lasten er opprettet med **Lastmal**-parameteren deaktiver, men før lastprosessen har startet. Gå til ønsket last, og aktiver deretter parameteren i hodevisningen.
- **Del antall til ny last**-alternativet fungerer også når noen av de gjenværende arbeidshodene har statusen *Pågår*. Derfor kan du fremdeles bruke funksjonaliteten selv om arbeiderne allerede kjører plukkordrene.
- Hvis du velger **Avbryt ikke-fullført antall** mens det er gjenstående arbeid som har statusen *Åpen* eller *Pågår*, får du følgende feilmelding: Kan ikke avbryte gjenstående antall for last. Arbeid finnes for lasten.
- Hvis du velger **Avbryt ikke-fullført antall** når det ikke er noe gjenstående arbeid, men det finnes frigitte lastlinjer, får du følgende feilmelding: Kan ikke bekrefte leveringen for lasten fordi antallet for varer overskrider prosenten som er definert for underlevering. For å unngå feilen kan du angi **Underlevering**-prosent på den ikke-frigitte lastlinjen til 100 prosent. Ikke-frigitte linjer vil ikke bli flyttet til en ny last, men gjeldende last vil bli bekreftet med underlevering. I dette tilfellet kan du ikke frigi den opprinnelige ordren på nytt. Derfor må du også håndtere den på en annen måte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]