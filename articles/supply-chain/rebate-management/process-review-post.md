---
title: Behandle, gjennomgå og postere rabatter
description: Dette emnet beskriver hvordan du behandler rabattbehandlingsavtalene, beregner rabattene, går gjennom transaksjonene som er generert, posterer transaksjoner og gjennomgår posteringene.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 82b8a4e6ba7ebea7df9f5dad5abc3dfc3ce2687d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270767"
---
# <a name="process-review-and-post-rebates"></a>Behandle, gjennomgå og postere rabatter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du behandler rabattbehandlingsavtalene, beregner rabattene, går gjennom transaksjonene som er generert, posterer transaksjoner og gjennomgår posteringene.

## <a name="change-the-status-of-a-deal"></a>Endre status for en avtale

Du kan tilordne en status til hver avtale for å spore den enklere. Statusen er bare beregnet til informasjon.

1. Velg en avtale (for eksempel på siden [**Alle rabattbehandlingsavtaler**](rebate-management-deals.md)).
1. I handlingsruten, på fanen **Rabattbehandlingsavtaler**, i **Vedlikehold**-gruppen, velger du **Endre status**.
1. I dialogboksen **Endre status** setter du **Rabattstatus**-feltet til ny status.
1. Velg **OK**.

## <a name="calculate-fifo-purchase-prices"></a>Beregn FIFO-innkjøpspriser

Den periodiske oppgaven **Beregn FIFO-innkjøpspriser** må kjøres for å beregne rabattene for [avtaler](rebate-management-deals.md) der **Prisgrunnlag**-feltet er satt til *FIFO*. Systemet bruker en FIFO-regel (først-inn-først-ut) til å beregne verdien av lageret som ble solgt. Denne verdien blir deretter brukt til å beregne leverandørrabattene.

Gå til **Rabattbehandling \> Periodiske oppgaver \> Beregn FIFO-innkjøpspriser**. Velg **OK** i dialogboksen som vises, for å kjøre beregningen.

## <a name="process-rebate-management-deals"></a>Behandle rabattbehandlingsavtaler

Når du behandler en avtale, beregner systemet alle relevante rabatter og royalty som er satt opp. Bare valgte avtaler som har beregningsperioder som er klare til å beregnes, og som har statusen *Aktiv*, blir behandlet. Når behandlingen er fullført, genererer systemet et sett med transaksjoner som du kan gå gjennom og deretter postere.

> [!NOTE]
> I alle tilfeller behandles rabatter på det nivået som er angitt av hver avtales innstilling for **Avstem etter** (*Avtale* eller *Linje*). Du kan bare utføre enkeltlinjeberegninger for avtaler der feltet **Avstem etter** er satt til *Linje*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Behandle alle linjer for én eller flere avtaler

1. Åpne den aktuelle [rabattavtalelistesiden](rebate-management-deals.md) for avtaletypen du vil arbeide med.
1. Velg raden for hver avtale du vil behandle (eller åpne avtalen du vil behandle).
1. I handlingsruten, på fanen **Rabattbehandlingsavtaler**, i **Generer**-gruppen, velger du én av følgende kommander:

    - **Behandle \> Klargjør** – Klargjør et sett med avsetninger for hver relevante rabattavtalen, men ikke poster dem. Dette menyelementet er ikke tilgjengelig for avtaler der **Rabattlevering**-feltet er satt til *Vare*.
    - **Behandle \> Rabattbehandling** – Behandle en serie med transaksjoner som oppgir verdien av rabatten for hver avtale.
    - **Prosess \> Avskrivning** – For hver kildetransaksjon for rabattavtalen og den angitte perioden behandler du avviket mellom beløpene som ble postert for en avsetning og for rabattbehandling. Dette menyelementet er ikke tilgjengelig for avtaler der **Rabattlevering**-feltet er satt til *Vare*.

1. I dialogboksen som vises, angir du feltene **Fra dato** og **Til dato** for å definere datoområdet for beregningen.
1. Velg **OK** for å kjøre beregningen.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Behandle én eller flere bestemte avtalelinjer for en valgt avtale

