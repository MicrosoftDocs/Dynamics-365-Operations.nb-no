---
title: Årsavslutning
description: Denne artikkelen beskriver den nødvendige konfigurasjonen og fremgangsmåten for å kjøre årsavslutningsprosessen i økonomimodulen.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032c572ec7b29bb6b2823ddde0c4fa76e5f8fcf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883220"
---
# <a name="year-end-close"></a>Årsavslutning

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver den nødvendige konfigurasjonen og fremgangsmåten for å kjøre årsavslutningsprosessen i økonomimodulen.

På slutten av et regnskapsår må du kjøre årsavslutningsprosessen for å overføre åpningssaldoer til det nye året. De fleste organisasjoner vil kjøre årsavslutningsprosessen flere ganger. Den første kjøringen flytter saldoene inn i det nye regnskapsåret. Prosessen kan deretter kjøres på nytt så mange ganger som nødvendig, for å flytte saldoene fra justeringsposter i det nye regnskapsåret.

Under årsavslutningsprosessen blir det opprettet to typer mulige transaksjoner. En åpningstransaksjon genereres alltid og brukes til å opprette åpningssaldoene i det nye regnskapsåret. Åpningstransaksjonen viser finanskontosaldoer for balanseregnskapet i det nye regnskapsåret, og saldoer fra finanskontosaldoer for resultat for opptjent egenkapital i det nye regnskapsåret. Avslutningstransaksjonen kan opprettes for å bringe saldoene for resultatkontoer ned til i regnskapsåret som avsluttes.

## <a name="prepare-to-run-the-year-end-close"></a>Klargjøre kjøring av årsavslutning

Før du kjører årsavslutningsprosessen, må du kontrollere innstillingene for følgende:

På **Hovedkonto**-siden:

- Kontroller at feltet **Hovedkontotype** er riktig angitt for hver hovedkonto. Hovedkontotypen brukes til å avgjøre om saldoen for hovedkontoen skal overføres som en startsaldo eller lukkes til opptjent egenkapital i åpningstransaksjonen.
- Saldoen for hovedkontoen kan overføres til en ny hovedkonto under årsavslutningen. Angi den nye hovedkontoen i feltet **Åpningskonto**. Vanligvis brukes dette feltet til hovedkontoer for balanseregnskap når hovedkontoen deaktiveres og en ny hovedkonto brukes for det nye regnskapsåret.

På siden **Parametere for økonomimodul** under **Årsavslutning**:

- Alternativet **Slett eksisterende årsavslutningsoppføringer når du avslutter året på nytt** brukes til å angi om den systemgenererte åpningstransaksjonen fra en tidligere årsavslutning skal slettes når årsavslutningen kjøres på nytt. Hvis dette alternativet er satt til **Ja**, slettes den forrige åpningstransaksjonen og den valgfrie avslutningstransaksjonen, og en ny åpnings- og avslutningstransaksjon opprettes basert på gjeldende saldoer. Hvis dette alternativet er satt til **Nei**, beholdes den forrige åpningstransaksjonen og en valgfri åpningstransaksjon, og en ekstra åpnings- eller avslutningstransaksjon opprettes for å flytte saldoene fremover fra justeringstransaksjoner som er postert etter den forrige årsavslutningen.
- Alternativet **Opprett avslutningstransaksjoner under overføring** brukes til å opprette avslutningstransaksjoner i regnskapsåret som lukkes, for å bringe saldoene i alle hovedkontoer til 0 (null). Hvis dette alternativet er satt til **Ja**, opprettes både åpningstransaksjonen og avslutningstransaksjonen. Hvis dette alternativet er satt til **Nei**, opprettes bare åpningstransaksjonen i det neste regnskapsåret for å overføre saldoene. Saldoene for hovedkontoen beholdes på slutten av regnskapsåret.
- Alternativet **Sett regnskapsårsstatusen til permanent lukket** brukes til å angi en permanent lukketstatus for regnskapsåret. Bruk dette alternativet nøye, fordi perioder med status permanent lukket, ikke kan åpnes på nytt. Justeringer kan derfor ikke posteres til regnskapsåret. Anbefalt fremgangsmåte er å sette alternativet til **Nei**.
- Alternativet **Bilagsnummeret må fylles ut** er fjernet. Et bilag er nå nødvendig når årsavslutningsprosessen kjøres. Da angis bilagsnummeret manuelt.

