---
title: Oversikt over funksjonsbehandling
description: Dette emnet beskriver funksjonsbehandling og hvordan du kan bruke det.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: c98bdbd64ee5488da20de3f5b23ae18ebce8c23f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068015"
---
# <a name="feature-management-overview"></a>Oversikt over funksjonsbehandling

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Funksjoner legges til og oppdateres i hver versjon. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Du kan deretter bruke arbeidsområdet til å vise dokumentasjon for funksjonen, og til å aktivere eller deaktivere funksjoner.

## <a name="the-feature-management-workspace"></a>Arbeidsområdet for funksjonsbehandling

Du kan åpne arbeidsområdet **Funksjonsbehandling** ved å velge den aktuelle flisen på instrumentbordet. Du vil se en side som viser en liste over funksjoner for alle versjoner som støttes av Funksjonsbehandling-opplevelsen. 

Funksjonslisten inneholder følgende informasjon:

- **Funksjonsnavn** – En beskrivelse av funksjonen som ble lagt til.
- **Status** – Et symbol angir om en funksjon er aktivert (hake), er deaktivert (tom), er planlagt aktivert (klokke) eller er obligatorisk (lås), trenger tilsyn før du aktiverer den (advarselssymbol) eller kan ikke aktiveres (X). Innstillingen som vises, brukes for alle juridiske enheter. Legg merke til at selv om en funksjon er aktivert, kontrolleres den fortsatt av sikkerhet. Funksjonen vil derfor bare være tilgjengelig for brukere som har tilgang til den, basert på sikkerhetsrollen deres. Den vil også bare være tilgjengelig i juridiske enheter som brukeren har tilgang til.
- **Aktiveringsdato** – Datoen da funksjonen ble aktivert eller planlegges å aktiveres.
- **Funksjon lagt til** – Datoen da funksjonen ble lagt til i miljøet ditt. Denne datoen angis automatisk når du oppdaterer miljøet under de månedlige versjonssyklusene.
- **Funksjonsstatus** – Gjeldende livssyklusstatus for funksjonen **Forhåndsvisning**, **Frigitt** (vist som tom), **Aktiver som standard** og **Obligatorisk**. Tilstandene er dekket i flere detaljer senere i dette emnet. 
- **Modul** – Modulen som påvirkes av den nye funksjonen.

> [!NOTE]
> Kolonnen **Funksjonsstatus** er inkludert fra versjon 10.0.21.

Når du velger en funksjon, vises mer informasjon i detaljruten til høyre for funksjonslisten. Øverst i ruten vil du se funksjonsnavnet, datoen da funksjonen ble lagt til, modulen som påvirkes av funksjonen, og en **Finn ut mer**-kobling. Velg denne koblingen for å vise dokumentasjonen for funksjonen. Hvis dokumentasjon ikke er tilgjengelig, vil du bli ført til en midlertidig side. Detaljruten inneholder også feltet **Kommentarer** der du kan legge til dine egne kommentarer om funksjonen.

Arbeidsområdet **Funksjonsbehandling** har også flere kategorier, som hver viser en liste med funksjoner.

- **Ny** – Denne fanen viser alle funksjoner som er lagt til siden den siste månedlige oppdateringen. Hvis du har hoppet over månedlige oppdateringer, viser fanen alle de nye funksjonene som er lagt til siden forrige gang du oppdaterte. De nyeste funksjonene vises øverst på listen. Totalt antall nye funksjoner vises også på en flis øverst på siden.
- **Ikke aktivert** – Denne fanen viser alle funksjoner som ikke er aktivert. De nyeste funksjonene vises øverst på listen. I tillegg viser en flis øverst på siden totalt antall nye funksjoner som for øyeblikket er deaktivert.
- **Planlagt** – Denne fanen viser alle funksjoner som er planlagt aktivert i fremtiden. Funksjonene som har den tidligste planlagte datoen, vises øverst i listen. I tillegg viser en flis øverst på siden totalt antall planlagte funksjoner.
- **Alle** – Denne fanen viser alle funksjoner. De nyeste funksjonene vises øverst på listen.

## <a name="feature-states"></a>Funksjonstilstander
Funksjoner kan gå over mellom flere tilstander, fra å bli lansert i Funksjonsstyring til eventuelt bli obligatoriske i produktet. Denne delen beskriver de gyldige funksjonstilstandene.

### <a name="preview-features-optional"></a>Forhåndsversjonsfunksjoner (valgfritt)