1. Åpne den aktuelle [rabattavtalelistesiden](rebate-management-deals.md) for avtaletypen du vil arbeide med.
1. Åpne avtalen du vil behandle en linje fra.
1. Velg **Linjer**-fanen i øvre høyre hjørne.
1. På **Rabattbehandling**-hurtigfanen velger du raden for hver avtalelinje du vil behandle.
1. På verktøylinjen på **Rabattbehandling**-hurtigfanen velger du en av følgende kommandoer. (Disse kommandoene er bare tilgjengelige for avtaler der **Avstem etter**-feltet er satt til *Linje*.)

    - **Behandle \> Klargjør** – Klargjør et sett med avsetninger for hver relevante avtalelinjen, men ikke poster dem. Dette menyelementet er ikke tilgjengelig for avtaler der **Rabattlevering**-feltet er satt til *Vare*.
    - **Behandle \> Rabattbehandling** – Behandle en serie med transaksjoner som oppgir verdien av rabatten for hver avtalelinje.
    - **Prosess \> Avskrivning** – For hver kildetransaksjon for rabattavtalen og den angitte perioden behandler du avviket mellom beløpene som ble postert for en avsetning og for rabattbehandling. Dette menyelementet er ikke tilgjengelig for avtaler der **Rabattlevering**-feltet er satt til *Vare*. 

1. I dialogboksen som vises, angir du feltene **Fra dato** og **Til dato** for å definere datoområdet for beregningen.
1. Velg **OK** for å kjøre beregningen.

### <a name="process-deals-using-a-batch-job"></a>Behandle avtaler ved hjelp av en satsvis jobb

I stedet for å behandle bestemte avtaler eller avtalelinjer kan du kjøre en satsvis jobb for å behandle flere avtaler samtidig. Du kan eventuelt bruke postfiltre og/eller definere en gjentakende plan. Følg denne fremgangsmåten for å behandle avtaler ved hjelp av en satsvis jobb.

1. Følg ett av disse trinnene:

    - Gå til **Rabattbehandling \> Periodiske oppgaver \> Behandle \> Klargjør** for å klargjøre et sett med avsetninger for hver relevante avtale, men uten å postere dem.
    - Gå til **Rabattbehandling \> Periodisk oppgaver \> Behandle \> Rabattbehandling** for å behandle en serie med transaksjoner som utgjør verdien av rabatten for hver avtale.
    - Gå til **Rabattbehandling \> Periodiske oppgaver \> Behandle \> Avskrivning** for å tilbakeføre tidligere posterte transaksjoner for å skrive dem av, slik at nye rabattavtaletransaksjoner kan beregnes.

1. I dialogboksen som vises, på **Parametere**-hurtigfanen, i **Periode**-delen setter du feltene **Fra dato** og **Til dato** for å definere datoområdet for transaksjoner for beregningen.
1. I delen **Garantiperiode** setter du feltene **Fra dato** og **Til dato** for å definere datoområdet for beregningen.
1. På hurtigfanen **Poster som skal inkluderes**, kan du definere filtre for å begrense settet med avtaler som den satsvise jobben skal behandle. Disse innstillingene fungerer på samme måte som de arbeider for andre typer satsvise jobber.
1. På hurtigfanen **Kjør i bakgrunnen** kan du konfigurere alternativer for satsvis behandling og planlegging etter behov. Disse innstillingene fungerer på samme måte som de arbeider for andre typer satsvise jobber.
1. Velg **OK** for å kjøre og/eller planlegge beregningen.

## <a name="view-and-edit-rebate-management-transactions"></a>Vis og rediger rabattbehandlingstransaksjoner

Når du behandler én eller flere avtaler, oppretter systemet transaksjoner som du kan vise og kanskje redigere før du posterer dem.

