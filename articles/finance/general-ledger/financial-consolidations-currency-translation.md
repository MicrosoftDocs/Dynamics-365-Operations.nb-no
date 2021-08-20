---
title: Oversikt over finanskonsolideringer og valutaomveksling
description: Dette emnet beskriver finanskonsolideringer og valutaomveksling i Økonomimodul.
author: aprilolson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0df16db842c159b4db469139a0b5463a82e3fe07b4e23f8f7cf0272caaf23602
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748986"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Oversikt over finanskonsolideringer og valutaomveksling

[!include [banner](../includes/banner.md)]

Dette emnet leder deg gjennom fremgangsmåten som både Microsoft Dynamics 365 Finance og Finansrapportering bruker for konsolideringer. Det beskriver scenarioer som involverer flerfirmarapportering, aggregering, eliminering og minoritetsrente. Det forklarer også hvordan du skal behandle spesielle situasjoner, for eksempel scenarier der juridiske enheter har forskjellige regnskapsperioder eller ulike kontoplaner.

Dette emnet er laget for brukere og funksjonelle konsulenter, og det antas at leserne har en grunnleggende forståelse av Finance og Finansrapportering. Grunnleggende oppsett er ikke dekket.

> [!NOTE]
> Begrepet *juridisk enhet* brukes i Finance, og begrepet *firma* brukes i Finansrapportering. Begge disse begrepene brukes i dette emnet. I henhold til formålene for dette emnet betyr de imidlertid det samme.

## <a name="audience"></a>Målgruppe
Dette emnet er ment for økonomi- og regnskapsbrukere og programkonsulenter som ønsker å bruke Finance and Reporting og Finansrapportering til å konsolidere data fra flere firmaer og flere valutaer.

## <a name="approach"></a>Metode
Finance bruker en separat juridisk enhet til å behandle en konsolidering. Dette gjør det mulig å konsolidere én enkelt forekomst, men gir et alternativ for å hente data fra andre kilder. Konsolideringsprosessen må kjøres hver gang det gjøres endringer i de juridiske enhetene for kilden.

Finansrapportering kan konsolidere flere firmaer under rapportgenerering. Selv om dataene er lagret i en oppstillingsdatabase, er versjonsdefinert og kan eksporteres, er hvert kildefirma eier og beholder for dataene. Rapporten kan kjøres når som helst, til og med hvert minutt (for eksempel). Den gir mange andre fordeler, for eksempel muligheten til å drille ned til alle firmaer og dimensjoner.

Brukere kan bruke Konsolider på nettet, Finansrapportering eller en kombinasjon. Valget avhenger av behovene til firmaet og hva deres revisorer foretrekker.

## <a name="consolidations"></a>Konsolideringer
**Konsolideringer**-modulen inneholder alternativer for å konsolidere flere juridiske enheter i løpet av konsolideringsprosessen, og for å importere eller eksportere saldoen til et firma. Du kan også definere elimineringer og postere elimineringsjournaler.

## <a name="benefits-of-using-consolidate-online"></a>Fordelene ved å bruke Konsolider på nettet
Kunder som bruker **Konsolideringer**-modulen, vil få diverse fordeler:

- **Datadybde** – du kan opprette konsoliderte rapporter som fører sammen faktiske data og budsjettdata både på kontonivå og dimensjonsnivå.
- **Dynamiske konsolideringer** – konsolideringer kan behandles flere ganger.
- **Overvåkningsfunksjoner** – dimensjoner og kontoer opprettholdes for analyse og rapportering, og saldoer opprettes etter dato.
- **Omregning av valuta** – du kan angi kontoområder og satser for å regne om fra regnskapsvalutaen for kildefirmaet til regnskapsvalutaen for konsolideringsfirmaet.
- **Behandle elimineringer i et konsolidert firma eller elimineringsfirma** – du kan behandle og postere elimineringer som én enkelt prosess i løpet av konsolideringen. Du kan eventuelt kjøre et forslag separat.

## <a name="supported-consolidation-scenarios"></a>Støttede konsolideringsscenarier
Her er noen av konsolideringsscenariene som Konsolider på nettet støtter:

- Enkeltnivåkonsolideringer på tvers av juridiske enheter
- Konsolideringer som involverer elimineringer
- Minoritetsrente (I dette scenariet må manuell beregning og oppføring i firmaet brukes.)
- Flere kontoplaner på tvers av juridiske enheter
- Ulike regnskapskalendere på tvers av flere juridiske enheter
- Konsolideringer som omfatter flere rapporteringsvalutaer