Produktteam kan bestemme at de først skal starte en ny funksjon som en forhåndsversjonsfunksjon. Forhåndsversjonsfunksjoner er ikke aktivert som standard, og de er valgfrie. Det eiende produktteamet oppdaterer funksjoner som frigis etter at de har fullført en vellykket forhåndsversjonsperiode.

> [!NOTE]
> Forhåndsversjonsfunksjoner er underlagt bestemte [forhåndsversjonsvilkår](https://go.microsoft.com/fwlink/?linkid=2105274). 

### <a name="released-features-optional"></a>Frigitte funksjoner (valgfritt)

**Funksjonstilstand**-kolonnen for disse funksjonene er tom. Funksjoner som først legges til som frigitte, er ikke aktivert som standard, og aktivering av dem er valgfrie. Funksjoner som oppdateres fra forhåndsversjons, beholder aktiveringstilstanden sin.

### <a name="on-by-default-features-optional"></a>Aktivert som standard-funksjoner (valgfritt)

Funksjoner som er oppdatert til **Aktivert som standard**, er aktivert som standard, men de kan deaktiveres. Etter at funksjoner som kan deaktiveres, har vært i **Frigitt**-tilstanden i minst seks måneder, forventes det at de flytter til denne statusen i den neste store versjonen. Funksjoner som går over til **Aktivert som standard**, forventes å bli kommunisert i emnet [Nyheter](../whats-new-changed.md) for versjonen. Oppdateringen startes av det eiende produktteamet.

> [!NOTE]
> Siden disse funksjonene blir aktivert automatisk, er det viktig at du fastslår om organisasjonen er klar til å innhente disse funksjonene, eller om det kreves mer tid. Hvis det kreves mer tid, kan det være nødvendig å deaktivere disse funksjonene midlertidig. Legg merke til at overgangen til en funksjon til **Aktivert som standard** vanligvis gjøres i hovedversjonen før funksjonen skal bli **obligatorisk**. På det tidspunktet har du ikke muligheten til å deaktivere funksjonen. 

### <a name="mandatory"></a>Obligatorisk

**Obligatorisk** er den forventede endelige tilstanden for funksjoner. Den indikerer at funksjonene er aktivert, og at du ikke kan deaktivere dem uten å kontakte Microsoft. Valgfrie funksjoner forventes å bli obligatoriske etter to hovedversjoner. Kritiske funksjoner kan, unntaksvis, introduseres som obligatoriske.

## <a name="example-of-expected-feature-lifecycles"></a>Eksempel på forventede livssykluser for funksjoner

Funksjoner som kan deaktiveres, og som ble lagt til som frigitt og valgfri før eller som del av april-utgivelsen, forventes å gå over til **Aktivert som standard** i oktober-utgivelsen. De forventes da å bli **obligatoriske** i april neste år.

Funksjoner som kan deaktiveres, og som ble lagt til som frigitt og valgfri før eller som del av april-utgivelsen, forventes å gå over til **obligatorisk** i april neste år.

## <a name="enable-a-feature"></a>Aktivere en funksjon

Hvis en funksjon ikke er aktivert, vises en **Aktiver nå**-knapp i detaljruten. Du kan bruke denne knappen til å aktivere funksjonen.

Noen funksjoner kan ikke deaktiveres etter at du har aktivert dem. Hvis funksjonen du prøver å aktivere, ikke kan aktiveres, får du en advarsel. På dette stadiet kan du velge **Avbryt** for å avbryte operasjonen og la funksjonen være deaktivert. Hvis du imidlertid velger **Aktiver** for å aktivere funksjonen, kan du ikke deaktivere den senere.

Noen funksjoner viser en melding som inneholder tilleggsinformasjon, før du aktiverer dem. Disse funksjonene indikeres av et gult advarselssymbol. Du bør lese tilleggsinformasjonen nøye for å sikre at du forstår hva som vil skje når funksjonen er aktivert. Du kan imidlertid fortsatt velge **Aktiver** for å aktivere funksjonen.

Noen funksjoner vil vise en melding om at funksjonen ikke kan aktiveres før en handling er utført. Disse funksjonene indikeres av et rødt X-symbol. Du må utføre handlingene som er beskrevet i beskrivelsen, før funksjonen aktiveres. Hvis du for eksempel ikke kan bruke en funksjon før en konfigurasjonsnøkkel er deaktivert, må du deaktivere konfigurasjonsnøkkelen først og deretter gå tilbake til funksjonsbehandling for å aktivere funksjonen.

Når en funksjon er aktivert, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir enten at funksjonen ble aktivert eller den fremtidige datoen når funksjonen er planlagt å bli aktivert. Den vises hver gang du velger funksjonen i funksjonslisten.

Funksjoner som er planlagt å aktiveres i fremtiden, vises i fanen **Planlagt**. En partiprosess slår den på ved midnatt på den angitte datoen basert på tidssonen som representeres av systemdatoen.

## <a name="reschedule-a-feature"></a>Planlegge en funksjon på nytt

Hvis en funksjon er planlagt å aktiveres i fremtiden, vises en **Planlegg**-knapp i detaljruten. Du kan bruke denne knappen til å endre verdien for **aktiveringsdatoen** til en annen dato.

1. Velg den planlagte funksjonen for å planlegge på nytt, og velg deretter **Planlegg** i detaljruten.
2. I **Aktiveringsdato**-feltet i dialogboksen som vises, angir du den nye datoen funksjonen skal aktiveres.
3. Velg **Aktiver** for å planlegge funksjonen på nytt, eller **Deaktiver** for å avbryte planen.

## <a name="disable-a-feature"></a>Deaktivere en funksjon

Hvis en funksjon er aktivert, vises en **Deaktiver**-knapp i detaljruten. Du kan bruke denne knappen til å deaktivere funksjonen. **Deaktiver**-knappen er ikke tilgjengelig hvis funksjonen ikke kan deaktiveres. 

Når en funksjon er deaktivert, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir at funksjonen ikke er aktivert. Den vises hver gang du velger funksjonen i funksjonslisten. Funksjoner som ikke er aktivert, vises i fanen **Ikke aktivert**.

## <a name="features-that-must-be-enabled"></a>Funksjoner som må aktiveres

Noen ganger forekommer en kritisk funksjon som må aktiveres automatisk når du gjør en oppdatering. Disse funksjonene aktiveres automatisk på datoen som er angitt i feltet **Aktiver dato**. For disse funksjonene vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir enten at funksjonen ble aktivert, eller den fremtidige datoen når funksjonen vil bli aktivert. Den vises hver gang du velger funksjonen i funksjonslisten.

## <a name="enable-all-features"></a>Aktiver alle funksjoner

Du kan aktivere alle funksjonene ved å velge **Aktiver alle**-knappen. 

Når du velger **Aktiver alle**, vises et alternativ der du må oppgi følgende informasjon:

- En liste over alle funksjoner som krever bekreftelse før de kan aktiveres. Hvis du vil aktivere funksjonene i listen, velger du **Ja** for knappen **Aktiver funksjoner som krever bekreftelse**.
- En liste over alle funksjoner som ikke kan aktiveres, vises. Disse funksjonene vil ikke bli aktivert.

Alle funksjoner som kan aktiveres, aktiveres. Hvis en funksjon allerede er planlagt aktivert i fremtiden, vil ikke tidsplanen endres. 

## <a name="enable-all-features-automatically"></a>Aktiver alle funksjoner automatisk

Hvis du vil aktivere alle nye funksjoner automatisk, kan du bruke rullegardinlisten under arbeidsområdetittelen til å endre hva som skjer når nye funksjoner legges til.

- Velg **Aktiver nye funksjoner automatisk** for å aktivere alle nye funksjoner automatisk når de legges til i ditt miljø.
- Velg **Ikke aktiver nye funksjoner automatisk** hvis alle gjeldende nye funksjoner skal deaktiveres som standard når de legges til i ditt miljø.

Når du aktiverer alle funksjonene automatisk, vil dette aktivere alle funksjonene som vil bli aktivert når du klikker på **Aktiver alle**-knappen. Det vil ikke aktivere funksjonene som krever bekreftelse eller funksjoner som ikke kan aktiveres før en handling er utført.

## <a name="check-for-updates"></a>Se etter oppdateringer

Funksjoner legges til i miljøet etter hver oppdatering. Imidlertid du kan manuelt sjekke for oppdateringer ved å klikke på **Se etter oppdateringer**-knappen. Alle funksjoner som ble lagt til systemet etter oppdateringen vil bli lagt til i listen over funksjoner. For eksempel, hvis en ny funksjon er aktivert etter en utgivelse, så kan du se etter oppdateringer og funksjonen vil bli lagt til i listen.

## <a name="assigning-roles"></a>Tilordne roller

Arbeidsområdet **Funksjonsbehandling** kan åpnes av systemansvarlige og også av brukere som er tilordnet funksjonsleder- eller funksjonsvisningsrollen. Disse to rollene ble opprettet for å støtte funksjonsbehandlingsopplevelsen. Brukere med funksjonslederrolle kan aktivere og deaktivere hvilken som helst funksjon. De kan også oppdatere **Kommentarer**-field for funksjonen. Brukere med funksjonsvisningsrolle kan bare vise **Funksjonsbehandling**-arbeidsområdet. De kan ikke aktivere eller deaktivere funksjoner.

Funksjonslederrollen og funksjonsvisningsrollen overstyrer ikke den eksisterende sikkerheten som en bruker har. De kontrollerer bare om brukeren kan aktivere og deaktivere funksjoner. De har ikke tilgang til selve funksjonene.

## <a name="features-that-use-configuration-keys"></a>Funksjoner som bruker konfigurasjonsnøkler

Hvis en funksjon bruker en konfigurasjonsnøkkel, men konfigurasjonsnøkkelen ikke er slått på, viser ikke arbeidsområdet **Funksjonsbehandling**-funksjonen i listen over tilgjengelige funksjoner. Når du har aktivert konfigurasjonsnøkkelen, må du oppdatere funksjonslisten ved hjelp av menyelementet **Se etter oppdatering**. Funksjonen vises deretter i funksjonslisten.

Hvis du deaktiverer konfigurasjonsnøkkelen, fjernes ikke funksjonen fra funksjonslisten.

## <a name="data-entities"></a>Dataenheter

En dataenhet som kalles **Funksjonsbehandling**, lar deg eksportere innstillingene for funksjonsbehandling fra ett miljø og deretter importere dem til et annet miljø. Denne enheten oppdaterer bare eksisterende funksjoner. Forretningslogikken i enheten bidrar også til å garantere at de samme reglene som brukes i arbeidsområdet **Funksjonsbehandling**, brukes når importen er fullført. Du kan for eksempel ikke overstyre en obligatorisk funksjonsinnstilling ved å fjerne datoen under importen.

Følgende eksempler beskriver hva som skjer når du bruker **Funksjonsbehandling** til å importere data.

- Hvis du endrer verdien i feltet **Aktivert** til **Ja**, aktiveres funksjonen, og feltet **Aktiveringsdato** settes til gjeldende dato.
- Hvis du endrer verdien i feltet **Aktivert** til **Nei** eller lar feltet **Aktiveringsdato** stå tomt, deaktiveres funksjonen, og merket i feltet **Aktiveringsdato** fjernes. Du kan ikke deaktivere en obligatorisk funksjon eller en funksjon som ikke kan deaktiveres når den er aktivert.
- Hvis du endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen for denne datoen.
- Hvis du endrer verdien i feltet **Aktivert** til **Ja** og endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen til denne datoen. 
- Hvis du endrer verdien i feltet **Aktivert** til **Nei**, men du også endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen til denne datoen.
- Hvis en funksjon aktiveres og du legger til et **Aktiveringsdato**-felt som er satt til en fremtidig dato, forblir funksjonen aktivert. Hvis du vil planlegge funksjonen på nytt, må du endre verdien i feltet **Aktivert** til **Nei**.

## <a name="feature-management-and-flighting"></a>Funksjonsbehandling og testversjonering

Funksjonsbehandling lar deg styre funksjonene som leveres i hver versjon. Testversjonering gir Microsoft Teams mulighet til å gi ut funksjoner til et begrenset antall kunder, slik at funksjonene kan testes og valideres uten at det påvirker alle kundene. Funksjonsbehandling styrer ikke testversjoneringen av funksjoner.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Bruke Funksjonsbehandling til å aktivere ISV-funksjoner eller egendefinerte funksjoner

Funksjonsbehandling er for øyeblikket ikke tilgjengelig for funksjoner fra uavhengige programvareleverandører og egendefinerte funksjoner. Microsoft legger imidlertid til flere funksjoner for å forbedre Funksjonsbehandling. Etter at disse forbedringene er fullført, vil Microsoft gjøre Funksjonsbehandling tilgjengelig for alle funksjoner og gi instruksjoner for hvordan du kan oppdatere funksjonene for å bruke den.

## <a name="frequently-asked-questions-faq"></a>Vanlige spørsmål

### <a name="when-are-features-added-removed-or-changed"></a>Når blir funksjoner lagt til, fjernet eller endret? 
Funksjoner legges til, fjernes og endres gjennom kodeendringer av eiende produktteam. Miljø må oppdateres for å kunne motta disse endringene.

### <a name="does-a-feature-become-mandatory-automatically"></a>Blir en funksjon obligatorisk automatisk? 
Nei, en funksjon blir ikke obligatorisk automatisk. Det eiende produktteamet må gjøre en kodeendring.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Hvorfor finnes det ikke en bestemt "obligatorisk aktivert-dato"? 
Tidspunkt for frigivelse av oppdatering varierer, miljøoppdateringstidspunkt varierer, og kunder kan velge å hoppe over enkelte oppdateringer. Derfor er bestemte datoer er vanskelige å bestemme. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Hvor er dokumentasjonen for funksjoner som er obligatoriske? 
Denne dokumentasjonen kommer hvert Dynamics 365-programteam. Ofte vil disse funksjonene bli nevnt i [Oppdateringer til klientfunksjonstilstander](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) eller [Funksjoner som er fjernet eller avskrevet](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Finnes det et varsel eller signal i produktet om at en funksjon skal bli obligatorisk aktivert? 
En varslingsmekanisme som er knyttet til å gjøre en funksjon obligatorisk, finnes ikke i dag.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Blir funksjoner noen gang aktivert uten at kunden vet om det? 
Ja, funksjoner kan aktiveres uten kundens viten i følgende situasjoner:
- En funksjon flyttes til **Aktivert som standard**. I denne tilstanden kan funksjonen fremdeles deaktiveres. 
- En funksjon er oppdatert til **Obligatorisk**. Denne endringen skjer bare i kombinasjon med en hovedversjon. Kritiske funksjoner kan, unntaksvis, flyttes til **Obligatorisk** ved enhver oppdatering.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Hva er testversjonering, og hvordan er det knyttet til funksjonshåndtering? 
Testversjonering av funksjoner er på/av-brytere i sanntid som Microsoft styrer. De er atskilt fra kundekontrollen som er levert av Funksjonsbehandling. 
- Funksjoner for privat forhåndsvisning blir ikke oppført i Funksjonsbehandling før de gjøres tilgjengelige. I produksjon må kunden godta å være en del av et spesialprogram for at dette skal skje.
- Offentlig forhåndsversjon og utgitte (generelt tilgjengelige) funksjoner vises i Funksjonsbehandling med mindre de er gjort utilgjengelige. Det å gjøre en funksjon utilgjengelig blir ansett som en siste utvei for produktteamene hvis et kritisk problem blir funnet, og er vanligvis en per-kunde-operasjon.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Blir funksjoner noen gang gjort utilgjengelige uten at kunden vet om det? 
Ja, hvis en funksjon påvirker virkemåten til et miljø som ikke har en funksjonell innvirkning, kan de aktiveres som standard.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Hvordan kan funksjonsaktivering kontrolleres i kode?
Bruk **isFeatureEnabled**-metoden i **FeatureStateProvider**-klassen, og send den som en forekomst av funksjonsklassen. Eksempel: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Hvordan kan funksjonsaktivering kontrolleres i metadata?
**FeatureClass**-egenskapen kan brukes til å angi at noen metadata er knyttet til en funksjon. Klassenavnet som brukes for funksjonen bør brukes, for eksempel **BatchContentionPreventionFeature**. Disse metadataene er bare synlig i den funksjonen. **FeatureClass**-egenskapen er tilgjengelig på menyer, menyelementer, opplistingsverdier og tabell-/visningsfelt.

### <a name="what-is-a-feature-class"></a>Hva er en funksjonsklasse?
Funksjoner i Funksjonsbehandling er definert som *funksjonsklasser*. En funksjonsklasse **implementerer IFeatureMetadata** og bruker funksjonsklasseattributtet til å identifisere seg overfor Funksjonsbehandling-arbeidsområdet. Det er flere eksempler på tilgjengelige funksjonsklasser som kan kontrolleres for aktivering i kode ved hjelp av **FeatureStateProvider**-API og i metadata som bruker **FeatureClass**-egenskapen. Eksempel: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Hva er IFeatureLifecycle som er implementert av noen funksjonsklasser?
IFeatureLifecycle er en Microsoft-intern mekanisme for å angi funksjonens livssyklusfase. Funksjoner kan være:
- `PrivatePreview` – krever at en testversjon er synlig.
- `PublicPreview` – vises som standard, men med en advarsel om at funksjonen er i forhåndsversjon.
- `Released`– fullstendig frigitt.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