På siden **Regnskapskalender**:

- Det neste regnskapsåret må finnes før du kjører årsavslutningen. Ellers kan ikke åpningssaldoene opprettes i åpningsperioden.

På siden **Finanskalender**:

- Valgfritt: Hver regnskapsperiode for regnskapsåret som lukkes, kan settes til **På vent** for å hindre at nye transaksjoner registreres. Når justeringsposter er identifisert, kan På vent-periodene åpnes på nytt for å postere justeringsposter, selv om årsavslutningsprosessen allerede er kjørt.

På siden **Konfigurasjon av årsavslutningsmal**:

- Når funksjonen **Årsavslutningsforbedringer for finans** er aktivert, skilles prosessen med konfigurasjon av årsavsluttingsmalen fra prosessen med å kjøre årsavslutningen. Malen kan defineres på siden **Konfigurasjon av årsavslutningsmal** (**Økonomimodul \> Finansoppsett \> Konfigurasjon av årsavslutningsmal**), eller den kan åpnes fra årsavslutningsprosessen.

## <a name="define-year-end-close-templates"></a>Definere maler for årsavslutning

Når systemet er konfigurert, kan du kjøre årsavslutningsprosessen. På siden **Konfigurasjon av årsavslutningsmal** kan en mal defineres for gruppen med juridiske enheter som årsavslutningsprosessen skal kjøres for. Malen brukes på nytt ved hver årsavslutning, men kan endres hvis organisasjonen endres.

Definer først **Gruppenavn**-feltet for malen, og velg regnskapskalenderen. Gruppenavnet må identifisere gruppen med juridiske enheter som er inkludert. Når du bestemmer gruppene med juridiske enheter, må du huske på at juridiske enheter bare kan inkluderes i samme gruppe hvis den samme regnskapskalenderen er valgt for dem. Malene kan for eksempel være definert basert på geografi, med separate grupper opprettet for juridiske enheter for Nord-Amerika, Europa, Midtøsten og Afrika (EMEA), og juridiske enheter i Asia/Stillehavskysten (APAC).

Deretter kan juridiske enheter legges til i malen. Juridiske enheter kan legges ved å velge et organisasjonshierarki eller ved å velge de juridiske enhetene. Hvis det velges et organisasjonshierarki, vil bare juridiske enheter i hierarkiet som bruker den valgte regnskapskalenderen legges til i malen. Hvis du bruker juridiske enheter for å legge til i malen, kan bare juridiske enheter med samme regnskapskalender legges til i malen. Den samme regnskapskalenderen er nødvendig fordi årsavslutningen kjøres ved å velge et regnskapsår, noe som kan variere fra kalender til kalender.

Når de juridiske enhetene er lagt til, kan du definere hovedkontoer for opptjent egenkapital for hver juridiske enhet.

Kategorien **Finansdimensjon** brukes til å definere hvilke finansdimensjoner som skal brukes på åpningstransaksjonen. Legg merke til at innstillingene du definerer i denne kategorien, bare gjelder for den juridiske enheten som er valgt i rutenettet **Juridiske enheter**. Du må gjenta oppsettet for hver juridiske enhet i rutenettet.