## <a name="legal-entity-setup"></a>Oppsett av juridisk enhet
Før du utfører en konsolidering, må du definere den juridiske enheten. Du kan kjøre konsolideringen så mange ganger du trenger, og alle data vil bli oversatt fra kildefirmaets regnskapsvaluta til valutaen som er definert for det konsoliderte selskapet. For følgende organisasjonsstruktur, hvis du må regne om alle firmaer i Nord-Amerika først til amerikanske dollar (USD) og deretter til euro (EUR), valutaen for moderselskapet, må du derfor ha minst to konsolideringsfirmaer.

![Organisasjonsstruktur.](./media/organizational-structure.png "Organisasjonsstruktur")

I den foregående organisasjonsstrukturen må du ha en juridisk enhet for Nord-Amerika-konsolideringen fordi konsolideringer alltid konsolideres fra regnskapsvalutaen for kildefirmaet til valutaen for det konsoliderte selskapet. I eksemplet, hvis alle firmaer er inkludert i en enkelt konsolidering, blir det meksikanske datterselskapet regnet om fra meksikanske pesos (MXN) til EUR, ikke fra MXN til USD til EUR.

Når du oppretter den juridiske enheten, kan du angi om firmaet skal brukes for både konsolideringsprosessen og elimineringsprosessen, eller bare én av disse prosessene. I illustrasjonen nedenfor brukes firmaet for begge prosessene. Vær oppmerksom på at du ikke kan postere daglige journaler i et konsolidert selskap, men du kan postere dem i et elimineringsfirma. Derfor kan det hende at du vil ha et eget elimineringsfirma.

![Juridisk enhet som brukes til både konsolidering og eliminering.](./media/sep-elimination-company.png "Juridisk enhet som brukes til både konsolidering og eliminering")

## <a name="main-accounts-and-consolidation-account-groups"></a>Hovedkontoer og konsolideringskontogrupper
Ett valg som du må ta, er hvordan du vil konsolidere fra kontoplanen. I konsolideringsprosessen har du tre alternativer for konsolidering av hovedkontoer.

Det første alternativet er å bruke hovedkontoene fra kildefirmaene. I så fall blir hver konto fra alle firmaer konsolidert. Hvis for eksempel Kontanter er konto 100000 i USMF-firmaet og konto 1100 i DEMF-firmaet, inkluderer konsolideringsfirmaet begge kontoene. Hver konto har sin respektive saldo.

Det andre alternativet er å angi en standard konsolideringskonto på siden **Hovedkontoer**. Kontoen tilordnes deretter til konsolideringskontoen. Dette alternativet kan være nyttig når du har ulike kontoplaner eller må tilordne til et diagram som er definert av hovedkontoret.

![Standard konsolideringskonto som er angitt på siden Hovedkontoer.](./media/main-accounts.png "Standard konsolideringskonto som er angitt på siden Hovedkontoer")

Det tredje alternativet er å bruke konsolideringskontogrupper. Du kan definere så mange konsolideringskontogrupper som du trenger. Deretter, på siden **Flere konsolideringskontoer** bare tilordner du hovedkontoen fra kontoplanen til kontoen som du trenger for denne gruppen.

![Tilordne på siden Flere konsolideringskontoer.](./media/additional-consolidation-accounts.png "Tilordne på siden Flere konsolideringskontoer")

