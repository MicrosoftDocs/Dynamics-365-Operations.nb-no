---
title: Behandle fradrag med arbeidsområdet for fradrag
description: Denne artikkelen beskriver hvordan du bruker fradragsarbeidsområdet til å behandle kundebetalinger som omfatter fradrag.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 607ad528b56d1f0c9a78e113f67c920cdae6e620
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873615"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Behandle fradrag med arbeidsområdet for fradrag

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker fradragsarbeidsområdet til å behandle kundebetalinger som omfatter fradrag.

En kunde det tilkommer en rabatt, kan velge å ikke vente på en rabattutbetaling. I stedet kan kunden sende en betaling som inkluderer et fradrag for rabattbeløpet. Hvis du vil håndtere denne typen transaksjon, kan du bruke arbeidsområdet for fradrag for å samsvare fradrag til åpne kredittransaksjoner, dele fradrag, nekte fradrag og skrive av fradrag.

> [!NOTE]
> Arbeidsområdet for fradrag har vært en del av salgs- og markedsføringsfunksjonaliteten i Microsoft Dynamics 365 Supply Chain Management i lang tid. Den er imidlertid nå utvidet slik at det også fungerer med den nyere modulen **Rabattbehandling**. Denne artikkelen beskriver hvordan du bruker både eldre funksjoner og rabattbehandlingsfunksjoner på arbeidsområdet for fradrag. Hvis du ikke har [aktivert modulen **Rabattbehandling** for systemet](rebate-management-enable.md), vil imidlertid noe av funksjonaliteten som beskrives her, være tilgjengelig for deg.

## <a name="prerequisites"></a>Forutsetninger

### <a name="set-up-the-old-deduction-management-system"></a>Konfigurer det gamle styringssystemet for fradrag

Du kan bruke arbeidsområdet for fradrag sammen med de gamle fratrekksadministrasjonsfunksjonene i Supply Chain Management, selv om du ikke bruker modulen **Rabattbehandling**. Først må du imidlertid klargjøre systemet som beskrevet i denne delen.