1. Følg ett av disse trinnene:

    - Velg avtalen du vil vise transaksjoner for (for eksempel på siden [**Alle rabattbehandlingsavtaler**](rebate-management-deals.md)). I handlingsruten, på fanen **Rabattbehandlingsavtaler**, i **Transaksjoner**-gruppen, velger du **Transaksjoner** eller **Garantitransaksjoner**, alt etter typen transaksjon du ønsker å vise.
    - Åpne en avtale (for eksempel på siden [**Alle rabattbehandlingsavtaler**](rebate-management-deals.md)) for å vise detaljene. På hurtigfanen **Rabattbehandling** velger du avtalelinjen du vil vise transaksjoner for. På verktøylinjen velger du deretter **Transaksjoner** eller **Garantitransaksjoner**, alt etter typen transaksjon du vil vise. (Disse knappene er bare tilgjengelige for avtaler der **Avstem etter**-feltet er satt til *Linje*.)

1. Siden **Datotransaksjoner for rabattbehandling** eller **Garantitransaksjoner for rabattbehandling** vises. Den inneholder et rutenett, der hver linje representerer en samling transaksjoner fra en enkelt rabatt- eller garantiperiode. Velg en rad i rutenettet, og velg deretter **Kildetransaksjoner** i handlingsruten for å vise transaksjonene som tilhører denne raden.
1. Siden som vises, viser en liste over transaksjonene av den valgte typen som tilhører den valgte raden. Hver transaksjon gir relevante detaljer, avhengig av transaksjonstypen. For garantitransaksjoner kan du bare vise listen. For andre transaksjonstyper kan du utføre følgende handlinger på denne siden:

    - Hvis du vil kontrollere totalverdien til alle innkrevde transaksjoner på siden, kan du vise feltet **Kravbeløp**.
    - Hvis du vil vise mer informasjon om en transaksjon, kan du velge den og deretter velge fanen **Generelt**, **Finansdimensjon** eller **Dimensjon**.
    - Hvis du vil vise reduksjoner som gjelder, velger du **Reduksjonstransaksjoner** i handlingsruten. Hvis du vil ha mer informasjon, kan du se [Prinsipper for rabattreduksjon](rebate-reduction-principle.md).
    - Hvis du vil merke transaksjoner som enten er gjort krav på eller ikke gjort krav på, hvis du bruker en kravprosess, velger du de relevante radene, og deretter velger du en av følgende kommandoer i handlingsruten: (Du aktiverer kravprosesser på siden [**Rabattbehandlingsparametere**](rebate-management-parameters.md).)

        - **Angi som gjort krav på \> Alle** – Merk alle transaksjoner som gjort krav på.
        - **Angi som gjort krav på \> Valgt** – Merk de valgte transaksjonene som gjort krav på.
        - **Angi som ikke gjort krav på \> Alle** – Merk alle transaksjoner som ikke gjort krav på.
        - **Angi som ikke gjort krav på \> Valgt** – Merk de valgte transaksjonene som ikke gjort krav på.

    - Velg **Poster** i handlingsruten for å postere kravet for alle de relevante linjene. Hvis du bruker en kravprosess (når alternativet **Bruk kravprosess** er aktivert på siden **Parametere for rabattstyring**), posteres bare linjene som er merket som **Gjort krav på**. Ellers posteres alle kildetransaksjonene for den valgte rabattransaksjonen. **Poster**-knappen er bare tilgjengelig for rabattransaksjoner. Den er ikke tilgjengelig for avsetnings- og avskrivingstransaksjoner. I dialogboksen **Poster** angis **Fra dato**- og **Til dato**-feltene automatisk. Velg **Posteringsdato**-feltet, og velg deretter **OK**.
    - Hvis du vil justere beløpet som vises for en åpen eller upostert transaksjon, velger du transaksjonen, og deretter følger du ett av disse trinnene:

        - Rediger verdien i feltet **Korrigert beløp**.
        - I handlingsruten velger du **Angi korreksjon**. Deretter angir du en verdi i feltet **Korrigert beløp** i rullegardinlisten som vises.