## <a name="consolidating-online"></a>Konsolidere på nettet
Hvis du vil vite hvordan du registrerer detaljer om konsolideringer på nettet, kan du se [Konsolideringer på nettet](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Administrere konsolideringstransaksjoner
Hvis du vil vise resultatene av konsolideringen, har du flere alternativer:

- Generer en finansrapport mot det konsoliderte selskapet.
- Se gjennom **Råbalanse**-listesiden i det konsoliderte selskapet.
- I listen over konsolideringstransaksjoner på siden **Konsolideringer**, se på saldoene som er opprettet etter dato for hvert kildefirma for hver periode.

    ![Konsolideringstransaksjoner på siden Konsolideringer.](./media/managing-consolidation-transactions.png "Konsolideringstransaksjoner på siden Konsolideringer")

Hvis du vil kjøre konsolideringen på nytt, kan du bare behandle konsolideringen. Alternativt kan du først velge **Fjern transaksjoner** på siden **Konsolideringer**.
I tilfelle saldoene i den konsoliderte kontoen ikke er riktige, kan disse saldoene korrigeres ved hjelp av siden **Justeringer for avslutningsperiode**.

## <a name="consolidate-with-import"></a>Konsolider med import
Konsolider med import-funksjonen fungerer som Konsolider på nettet-funksjonen. Når du velger de juridiske enhetene, går du ut til kildefilen som inneholder dataene.

## <a name="export-company-balances"></a>Eksport av firmasaldoer
Eksport av firmasaldoer-funksjonen fungerer også som Konsolider på nettet-funksjonen. Når du velger de juridiske enhetene, angir du en filbane for utdataene.

## <a name="elimination-rules"></a>Elimineringsregler
Hvis du vil eliminere konserninterne transaksjoner, kan du opprette en elimineringsregel. Du kan også gjøre en manuell elimineringsoppføring i et firma som er tilordnet et elimineringsfirma. Hvis du oppretter en elimineringsregel, har du to alternativer for elimineringsmetoden: **Netto endring** og **Fast**.

### <a name="set-up-elimination-rules"></a>Definere elimineringsregler
Når du definerer elimineringsregler i Finance, kan du opprette en finansdimensjon som brukes spesielt for eliminering. De fleste kunder gir denne finansdimensjonen navnet **Handelspartner** eller noe lignende. Hvis du bestemmer deg for ikke å bruke en finansdimensjon, må du sørge for å ha hovedkontoer som bare brukes for konserninterne transaksjoner.

Du kan finne oppsettet for elimineringer i **Oppsett**-området i modulen **Konsolideringer**. Når du har skrevet inn en beskrivelse av regelen, må du velge firmaet som elimineringsjournalen skal posteres til. Firmaet du velger, bør ha valgt **Brukes til finanseliminering** under oppsettet av den juridiske enheten.

Du kan angi datoen når elimineringsregelen trer i kraft, og datoen når den utløper, etter behov. Du må angi **Aktiv** til **Ja** hvis du vil at elimineringsregelen skal være tilgjengelig i elimineringsforslagsprosessen. Velg et journalnavn av typen **Eliminering**.

![Grunnleggende egenskaper for en elimineringsregel.](./media/ledger-elimination-rule-journal.png "Grunnleggende egenskaper for en elimineringsregel")

Når du har definert de grunnleggende egenskapene, kan du velg **Linjer** for å definere de faktiske behandlingsreglene. Det finnes to alternativer for elimineringer: eliminere netto endringsbeløp eller definere et fast beløp.

Velg kildekontoene. Du kan bruke stjerne (\*) som et jokertegn.  **1\**velger for eksempel alle kontoer som starter med* 1**, som en kilde for datatildelingen.

Når du har valgt kildekontoene, bruker du feltet **Kontospesifikasjon** til å angi kontoen som brukes fra målfirmaet. Velg **Kilde** hvis du vil bruke den samme hovedkontoen som er definert i kildekontoen. Hvis du velger **Brukerdefinert**, må du angi en målkonto.

![Siden Elimineringsregellinje, finans.](./media/ledger-elimination-rule-line.png "Siden Elimineringsregellinje, finans")

Feltet **Dimensjonsspesifikasjon** fungerer som feltet **Kontospesifikasjon**. Velg **Kilde** for å bruke de samme dimensjonene i målfirmaet og kildefirmaet. Hvis du velger **Brukerdefinert**, må du angi dimensjoner i målfirmaet ved å velge **Måldimensjoner**. Velg deretter kildedimensjoner og finansdimensjoner og verdiene som brukes som en kilde for eliminering.

### <a name="process-elimination-transactions"></a>Behandle elimineringstransaksjoner
Det finnes to måter å behandle elimineringstransaksjoner på. Transaksjonen kan behandles under den elektroniske konsolideringsprosessen, eller du kan opprette en elimineringsjournal og kjøre elimineringsforslagsprosessen. Denne delen fokuserer på det andre alternativet.

I et firma som er definert som et elimineringsfirma, velger du **Elimineringsjournal** i modulen **Konsolideringer**. Når du har valgt journalnavnet, velger du **Linjer**. Hvis du vil kjøre forslaget, velger du **Forslag** \> **Elimineringsforslag**.

Velg firmaet som er kilden til de konsoliderte dataene, og velg deretter regelen som skal behandles. Angi start- og sluttdatoene for å definere datointervallet som det skal søkes i, for elimineringsbeløp. Feltet **FIN-posteringsdato** spesifiserer datoen som brukes til å postere journalen til økonomimodulen. Når du har valgt **OK**, kan du se gjennom beløpene og postere journalen.

> [!NOTE]
> Elimineringsjournalen viser beløpene for kontoverdiene i valutaen til de opprinnelige transaksjonene, ikke i regnskapsvalutaen. Når du ser gjennom beløpene i elimineringsjournalen, kan det hende at dette er forvirrende.

Hvis du vil ha mer informasjon og flere eksempler, kan du se [Elimineringsregler](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Revaluering av valuta i et konsolideringsfirma
Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte. Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene som skal brukes for omveksling i løpet av konsolideringsprosessen. Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene. Urealisert fortjeneste og tap oppdateres deretter, basert på den nye valutakursen og datoen.

Du finner mer informasjon om revaluering av valuta i et konsolideringsfirma ved å se [Revaluering av valuta i et konsolideringsfirma](currency-revaluation-consolidation-company.md).

Hvis du vil ha mer informasjon om hvordan valutarevaluering fungerer i **Økonomimodule**, kan du se [Revaluering av utenlandsk valuta for økonomimodul](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Tilleggsinformasjon
- Alle posteringslag konsolideres når konsolideringen utføres.
- Elimineringsjournaler kan posteres bare for det gjeldende laget.
- Bare operative saldoer konsolideres. Derfor, for å se startsaldoer, må du fremdeles kjøre en årsavslutning i det konsoliderte selskapet.
- Du kan postere en daglig journal i et elimineringsfirma, men ikke i et konsolidert selskap.
- Justeringer av saldoer i et konsolideringsfirma kan bare gjøres ved hjelp av siden **Justeringer for avslutningsperiode**. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Fordelene ved å bruke Finansrapportering for økonomiske konsolideringer og omregning av valuta eller fylle ut Konsolider på nettet for konsolidert rapportering
Kunder som bruker Finansrapportering for økonomiske konsolideringer og omregning av valuta, eller som fyller ut Konsolider på nettet for konsolidert rapportering, oppnår forskjellige fordeler:

- **Datadybde** – du kan opprette konsoliderte rapporter som fører sammen faktiske data og budsjettdata både på kontonivå og dimensjonsnivå. For Finance inkluderer disse dataene data både fra budsjettkontroll og budsjettplanlegging.
- **Dynamiske konsolideringer** – konsolideringer kan gjøres når som helst og på alle nivåer i organisasjonshierarkiet.
- **Komplette overvåkingsfunksjonene** – alle dimensjoner, kontoer og transaksjonsdetaljer opprettholdes for analyse og gjennomgang. I tillegg gir Finansrapportering full drilling bakover til den opprinnelige transaksjonen i alle de juridiske enhetene som er konsolidert.
- **Strømlinjeformet omregning av valuta** – etter minimalt oppsett i Finance kan du regne om en hvilken som helst Finansrapportering-rapport til en hvilken som helst rapporteringsvaluta som er definert. I tillegg kan du definere et ubegrenset antall rapporteringsvalutaer.
- **Poster elimineringer ved kilden** – du kan opprette og skrive ut en elimineringsrapport for å verifisere elimineringstransaksjoner. Deretter kan du postere alle nye elimineringer som standard konserninterne transaksjoner. Du kan også bruke en juridisk elimineringsenhet for alle transaksjoner som du ikke vil ha i juridiske enheter.

## <a name="supported-consolidation-scenarios-for-financial-reporting"></a>Støttede konsolideringsscenarioer for Financial Reporting

Her er noen av konsolideringsscenariene som Finansrapportering støtter:

- Enkeltnivå- og flernivåkonsolideringer på tvers av juridiske enheter
- Konsolideringer som bruker organisasjonsstrukturer som opprettes fra juridiske enheter
- Konsolideringer som involverer elimineringer
- Minoritetsrente
- Flere kontoplaner på tvers av juridiske enheter
- Ulike regnskapskalendere på tvers av flere juridiske enheter
- Konsolideringer som omfatter flere rapporteringsvalutaer
- Forretningsenhetskonsolideringer

## <a name="generating-consolidated-financial-statements"></a>Generere konsoliderte regnskapsoppgjør
For informasjon om situasjoner der du kan generere konsoliderte regnskapsoppgjør, kan du se [Generere konsoliderte regnskapsoppgjør](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]