Før du kan bruke arbeidsområdet for fradrag, må du fullføre oppsettoppgavene som beskrives under [Konfigurer fradragsstyring](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Du bør også ha en type rabattavtale definert for kunden: enten en kunderabatt, som beskrevet i [Definere og vedlikeholde kunderabatter](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), eller en handelsrabatt.

Hvis du bruker et fradrag på en kunderabatt, må du fullføre disse oppgavene:

- [Konfigurer kunderabattene](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Godkjenn og behandle rabatten slik at du kan bruke arbeidsområdet for fradrag.

Hvis du bruker et fradrag på en handelsrabatt, må du fullføre disse oppgavene:

- Angi tilbakebetalingsrabatter.
- Bruk tilbakebetalingsrabatter.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Konfigurer kunder og fradrag

Systemet registrerer alle fradragshendelser i en kravjournal. Derfor må systemet inneholde en journal som kan brukes til dette formålet. Hvis du ikke allerede har en kravjournal, definerer du den nå. Denne journalen er nødvendig for å opprette fradrag direkte på siden for arbeidsområdet for fradrag, kundeutligning eller kunden.

Hvis du vil konfigurere en ny kravjournal for fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Økonomimodul \> Journaloppsett \> Journalnavn**.
1. Velg **Ny**, og sett følgende felter for det nye journalnavnet:

    - **Navn** – Angi et unikt navn for kravjournalen.
    - **Beskrivelse** – Angi en beskrivelse av den nye journalen.
    - **Journaltype** – Velg *Daglig*.
    - **Bilagsserie** – Tilordne en eksisterende nummerserie. Du kan også opprette en ny nummerserie som har firmaområde, og tilordne den til det nye journalnavnet.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
1. Sett **Navn på kravjournal**-feltet til journalnavnet du nettopp opprettet, i hurtigfanen **Generelt** på fanen **Fradrag**.
1. På **Returnordre**-hurtigfanen angir du følgende felter:

    - **Opprett returordre** – Angi dette alternativet for å angi hva systemet skal gjøre når et antallsbasert krav godkjennes:

        - *Ja* – Opprett en returordre.
        - *Nei* – Opprett en negativ salgsordre.

    - **Oppretting uten tilknyttet faktura** – Velg en verdi for å angi hva systemet skal gjøre når et antallsbasert krav godkjennes, men ingen faktura er tilknyttet:

        - *Godta* – Opprett en innkjøpsreturordre.
        - *Advarsel* – Opprett en returordre, men vis følgende advarsel: Kravet er ikke knyttet til en faktura.
        - *Feil* – Ikke opprett en returordre, og vis følgende feilmelding: Kravet er ikke knyttet til en faktura. Oppdateringen er avbrutt.

    - **Opprett returordre før fradragsgodkjenning** – Sett dette alternativet til *Ja* hvis det kan opprettes returordrer før kravet godkjennes. Denne innstillingen gjelder bare for antallsbaserte krav der alternativet **Opprett returordre** er angitt til *Ja*.

### <a name="configure-general-ledger-parameters"></a>Konfigurere finansparametere

Når systemet oppretter en kravjournal for et nytt fradrag, oppretter det også to nye kundetransaksjoner: en for å motpostere kravbeløpet mot den opprinnelige fakturaen, og en for å registrere kundens gjeld på kravbeløpet (fordi kravet ennå ikke er godkjent). Derfor må du sette opp systemet slik at ett enkelt bilag kan ha flere kundelinjer.

Følg denne fremgangsmåten for å aktivere ett enkelt bilag for å ha flere kundelinjer.

1. Gå til **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**.
1. I fanen **Finans** på hurtigfanen **Generelt** angir du **Tillat flere transaksjoner innenfor ett bilag** til *Ja*.
1. Hvis du får en advarsel, velger du **Lukk** for å godta endringen.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Opprett fradragsårsaker

Systemet krever at brukere angir en årsak for hvert fradrag de legger inn direkte på siden for arbeidsområdet, kundeutligning eller kunden. Årsaken avgjør hvordan fradraget håndteres når det godkjennes.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Fradragsårsaker**.
1. Velg **Ny** for å legge til en rad i rutenettet, og angi deretter følgende felter for den:

    - **Kravårsak** – Angi et unikt navn for årsaken.
    - **Beskrivelse** – Angi en beskrivelse av årsaken for å få mer informasjon om hvordan den skal brukes.
    - **Kravgrunnlag** – Velg et kravgrunnlag for kravets årsak:

        - *Prisbasert* – Opprett en fritekstkreditt ved godkjenning.
        - *Antallsbasert* – Opprett en negativ salgsordre eller returordre ved godkjenning.

    - **Kode for returårsak** – Velg en returårsakskode som skal brukes som verdien **Returårsakskode** for returordren.
    - **Type** – Velg en fradragstype. Verdien for **Fradragsforskyvning** for den valgte typen brukes til å angi **Fradragsforskyvning**-feltet når det opprettes et fradrag eller krav. Fradragstyper defineres på siden **Fradragstyper** (**Salg og markedsføring \> Handelsrabatter \> Fradrag \> Fradragstyper**).
    - **Kravposteringskonto** – Dette feltet er bare tilgjengelig når feltet **Kravgrunnlag** er satt til *Prisbasert*. Når et prisbasert krav godkjennes, tilordner systemet finanskontoen som du velger her som **hovedkontoverdi** for fritekstkreditnotaen.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Definer en periodisk oppgave for å utligne godkjente fradrag

For fradrag som opprettes ved å bruke kommandoen **Ny fradrag** på arbeidsområdet, kundeutligning eller kundesiden, kan du konfigurere periodiske oppgaver for *Utligning av godkjente fradrag* slik at de samsvarer med fradrag og kreditt som samsvarer med **Fradrags-ID**-verdier og beløp.

Hvis du vil planlegge denne oppgaven, kan du gå til **Salg og markedsføring \> Periodiske oppgaver \> Utligne godkjente fradrag** og definere alternativer, filtre og en plan, på samme måte som for andre typer periodiske oppgaver.

> [!NOTE]
> Hvis alternativet **Automatisk utligning** er satt til *Ja* på fanen **Utligning** på siden **Kundeparametere** (**Kundeoppsett \> Oppsett \> Kundeparametere**), vil ikke de periodiske oppgavene for *Utlign godkjente fradrag* gjøre noe fordi kreditten utlignes automatisk.

## <a name="create-a-deduction"></a>Opprette et fradrag

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Opprett en journaloppføring for fradrag ved hjelp av kundebetalingsjournalen

Hvis du vil opprette en journaloppføring for fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Kunder \> Betalinger \> Kundebetalingsjournal**.
1. Velg **Ny** for å legge til en rad i rutenettet.
1. Velg navnet på journalen i **Navn**-feltet for den nye raden.
1. I handlingsruten velger du **Linjer**.
1. Angi dato, firmakonto og kundekontonummer.
1. I **Faktura**-feltet velger du fakturaen som fradraget er knyttet til.
1. I **Kredit**-feltet angir du beløpet kunden betalte.
1. Velg **OK** for å bekrefte at beløpet er mindre enn totalbeløpet av den merkede transaksjonen.
1. Velg motkontotypen og motkontoen.
1. Velg **Fradrag** på verktøylinjen over rutenettet.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet på siden **Fradrag**. Feltet **Fradrags-ID** for den nye raden angis automatisk.
1. Velg fradragstypen i **Type**-feltet.
1. I **Beløp**-feltet angir du beløpet som vises i **Saldo**-feltet under fradragslisten. Dette beløpet representerer beløpet som kunden trakk fra betalingen.
1. Lukk **Fradrag**-siden. Du returneres til **Kundebetalinger**-siden, som nå viser en ny linje for fradraget.
1. Velg **Valider \> Valider** i handlingsruten. Du skal motta følgende melding: Journalen er OK.
1. Velg **Poster** i handlingsruten.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Opprett et fradrag med arbeidsområdet for fradrag

Opprett et nytt fradrag i arbeidsområdet for fradrag, gjør følgende:

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. I handlingsruten velger du **Oppretthold \> Nytt fradrag**.

    I dialogboksen **Nytt fradrag** defineres feltet **Fradrags-ID** basert på nummerserien for **fradrags-ID** som er definert på siden **Parametere for handelsrabattstyring** (**Salg og markedsføring \> Oppsett \> Handelsrabatter \> Parametere for handelsrabattstyring**).

1. Angi følgende felter:

    - **Kundekonto** – Velg kundekontoen som fradraget gjelder for.
    - **Eksternt kravnummer** – Angi kundens kravreferanse.
    - **Kravbeløp** – Angi avgiftsinklusivt kravbeløp. Verdien må være positiv.
    - **Valuta** – Velg valutaen for fradraget. Standardverdien er valutaen som er angitt for den valgte kundekontoen.
    - **Kravgrunnlag** – Velg kravgrunnlaget. Kravgrunnlaget bestemmer hvilken type kredittransaksjon som opprettes etter at fradraget eller kravet er godkjent.

        - *Prisbasert* – Det opprettes en utkast til fritekstfaktura.
        - *Antallsbasert* – En negativ salgsordre eller returordre opprettes.

    - **Kravdato** – Velg datoen for kravet. Standardverdi er gjeldende dato.
    - **Kravårsak** – Velg årsakskoden som gjelder for gjeldende fradrag. Kravgrunnlaget du valgte, påvirker alternativene som gjelder. Hvis du vil ha mer informasjon om hvordan du oppretter og konfigurerer kravsårsakene som kan velges her, kan du se delen [Opprett fradragsårsaker](#deduction-reasons) tidligere i denne artikkelen.
    - **Merknader** – Legg til eventuelle merknader som gjelder. Når kravet er godkjent, kan godkjenneren redigere eller legge til i kravets merknader.
    - **Opprett kravjournal** – Angi dette alternativet for å angi om det skal opprettes kravjournal når kravet eller fradraget opprettes:

        - *Ja* – Systemet vil opprette og postere en generell journal ved hjelp av kravjournalen som er definert på siden **Kundeparametere**. (Hvis du vil ha mer informasjon, kan du se [Konfigurer kunder og fradrag](#accounts-receivable-deductions) tidligere i denne artikkelen.) Når en faktura er knyttet til kravet, brukes kravjournalen til å redusere saldoen på gjeldende faktura. Hvis kravet senere avvises, tilbakeføres kravjournalen og utligningene (hvis en faktura var tilknyttet).
        - *Nei* – Det opprettes ikke en kravjournal nå. Det blir opprettet når kravet godkjennes. En faktura kan fremdeles knyttes til det nye kravet, selv om det ikke er opprettet en journal for krav. Utligningen kan imidlertid ikke utføres uten kravjournalen.

1. Velg **OK**.

    Det opprettes et nytt fradrag. Hvis du setter alternativet **Opprett kravjournal** til *Ja*, posteres følgende transaksjoner:

    - **To nye kundetransaksjoner** – En transaksjon motposterer kravbeløpet mot den opprinnelige fakturaen. Den andre transaksjonen registrerer en kundes gjeld på kravbeløpet fordi kravet ennå ikke er godkjent. Den opprinnelige fakturatransaksjonen og den motposterte kravtransaksjonen blir automatisk merket for utligning når du knytter fakturaen til fakturaen ved å velge **Vedlikehold \> Tilknytt faktura** i handlingsruten.
    - **To motposteringstransaksjoner** – Disse transaksjonene posteres til finanskontoen **Fradragsforskyvning**.
    - **Kravjournal** – Hvis du vil vise kravjournalen for hvert fradrag som vises på arbeidsområdet for fradrag, velger du fanen **Referanser**. Kravjournalen vises i feltet **Journalpartinummer**. Du kan også vise kravjournalen i fanen **Fradragshendelser**. Der vil det ha **Oppdateringstype**-verdien *Match*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Opprett et fradrag fra en kundeutligning

Prosessen med å opprette et fradrag fra en kundeutligning ligner prosessen med å opprette et fradrag via arbeidsområde for fradrag. Kunde- og fakturavalutaen angis imidlertid automatisk, og fakturaen er tilknyttet. Du trenger ikke å velge **Vedlikehold \> Tilknytt faktura** i handlingsruten når du oppretter et krav eller fradrag via utligningssiden for kunde.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden du vil opprette et fradrag for.
1. Velg **Utlign transaksjoner** i **Send og motta**-fanen i **Utlign**-gruppen i handlingsruten.
1. Velg fakturaen som du vil opprette fradraget mot, i fanen **Oversikt** i dialogboksen **Utlign transaksjoner**.
1. På verktøylinjen velger du **Fradrag \> Nytt fradrag**.

    I dialogboksen **Nytt fradrag** defineres feltet **Fradrags-ID** basert på nummerserien for **fradrags-ID** som er definert på siden **Parametere for handelsrabattstyring** (**Salg og markedsføring \> Oppsett \> Handelsrabatter \> Parametere for handelsrabattstyring**). **Kundekonto**-feltet er angitt til kundekontoen som fradraget gjelder for.

1. Angi følgende felter:

    - **Eksternt kravnummer** – Angi kundens kravreferanse.
    - **Kravbeløp** – Angi avgiftsinklusivt kravbeløp. Verdien må være positiv.
    - **Valuta** – Velg valutaen for fradraget. Standardverdien er valutaen som er angitt for den valgte kundekontoen.
    - **Kravgrunnlag** – Velg kravgrunnlaget. Kravgrunnlaget bestemmer hvilken type kredittransaksjon som opprettes etter at fradraget eller kravet er godkjent.

        - *Prisbasert* – Det opprettes en utkast til fritekstfaktura.
        - *Antallsbasert* – En negativ salgsordre eller returordre opprettes.

    - **Kravdato** – Velg datoen for kravet. Standardverdi er gjeldende dato.
    - **Kravårsak** – Velg årsakskoden som gjelder for gjeldende fradrag. Kravgrunnlaget du valgte, påvirker alternativene som gjelder. Hvis du vil ha mer informasjon om hvordan du oppretter og konfigurerer kravsårsakene som kan velges her, kan du se delen [Opprett fradragsårsaker](#deduction-reasons) tidligere i denne artikkelen.
    - **Merknader** – Legg til eventuelle merknader som gjelder. Når kravet er godkjent, kan godkjenneren redigere eller legge til i kravets merknader.
    - **Opprett kravjournal** – Angi dette alternativet for å angi om det skal opprettes kravjournal når kravet eller fradraget opprettes:

        - *Ja* – Systemet vil opprette og postere en generell journal ved hjelp av kravjournalen som er definert på siden **Kundeparametere**. (Hvis du vil ha mer informasjon, kan du se [Konfigurer kunder og fradrag](#accounts-receivable-deductions) tidligere i denne artikkelen.) Når en faktura er knyttet til kravet, brukes kravjournalen til å redusere saldoen på gjeldende faktura. Hvis kravet senere avvises, tilbakeføres kravjournalen og utligningene (hvis en faktura var tilknyttet).
        - *Nei* – Det opprettes ikke en kravjournal nå. Det blir opprettet når kravet godkjennes. En faktura kan fremdeles knyttes til det nye kravet, selv om det ikke er opprettet en journal for krav. Utligningen kan imidlertid ikke utføres uten kravjournalen.

1. Velg **OK**.

    Det opprettes et nytt fradrag. Hvis du setter alternativet **Opprett kravjournal** til *Ja*, posteres følgende transaksjoner:

    - **To nye kundetransaksjoner** – En transaksjon motposterer kravbeløpet mot den opprinnelige fakturaen. Den andre transaksjonen registrerer en kundes gjeld på kravbeløpet fordi kravet ennå ikke er godkjent. Den opprinnelige fakturatransaksjonen og den motposterte kravtransaksjonen blir automatisk merket for utligning når du knytter fakturaen til fakturaen ved å velge **Vedlikehold \> Tilknytt faktura** i handlingsruten.
    - **To motposteringstransaksjoner** – Disse transaksjonene posteres til finanskontoen **Fradragsforskyvning**.
    - **Kravjournal** – Hvis du vil vise kravjournalen for hvert fradrag som vises på arbeidsområdet for fradrag, velger du fanen **Referanser**. Kravjournalen vises i feltet **Journalpartinummer**. Du kan også vise kravjournalen i fanen **Fradragshendelser**. Der vil det ha **Oppdateringstype**-verdien *Match*.

    Du kommer tilbake til siden **Utligningstransaksjoner**, som nå viser den valgte fakturaen som merket. **Poster**-knappen er bare tilgjengelig hvis du setter alternativet **Opprett kravjournal** til *Ja*. Hvis den er tilgjengelig, velger du **Poster** for å redusere saldoen på fakturaen med verdien for **Kravsbeløp**.

### <a name="create-a-deduction-from-a-customer-page"></a>Opprett et fradrag fra en kundeside

Prosessen med å opprette et fradrag fra en kundeside ligner prosessen med å opprette et fradrag via arbeidsområde for fradrag. Kunden angis imidlertid automatisk.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden du vil opprette et fradrag for.
1. Velg **Opprett fradrag** i gruppen **Fradrag** i fanen **Innhent** i handlingsruten.

    I dialogboksen **Nytt fradrag** defineres feltet **Fradrags-ID** basert på nummerserien for **fradrags-ID** som er definert på siden **Parametere for handelsrabattstyring** (**Salg og markedsføring \> Oppsett \> Handelsrabatter \> Parametere for handelsrabattstyring**). **Kundekonto**-feltet er angitt til kundekontoen som fradraget gjelder for.

1. Angi følgende felter:

    - **Eksternt kravnummer** – Angi kundens kravreferanse.
    - **Kravbeløp** – Angi avgiftsinklusivt kravbeløp. Verdien må være positiv.
    - **Valuta** – Velg valutaen for fradraget. Standardverdien er valutaen som er angitt for den valgte kundekontoen.
    - **Kravgrunnlag** – Velg kravgrunnlaget. Kravgrunnlaget bestemmer hvilken type kredittransaksjon som opprettes etter at fradraget eller kravet er godkjent.

        - *Prisbasert* – Det opprettes en utkast til fritekstfaktura.
        - *Antallsbasert* – En negativ salgsordre eller returordre opprettes.

    - **Kravdato** – Velg datoen for kravet. Standardverdi er gjeldende dato.
    - **Kravårsak** – Velg årsakskoden som gjelder for gjeldende fradrag. Kravgrunnlaget du valgte, påvirker alternativene som gjelder. Hvis du vil ha mer informasjon om hvordan du oppretter og konfigurerer kravsårsakene som kan velges her, kan du se delen [Opprett fradragsårsaker](#deduction-reasons) tidligere i denne artikkelen.
    - **Merknader** – Legg til eventuelle merknader som gjelder. Når kravet er godkjent, kan godkjenneren redigere eller legge til i kravets merknader.
    - **Opprett kravjournal** – Angi dette alternativet for å angi om det skal opprettes kravjournal når kravet eller fradraget opprettes:

        - *Ja* – Systemet vil opprette og postere en generell journal ved hjelp av kravjournalen som er definert på siden **Kundeparametere**. (Hvis du vil ha mer informasjon, kan du se [Konfigurer kunder og fradrag](#accounts-receivable-deductions) tidligere i denne artikkelen.) Når en faktura er knyttet til kravet, brukes kravjournalen til å redusere saldoen på gjeldende faktura. Hvis kravet senere avvises, tilbakeføres kravjournalen og utligningene (hvis en faktura var tilknyttet).
        - *Nei* – Det opprettes ikke en kravjournal nå. Det blir opprettet når kravet godkjennes. En faktura kan fremdeles knyttes til det nye kravet, selv om det ikke er opprettet en journal for krav. Utligningen kan imidlertid ikke utføres uten kravjournalen.

1. Velg **OK**.

    Det opprettes et nytt fradrag. Hvis du setter alternativet **Opprett kravjournal** til *Ja*, posteres følgende transaksjoner:

    - **To nye kundetransaksjoner** – En transaksjon motposterer kravbeløpet mot den opprinnelige fakturaen. Den andre transaksjonen registrerer en kundes gjeld på kravbeløpet fordi kravet ennå ikke er godkjent. Den opprinnelige fakturatransaksjonen og den motposterte kravtransaksjonen blir automatisk merket for utligning når du knytter fakturaen til fakturaen ved å velge **Vedlikehold \> Tilknytt faktura** i handlingsruten.
    - **To motposteringstransaksjoner** – Disse transaksjonene posteres til finanskontoen **Fradragsforskyvning**.
    - **Kravjournal** – Hvis du vil vise kravjournalen for hvert fradrag som vises på arbeidsområdet for fradrag, velger du fanen **Referanser**. Kravjournalen vises i feltet **Journalpartinummer**. Du kan også vise kravjournalen i fanen **Fradragshendelser**. Der vil det ha **Oppdateringstype**-verdien *Match*.

## <a name="create-a-credit-note-for-a-customer"></a>Opprett en kredittnota for kunden

Etter en godkjent rabatt finnes for en kunden, kan du opprette en kreditnota på kundens konto for rabatten etter behov. Kreditten vises deretter i arbeidsområdet for fradrag, der den kan utlignes med et fradrag.

Hvis du vil opprette en kreditnota, gjør du følgende:

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Velg kunden.
1. Velg **Utlign transaksjoner** i **Send og motta**-fanen i **Utlign**-gruppen i handlingsruten.
1. Velg transaksjonen som rabatten ble brukt på, i dialogboksen **Utligne transaksjoner**.
1. Velg det valgte rabattprogrammet som gjelder, på **Funksjoner**-menyen på verktøylinjen.
1. Velg **Merk av**-boksen for den aktuelle rabatt-ID-en på **Rabatt**-siden i fanen **Oversikt**.
1. Velg **Funksjoner \> Opprett kreditnota** i handlingsruten.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Behandle et fradrag i arbeidsområdet for fradrag

I arbeidsområdet for fradrag kan du samsvare fradrag til åpne kredittransaksjoner, dele fradrag, nekte fradrag og skrive av fradrag.

Avhengig av hvordan du vil behandle et fradrag, kan du utføre en eller flere av følgende prosedyrer i følgende underdeler. Du kan kombinere fremgangsmåtene etter behov. Du kan for eksempel dele et fradrag i to deler, og deretter samsvare én del med en kreditering, men legge den gjenværende delen igjen i arbeidsområdet for å samsvare den med en annen kreditering senere. Du kan også samsvare et fradrag med en kreditt som er mindre enn fradragsbeløpet og deretter avslå eller avskrive den gjenstående saldoen for fradraget.

### <a name="match-a-deduction-to-a-credit"></a>Samsvar et fradrag med en kreditt

Følg denne fremgangsmåten for å få samsvar mellom et fradrag og kreditering.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. Velg **Merk av**-boksen for krediten som skal samsvare med fradraget, i delen **Åpne transaksjoner**. Hvis flere kreditter er oppført, kan du velge flere enn én kreditt du vil samsvare med fradraget. Hvis du vil at systemet automatisk skal velge kreditt som samsvarer med beløpet i fradraget, velger du et passende alternativ på menyen **Velg fradragsbeløp**.
1. Klikk på **Vedlikehold \> Samsvar** i handlingsruten. Systemet samsvarer fradraget til kreditten. Hvis det gjenstår en saldo i fradraget, vises det i **Gjenværende beløp**-feltet i fanen **Fradrag**.

    > [!NOTE]
    > For fradrag som ble opprettet ved å bruke kommandoen **Ny fratrekk** på arbeidsområdet, kundeutligning eller kundesiden, er kommandoen **Vedlikehold \> Samsvar** bare tilgjengelig hvis feltet **Kravstatus** er satt til *Godkjenn*. Denne kommandoen kan brukes til å samsvare den prisbaserte eller antallsbaserte transaksjonen manuelt med den tilknyttede kreditten i **Åpne transaksjoner**-delen. Denne kreditten opprettes enten når fradraget godkjennes (ved å bruke kommandoen **Vedlikehold \> Godkjenn fradrag**), eller når det er knyttet til en eksisterende kreditt som beskrevet i delen [Kreditter som er opprettet utenfor godkjenningsfradragsprosessen](#credits-outside-approval) senere i denne artikkelen. Den periodiske oppgaven *Utligne godkjente fradrag* (**Salgsmarkedsføring \> Periodiske oppgaver \> Utligne godkjente fradrag**) kan også brukes til å samsvare automatisk fradrag og kreditt som har samsvarende **fradrags-ID**-verdier og -beløp.

### <a name="split-a-deduction"></a>Del et fradrag

Hvis du vil dele et fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. Klikk på **Vedlikehold \> Del** i handlingsruten.
1. Angi beløpet som skal deles fra hovedfradraget, i **Delt beløp**-feltet i **Del**-dialogboksen Del. Velg deretter **OK**.
1. I fanen **Fradrag** kan du legge merke til at det vises en ny post for det delte beløpet. Den opprinnelige fradragsposten inneholder resten av fradragssaldoen. Du kan nå administrere de to delene av den opprinnelige rabatten separat.
1. Velg den opprinnelige fradragsposten, og velg deretter fanen **Referanser**. **Delt beløp**-feltet viser beløpet som ble delt opp fra det opprinnelige beløpet.

### <a name="attach-an-invoice-to-a-deduction"></a>Knytt en faktura til et fradrag

Du kan knytte en faktura til et fradrag hvis fradraget ble opprettet ved hjelp av kommandoen **Nytt fradrag**-kommando på arbeidsområdet for fradrag, kundeutligning eller kundesiden, og hvis det ikke er knyttet noen faktura til det (det vil si at **Faktura**-kolonnen er tom).

Følg denne fremgangsmåten for å knytte en faktura til et fradrag.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. I handlingsruten velger du **Oppretthold \> Tilknytt faktura**.
1. Velg en faktura i dialogboksen **Tilknytt faktura**, og velg deretter **OK**.
1. Følg et av disse trinnene i dialogboksen **Utligne transaksjoner**, avhengig av om det ble postert en kravjournal da fradraget ble opprettet:

    - Hvis en kravjournal er postert, viser fakturaen du valgte, og kravjournalens kundekredittransaksjon er merket i **Merk**-kolonnen. Velg **Poster**. Gjenværende saldo på den tilknyttede fakturaen reduseres med kravbeløpet.
    - Hvis en kravjournal ikke er postert, vises det en hake i **Merk**-kolonnen. Fordi du ikke kan motpostere mot en kravjournal før fradraget er godkjent, velger du **Avbryt**.

### <a name="detach-an-invoice-from-a-deduction"></a>Koble en faktura fra et fradrag

Du kan koble en faktura fra et fradrag hvis fradraget ble opprettet ved hjelp av kommandoen **Nytt fradrag**-kommando på arbeidsområdet for fradrag, kundeutligning eller kundesiden, og hvis det er knyttet en faktura til det (det vil si at **Faktura**-kolonnen viser et fakturanummer), og hvis **Kravstatus**-feltet er angitt til *Åpen*. Du kan fullføre denne oppgaven fordi du har lagt ved uriktig faktura. Fakturaen fjernes fra fradraget, og den gjenværende saldoen oppdateres hvis den ble redusert da fakturaen var tilknyttet.

Hvis du vil koble fra en faktura, gjør du følgende.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. I handlingsruten velger du **Oppretthold \> Koble fra faktura**.

### <a name="approve-a-deduction"></a>Godkjenn et fradrag

Du kan godkjenne fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden. Du kan imidlertid bare godkjenne fradrag der **Kravstatus**-feltet er satt til *Åpen*.

Hvis du vil godkjenne et fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. I handlingsruten velger du **Oppretthold \> Godkjenn fradrag**.
1. Rediger eller legg til informasjon i **merknadsverdien** i dialogboksen **Godkjenn fradrag** etter behov.
1. Hvis fradraget er prisbasert og en faktura ikke er knyttet til det, velger du en mva-gruppe for vare. Vanligvis angis mva-varegruppen på fakturaen. Derfor må mva-varekoden angis når den ikke er knyttet til en faktura.
1. Velg **OK**.

    På dette tidspunktet kan det ikke gjøres flere endringer i fradraget. Hvis alternativet **Opprett kravjournal** ble satt til *Nei* da fradraget ble opprettet, opprettes kravjournalen og posteres når fradraget godkjennes. Når fradraget er godkjent, opprettes og åpnes kreditten automatisk. Typen avhenger av fradragets verdi for **kravgrunnlagsverdi**:

    - *Prisbasert* – Hvis fradraget er prisbasert, opprettes det en fritekstfaktura for kundekontoen. Du kan legge til en beskrivelse og postere kreditten. Følgende felter fylles ut av fradraget når utkastet opprettes:

        - **Fradrags-ID** – Dette feltet legges til i hodet for å aktivere sporbarhet tilbake til fradraget.
        - **Hovedkonto** – Verdien bestemmes av verdien for **posteringskonto for krav** som er angitt for fradragsårsaken som er tilordnet fradraget.
        - **Mva-gruppe for vare** – Verdien bestemmes av den tilknyttede fakturaen eller av verdien du valgte da du godkjente fradraget.
        - **Enhetspris** – Verdien er krediten av fradragets kravbeløp.
        - **Fakturatekst** – Som standard er dette feltet satt til fradragets **Merknader**-verdi.

    - *Antallsbasert* – Hvis fradraget er antallsbasert, opprettes det en åpen salgsordre eller returordre. Innstillingen **Opprett returordre** på siden **[Kundeparametere](#accounts-receivable-deductions)** bestemmer om det opprettes en salgsordre eller en returordre når fradraget godkjennes. **Kopier ordrer**-siden vises og filtreres for å vise rader der **Fakturakonto**-feltet er satt til fradragets kundekonto. Følg disse trinnene:

        1. I hurtigfanen **Fakturaer** viser **Hoder**-delen salgsfakturaer der **Fakturakonto**-verdien samsvarer med fradragets kundekonto. Velg en salgsfaktura som gjelder.
        1. **Linjer**-delen viser linjer fra den valgte salgsfakturaen. Merk av for **Velg** for hver linje du vil kopiere. I **Hoder**-delen kan du eventuelt merke av for **Merk alle** for salgsordren hvis du vil merke alle linjene i den.
        1. Juster **Antall**-verdien for en eller flere linjer etter behov.

            Alle linjene du har valgt hittil, vises i hurtigfanen **Valgte linjer eller hoder som skal kopieres**.

        1. Gjenta de to foregående trinnene etter behov til alle de obligatoriske linjene er oppført i hurtigfanen **Valgte linjer eller hoder som skal kopieres**.
        1. Velg **OK**.

            Den nye returordren åpnes, og følgende felter angis automatisk:

            - **Fradrags-ID** – Dette feltet legges til i hodet for å aktivere sporbarhet tilbake til fradraget.
            - **Kode for returårsak** – Som standard er dette feltet satt til verdien for **returårsakskode** som er angitt for fradragsårsaken som er tilordnet fradraget.

Når kreditten er fakturert, vises den i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag mot gjeldende **Fradrags-ID**-verdi for fradrag, og feltet **Kravstype** er satt til *Andre kreditter*. Kreditten vil være tilgjengelig til den er utlignet med fradraget på en av følgende måter:

- Du utligner det manuelt ved å velge **Vedlikehold \> Samsvar** i handlingsruten.
- Den utlignes automatisk av den periodiske jobben *Utligne godkjente krav* (**Salg og markedsføring \> Periodiske oppgaver \> Utligne godkjente krav**).
- Den utlignes automatisk, fordi alternativet **Automatisk utligning** i fanen **Utligning** på siden **Kundeparametere** er satt til *Ja*.

Hvis du vil vise kreditten som opprettes når fradraget godkjennes, kan du også bruke **Åpne kreditt**-knappen i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag.

### <a name="create-a-return-order"></a>Opprette en returordre

Du kan opprette en returordre for fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden. Alle følgende betingelser må imidlertid være oppfylt:

- **Kravgrunnlag**-feltet er satt til *Antallsbasert*.
- **Kravstatus** – Dette feltet er satt til *Åpen*.
- Alternativet **Opprett returordre** i fanen **Fradrag** på siden **[Kundeparametere](#accounts-receivable-deductions)** er satt til *Ja*.
- Alternativet **Opprett returordre før fradragsgodkjenning** i fanen **Fradrag** på siden **[Kundeparametere](#accounts-receivable-deductions)** er satt til *Ja*.

Følg denne fremgangsmåten for å opprette en returordre.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. I handlingsruten velger du **Vedlikehold \> Opprett returordre**.
1. Rediger eller legg til informasjon i **Merknader**-verdien i dialogboksen **Godkjenn fradrag** etter behov, og velg **OK**.
1. I dialogboksen **Kopier ordrer** i hurtigfanen **Fakturaer** viser **Hoder**-delen salgsfakturaer der **Fakturakonto**-verdien samsvarer med fradragets kundekonto. Velg en salgsfaktura som gjelder.
1. **Linjer**-delen viser linjer fra den valgte salgsfakturaen. Merk av for **Velg** for hver linje du vil kopiere. I **Hoder**-delen kan du eventuelt merke av for **Merk alle** for salgsordren hvis du vil merke alle linjene i den.
1. Juster **Antall**-verdien for en eller flere linjer etter behov.

    Alle linjene du har valgt hittil, vises i hurtigfanen **Valgte linjer eller hoder som skal kopieres**.

1. Gjenta de to foregående trinnene etter behov til alle de obligatoriske linjene er oppført i hurtigfanen **Valgte linjer eller hoder som skal kopieres**.
1. Velg **OK**.

    Den nye returordren åpnes, og følgende felter angis automatisk:

    - **Fradrags-ID** – Dette feltet legges til i hodet for å aktivere sporbarhet tilbake til fradraget.
    - **Kode for returårsak** – Som standard er dette feltet satt til verdien for **returårsakskode** som er angitt for fradragsårsaken som er tilordnet fradraget.

### <a name="deny-a-deduction"></a>Avvis et fradrag

Hvis du vil avvise et fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. Klikk på **Vedlikehold \> Avvis** i handlingsruten.
1. Velg årsakskoden for avvisning i dialogboksen **Avvis**, og velg deretter **OK**.
1. Velg *Lukket* i **Vis**-feltet under handlingsruten.

    Fanen **Fradrag** viser det avviste fradraget, og **Gjenværende beløp**-feltet for fradraget er satt til *0,00*.

    For fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden, forekommer følgende hendelser.

    - Feltene i **Avvisning**-delen oppdateres i fanen **Referanser**.
    - Hvis du valgte å opprette kravjournalen da fradraget ble opprettet, og hvis en faktura er knyttet til fradraget som reduserte fakturaens saldo, blir fakturaen koblet fra, og den gjenværende saldoen til den tidligere tilknyttede fakturaen økes med det avviste beløpet for kravet.
    - **Statusfeltet** for fradraget er satt til *Lukket*.
    - **Kravstatus**-feltet for fradraget er satt til *Avvist*.

Hvis du vil omgjøre en avvisning, følger du fremgangsmåten nedenfor.

1. Velg et avvist fradrag i fanen **Fradrag**.
1. Velg **Angre avvisning** i handlingsruten.

    For fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden, forekommer følgende hendelser.

    - Feltene i **Avvisning**-delen oppdateres i fanen **Referanser**.
    - **Statusfeltet** for fradraget er satt til *Åpen*.
    - **Kravstatus**-feltet for fradraget er satt til *Åpen*.

### <a name="write-off-a-deduction"></a>Avskriv et fradrag

Hvis du vil avskrive et fradrag, følger du fremgangsmåten nedenfor.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen for fradraget som skal behandles.
1. Klikk på **Vedlikehold \> Avskrivning** i handlingsruten.
1. Velg årsakskoden for avskrivningen i dialogboksen **Avskriving**, og velg deretter **OK**.
1. I **Vis**-feltet velger du *Lukket*.

    Fanen **Fradrag** viser det avskrevne fradraget, og **Gjenværende beløp**-feltet for fradraget er satt til *0,00*.

    For fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden, forekommer følgende hendelser.

    - Feltene i **Avskrivning**-delen oppdateres i fanen **Referanser**.
    - Hvis du opprettet kravjournalen da fradraget ble opprettet, posteres en kravjournal til fradragets årsakskode for avskrivning. Du kan vise denne oppføringen i fanen **Fradragshendelser**, der den har **oppdateringstypeverdien** *Avskrivning*.
    - **Statusfeltet** for fradraget er satt til *Lukket*
    - **Kravstatus**-feltet for fradraget er satt til *Avskrivning*.

Hvis du vil reversere en avskrivning, følger du fremgangsmåten nedenfor.

1. Velg et avvist fradrag i fanen **Fradrag**.
1. Klikk på **Reverser avskrivning** i handlingsruten.

    For fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden, forekommer følgende hendelser.

    - Feltene i **Avskrivning**-delen oppdateres i fanen **Referanser**.
    - Hvis du opprettet kravjournalen da fradraget ble opprettet, posteres en kravjournal til fradragets årsakskode for avskrivning. Du kan vise denne oppføringen i fanen **Fradragshendelser**, der den har **oppdateringstypeverdien** *Reverser avskrivning*.
    - **Statusfeltet** for fradraget er satt til *Åpen*.
    - **Kravstatus**-feltet for fradraget er satt til *Åpen*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kreditter opprettet utenfor Godkjenn fradrag-prosessen

Denne delen gjelder bare fradrag som ble opprettet ved hjelp av kommandoen **Nytt fradrag** på arbeidsområdet for fradrag, kundeutligning eller kundesiden.

Det kan hende at forskjellige brukere allerede har opprettet en fritekstfaktura, en returordre eller en negativ salgsordre for en kundes krav utenfor **Godkjenn fradrag**-prosessen. Når det eksisterende fradraget godkjennes på arbeidsområdet for fradrag, oppretter systemet automatisk en annen fritekstfaktura, returordre eller negativ salgsordre. Denne delen beskriver hvordan du knytter eksisterende kreditt til et fradrag før fradraget godkjennes, for å forhindre dupliserte kreditter.

### <a name="attach-a-credit-to-deduction"></a>Knytte en kreditt til fradrag

Denne delen beskriver hvordan du kan knytter en kreditt til et fradrag fra kreditten.

Etter at en kredit er knyttet til fradraget, kan du vise den ved å bruke **Åpne kreditt**-knappen på verktøylinjen i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag.

Når en kredit er fakturert og fradraget er godkjent, vises krediten i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag mot gjeldende **Fradrags-ID**-verdi for fradrag, og feltet **Kravstype** er satt til *Andre kreditter*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Knytt en fritekstfaktura til et fradrag

Følg denne fremgangsmåten for å knytte en fritekstfaktura til et fradrag.

1. Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.
1. Velg den aktuelle fakturaen.
1. Velg **Knytt kredit til fradrag** i **Faktura**-fanen i handlingsruten. Denne knappen er tilgjengelig bare hvis fritekstfakturaens **Fradrags-ID**-felt er tomt. Et tomt felt angir at fritekstfakturaen ikke allerede er knyttet til et fradrag.
1. På siden **Knytt kreditt til fradrag** kan du velge *ett* fradrag. Bare åpne *prisbaserte* fradrag kan velges.
1. Velg **OK**. **Fradrags-ID**-feltet er definert på hodet til fritekstfakturaen.

#### <a name="attach-a-return-order-to-a-deduction"></a>Knytt en returordre til et fradrag

Følg denne fremgangsmåten for å knytte en returordre til et fradrag.

1. Gå til **Kunde \> Ordrer \> Alle returordrer**.
1. Velg det mottatte eller åpne autorisasjonsreturnummeret (RMA).
1. Velg **Knytt kredit til fradrag** i **Returordre**-fanen i handlingsruten. Denne knappen er tilgjengelig bare hvis returordrens **Fradrags-ID**-felt er tomt. Et tomt felt angir at returordre ikke allerede er knyttet til et fradrag.
1. På siden **Knytt kreditt til fradrag** kan du velge *ett* fradrag. Bare åpne *antallsbaserte* fradrag kan velges.
1. Velg **OK**. **Fradrags-ID**-feltet er definert på hodet til returordren.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Knytt en salgsordre til et fradrag

Følg denne fremgangsmåten for å knytte en salgsordre til et fradrag.

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**.
1. Velg den aktuelle åpne, leverte eller fakturerte salgsordren.
1. Velg **Knytt kredit til fradrag** i **Faktura**-fanen i handlingsruten. Denne knappen er tilgjengelig bare hvis salgsordrens **Fradrags-ID**-felt er tomt. Et tomt felt angir at salgsordre ikke allerede er knyttet til et fradrag.
1. På siden **Knytt til fradrag** kan du velge *ett* fradrag. Bare åpne *antallsbaserte* fradrag kan velges.
1. Velg **OK**. **Fradrags-ID**-feltet er definert på hodet til salgsordren.

#### <a name="detach-a-deduction-from-a-credit"></a>Koble et fradrag fra en kredit

Hvis feil fradrag er tilknyttet, kan du koble det fra kreditten. Alle følgende betingelser må imidlertid være oppfylt:

- En kreditt er knyttet til fradraget.
- **Kravstatus** – Dette feltet er satt til *Åpen*.

Følg et av disse trinnene for å koble et fradrag fra en kredit, avhengig av kredittypen:

- **Fritekstfakturaer:** Velg en faktura på siden **Alle fritekstfakturaer**. Velg deretter **Koble kredit fra fradrag** i **Faktura**-fanen i handlingsruten.
- **Returordrer:** Velg en ordre på siden **Alle returordrer**. Velg deretter **Koble kredit fra fradrag** i **Returordre**-fanen i handlingsruten.
- **Salgsordrer:** Velg en ordre på siden **Alle salgsordrer**. Velg deretter **Koble kredit fra fradrag** i **Faktura**-fanen i handlingsruten.

### <a name="attach-a-deduction-to-a-credit"></a>Knytt et fradrag til en kreditt

Denne delen beskriver hvordan du kan knytter et fradrag til en kreditt fra fradraget.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Knytt et fradrag til en fritekst-, returordre- eller salgsordrekreditt

Følg denne fremgangsmåten for å knytte et fradrag til en fritekst-, returordre- eller salgsordrekreditt.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. Velg det åpne fradraget som skal brukes.
1. I handlingsruten velger du **Oppretthold \> Knytt fradrag til kredit**. Denne knappen er bare tilgjengelig hvis **Kravstatus**-feltet er satt til *Åpen*.
1. På siden **Knytt til kredit** kan du velge *én* kredit. Typen kreditt som vises, er avhengig av fradragets **kravgrunnlagsverdi**:

    - *Prisbasert* – Siden viser fritekstfakturaer for kundekontoen der feltet **Fradrags-ID** er tomt. Kunderekvisisjoner vises også, fordi fritekstfakturaen kan være upostert. Derfor er det ikke sikkert at det har et tall som det er referanse til.
    - *Antallsbasert* – Typen kreditt som vises, avhenger av innstillingen for alternativet **Opprett returordre** på siden **[Kundeparametere](#accounts-receivable-deductions)**:

        - *Ja* – Siden viser returordrer for kundekontoen der feltet **Fradrags-ID** er tomt.
        - *Nei* – Siden viser salgsordrer for kundekontoen der feltet **Fradrags-ID** er tomt.

1. Velg **OK**. **Fradrags-ID**-feltet er definert på hodet til kreditten.

Etter at en kredit er knyttet til fradraget, kan du vise den ved å bruke **Åpne kreditt**-knappen på verktøylinjen i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag.

Når en kredit er fakturert og fradraget er godkjent, vises krediten i **Åpne transaksjoner**-delen i arbeidsområdet for fradrag mot gjeldende **Fradrags-ID**-verdi for fradrag, og feltet **Kravstype** er satt til *Andre kreditter*.

#### <a name="detach-a-credit-from-the-deduction"></a>Koble en kredit fra fradraget

Hvis feil kredit er tilknyttet, kan du koble det fra fradraget. Velg **Koble fradrag fra kredit** i **Vedlikehold**-gruppen i handlingsruten. Verdien **Fradrags-ID** fjernes fra kreditten.

Knappen **Koble fradrag fra kredit** er bare tilgjengelig hvis følgende betingelser er oppfylt:

- En kreditt er knyttet til fradraget.
- **Kravstatus** – Dette feltet er satt til *Åpen*.

## <a name="create-a-one-time-promotion"></a>Opprett en engangskampanje

Noen ganger kan det hende du ikke har en godkjent rabatt som du kan samsvare med et fradrag. I dette tilfellet kan du bruke funksjonen *engangskampanje* for å samsvare fradraget med en handelsrabatt som er knyttet til kunden. Funksjonen *engangskampanje* oppretter en ny handelsrabattavtale og en varehandelshendelse for engangsbeløp. Den samsvarer deretter engangsbeløpet med fradraget, og gjør de nødvendige posteringene for å lukke fradraget.

Denne funksjonen er nyttig hvis du bruker handelsrabatter. Hvis du vil ha mer informasjon om handelsrabatter, kan du se [Handelsrabattstyring](../sales-marketing/trade-allowance.md).

Du må først definere en mal som kan brukes til å opprette den nye handelsrabattavtalen. Hvis du vil konfigurere en mal, følger du fremgangsmåten nedenfor.

1. Gå til **Salg og markedsføring \> Handelsrabatter \> Maler**.
1. Velg **Ny** i handlingsruten.
1. I feltene angir du informasjonen som skal vises i avtalene som er opprettet fra malen.
1. I hurtigfanen **Kunder** i feltet **Hierarki** velger du et hierarkinivå.
1. Velg kunden som har et trekk uten samsvar, i hierarkilisten, og velg deretter pil høyre (**\>**). Kunden legges til i **kundelisten for handelsrabattavtale**.
1. Angi de gjenværende feltene etter behov, og lukk deretter siden.
1. Gå til **Salg og markedsføring \> Oppsett \> Handelsrabatt \> Parametere for handelsrabattstyring**.
1. Velg navnet på malen som skal brukes til å opprette engangskampanjer, i feltet **Mal for engangskampanje** i fanen **Oversikt**.

Du kan deretter opprette en engangskampanje i arbeidsområdet for fradrag. Hvis du vil opprette en engangskampanje, gjør du følgende.

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. **Merk av**-boksen ved siden av fradraget som skal behandles.
1. Velg **Vedlikehold \> Utligningsfradrag som engangskampanje** i handlingsruten.
1. Bruk følgende fremgangsmåte i dialogboksen **Engangskampanje** for å knytte fradraget til en eller flere finansieringer:

    1. Velg **Ny**, og velg en finansierings-ID i feltet **Finansierings-ID**. Gjenta dette trinnet for å legge til så mye midler som du trenger.
    1. I **Prosent**-feltet ved siden av hver finansierings-ID angir du prosentandelen av fradraget som skal tildeles finansieringen. Beløpene du angir i **Prosent**-feltene, må utgjøre 100 prosent.

1. Velg **OK**. Systemet oppretter en ny handelsrabattavtale med et engangsbeløp for en varehandelshendelse, og samsvarer engangsbeløpet med fradraget.

## <a name="do-a-mass-update-of-deductions"></a>Utføre en masseoppdatering av fradrag

Hvis du må gjøre samme endring i flere fradrag, kan du velge disse fradragene og utføre en masseoppdatering av feltene for dem.

Hvis du vil utføre en masseoppdatering, gjør du følgende:

1. Gå til **Salg og markedføring \> Handelsrabatter \> Fradrag \> Arbeidsområde for fradrag**.
1. Velg fradragstypen du vil vise, i **Vis**-feltet under handlingsruten.
1. Merk av ved siden av hvert fradrag du vil oppdatere. I handlingsruten velger du **Oppretthold \> Masseoppdatering**.
1. Dialogboksen **Masseoppdatering** viser de valgte fradragene. Oppdater feltene etter behov, og velg deretter **OK** for å godta endringene.
