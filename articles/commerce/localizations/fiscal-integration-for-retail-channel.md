---
title: Oversikt over regnskapsintegrering for Commerce-kanaler
description: Dette emnet gir en oversikt over funksjonene for regnskapsintegrering som er tilgjengelige i Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 46e0afd5a8cb692da56a7d5f261ca30d9b3aaa80
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388319"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Oversikt over regnskapsintegrering for Commerce-kanaler

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dette emnet er en oversikt over funksjonene for regnskapsintegrering som er tilgjengelige i Dynamics 365 Commerce. 

Regnskapsintegrering omfatter integrering med ulike regnskapsenheter og -tjenester som gir mulighet for bilagsregistrering av salg i samsvar med lokale regnskapslover som er rettet mot å hindre avgiftssvindel i detaljhandelen. Her er noen vanlige scenarier som kan dekkes ved å bruke regnskapsintegrering:

- Registrer et salg på en regnskapsenhet som er koblet til salgsstedet, for eksempel en bilagsskriver, og skriv ut en bilagskvittering for kunden.
- Send informasjon som er knyttet til salg og returer som er fullført i Retail POS, sikkert til en ekstern webtjeneste som styres av skattemyndighetene.
- Bidra til å sikre at salgstransaksjonsdata ikke kan endres, gjennom digitale signaturer.