Alternativet **Overfør balansedimensjoner** brukes til å angi om finansdimensjoner på transaksjoner som er postert til balansekonti, skal beholdes på åpningstransaksjonen. Anbefalt fremgangsmåte er å sette alternativet til **Ja**. Innstillingen for balansedimensjonene påvirker ikke eksisterende saldoer i finanskontoene for opptjente inntekter. Disse saldoene bestemmes av resultatdimensjonene som er definert i neste del. Regnskapsåret 2019 var for eksempel det første året som ble avsluttet, og alternativet **Lukk alle** ble brukt til å velge **Avdeling**- og **Kostsenter**-dimensjonene for avslutning. I dette tilfellet ble det opprettet en egen konto for opptjente inntekter for hver kombinasjon av en avdeling og et kostsenter. Når årsavslutningen kjøres for regnskapsåret 2020, beholdes inntektene fra forrige år akkurat slik de ble postert, selv om **Overfør balansedimensjoner** er satt til **Nei**. Saldoer som posteres til opptjente inntekter fra forrige års avslutning, blir aldri endret.

Delen **Overfør resultatdimensjoner** brukes til å definere hvilke finansdimensjoner på transaksjoner som er postert til resultatkonti, som skal overføres til hovedkontoen for opptjent egenkapital. Først må du angi finansdimensjonene som er relevante for den valgte juridiske enheten. Dette omfatter alle finansdimensjoner det er postert mot i løpet av året, selv om finansdimensjonen ikke er en del av en aktiv kontostruktur. Deretter definerer du hver dimensjon som **Lukk én** eller **Lukk alle**. Standardvalget er **Lukk alle**. Dette alternativet beholder de opprinnelige finansdimensjonsverdiene fra posterte transaksjoner, og bruker dem til å lage åpningssaldoer for kontoen for opptjent egenkapital. Separate startsaldoer for opptjent egenkapital opprettes for hver unike kombinasjon av finansdimensjonsverdier. Hvis **Lukk én** er valgt, vil alle transaksjoner som er postert med denne finansdimensjonen, blir summert i en startsaldo for opptjent egenkapital for dimensjonsverdien som er angitt i feltet som vises etter **Lukk én**. Alle transaksjonene for regnskapsåret ble f.eks. postert med kontostrukturen **Hovedkonto – Avdeling**. For **Avdeling**-finansdimensjonen i malen er **Lukk én** valgt, og **100** angis som dimensjonsverdien. Hvis totalinntekt for alle transaksjoner som er postert til avdeling 200, 300 og 400 er USD 100 000, opprettes det én startsaldo for **Tilbakeholdt overskudd – 100**. Hvis du velger **Lukk én**, men lar finansdimensjonsverdien være tom, vil alle transaksjoner posteres til tilbakeholds overskudd med denne dimensjonsverdien tom.

## <a name="run-the-year-end-close-process"></a>Kjøre årsavslutningsprosessen

Når du har opprettet malene for årsavslutning, kan du starte årsavslutningsprosessen på siden **Årsavslutning** (**Økonomimodul \> Periodeavslutning \> Årsavslutning**). Før du kjører årsavslutningen, kan du legge til nye årsavslutningsmaler eller endre eksisterende maler ved å velge oppsettet **Konfigurasjon av årsavslutningsmal** for å åpne oppsettsiden for malene.

Velg årsavslutningsmalen, og velg deretter **Kjør årsavslutning** i handlingsruten. Velg enten alle juridiske enheter eller et delsett med juridiske enheter fra malen som årsavslutningen kjøres for. Hvis du kjører i årsavslutningen for første gang i et regnskapsår, velger du sannsynligvis alle juridiske enheter, slik at du oppretter startsaldoer for dem alle. Hvis du tidligere har kjørt årsavslutningen, kan du velge å kjøre den på nytt for bare juridiske enheter som det ble postert justeringsposter for.

Deretter velger du regnskapsåret som du vil kjøre årsavslutningen mot. Hvis det finnes mer enn én avslutningsperiode for den siste perioden i regnskapsåret, blir feltet **Periodenavn** tilgjengelig. Du kan deretter velge avslutningsperioden som skal brukes til å postere avslutningstransaksjonen, hvis oppsettet er definert til å opprette avslutningstransaksjonen.

