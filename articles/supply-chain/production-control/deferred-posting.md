---
title: Gjør ferdigvarer fysisk tilgjengelige før postering til journaler
description: Når en produsert vare rapporteres som ferdig, blir den registrert som tilgjengelig for videre fysisk behandling, og en eller flere journaler posteres. Denne artikkelen beskriver hvordan du utsetter journalposteringer ved å aktivere dem for behandling av en satsvis jobb i en meldingskø.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689347"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Gjør ferdigvarer fysisk tilgjengelige før postering til journaler

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Når en arbeider rapporterer en produsert vare som ferdig, registrerer systemet den som tilgjengelig for mer fysisk behandling (for eksempel forsendelse eller puten). I løpet av denne prosessen posteres også en eller flere journaler (for eksempel rapporten som ferdigjournalen, plukklistejournalen og rutekortjournalen). Hvis du vil gjøre varene fysisk tilgjengelige før alle posteringene er behandlet, kan du konfigurere systemet til å utsette journalposteringene. Utsatte posteringer behandles deretter av en satsvis jobb som behandler posteringene som systemressurser tillater.

Illustrasjonen nedenfor viser hvordan prosesser for postering av journaler startes både med og uten utsatt postering.

![Ferdigmeldingsprosessen med og uten utsatt journalpostering.](media/deferred-posting-flowchart.png "Ferdigmeldingsprosessen med og uten utsatt journalpostering")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Aktiver utsatt journalpostering for systemet

Før du kan bruke utsatt journalpostering må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Produksjonskontroll*
- **Funksjonsnavn:** *(Forhåndsversjon) Gjør ferdigvarer fysisk tilgjengelige før postering til journaler*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Definer alternativer for journalpostering for ferdigmelding

Arbeidere kan ferdigmelde varer ved å bruke en av følgende klienter:

- Webklient
- Mobilappen Warehouse Management
- Grensesnittet for produksjonsutførelse

Nettklienten bruker samme posteringsmetodekonfigurasjon som mobilappen Warehouse Management. Posteringsmetoden som grensesnittet for produksjonsutførelse bruker, må imidlertid konfigureres separat.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Angi journalposteringsalternativer for nettklienten og mobilappen Warehouse Management

I mobilappen rapporterer arbeidere varer som ferdige, ved å åpne et menyelement for mobilenhet der verdien **Arbeidsopprettingsprosess** er *Ferdigmeldt* eller *Ferdigmeldt og plassert*. I nettklienten rapporterer arbeidere varer som ferdigmeldt fra listesiden **Alle produksjonsordrer** eller siden **Produksjonsordre (detaljer)**. Du kan konfigurere en standardmetode for hele firmaet, og du kan også definere lagerspesifikke overstyringer etter behov.

Bruk fremgangsmåten nedenfor til å konfigurere standardposteringsmetoden for hele firmaet for ferdigmelding av varer fra nettklienten eller mobilappen Warehouse Management.

1. Gå til **Produksjonskontroll \> Oppsett \> Parametere for produksjonskontroll**.
1. I fanen **Journaler**, i delen **Ferdigmeldingsjournal**, setter du feltet **Posteringsmetoden** til en av følgende verdier:

    - *Umiddelbar* – Når en vare rapporteres som ferdig, behandler systemet alle relaterte journalposteringer fullt ut før den merker den ferdige varen som fysisk tilgjengelig.
    - *Utsatt* – Når en vare rapporteres som ferdig, merker systemet den ferdige varen som fysisk tilgjengelig og legger til journalposteringene til en meldingskø. Systemet venter ikke til posteringene er fullstendig behandlet før den merker den ferdige varen som fysisk tilgjengelig.

Bruk fremgangsmåten nedenfor til å konfigurere lagerspesifikke overstyringer for standard posteringsmetode som er konfigurert på siden **Produksjonskontrollparametere**.

1. Gå til **Lagerstyring \> Oppsett \> Lageroppdeling \> Lagre**.
1. Velg lageret du vil konfigurere.
1. I handlingsruten velger du **Rediger**.
1. I hurtigfanen **Lager**, i delen **Produksjonsordrer**, setter du feltet **Posteringsmetoden** til en av følgende verdier:

    - *Arv* – Det valgte lageret arver innstillingen fra siden **Produksjonskontrollparametere**.
    - *Umiddelbar* – Når en vare rapporteres som ferdig, behandler systemet alle relaterte journalposteringer fullt ut før den merker den ferdige varen som fysisk tilgjengelig.
    - *Utsatt* – Når en vare rapporteres som ferdig, merker systemet den ferdige varen som fysisk tilgjengelig og legger til journalposteringene til en meldingskø. Systemet venter ikke til posteringene er fullstendig behandlet før den merker den ferdige varen som fysisk tilgjengelig.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Angi journalposteringsalternativer for grensesnittet for produksjonsutførelse

Bruk fremgangsmåten nedenfor til å konfigurere posteringsmetoden som brukes når varer rapporteres som ferdigmeldt fra grensesnittet for produksjonsutførelse.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Standarder for produksjonsordre**.
1. I fanen **Ferdigmeldt**, i delen **Ferdigmeldingsjournal**, setter du feltet **Posteringsmetoden** til en av følgende verdier:

    - *Umiddelbar* – Når en vare rapporteres som ferdig, behandler systemet alle relaterte journalposteringer fullt ut før den merker den ferdige varen som fysisk tilgjengelig.
    - *Utsatt* – Når en vare rapporteres som ferdig, merker systemet den ferdige varen som fysisk tilgjengelig og legger til journalposteringene til en meldingskø. Systemet venter ikke til posteringene er fullstendig behandlet før den merker den ferdige varen som fysisk tilgjengelig.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Planlegg den satsvise jobben for meldingsbehandler for å behandle utsatte posteringer

