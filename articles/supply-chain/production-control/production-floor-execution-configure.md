---
title: Konfigurere grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du oppretter en eller flere konfigurasjoner for grensesnittet for produksjonsutførelse. Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 30f36ccf967c47d6a034c00544d45cdfdc3d1907
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103394"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Produksjonsarbeidere bruker grensesnittet for produksjonsutførelse til å registrere det daglige arbeidet deres, for eksempel når de begynner på jobber, rapporterer tilbakemeldinger om jobber, registrerer indirekte aktiviteter og rapporterer fravær. Disse registreringene er grunnlaget for sporing av fremdriften og kostnaden av produksjonsordrer, samt for beregning av grunnlaget for arbeidernes lønn.

Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk. Her er noen eksempler på bruk:

- På en enhet i firmahallen stempler ansatte inn når de kommer på kontoret, og de stempler ut når de går hjem for dagen.
- På en enhet i produksjonen registrerer maskinoperatører når de starter og fullfører jobbene. De registrerer også pauser og indirekte aktiviteter.

Dette emnet beskriver de ulike alternativene for konfigurasjon av et grensesnitt for produksjonsutførelse for hver enhet som brukes på stedet.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktiver grensesnittet for produksjonsutførelse og de relaterte valgfrie funksjonene

Selve grensesnittet for produksjonsutførelse, pluss flere av de valgfrie innstillingene som beskrives i dette emnet, må aktiveres i systemet før du kan bruke dem. Bruk siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere noen av eller alle funksjonene som er beskrevet under følgende underavsnitt.

### <a name="the-production-floor-execution-interface"></a>Grensesnittet for produksjonsutførelse

Dette er hovedfunksjonen som beskrives i dette emnet, og er en forutsetning for alle andre funksjoner som nevnes i denne delen. Den er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Generer nummerskilter

Disse funksjonene gjør nummerskiltfunksjoner tilgjengelige for grensesnittet for produksjonsutførelse. Hvis du vil bruke dem, aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. *Nummerskilt for ferdigmelding lagt til i jobbkortenheten*<br>(Fra og med Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management versjon 10.0.25.)
1. *Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten*<br>(Denne funksjonen er obligatorisk fra og med Supply Chain Management versjon 10.0.25.)

### <a name="print-labels"></a>Skriv ut etiketter

Disse funksjonene gjør etikettutskriftsfunksjoner tilgjengelige for grensesnittet for produksjonsutførelse. Hvis du vil bruke dem, aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. *Nummerskilt for ferdigmelding lagt til i jobbkortenheten*<br>(Fra og med Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management versjon 10.0.25.)
1. *Skriv ut etikett fra jobbkortenhet*<br>(Denne funksjonen er obligatorisk fra og med Supply Chain Management versjon 10.0.25.)

### <a name="allow-locking-the-touch-screen"></a>Tillate låsing av berøringsskjermen

Denne funksjonen gjør at arbeidere kan løse berøringsskjermen, slik at de kan rengjøre den.

Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Funksjonalitet for anleggsmiddelstyring for grensesnittet for produksjonsutførelse

Denne funksjonen legger til en fane for aktivastyring i grensesnittet for produksjonsutførelse. Arbeidere kan bruke denne fanen til å velge et aktivum som er koblet til en maskinressurs som er innenfor det valgte filteret for jobblisten. Arbeideren kan vise statusen og tilstanden til det valgte maskinaktivumet fra tellerverdier for opptil fire valgte tellere. Hvis du vil bruke denne funksjonen, aktiverer du følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Funksjonalitet for anleggsmiddelstyring for grensesnittet for produksjonsutførelse*<br>(Denne funksjonen er aktivert som standard fra og med Supply Chain Management versjon 10.0.25.)

### <a name="enable-job-search"></a>Aktivere jobbsøk

