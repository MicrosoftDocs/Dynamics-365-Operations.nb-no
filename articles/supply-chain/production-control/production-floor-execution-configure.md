---
title: Konfigurere grensesnittet for produksjonsutførelse
description: Denne artikkelen beskriver hvordan du oppretter en eller flere konfigurasjoner for grensesnittet for produksjonsutførelse. Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk.
author: johanhoffmann
ms.date: 08/05/2022
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
ms.openlocfilehash: 7196306b34a72e4c53113dd644f666346f170ed7
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708732"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Produksjonsarbeidere bruker grensesnittet for produksjonsutførelse til å registrere det daglige arbeidet deres, for eksempel når de begynner på jobber, rapporterer tilbakemeldinger om jobber, registrerer indirekte aktiviteter og rapporterer fravær. Disse registreringene er grunnlaget for sporing av fremdriften og kostnaden av produksjonsordrer, samt for beregning av grunnlaget for arbeidernes lønn.

Når du åpner grensesnittet for produksjonsutførelse, laster det automatisk inn et valgt konfigurasjons- og jobbfilter som gjelder spesielt for nettleseren og enheten. I konfigurasjonen angir du policyer som må gjelde for et bestemt forbruk. Her er noen eksempler på bruk:

- På en enhet i firmahallen stempler ansatte inn når de kommer på kontoret, og de stempler ut når de går hjem for dagen.
- På en enhet i produksjonen registrerer maskinoperatører når de starter og fullfører jobbene. De registrerer også pauser og indirekte aktiviteter.

Denne artikkelen beskriver de ulike alternativene for konfigurasjon av et grensesnitt for produksjonsutførelse for hver enhet som brukes på stedet.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktiver grensesnittet for produksjonsutførelse og de relaterte valgfrie funksjonene

Selve grensesnittet for produksjonsutførelse, pluss flere av de valgfrie innstillingene som beskrives i denne artikkelen, må aktiveres for systemet før du kan bruke dem. Bruk siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere noen av eller alle funksjonene som er beskrevet under følgende underavsnitt.

### <a name="the-production-floor-execution-interface"></a>Grensesnittet for produksjonsutførelse

Dette er hovedfunksjonen som beskrives i denne artikkelen, og er en forutsetning for alle andre funksjoner som nevnes i denne delen. Den er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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

Denne funksjonen legger til en fane for aktivastyring i grensesnittet for produksjonsutførelse. Arbeidere kan bruke denne fanen til å velge et aktivum som er koblet til en maskinressurs som er innenfor det valgte filteret for jobblisten. Arbeideren kan vise statusen og tilstanden til det valgte maskinaktivumet fra tellerverdier for opptil fire valgte tellere.

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Funksjonalitet for anleggsmiddelstyring for grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Jobbsøk

Ved hjelp av denne funksjonen kan du legge til et søkefelt i jobblisten. Arbeidere kan finne en bestemt jobb ved å angi jobb-IDen eller finne alle jobber for en bestemt ordre ved å angi ordre-IDen. Arbeidere kan angi IDen ved å bruke et tastatur eller ved å skanne en strekkode.

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Jobbsøk for grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Rapport om koprodukter og biprodukter

Denne funksjonen gjør det enkelt for ansatte å bruke grensesnittet for produksjonsgulvutførelse til å rapportere fremdrift for partiordrer. Denne rapporten inkluderer rapportering på koprodukter og biprodukter.

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.29 er funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Rapport om ko- og biprodukter fra grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Vis fullstendige serie-, parti- og skiltnumre

Denne funksjonen gir en forbedret erfaring for visning av lister over serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse. Visningen endres fra en kortvisning som viser et begrenset antall tegn, til en listevisning som gir nok plass til å vise de fullstendige verdiene. Listen gir også muligheten til å søke etter bestemte numre.

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.25 er funksjonen aktivert som standard. Funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en versjon eldre enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).


Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Registrer materialforbruk

Ved hjelp av denne funksjonen kan arbeidere bruke grensesnittet for produksjonsutførelse til å registrere materialforbruk, partinumre og serienumre. Noen produsenter, særlig de i prosessindustrien, må uttrykkelig registrere mengden material som forbrukes for hvert parti eller hver produksjonsordre. Arbeidere kan for eksempel bruke en vekt til å veie mengden material som forbrukes når de arbeider. For å sikre full materialsporing må disse organisasjonene også registrere partinumrene som ble brukt til å produsere hvert produkt.