> [!NOTE]
> Hvis du bruker en kravprosess når du behandler den neste perioden, vil transaksjonslisten inneholde alle transaksjoner det ikke er gjort krav på, fra den forrige posteringen, i tillegg til eventuelle nye transaksjoner for den valgte perioden.

## <a name="post-rebates-transactions"></a>Poster rabattransaksjoner

Hvis du vil postere verdien av en behandlet avsetning, et rabattbehandlingsbeløp og en avskriving, må du kjøre posteringsprosessen. Posteringsprosessen merker avsetnings-, rabattbehandlings- eller avskrivingstransaksjonene som postert, og oppretter måltransaksjonen. Hvis du ikke trenger å gå gjennom måltransaksjonen, kan disse transaksjonene defineres slik at de posteres automatisk.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Konfigurer systemet til å postere alle måltransaksjoner automatisk

Hvis du vil konfigurere systemet til å postere alle måltransaksjoner så snart de er generert av en posteringsavsetning, rabattbehandlingbeløp og avskrivning, aktiverer du alternativet **Poster journaler automatisk** og/eller **Poster fritekstfakturaer automatisk** på siden **Rabattbehandlingsparametere**. Hvis du vil ha mer informasjon, kan du se [Rabattbehandlingsparametere](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Poster transaksjoner for alle linjer for én eller flere avtaler

Etter at du har behandlet de relevante avtalene, følger du disse trinnene for å gå gjennom og postere de genererte transaksjonene for alle linjene for én eller flere avtaler.

1. Åpne den aktuelle [rabattavtalelistesiden](rebate-management-deals.md) for avtaletypen du vil arbeide med.
1. Velg raden for hver avtale du vil postere (eller åpne avtalen du vil postere).
1. I handlingsruten, på fanen **Rabattbehandlingsavtaler**, i **Generer**-gruppen, velger du én av følgende kommander:

    - **Poster \> Klargjør** – Poster tilgjengelige avsetningstransaksjoner som du har opprettet.
    - **Poster \> Rabattbehandling** – Poster tilgjengelige rabattransaksjoner som du har opprettet.
    - **Poster \> Avskrivning** – Poster tilgjengelige avskrivningstransaksjoner som du har opprettet.

1. I dialogboksen som vises, angir du **Posteringsdato**-feltet. Deretter angir du feltene **Fra dato** og **Til dato** for å definere datoområdet for transaksjonene som må posteres.
1. Velg **OK** for å postere transaksjonene.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Poster transaksjoner for én eller flere bestemte avtalelinjer for en valgt avtale

Etter at du har behandlet de relevante avtalene, følger du disse trinnene for å gå gjennom og postere de genererte transaksjonene for alle linjene for én eller flere spesifikke avtalelinjer for en valgt avtale. Denne prosedyrer gjelder bare for avtaler der **Avstem etter**-feltet er satt til *Linje*.

1. Åpne den aktuelle [rabattavtalelistesiden](rebate-management-deals.md) for avtaletypen du vil arbeide med.
1. Åpne avtalen som har en linje du vil postere transaksjoner for.
1. Velg **Linjer**-fanen i øvre høyre hjørne.
1. På **Rabattbehandling**-hurtigfanen velger du raden for hver avtalelinje du vil postere.
1. På verktøylinjen på **Rabattbehandling**-hurtigfanen velger du en av følgende kommandoer. (Disse kommandoene er bare tilgjengelige for avtaler der **Avstem etter** er satt til *Linje*.)

    - **Poster \> Klargjør** – Poster tilgjengelige avsetningstransaksjoner som du har opprettet.
    - **Poster \> Rabattbehandling** – Poster tilgjengelige rabattransaksjoner som du har opprettet.
    - **Poster \> Avskrivning** – Poster tilgjengelige avskrivningstransaksjoner som du har opprettet.

1. I dialogboksen som vises, angir du **Posteringsdato**-feltet. Deretter angir du feltene **Fra dato** og **Til dato** for å definere datoområdet for transaksjonene som må posteres.
1. Velg **OK** for å postere transaksjonene.

### <a name="post-transactions-using-a-batch-job"></a>Poster transaksjoner ved hjelp av en satsvis jobb

I stedet for å postere transaksjoner for bestemte avtaler eller avtalelinjer kan du kjøre en satsvis jobb for å postere transaksjoner for flere avtaler samtidig. Du kan eventuelt bruke postfiltre og/eller definere en gjentakende plan. Følg denne fremgangsmåten for å postere transaksjoner ved hjelp av en satsvis jobb.

1. Følg ett av disse trinnene:

    - Gå til **Rabattbehandling \> Periodiske oppgaver \> Poster \> Klargjør** for å postere tilgjengelige avsetningstransaksjoner som du har opprettet.
    - Gå til **Rabattbehandling \> Periodiske oppgaver \> Poster \> Rabattbehandling** for å postere tilgjengelige rabattransaksjoner som du har opprettet.
    - Gå til **Rabattbehandling \> Periodiske oppgaver \> Poster \> Avskrivning** for å postere tilgjengelige avskrivningstransaksjoner som du har opprettet.

1. I dialogboksen som vises, på **Parametere**-hurtigfanen, i **Periode**-delen, angir du **Posteringsdato**-feltet. Deretter angir du feltene **Fra dato** og **Til dato** for å definere datoområdet for transaksjonene som må posteres.
1. I delen **Garantiperiode** setter du feltene **Fra dato** og **Til dato** for å definere datoområdet for garantiene som må posteres.
1. På hurtigfanen **Poster som skal inkluderes**, kan du definere filtre for å begrense settet med avtaler som den satsvise jobben skal behandle. Disse innstillingene fungerer på samme måte som de arbeider for andre typer satsvise jobber.
1. På hurtigfanen **Kjør i bakgrunnen** kan du konfigurere alternativer for satsvis behandling og planlegging etter behov. Disse innstillingene fungerer på samme måte som de arbeider for andre typer satsvise jobber.
1. Velg **OK** for å kjøre og/eller planlegge beregningen.

## <a name="review-rebate-management-journals"></a>Gå gjennom rabattbehandlingsjournaler

Når transaksjonene er postert, kan du se gjennom de resulterende journalene, dokumentene eller varene. Måltransaksjoner for rabatter og royalty baseres på betalingstypen som er definert i posteringsprofilen og rabattens utleveringstype. Hvis for eksempel rabattutdataene er satt til *Vare*, opprettes det en salgsordre for en kunderabatt, og det opprettes en bestilling for en leverandørrabatt. Disse ordrene kan vises via måltransaksjonene. Hvis betalingen er definert til å bruke Leverandør, kan det imidlertid opprettes en leverandørfaktura for leverandøren som er definert for kunden, for kunderabatter.

Følg denne fremgangsmåten for å gå gjennom journaloppføringene som er knyttet til en avtale for rabattstyring.

1. Åpne den aktuelle [rabattavtalelistesiden](rebate-management-deals.md) for avtaletypen du vil arbeide med.
1. Velg avtalen du vil kontrollere journaloppføringer for.
1. I handlingsruten, på fanen **Rabattbehandlingsavtaler**, i **Transaksjoner**-gruppen, velger du **Transaksjoner** eller **Garantitransaksjoner**, alt etter typen transaksjoner du ønsker å se på.
1. Kontroller at **Vis**-feltet er satt til *Alle* eller *Postert*.
1. Finn og velg transaksjonssamlingen du vil undersøke, og velg deretter en av knappene nedenfor i handlingsruten. (Disse knappene er bare tilgjengelige når det finnes relevante posteringer for den valgte transaksjonssamlingen.)

    - **Måltransaksjoner** – Gå gjennom relevante journaler og andre typer dokumenter som ble generert av den valgte avtalen.
    - **Varer** – Gå gjennom relevante salgsordrer eller bestillinger som ble generert av den valgte avtalen.

1. En liste over relevante journaler, dokumenter eller varer vises. Hvis du vil vise mer informasjon om en journal, et dokument eller et element, merker du den aktuelle raden og velger deretter **Vis detaljer** i handlingsruten.