Ved hjelp av denne funksjonen kan du legge til et søkefelt i jobblisten. Arbeidere kan finne en bestemt jobb ved å angi jobb-IDen eller finne alle jobber for en bestemt ordre ved å angi ordre-IDen. Arbeidere kan angi IDen ved å bruke et tastatur eller ved å skanne en strekkode. Hvis du vil bruke den, aktiverer du følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Jobbsøk for grensesnittet for produksjonsutførelse*<br>(Denne funksjonen er aktivert som standard fra og med Supply Chain Management versjon 10.0.25.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Aktivere rapportering på koprodukter og biprodukter

Denne funksjonen gjør det enkelt for ansatte å bruke grensesnittet for produksjonsgulvutførelse til å rapportere fremdrift for partiordrer. Denne rapporten inkluderer rapportering på koprodukter og biprodukter. For å kunne bruke denne funksjonen aktiverer du følgende funksjon i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Rapport om ko- og biprodukter fra grensesnittet for produksjonsutførelse*

## <a name="work-with-production-floor-execution-configurations"></a>Arbeide med grensesnittet for produksjonsutførelse

Du kan opprette og vedlikeholde konfigurasjoner av produksjonsutførelse ved å gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurer produksjonsutførelse**. Siden **Konfigurere produksjonsutførelse** viser en liste over eksisterende konfigurasjoner. På denne siden kan du utføre følgende handlinger:

- Velg en hvilken som helst produksjonskonfigurasjon som er oppført i venstre kolonne, for å vise og redigere den.
- Velg **Ny** i handlingsruten for å legge til en ny konfigurasjon i listen. Deretter angir du et navn i **Konfigurasjon**-feltet slik at du kan identifisere den nye konfigurasjonen. Navnet du angir, må være unikt blant alle konfigurasjoner, og du kan ikke redigere det senere.

Konfigurer deretter de ulike innstillingene for den valgte konfigurasjonen. Følgende felt er tilgjengelige:

- **Bare stemple inn og ut** – Sett dette alternativet til *Ja* for å opprette et forenklet grensesnitt som bare gir inn- og utstemplingsfunksjonalitet. Dette deaktiverer de fleste andre alternativene på denne siden. Du må fjerne alle linjene fra hurtigfanen **Fanevalg** før du kan aktivere dette alternativet.
- **Aktiver søk** - Sett dette alternativet til *Ja* hvis du vil inkludere et søkefelt i jobblisten. Arbeidere kan finne en bestemt jobb ved å angi jobb-IDen eller finne alle jobber for en bestemt ordre ved å angi ordre-IDen. Arbeidere kan angi IDen ved å bruke et tastatur eller ved å skanne en strekkode.
- **Rapporter antall ved utstempling** – Sett dette alternativet til *Ja* for å be arbeiderne om å rapportere tilbakemelding om jobber som pågår ved utstempling. Når *Nei* er valgt, blir ikke arbeiderne spurt om dette.
- **Lås ansatt** – Når dette alternativet er satt til *Nei*, blir arbeidere logget av umiddelbart etter at de har utført en registrering (for eksempel en ny jobb). Grensesnittet går deretter tilbake til påloggingssiden. Når *Ja* er angitt for dette alternativet, forblir arbeidere logget på grensesnittet for produksjonsutførelse. En arbeider kan imidlertid logge seg av manuelt slik at en annen arbeider kan logge seg på når grensesnittet for produksjonsutførelse fortsetter å kjøre under den samme systembrukerkontoen. Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](config-job-card-device.md#assigned-users).
- **Bruk det faktiske registreringstidspunktet** – Velg *Ja* for å angi at tidspunktet for hver nye registrering skal være likt det nøyaktige tidspunktet da registreringen ble sendt av en arbeider. Når dette alternativet er satt til *Nei*, brukes påloggingstidspunktet i stedet. Du bør normalt velge *Ja* hvis du har satt **Lås ansatt** og/eller **Én arbeider**-alternativet til *Ja*, i tilfeller der arbeiderne ofte er logget på i lengre perioder.
- **Én arbeider** – Velg *Ja* hvis bare én arbeider bruker hvert grensesnitt for produksjonsutførelse der denne konfigurasjonen er aktiv. Når alternativet er satt til *Ja*, er **Lås ansatt**-alternativet automatisk satt til *Ja*. I tillegg fjerner dette alternativet behovet (og muligheten) for at arbeideren kan logge på med en kort-ID (eller lignende). I stedet logger arbeideren seg på Microsoft Dynamics 365 Supply Chain Management ved hjelp av en systembrukerkonto som er koblet til en *tidsregistrert arbeider* (fra *arbeidere*-tabellen), og blir samtidig logget på grensesnittet for produksjonsutførelse som den aktuelle arbeideren.
- **Tillat låsing av berøringsskjermen** – Velg *Ja* for å tillate at arbeiderne kan låse berøringsskjermen for grensesnittet for produksjonsutførelse, slik at de kan rengjøre den. Når *Ja* er angitt for dette alternativet, blir knappen **Lås skjerm for rengjøring** lagt til på påloggingssiden. Når en arbeider velger denne knappen, låses berøringsskjermen midlertidig for å hindre uønskede inndata. En nedtellingstidtaker vises også. Arbeideren kan da trygt rengjøre enheten og skjermen. Når nedtellingen er fullført, låses berøringsskjermen automatisk opp igjen.
- **Varighet for skjermlås** – Når alternativet **Tillat låsing av berøringsskjerm** er satt til *Ja*, bruker du dette alternativet til å angi antall sekunder berøringsskjermen skal være låst for rengjøring. Varigheten må være mellom 5 og 120 sekunder.
- **Generer nummerskilt** – Sett dette alternativet til *Ja* for å generere et nytt nummerskilt hver gang en arbeider bruker et grensesnitt for produksjonsutførelse for å ferdigmelde. Skiltnummeret genereres fra en nummerserie som er definert på **Parametere for lagerstyring**-siden. Når den er satt til *Nei*, må arbeiderne angi et eksisterende nummerskilt når de ferdigmelder seg.
- **Skriv ut etikett** – Sett dette alternativet til *Ja* for å skrive ut en nummerskiltetikett når en arbeider bruker grensesnittet for produksjonsutførelse til å ferdigmelde. Konfigurasjonen av etiketten defineres i dokumentruting, som beskrevet i [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).
- **Fanevalg** – Bruk innstillingene i denne delen til å velge hvilke faner som skal vises av grensesnittet for produksjonsutførelse når den gjeldende konfigurasjonen er aktiv. Du kan utforme så mange faner du trenger, og deretter legge dem til og ordne dem her etter behov. Hvis du vil ha mer informasjon om hvordan du utformer faner og arbeider med innstillingene her, kan du se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Rydd opp i jobbkonfigurasjoner

Når arbeidslederen konfigurerer grensesnittet for produksjonsutførelse, velger de en konfigurasjon og et jobbfilter. Disse valgene er lagret i en referansetabell i Supply Chain Management, og nettleseren bruker en ID som er lagret i en lokal informasjonskapsel for å finne riktig rad i tabellen. Tabellen logger også datoen og klokkeslettet da en arbeider sist logget på hver enhet.

En satsvis jobb rydder regelmessig oppføringer i referansetabellen for enheter som ikke har logget aktiviteter i løpet av de siste 60 dagene. Du kan også rense postene manuelt når som helst ved å følge disse trinnene.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.
1. I handlingsruten velger du **Rydd opp klientkonfigurasjoner**.
1. I dialogboksen **Rydd opp klientkonfigurasjon** angir du **Antall dager**-feltet til antallet dager uten aktivitet (før i dag) som skal vurderes. Du vil fjerne alle konfigurasjoner og påloggingsoppføringer for enheter som ikke er aktive i den perioden.
1. Velg **OK** for å rydde opp i de relevante konfigurasjonene, basert på innstillingen for **Antall dager**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