Den satsvise jobben for meldingsbehandleren er ansvarlig for å behandle journalposteringene etter at de har blitt satt i kø. Hvis du vil være sikker på at journalposteringene blir behandlet, må du konfigurere denne jobben til å kjøre med et vanlig intervall. Bruk fremgangsmåten nedenfor til å konfigurere den nødvendige satsvise jobben.

1. Gå til **Systemadministrasjon \> Meldingsbehandler \> Meldingsbehandler**.
1. I hurtigfanen **Parametere** setter du feltet **Meldingskø** til *Produksjon*.
1. På hurtigfanen **Kjør i bakgrunnen** setter du **Satsvis behandling** til *Ja*. Deretter konfigurerer du en gjentakende plan, og konfigurerer andre innstillinger etter behov. Innstillingene fungerer på samme måte som for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Spor fremdriften for utsatte posteringer

Utsatte journalposteringer er satt i kø som *meldingsbehandlermeldinger* som venter til de behandles av *meldingsbehandleren*. Meldingsbehandleren må være definert til å kjøre som en planlagt satsvis jobb. Hvis du vil vise utsatte posteringsmeldinger som er eller skal behandles av meldingsbehandleren, kan du gå til **Produksjonskontroll \> Produksjonsordrer \> Utsatt produksjonsordrepostering**.

### <a name="message-grid-columns-and-filters"></a>Meldingsrutenettkolonner og -filtre

Du kan bruke feltene øverst på siden **Utsatt produksjonsordrepostering** for å finne bestemte meldinger du er på jakt etter.

Følgende filtre er tilgjengelige:

- **Meldingstype** – Angi hvilken type meldinger som skal vises i rutenettet.
- **Meldingstilstand** – Angi hvilken tilstanden for meldingene som skal vises i rutenettet. Følgende statuser finnes:

    - *Satt i kø* – Meldingen er klar til å behandles av meldingsprosessoren.
    - *Behandlet* – Meldingen ble behandlet av meldingsprosessoren.
    - *Avbrutt* – Meldingen ble ikke behandlet under det siste forsøket, og ble deretter avbrutt av brukeren.
    - *Mislykket* – Meldingen ble ikke behandlet under det siste forsøket. Systemet vil gjøre nye forsøk på å sende meldinger tre ganger. Deretter gis meldingen til tilstanden *Mislykket*. Legg merke til at du ikke kan avbryte eller redigere en melding manuelt før etter de siste tre forsøkene.

- **Meldingsinnhold** – Dette filteret utfører et fullstendig tekstsøk av meldingsinnholdet. (Meldingsinnhold vises ikke i rutenettet). Filteret behandler de fleste spesielle symboler (for eksempel bindestreker) som mellomrom, og den behandler alle mellomromstegn som boolske OR-operatorer. Hvis du for eksempel søker etter en bestemt `journalid`-verdi som er lik *USMF-123456*, finner systemet alle meldinger som inneholder USMF eller 123456. I dette tilfellet vil listen over resultater sannsynligvis være lang. Derfor er det bedre å angi bare *123456* alene, fordi det vil få mer spesifikke resultater.

Du kan også sortere og filtrere listen ved å velge en av kolonneoverskriftene og angi kriterier i rullegardinlisten.

### <a name="view-the-message-log-message-content-and-details"></a>Vise meldingslogg, meldingsinnhold og detaljer

Du kan finne detaljert informasjon om en melding ved å velge den i rutenettet og deretter velge fanen **Logg** eller **Råinnhold** under meldingsrutenettet, der hver behandlingshendelse vises.

Verktøylinjen i kategorien **Logg** inneholder følgende knapper:

- **Logg** – Velg denne knappen for å vise behandlingsresultatene. Denne knappen er særlig nyttig når meldinger har en **Behandlingsresultat**-verdien på *Mislykket*, og du vil vite årsakene til behandlingsfeilen.
- **Bunt** – Flere meldingsbehandlingsoperasjoner kan kjøres som en del av den samme satsvise prosessen. Velg denne knappen for å vise disse detaljerte dataene. Du kan for eksempel se om det finnes avhengigheter som krever at en bestemt behandlingsordre for bestemte meldinger.

### <a name="manually-process-or-cancel-a-message"></a>Behandle eller avbryte en melding manuelt

Du kan behandle eller avbryte en melding manuelt etter behov, avhengig av gjeldende status. Velg meldingen i rutenettet og deretter velge **Behandle** eller **Avbryt** i handlingsruten.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Konfigurere forretningshendelser for å levere varsler for mislykkede behandlingsresultater

Du kan konfigurere [forretningshendelser](../../fin-ops-core/dev-itpro/business-events/home-page.md) som varsler deg om mislykkede behandlingsresultater. Gå til **Systemadministrasjon \> Oppsett \> Forretningshendelser \> Forretningshendelseskatalog** og aktiver forretningshendelsen som er kalt *Meldingsbehandlingsmelding behandlet*.

Som en del av aktiveringsprosessen blir du bedt om å angi om hendelsen er spesifikk for én juridisk enhet, eller gjelder alle juridiske enheter. Du blir også bedt om å angi en **Endepunktnavn**-verdi. Denne verdien må defineres først.

> [!NOTE]
> Hvis feltet **Når en forretningshendelse oppstår** er satt til *Microsoft Power Automate* (i stedet for *HTTPS* for eksempel) opprettes **Endepunktnavn**-automatisk i Supply Chain Management basert på *Microsoft Power Automate*-oppsettet.