Deretter angir du et bilagsnummer. Det samme bilagsnummeret brukes for alle juridiske enheter som er valgt for årsavslutningsprosessen. Bilagsnummeret genereres ikke med en nummerserie.

Standardinnstillingen for årsavslutningsprosessen er å kjøre i satsvis modus. Du kan derfor gå tilbake til andre aktiviteter etter at du har startet det.

Fordi kontostrukturer kan endres gjennom et regnskapsår, kan ikke den relevante kontostrukturen alltid identifiseres. Årsavslutningsprosessen overholder derfor ikke kontostrukturer. Når åpningstransaksjoner opprettes, vil saldoene overføres fremover med finansdimensjoner som er definert i årsavslutningsmalen. Startsaldopostene kan inneholde finansdimensjoner som ikke lenger er i gjeldende kontostruktur og segmentkombinasjoner som er ikke lenger er gyldig i gjeldende kontostruktur. Hvis organisasjonen vil utelate en finansdimensjon for startsaldoen for tilbakeholdt overskudd, må finansdimensjonen settes til **Lukk én**, og dimensjonsverdien må være tom.

Når prosessen er fullført, opprettes det en post for hver kombinasjon av en juridisk enhet og et regnskapsår. Du vil bare se poster for juridiske enheter du har tilgang til. Hver post inneholder systemdatoen og -klokkeslettet da prosessen ble kjørt, og en direkte kobling til bilagene som ble opprettet for årsavslutningen.

[![Poster opprettet i hurtigfanen Årsavslutning på siden for årsavslutning](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Hvis du kjører årsavslutningen på nytt, vil du se én eller flere poster for hver kombinasjon av en juridisk enhet og et regnskapsår, avhengig av innstillingen for alternativet **Slett eksisterende årsavslutningsoppføringer når du avslutter året på nytt** på siden **Parametere for økonomimodul**:

- Hvis alternativet settes til **Ja**, slettes bilaget for forrige årsavslutning. Posten merkes som **Tilbakeført** og stemples med datoen og klokkeslettet da tilbakeføringen ble utført. I tillegg fjernes koblingen til bilagsnummeret. Når årsavslutningen er fullført, opprettes det en ny post for det nye bilaget som opprettes.
- Hvis alternativet er satt til **Nei**, blir posten for forrige årsavslutning stående, sammen med koblingen til bilaget. Hver gang denne årsavslutningen kjøres på nytt, opprettes det en ny post sammen med en kobling til de nye bilagene.

## <a name="reverse-the-year-end-close-process"></a>Tilbakefør årsavslutningsprosessen

På siden **Årsavslutning** kan du tilbakeføre en årsavslutning. Velg posten for kombinasjonen av en juridisk enhet og et regnskapsår som må tilbakeføres, og velg deretter **Tilbakefør årsavslutning**. Tilbakeføringsprosessen sletter alle åpnings- og avslutningsbilagene som ble opprettet for regnskapsåret. Posten merkes som **Tilbakeført** og stemples med datoen og klokkeslettet da tilbakeføringen ble utført. I tillegg fjernes koblingen til bilagsnummeret. På samme måte som årsavslutningsprosessen kjøres tilbakeføringen i satsvis modus.

Hvis du merker av for **Vis tilbakeførte** som er tilgjengelig over rutenettet, kan du skjule eller vise poster for tilbakeførte årsavslutningsprosesser. Når du har kjørt prosessen **Tilbakefør årsavslutning**, må du kanskje merke av for **Vis tilbakeførte** for å se posten. Du kan definere flere filtre for å vise annen informasjon.

[![Bruke avmerkingsboksen Vis tilbakeførte for å se poster for tilbakeførte årsavslutningsprosesser på siden for årsavslutning](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Hvis du vil ha mer informasjon, kan du se [Lukke økonomimodulen ved periodeslutt](close-general-ledger-at-period-end.md) og [Avslutte regnskapsåret](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