Det finnes to versjoner av denne funksjonen. Den ene støtter bare varer som *ikke er* aktivert slik at den bruker Warehouse Management-prosesser (WMS). Den andre støtter varer som *er* aktivert slik at den bruker WMS. Hvis du vil bruke denne funksjonaliteten, aktiverer du den ene av eller begge følgende funksjoner i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen), avhengig av om du har varer som er aktivert for WMS:

- *Registrer materialforbruk i grensesnittet for produksjonsutførelse (ikke lagerstyring)*
- *Registrer materialforbruk i grensesnittet for produksjonsutførelse (WMS-aktivert)*

> [!IMPORTANT]
> Du kan velge å bruke bare ikke-WMS-funksjonen. Hvis du imidlertid bruker WMS, må du aktivere begge funksjonene.

### <a name="report-on-catch-weight-items"></a>Rapport om faktisk vekt-varer

Arbeidere kan bruke grensesnittet for produksjonsutførelse til å rapportere fremdrift for partiordrer for faktisk vekt-varer. Partiordrer opprettes fra formler, som kan defineres slik at de har faktisk vekt-varer som formelvarer, koprodukter og biprodukter. En formel kan også defineres slik at den har formellinjer for ingredienser som er definert for faktisk vekt. Faktisk vekt-varer bruker to måleenheter til å spore lager: faktisk vekt-antall og lagerantall. I næringsmiddelindustrien kan for eksempel kjøtt på boks defineres som en faktisk vekt-vare, der faktisk vekt-antallet brukes til å spore antall bokser og lagerantallet brukes til å spore vekten på boksene.

For å kunne bruke denne funksjonaliteten aktiverer du følgende funksjon i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Rapport om faktisk vekt-varer fra grensesnittet for produksjonsutførelse*

### <a name="the-my-day-dialog"></a>Dialogboksen Min dag

Dialogboksen **Min dag** gir arbeidere en oversikt over de daglige registreringene og gjeldende saldoer for betalt tid, betalt overtid, fravær og betalt fravær.

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.29 er funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Visningen Min dag for grensesnittet for produksjonsutførelse* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Team

Når flere arbeidere er tildelt samme produksjonsjobb, kan de opprette en gruppe. Gruppen kan nominere én arbeider som leder. De gjenværende arbeiderne blir deretter automatisk assistenter til lederen. For gruppen som opprettes, må bare lederen registrere jobbstatus. Tidsposter gjelder alle gruppemedlemmer.

For å kunne bruke denne funksjonaliteten aktiverer du følgende funksjon i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Produksjonsteam i grensesnittet for produksjonsutførelse*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Tilleggskonfigurasjon i grensesnittet for produksjonsutførelse

Denne funksjonen legger til innstillinger for følgende funksjonalitet på siden **Konfigurer produksjonsgulvutførelse**:

- Åpne dialogboksen **Start jobb** automatisk når et søk er fullført.
- Åpne dialogboksen **Rapportfremdrift** automatisk når et søk er fullført.
- Fyll ut gjenstående antall på forhåndsfylling i dialogboksen **Rapportfremdrift**.
- Aktiver materialforbruksjusteringer fra dialogboksen **Rapportfremdrift**. (Denne funksjonaliteten krever også funksjonen *Registrer materialforbruk i grensesnittet for produksjonsutførelse (ikke-lager)*.)
- Aktiver søker etter prosjekt-ID.

Informasjon om hvordan du bruker innstillingene, finner du senere i denne artikkelen.

For å kunne bruke denne funksjonaliteten aktiverer du følgende funksjon i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Tilleggskonfigurasjon i grensesnittet for produksjonsutførelse*

## <a name="work-with-production-floor-execution-configurations"></a>Arbeide med grensesnittet for produksjonsutførelse

Du kan opprette og vedlikeholde konfigurasjoner av produksjonsutførelse ved å gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurer produksjonsutførelse**. Siden **Konfigurere produksjonsutførelse** viser en liste over eksisterende konfigurasjoner. På denne siden kan du utføre følgende handlinger:

- Velg en hvilken som helst produksjonskonfigurasjon som er oppført i venstre kolonne, for å vise og redigere den.
- På handlingsruten velger du **Ny** for å legge til en ny konfigurasjon i listen. Deretter angir du et navn i **Konfigurasjon**-feltet slik at du kan identifisere den nye konfigurasjonen. Navnet du angir, må være unikt blant alle konfigurasjoner, og du kan ikke redigere det senere. Du kan også angi en beskrivelse av konfigurasjonen i **Beskrivelse**-feltet.

Deretter konfigurerer du de ulike innstillingene for den valgte konfigurasjonen, som beskrevet i følgende underdeler.

### <a name="the-general-fasttab"></a>Hurtigfanen Generelt

Følgende innstillinger er tilgjengelige i **Generelt**-hurtigfanen:

- **Bare stemple inn og ut** – Sett dette alternativet til *Ja* for å opprette et forenklet grensesnitt som bare gir inn- og utstemplingsfunksjonalitet. Denne innstillingen deaktiverer de fleste andre alternativene på denne siden. Du må fjerne alle linjene fra hurtigfanen **Fanevalg** før du kan aktivere dette alternativet.
- **Aktiver søk** – Sett dette alternativet til *Ja* hvis du vil inkludere et søkefelt i jobblisten. Arbeidere kan finne en bestemt jobb ved å angi jobb-ID-en, eller de kan finne alle jobber for en bestemt ordre ved å angi ordre-ID-en. Arbeidere kan angi ID-en ved å bruke et tastatur eller ved å skanne en strekkode.
- **Aktiver søk etter prosjekt-ID** – Sett dette alternativet til *Ja* for å gjøre det mulig for ansatte å søke etter prosjekt-ID (i tillegg til jobb-ID og ordre-ID) i søkefeltet i grensesnittet for utførelse av produksjonsgulvet. Du kan bare sette dette alternativet til *Ja* når alternativet **Aktiver søk** også er satt til *Ja*.
- **Åpne startdialogboks automatisk** – Når dette alternativet er satt til *Ja*, åpnes dialogboksen **Start jobb** automatisk når arbeidere bruker søkefeltet til å finne en jobb.
- **Åpne dialogboks for rapportfremdrift automatisk** – Når dette alternativet er satt til *Ja*, åpnes dialogboksen **Rapportfremdrift** automatisk når arbeidere bruker søkefeltet til å finne en jobb.
- **Aktiver justering av materiale** – Sett dette alternativet til *Ja* for å aktivere **Juster materiale**-knappen i dialogboksen **Rapportfremdrift**. Arbeidere kan velge denne knappen for å justere materialforbruket for jobben.
- **Rapporter antall ved utstempling** – Sett dette alternativet til *Ja* for å be arbeiderne om å rapportere tilbakemelding om jobber som pågår ved utstempling. Når *Nei* er valgt, blir ikke arbeiderne spurt om dette.
- **Lås ansatt** – Når dette alternativet er satt til *Nei*, blir arbeidere logget av umiddelbart etter at de har utført en registrering (for eksempel en ny jobb). Grensesnittet går deretter tilbake til påloggingssiden. Når *Ja* er angitt for dette alternativet, forblir arbeidere logget på grensesnittet for produksjonsutførelse. En arbeider kan imidlertid logge seg av manuelt slik at en annen arbeider kan logge seg på når grensesnittet for produksjonsutførelse fortsetter å kjøre under den samme systembrukerkontoen. Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](config-job-card-device.md#assigned-users).
- **Bruk det faktiske registreringstidspunktet** – Velg *Ja* for å angi at tidspunktet for hver nye registrering skal være likt det nøyaktige tidspunktet da registreringen ble sendt av en arbeider. Når dette alternativet er satt til *Nei*, brukes påloggingstidspunktet i stedet. Du bør normalt velge *Ja* hvis du har satt **Lås ansatt** og/eller **Én arbeider**-alternativet til *Ja*, i tilfeller der arbeiderne ofte er logget på i lengre perioder.
- **Én arbeider** – Velg *Ja* hvis bare én arbeider bruker hvert grensesnitt for produksjonsutførelse der denne konfigurasjonen er aktiv. Når alternativet er satt til *Ja*, er **Lås ansatt**-alternativet automatisk satt til *Ja*. I tillegg fjerner dette alternativet behovet (og muligheten) for at arbeideren kan logge på med en kort-ID (eller lignende). I stedet logger arbeideren seg på Microsoft Dynamics 365 Supply Chain Management ved hjelp av en systembrukerkonto som er koblet til en *tidsregistrert arbeider* (fra *arbeidere*-tabellen), og blir samtidig logget på grensesnittet for produksjonsutførelse som den aktuelle arbeideren.
- **Tillat låsing av berøringsskjermen** – Velg *Ja* for å tillate at arbeiderne kan låse berøringsskjermen for grensesnittet for produksjonsutførelse, slik at de kan rengjøre den. Når *Ja* er angitt for dette alternativet, blir knappen **Lås skjerm for rengjøring** lagt til på påloggingssiden. Når en arbeider velger denne knappen, låses berøringsskjermen midlertidig for å hindre uønskede inndata. En nedtellingstidtaker vises også. Arbeideren kan da trygt rengjøre enheten og skjermen. Når nedtellingen er fullført, låses berøringsskjermen automatisk opp igjen.
- **Varighet for skjermlås** – Når alternativet **Tillat låsing av berøringsskjerm** er satt til *Ja*, bruker du dette alternativet til å angi antall sekunder berøringsskjermen skal være låst for rengjøring. Varigheten må være mellom 5 og 120 sekunder.
- **Generer nummerskilt** – Sett dette alternativet til *Ja* for å generere et nytt nummerskilt hver gang en arbeider bruker et grensesnitt for produksjonsutførelse for å ferdigmelde. Skiltnummeret genereres fra en nummerserie som er definert på **Parametere for lagerstyring**-siden. Når den er satt til *Nei*, må arbeiderne angi et eksisterende nummerskilt når de ferdigmelder seg.
- **Skriv ut etikett** – Sett dette alternativet til *Ja* for å skrive ut en nummerskiltetikett når en arbeider bruker grensesnittet for produksjonsutførelse til å ferdigmelde. Konfigurasjonen av etiketten defineres i dokumentruting, som beskrevet i [Etikettoppsett for dokumentruting](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Hurtigfanen Fanevalg

Bruk innstillingene på hurtigfanen **Fanevalg** til å velge hvilke faner som skal vises av grensesnittet for produksjonsutførelse når den nåværende konfigurasjonen er aktiv. Du kan utforme så mange fanen du trenger, og deretter legge til og ordne dem etter behov ved å bruke knappene på hurtigfaneverktøylinjen. Hvis du vil ha mer informasjon om hvordan du utformer faner og arbeider med innstillingene her, kan du se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Hurtigfanen Rapportfremdrift

Følgende innstillinger er tilgjengelige i **Rapportfremdrift**-hurtigfanen:

- **Aktiver justering av materiale** – Sett dette alternativet til *Ja* for å ta med **Juster materiale**-knappen i dialogboksen **Rapportfremdrift**. Arbeidere kan velge denne knappen for å justere materialforbruket for jobben.
- **Standard restantall** – Sett dette alternativet til *Ja* for å forhåndsfylle det forventede restantallet for en produksjonsjobb i dialogboksen **Rapportfremdrift**.

## <a name="clean-up-job-configurations"></a>Rydd opp i jobbkonfigurasjoner

Når arbeidslederen konfigurerer grensesnittet for produksjonsutførelse, velger de en konfigurasjon og et jobbfilter. Disse valgene er lagret i en referansetabell i Supply Chain Management, og nettleseren bruker en ID som er lagret i en lokal informasjonskapsel for å finne riktig rad i tabellen. Tabellen logger også datoen og klokkeslettet da en arbeider sist logget på hver enhet.

En satsvis jobb rydder regelmessig oppføringer i referansetabellen for enheter som ikke har logget aktiviteter i løpet av de siste 60 dagene. Du kan også rense postene manuelt når som helst ved å følge disse trinnene.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.
1. I handlingsruten velger du **Rydd opp klientkonfigurasjoner**.
1. I dialogboksen **Rydd opp klientkonfigurasjon** angir du **Antall dager**-feltet til antallet dager uten aktivitet (før i dag) som skal vurderes. Du vil fjerne alle konfigurasjoner og påloggingsoppføringer for enheter som ikke er aktive i den perioden.
1. Velg **OK** for å rydde opp i de relevante konfigurasjonene, basert på innstillingen for **Antall dager**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