Funksjonen for regnskapsintegrering er et rammeverk som gir en felles løsning for videre utvikling og tilpassing av integreringen mellom Retail POS og regnskapsenheter og -tjenester. Funksjonen inneholder også eksempler på regnskapsintegrering som støtter grunnleggende scenarioer for bestemte land eller områder, og som fungerer med bestemte regnskapsenheter eller -tjenester. Et eksempel på regnskapsintegrering består av flere utvidelser for handelskomponenter og er inkludert i software development kit (SDK). Hvis du vil ha mer informasjon om eksemplene på regnskapsintegrering, kan du se [Eksempler på regnskapsintegrering i SDK for Commerce](#fiscal-integration-samples-in-the-commerce-sdk). Hvis du vil ha informasjon om hvordan du installerer og bruker Commerce SDK, se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

For å støtte andre scenarier som ikke støttes av et regnskapsintegreringseksempel, for å integrere Retail POS med andre regnskapsenheter eller -tjenester, eller for å oppfylle kravene til andre land eller regioner, må du enten utvide et eksisterende regnskapsintegreringseksempel eller lage et nytt eksempel ved hjelp av et eksisterende eksempel.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Bilagsregistreringsprosess og regnskapsintegreringseksempler for regnskapsenheter og -tjenester

En bilagsregistreringsprosess i Retail POS kan bestå av ett eller flere trinn. Hvert trinn omfatter bilagsregistrering av bestemte transaksjoner eller hendelser i én regnskapsenhet eller -tjeneste. Følgende løsningskomponenter deltar i bilagsregistreringen i en regnskapsenhet eller -tjeneste:

- **Regnskapsdokumentleverandør** – Denne komponenten serialiserer data fra transaksjoner/hendelser i formatet som også brukes for samhandling med regnskapsenheten eller -tjenesten, analyserer svar fra regnskapsenheten eller -tjenestsen og lagrer svarene i kanaldatabasen. Utvidelsen definerer også bestemte transaksjoner og hendelser som skal registreres.
- **Regnskapskobling** – Denne komponenten starter kommunikasjonen med regnskapsenheten eller -tjenesten, sender forespørsler og dirigerer kommandoer til regnskapsenheten eller -tjenestenpå grunnlag av data fra transaksjonene/hendelsene som er hentet fra regnskapsdokumentet, og mottar svar fra regnskapsenheten eller -tjenesten.

Et eksempel på regnskapsintegrering kan inneholde Commerce Runtime (CRT), maskinvarestasjon og POS-tillegg for en regnskapsdokumentleverandør og en regnskapskobling. Det inneholder også følgende komponentkonfigurasjoner:

- **Konfigurasjon av regnskapsdokumentleverandør** – Denne konfigurasjonen definerer en utdatametode og et format for regnskapsdokumenter. Den inneholder også en datatilordning for avgifter og betalingsmåter for å gjøre data fra Retail POS kompatible med verdiene som er forhåndsdefinert i fastvaren til regnskapsenheten eller -tjenesten.
- **Konfigurasjon av regnskapskobling** – Denne konfigurasjonen definerer den fysiske kommunikasjonen med en bestemt regnskapsenhet eller -tjeneste.

En bilagsregistreringsprosess for en bestemt salgsstedskasse er definert av en tilsvarende innstilling i funksjonalitetsprofilen for salgsstedet. Hvis du vil ha mer informasjon om hvordan du konfigurerer en bilagsregistreringsprosess, laster opp konfigurasjoner for regnskapsdokumentleverandører og regnskapskoblinger, og endrer konfigurasjonsparametere, kan du se [Konfigurere en bilagsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Hvis du trenger enheter til ikke-regnskapsoperasjoner, for eksempel søk i produktkatalog, kundeoppslag eller opprettelse av transaksjonsutkast, kan du velge disse som kasser med begrensninger for regnskapsprosess. Hvis du vil ha mer informasjon, kan du se [Konfigurere kasser med begrensninger for regnskapsregistrering](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Følgende vanlige regnskapsregistreringsflyt starter med en hendelse i POS (for eksempel avslutning av en salgstransaksjon), og implementerer en forhåndsdefinert trinnsekvens som involverer andre Commerce-komponenter (for eksempel CRT og maskinvarestasjon).

1. POS ber om et regnskapsdokument fra FIF (Fiscal Integration Framework – rammeverket for regnskapsintegrering).
1. FIF bestemmer om den gjeldende hendelsen krever bilagsregistrering.
1. Basert på innstillingene for bilagsregistreringsprosessen identifiserer FIF en regnskapskobling og en tilsvarende regnskapsdokumentleverandør som skal brukes i bilagsregistreringen.
1. FIF kjører regnskapsdokumentleverandøren som genererer et regnskapsdokument (for eksempel et XML-dokument) som representerer transaksjonen eller hendelsen.
1. FIF returnerer det genererte regnskapsdokumentet til POS.
1. POS ber om at FIF sender regnskapsdokumentet til regnskapsenheten eller -tjenesten.
1. FIF kjører regnskapskoblingen som behandler regnskapsdokumentet, og sender det til regnskapsenheten eller -tjenesten.
1. FIF returnerer det regnskapsmessige svaret (det vil si svaret fra regnskapsenheten eller -tjenesten) til POS.
1. Salgsstedet analyserer det regnskapsmessige svaret for å bestemme om bilagsregistreringen var vellykket. Etter behov ber POS om at FIF håndterer eventuelle feil som oppstod. 
1. POS ber om at FIF behandler og lagrer det regnskapsmessige svaret.
1. Regnskapsdokumentleverandøren behandler regnskapssvaret. Som en del av denne behandlingen analyserer regnskapsdokumentleverandøren svaret og henter utvidede data fra det.
1. FIF lagrer svaret og de utvidede dataene til kanaldatabasen.
1. Etter behov skriver POS ut en kvittering via en vanlig kvitteringsskriver som er koblet til maskinvarestasjonen. Kvitteringen kan inneholde nødvendige data fra det regnskapsmessige svaret.
 
Følgende eksempler viser kjøringsflyter for bilagsregistrering for vanlige regnskapsenheter eller -tjenester.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Regnskapsregistrering utføres via en enhet som er koblet til maskinvarestasjonen

Denne konfigurasjonen brukes når en fysisk regnskapsenhet, for eksempel en regnskapsskriver, er koblet til maskinvarestasjonen. Dette gjelder også når kommunikasjonen med en regnskapsenhet eller -tjeneste utføres via programvare som er installert på maskinvarestasjonen. I dette tilfellet er regnskapsdokumentleverandøren plassert i CRT, og regnskapskontakten er plassert på maskinvarestasjonen.

![Regnskapsregistrering utføres via en enhet som er koblet til maskinvarestasjonen.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Regnskapsregistrering utføres via en ekstern tjeneste

Denne konfigurasjonen brukes når regnskapsregistrering utføres via en ekstern tjeneste, for eksempel en webtjeneste som drives av skattemyndighetene. I dette tilfellet er både regnskapsdokumentleverandøren og regnskapskontakten plassert i CRT.

![Regnskapsregistrering utføres via en ekstern tjeneste.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Regnskapsregistrering utføres internt i CRT

Denne konfigurasjonen brukes når ingen ekstern regnskapsenhet eller -tjeneste er nødvendig for regnskapsregistrering. Den brukes for eksempel når regnskapsregistrering utføres via digital signering av salgstransaksjoner. I dette tilfellet er både regnskapsdokumentleverandøren og regnskapskontakten plassert i CRT.

![Regnskapsregistrering utføres internt i CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Bilagsregistrering utføres via en enhet eller tjeneste i det lokale nettverket

Denne konfigurasjonen brukes når en fysisk regnskapsenhet eller regnskapstjeneste finnes i det lokale nettverket i butikken, og har et HTTPS-grensesnitt for programmering av apper (API). I dette tilfellet er regnskapsdokumentleverandøren plassert i CRT, og regnskapskontakten er plassert på POS.

![Bilagsregistrering utføres via en enhet eller tjeneste i det lokale nettverket.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Feilbehandling

Rammeverket for regnskapsintegrering har følgende alternativer for å håndtere feil under bilagsregistreringen:

- **Prøv på nytt** – Operatører kan bruke dette alternativet når feilen kan løses raskt, og bilagsregistreringen kan kjøres på nytt. Dette alternativet kan for eksempel brukes når regnskapsenheten ikke er tilkoblet, bilagsskriveren er tom for papir, eller det er papirstopp i bilagsskriveren.
- **Avbryt** – Dette alternativet lar operatører utsette bilagsregistreringen av den gjeldende transaksjonen eller hendelsen hvis den mislykkes. Når registreringen utsettes, kan operatøren fortsette å arbeide på salgsstedet, og kan utføre alle operasjoner som bilagsregistreringen ikke er nødvendig for. Når en hendelse som krever bilagsregistrering, skjer på salgsstedet (for eksempel en ny transaksjon åpnes), vises automatisk dialogboksen for feilhåndtering for å varsle operatøren at den forrige transaksjonen ikke ble riktig registrert, og for å gi alternativer for å håndtere feilen.
- **Hopp over** – Operatører kan bruke dette alternativet når bilagsregistreringen kan utelates ved bestemte betingelser, og det kan fortsettes med vanlige operasjoner på salgsstedet. Dette alternativet kan for eksempel brukes når en salgstransaksjon som bilagsregistreringen mislyktes for, kan registreres i en bestemt papirjournal.
- **Merk som registrert** – Operatører kan bruke dette alternativet når transaksjonen faktisk ble registrert i regnskapsenheten (for eksempel en bilagskvittering ble skrevet ut), men det oppstod en feil under lagring av regnskapssvaret i kanaldatabasen.
- **Utsett** – Operatører kan bruke dette alternativet når transaksjonen ikke ble registrert fordi registreringstjenesten ikke var tilgjengelig. 

> [!NOTE]
> Alternativene **Hopp over**, **Merk som registrert** og **Utsett** må aktiveres i bilagsregistreringsprosessen før de brukes. I tillegg må tilsvarende tillatelser gis til operatører.

Alternativene **Hopp over**, **Merk som registrert** og **Utsett** gjør at informasjonskoder kan hente bestemt informasjon om en feil, for eksempel årsaken til feilen eller en begrunnelse for å hoppe over bilagsregistreringen eller merke transaksjonen som registrert. Hvis du vil ha mer informasjon om hvordan du definerer parametere for feilbehandling, se [Konfigurere innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valgfri bilagsregistrering

Bilagsregistrering kan være obligatorisk for enkelte operasjoner, men valgfritt for andre. For eksempel kan bilagsregistrering av vanlig salg og returer være obligatorisk, men bilagsregistrering av operasjoner som er knyttet til kundeinnbetalinger, kan være valgfritt. I dette tilfellet skal manglende fullføring av bilagsregistrering av salg blokkere videre salg, men manglende fullføring av bilagsregistrering for en kundeinnbetaling skal ikke blokkere videre salg. For å skille mellom obligatoriske og valgfrie operasjoner anbefales det å håndtere dem gjennom ulike dokumentleverandører, og du bør definere separate trinn i bilagsregistreringsprosessen for disse leverandørene. Parameteren **Fortsett ved feil** skal aktiveres for alle trinn som er knyttet til valgfri bilagsregistrering. Hvis du vil ha mer informasjon om hvordan du definerer parametere for feilbehandling, se [Konfigurere innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Kjøre bilagsregistrering på nytt manuelt

Hvis bilagsregistrering av en transaksjon eller hendelse er utsatt etter en feil (for eksempel hvis operatoren valgte **Avbryt** i dialogboksen for feilbehandling), kan du kjøre bilagsregistreringen på nytt manuelt ved å bruke en tilsvarende operasjon. Hvis du vil ha mer informasjon, se [Aktivere manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Utsett-alternativet

Med **Utsett**-alternativet kan du fortsette med bilagsregistreringsprosessen hvis det gjeldende trinnet mislykkes. Det kan brukes når det finnes et reservealternativ for bilagsregistrering.

### <a name="fiscal-registration-health-check"></a>Tilstandskontroll for bilagsregistrering

Tilstandskontrollprosedyren for bilagsregistreringer kontrollerer tilgjengeligheten av regnskapsenheten eller -tjenesten når bestemte hendelser skjer. Hvis bilagsregistreringen ikke for øyeblikket kan fullføres, varsles operatøren på forhånd.

Salgsstedet kjører tilstandskontrollen når det oppstår følgende hendelser:

- Det åpnes en ny transaksjon.
- En suspendert transaksjon tilbakekalles.
- En transaksjon for salg eller retur er fullført.

Hvis tilstandskontrollen mislykkes, viser salgsstedet dialogboksen for tilstandskontroll. Denne dialogboksen inneholder følgende knapper:

- **OK** – Med denne knappen kan operatøren ignorere tilstandskontrollfeil og fortsette å behandle operasjonen. Operatører kan velge denne knappen hvis tillatelsen **Tillat å hoppe over tilstandskontrollfeil** er aktivert for dem.
- **Avbryt** – Hvis operatøren velger denne knappen, avbryter salgsstedet siste handling (for eksempel når en vare ikke er lagt til en ny transaksjon).

> [!NOTE]
> Tilstandskontrollen kjøres bare hvis den gjeldende operasjonen krever bilagsregistrering, og hvis parameteren **Fortsett ved feil** er deaktivert for gjeldende trinn i bilagsregistreringsprosessen. Hvis du vil ha mer informasjon, se [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Lagre regnskapssvar i regnskapstransaksjon

Når bilagsregistrering av en transaksjon eller hendelse er vellykket, opprettes en regnskapstransaksjon i kanaldatabasen og kobles til den opprinnelige transaksjonen eller hendelsen. På samme måte, hvis alternativet **Hopp over** eller **Merk som registrert** er valgt for en mislykket bilagsregistrering, lagres denne informasjonen i en regnskapstransaksjon. En regnskapstransaksjon inneholder regnskapssvaret for regnskapsenheten eller -tjenesten. Hvis bilagsregistreringsprosessen består av flere trinn, opprettes en regnskapstransaksjon for hvert trinn i prosessen som resulterte i en vellykket eller mislykket registrering.

Regnskapstransaksjoner overføres til hovedkontoret av *P-jobb* sammen med transaksjoner. I hurtigfanen **Regnskapstransaksjoner** på siden **Butikktransaksjoner** kan du vise regnskapstransaksjonene som er koblet til transaksjoner.

En regnskapstransaksjon lagrer følgende detaljer:

- Detaljer om bilagsregistreringsprosessen (prosess, koblingsgruppe, kobling og så videre). Den lagrer også serienummeret til regnskapsenheten i **Registernummer**-feltet, hvis denne informasjonen er inkludert i regnskapssvaret.
- Statusen for bilagsregistreringen: **Fullført** for vellykket registrering, **Hoppet over** hvis operatøren merket av for **Hopp over**-alternativet for en mislykket registrering, **Merket som registrert** hvis operatøren merket av for **Merk som registrert** eller **Utsatt** hvis operatøren valgte **Utsett**-alternativet.
- Informasjonskodetransaksjoner som er knyttet til en valgt regnskapstransaksjon. Hvis du vil vise informasjonskodetransaksjonene på hurtigfanen **Finansielle transaksjoner**, velger du en regnskapstransaksjon med statusen **Hoppet over**, **Merket som registrert** eller **Utsatt** og velger deretter **Informasjonskodetransaksjoner**.

Hvis du velger **Utvidede data**, kan du også vise noen egenskaper for regnskapstransaksjonen. Listen over egenskaper som kan vises, er spesifikk for regnskapsregistreringsfunksjonaliteten som genererte regnskapstransaksjonen. Du kan for eksempel vise den digitale signaturen, det sekvensielle nummeret, identiteten til sertifikatutførelse, nummeralgoritme-ID og andre regnskapstransaksjonsegenskaper for funksjonaliteten for digital signering for Frankrike.

## <a name="fiscal-texts-for-discounts"></a>Bilagstekster for rabatter

Noen land/områder har spesielle krav til ekstra tekst som må skrives på bilagskvitteringer når det brukes ulike typer rabatter. Med funksjonen for regnskapsintegrasjon kan du definere en spesiell tekst for en rabatt som skrives etter en rabattlinje på en bilagskvittering. For manuelle rabatter kan du konfigurere en bilagstekst for informasjonskoden som er angitt som **Produktrabatt**-informasjonskoden, i funksjonsprofilen for salgssted. Hvis du vil ha mer informasjon om hvordan du konfigurerer bilagstekster for rabatter, se [Konfigurere bilagstekster for rabatter](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Skrive ut regnskap X- og regnskap Z-rapporter

Funksjonen for regnskapsintegrasjon støtter generering av dagsoppgjørsutdrag som er spesifikke for den integrerte regnskapsenheten eller -tjenesten:

- Nye knapper som utfører tilsvarende operasjoner, må legges til skjermoppsettet for salgssted. Hvis du vil ha mer informasjon, se [Konfigurere X-/Z-regnskapsrapporter fra salgsstedet](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- I regnskapsintegreringseksemplet må disse operasjonene samsvares med tilsvarende operasjoner i regnskapsenheten.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Eksempler på regnskapsintegrering i SDK for Commerce

Følgende eksempler på regnskapsintegrering er for øyeblikket tilgjengelige i SDK for Commerce:

- [Eksempel på integrering av bilagsskriver for Italia](./emea-ita-fpi-sample.md)
- [Eksempel på integrering av bilagsskriver for Polen](./emea-pol-fpi-sample.md)
- [Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Østerrike](./emea-aut-fi-sample.md)
- [Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Tsjekkia](./emea-cze-fi-sample.md)
- [Eksempel på integrering med kontrollenheter for Sverige](./emea-swe-fi-sample.md)
- [Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Tyskland](./emea-deu-fi-sample.md)
- [Eksempel på integrering av bilagsskriver for Russland](./rus-fpi-sample.md)

Følgende regnskapsintegreringsfunksjonalitet implementeres også ved hjelp av rammeverket for regnskapsintegrering, men er tilgjengelig ut av boksen og innhold som ikke er inkludert i Commerce SDK:

- [Avgiftsregistrering for Brasil](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digital signatur for Frankrike](./emea-fra-cash-registers.md)

Følgende funksjon for regnskapsintegrering er også tilgjengelig i SDK for Commerce, men drar for øyeblikket ikke nytte av regnskapsintegreringsrammeverket. Overføring av denne funksjonaliteten til rammeverket for regnskapsintegrering er planlagt i senere oppdateringer.

- [Digital signatur for Norge](./emea-nor-cash-registers.md)

Følgende eldre funksjonalitet for økonomisk integrasjon som er tilgjengelig i SDK for Commerce bruker ikke rammeverket for økonomisk integrasjon og vil bli avskrevet i senere oppdateringer:

- [Eksempel på integrering med kontrollenheter for Sverige (eldre)](./retail-sdk-control-unit-sample.md)
- [Digital signatur for Frankrike (eldre)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
