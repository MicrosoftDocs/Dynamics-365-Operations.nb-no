---
title: Konfigurere grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du oppretter en eller flere konfigurasjoner for grensesnittet for produksjonsutførelse. Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ff68761ce1cf2174be8ebb9732b9348439a53a32
ms.sourcegitcommit: d24ebce50421f8656d23bb1e47cd636ad2e2ca0a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664302"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Produksjonsarbeidere bruker grensesnittet for produksjonsutførelse til å registrere det daglige arbeidet deres, for eksempel når de begynner på jobber, rapporterer tilbakemeldinger om jobber, registrerer indirekte aktiviteter og rapporterer fravær. Disse registreringene er grunnlaget for sporing av fremdriften og kostnaden av produksjonsordrer, samt for beregning av grunnlaget for arbeidernes lønn.

Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk. Her er noen eksempler på bruk:

- På en enhet i firmahallen stempler ansatte inn når de kommer på kontoret, og de stempler ut når de går hjem for dagen.
- På en enhet i produksjonen registrerer maskinoperatører når de starter og fullfører jobbene. De registrerer også pauser og indirekte aktiviteter.

Dette emnet beskriver de ulike alternativene for konfigurasjon av jobbkortenheter.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktiver grensesnittet for produksjonsutførelse og de relaterte valgfrie funksjonene

Selve grensesnittet for produksjonsutførelse, pluss flere av de valgfrie innstillingene som beskrives i dette emnet, må aktiveres i systemet før du kan bruke dem. Bruk siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere noen av eller alle funksjonene som er beskrevet under følgende underavsnitt.

### <a name="the-production-floor-execution-interface"></a>Grensesnittet for produksjonsutførelse

Dette er primærfunksjonen som beskrives i dette emnet. Det legger til grensesnittet for produksjonsutførelse i systemet. Aktiver følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere det:  
- Produksjonsutførelse

### <a name="generate-license-plates"></a>Generer nummerskilter

Disse funksjonene gjør nummerskiltfunksjoner tilgjengelige for grensesnittet for produksjonsutførelse. Hvis du vil bruke dem, aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. Nummerskilt for ferdigmelding lagt til i jobbkortenheten
1. Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten

### <a name="print-labels"></a>Skriv ut etiketter

Disse funksjonene gjør etikettutskriftsfunksjoner tilgjengelige for grensesnittet for produksjonsutførelse. Hvis du vil bruke dem, aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. Nummerskilt for ferdigmelding lagt til i jobbkortenheten
1. Skriv ut etikett fra jobbkortenhet

### <a name="allow-locking-the-touch-screen"></a>Tillate låsing av berøringsskjermen

Denne funksjonen legger til en knapp i grensesnittet for produksjonsutførelse, som gjør at ansatte kan rengjøres på berøringsskjermen. Hvis du vil bruke den, aktiverer du følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres

## <a name="work-with-production-floor-execution-configurations"></a>Arbeide med grensesnittet for produksjonsutførelse

Slik oppretter og vedlikeholder du enhetskonfigurasjoner: Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**. Siden **Konfigurere produksjonsutførelse** viser en liste over eksisterende konfigurasjoner. På denne siden kan du utføre følgende handlinger:

- Velg en hvilken som helst produksjonskonfigurasjon som er oppført i venstre kolonne, for å vise og redigere den.
- Velg **Ny** i handlingsruten for å legge til en ny enhetskonfigurasjon i listen. Deretter angir du et navn i **Konfigurasjon**-feltet slik at du kan identifisere den nye konfigurasjonen. Navnet du angir her, må være unik blant alle enhetskonfigurasjoner, og du vil ikke kunne redigere den senere.

Deretter konfigurerer du de ulike innstillingene for den valgte enhetskonfigurasjonen. Følgende felt er tilgjengelige:

- **Rapporter antall ved utstempling** – Sett dette alternativet til *Ja* for å be arbeiderne om å rapportere tilbakemelding om jobber som pågår ved utstempling. Når *Nei* er valgt, blir ikke arbeiderne spurt om dette.
- **Lås ansatt** – Når dette alternativet er satt til *Nei*, blir arbeidere logget av umiddelbart etter at de har utført en registrering (for eksempel en ny jobb). Enheten vil deretter gå tilbake til påloggingssiden. Når dette alternativet er satt til *Ja*, vil arbeidere forbli logget på jobbkortenheten. En arbeider kan imidlertid logge av manuelt slik at en annen arbeider kan logge på når jobbkortetheten fortsetter å kjøre under den samme systembrukerkontoen. Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](config-job-card-device.md#assigned-users).
- **Bruk det faktiske registreringstidspunktet** – Velg *Ja* for å angi at tidspunktet for hver nye registrering skal være likt det nøyaktige tidspunktet da registreringen ble sendt av en arbeider. Når dette alternativet er satt til *Nei*, brukes påloggingstidspunktet i stedet. Du bør normalt velge *Ja* hvis du har satt **Lås ansatt** og/eller **Én arbeider**-alternativet til *Ja*, i tilfeller der arbeiderne ofte er logget på i lengre perioder.
- **Én arbeider** – Velg *Ja* hvis bare én arbeider bruker hver jobbkortenhet der denne konfigurasjonen er aktiv. Når alternativet er satt til *Ja*, er **Lås ansatt**-alternativet automatisk satt til *Ja*. I tillegg fjerner dette alternativet behovet (og muligheten) for at arbeideren kan logge på med en kort-ID (eller lignende). I stedet logger arbeideren seg på Microsoft Dynamics 365 Supply Chain Management ved hjelp av en systembrukerkonto som er koblet til en *tidsregistrert arbeider* (fra *arbeidere*-tabellen), og blir samtidig logget på jobbkortenheten som den aktuelle arbeideren.
- **Tillat låsing av berøringsskjermen** – Velg *Ja* for å tillate at arbeiderne kan låse berøringsskjermen for jobbkortenheten slik at de kan rengjøre den. Når dette alternativet er satt til *Ja*, legges det til en **Lås skjerm for rengjøring**-knapp på siden for enhetspålogging. Når en arbeider velger denne knappen, låses berøringsskjermen midlertidig for å hindre uønskede inndata. En nedtellingstidtaker vises også. Arbeideren kan da trygt rengjøre enheten og skjermen. Når nedtellingen er fullført, låses berøringsskjermen automatisk opp igjen.
- **Varighet for skjermlås** – Når alternativet **Tillat låsing av berøringsskjerm** er satt til *Ja*, bruker du dette alternativet til å angi antall sekunder berøringsskjermen skal være låst for rengjøring. Varigheten må være mellom 5 og 120 sekunder.
- **Generer nummerskilt** – Sett dette alternativet til *Ja* for å generere et nytt nummerskilt hver gang en arbeider bruker en jobbkortenhet for å ferdigmelde. Skiltnummeret genereres fra en nummerserie som er definert på **Parametere for lagerstyring**-siden. Når den er satt til *Nei*, må arbeiderne angi et eksisterende nummerskilt når de ferdigmelder seg.
- **Skriv ut etikett** – Sett dette alternativet til *Ja* for å skrive ut en nummerskiltetikett når en arbeider bruker jobbkortenheten til å ferdigmelde. Konfigurasjonen av etiketten defineres i dokumentruting, som beskrevet i [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).
- **Fanevalg** – Bruk innstillingene i denne delen til å velge hvilke faner som skal vises av grensesnittet for produksjonsutførelse når den gjeldende konfigurasjonen er aktiv. Du kan utforme så mange faner du trenger, og deretter legge dem til og ordne dem her etter behov. Hvis du vil ha mer informasjon om hvordan du utformer faner og arbeider med innstillingene her, kan du se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Rydd opp i jobbkonfigurasjoner

Når arbeidslederen konfigurerer grensesnittet for produksjonsutførelse, velger de en konfigurasjon og et jobbfilter. Disse valgene er lagret i en referansetabell i Supply Chain Management, og nettleseren bruker en ID som er lagret i en lokal informasjonskapsel for å finne riktig rad i tabellen. Tabellen logger også datoen og klokkeslettet da en arbeider sist logget på hver enhet.

En satsvis jobb rydder regelmessig oppføringer i referansetabellen for enheter som ikke har logget aktiviteter i løpet av de siste 60 dagene. Du kan også rense postene manuelt når som helst ved å følge disse trinnene.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.
1. I handlingsruten velger du **Rydd opp klientkonfigurasjoner**.
1. I dialogboksen **Rydd opp klientkonfigurasjon** angir du **Antall dager**-feltet til antallet dager uten aktivitet (før i dag) som skal vurderes. Du vil fjerne alle konfigurasjoner og påloggingsoppføringer for enheter som ikke er aktive i den perioden.
1. Velg **OK** for å rydde opp i de relevante konfigurasjonene, basert på innstillingen for **Antall dager**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]