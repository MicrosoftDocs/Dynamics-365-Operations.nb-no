---
title: Forseglede bud for tilbudsforespørsler
description: Dette emnet beskriver hvordan du konfigurerer forseglet budgivning for å holde svarene på leverandørbudene forseglet til de ikke er forseglet av innkjøpspersonale.
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578086"
---
# <a name="sealed-bidding-for-rfqs"></a>Forseglede bud for tilbudsforespørsler

[!include [banner](../includes/banner.md)]

Forseglet budgivning holder svar på leverandørbudene forseglet til de ikke er forseglet av innkjøpspersonale. Alle tilbud som er relatert til en tilbudsforespørsel, er først tilgjengelige for oppheving når budet utløper. Før forseglingen for et bud oppheves, vil bare brukere som har dedikerte brukerroller og som representerer leverandøren, få tilgang til det.

> [!IMPORTANT]
> Ved endring eller utvidelse av skjemaer, eller oppretting av nye skjemaer eller forretningslogikk, kan det oppstå forseglet budgivning fra Microsoft. Du bærer risikoen ved å bruke endringer, utvidelser, nye skjemaer eller forretningslogikk, eller manglende evne til å bruke den forseglede budgivningsfunksjonen på grunn av slike endringer, utvidelser, nye skjemaer eller forretningslogikk.  Microsoft er ikke ansvarlig for eventuell skade som følge av endringer eller utvidelser i skjemaer, eller nye skjemaer eller forretningslogikk som du oppretter eller tredjepart oppretter for deg. Microsoft gir ikke teknisk eller annen støtte for endringer, utvidelser, nye skjemaer eller forretningslogikk som gjøres av deg eller tredjepart på dine vegne. Du er eneansvarlig for å overholde alle gjeldende lover eller bestemmelser som gjelder forseglet bud.

## <a name="how-bids-are-kept-secure"></a>Hvordan bud holdes sikre

Forseglet budgivning bruker asymmetrisk kryptering til å kryptere budkrypteringsnøkkelen (KEK) og symmetrisk kryptering for å kryptere det faktiske budet. Systemet integreres med Microsoft Azure Key Vault for å generere og administrere krypteringsnøklene som brukes til å kryptere forseglet tilbud. Hvert bud har sin egen krypteringsnøkkel. Denne krypteringen holdes sikkert i et nøkkelhvelv som eies av organisasjonen som kjører Dynamics 365 Supply Chain Management. Systemet får tilgang til nøkkelen ved behov, hver gang kryptering og dekryptering kreves.

## <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Denne delen beskriver forutsetningene som må være på plass før du kan sende ut tilbud som krever forseglet bud.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Trinn 1: Angi brukertilgang til forseglet budgivning

Når du bruker forseglet budgivning, kan bare brukere som er angitt som kontaktperson for en leverandør, vise, redigere og sende inn bud for denne leverandøren til budperioden er utløpt. Disse brukerne må ha rollen **Leverandør (ekstern)**, og de må angis som kontaktperson for leverandørkontoen. Kontaktpersonen må også ha tillatelse til å samarbeide med leverandøren, som beskrevet i [Oppsett og vedlikehold av leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).

Siden brukere som har de nødvendige tillatelsene, og som er definert som leverandørkontakter, kan få tilgang til de forseglede tilbudene for en leverandør, er det viktig å spore hvem disse brukerne er. Systemadministratoren som definerer brukere og sikkerhetsroller, er ansvarlig for å begrense tilgang til forseglet tilbud til de brukerne som virkelig har tillatelse til å vise dem.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Trinn 2: Aktiver funksjonen for forseglet budgivning

Før du starter å definere eller bruke denne funksjonen må du kontrollere at den er tilgjengelig i systemet. Administratorer kan bruke arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** til å kontrollere statusen for funksjonen og aktivere den om nødvendig. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Innkjøp og leverandører*
- **Funksjonsnavn:** *Forseglet bud på tilbudsforespørsel*

### <a name="step-3-set-up-azure-key-vault"></a>Trinn 3: Konfigurer Azure Key Vault

Supply Chain Management bruker krypteringsnøkler til å beskytte alle forseglede bud, og holde dem sammen til riktig tid. Det benytter seg av funksjonene i Key Vault til å generere og behandle de nødvendige nøklene. Derfor må du sette opp en tilkobling fra Supply Chain Management til et nøkkelhvelv for å aktivere systemet.

> [!IMPORTANT]
> Nøkkelhvelvene du bruker til forseglet budgivning, må oppfylle følgende krav:
>
> - Hvis du bruker en sandkasse til utvikling og testing, må du ha et dedikert nøkkelhvelv for sandkassen og en separat nøkkel for produksjon.
> - Hvert nøkkelhvelv må opprettes i et Azure-abonnement som eies av organisasjonen (ikke abonnementet der du kjører Supply Chain Management).
> - Hvert nøkkelhvelv må brukes utelukkende for forseglet budgivning. Du må ikke bruke nøkkelhvelv for forseglet budgivning til noe annet formål.

Hvert bud henter sin egen hurtigtast. Denne nøkkelen brukes hver gang en bruker viser, oppdaterer eller opphever budet.

Key Hvelv genererer nøkkelen som brukes til å hente meldingen når leverandøren velger **Bud** i grensesnittet for leverandørsamarbeid. Nøkkelen utløper deretter etter et fast tidspunkt som innkjøpssjefen setter opp på siden **Parametere for innkjøp og leverandører** i Supply Chain Management. Når nøkkelen er utløpt, kan du vise, redigere eller fjerne budet. Det er derfor viktig å konfigurere utløp av nøkkel slik at det er nok tid til at budprosessen kan fullføres.

I de neste tre trinnene konfigurerer du tilkoblingen til Key Vault. Først definerer du et nøkkelhvelv som skal brukes med forseglet bud. Deretter konfigurerer du Supply Chain Management til å kommunisere med nøkkelhvelvet. Til slutt angir du utløpstid for nøkkelen.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Trinn 4: Definer et nøkkelhvelv som skal brukes med forseglet bud

Gjør følgende for å konfigurere nøkkelhvelvet. Rekkefølgen på trinnene er svært viktig.

1. Hvis du ikke allerede har konfigurert et Azure-abonnement fra abonnementet som er separat fra abonnementet der du kjører Supply Chain Management, konfigurerer du det.
1. Definer et nøkkelhvelv i separat Azure-lagring. Hvis du vil ha mer informasjon, se [Vedlikeholde Azure Key Vault-lagring](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Konfigurer Supply Chain Management-appen for å fungere som en klient for nøkkelhvelvet. Hvis du vil ha mer informasjon, se [Konfigurere Azure Key Vault-klient](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Trinn 5: Konfigurer Key Vault-parametere i Supply Chain Management

Følg denne fremgangsmåten for å konfigurere Supply Chain Management til å kommunisere med nøkkelhvelvet under forseglet budgivning.

1. Logg deg på Supply Chain Management, og gå til **Systemadministrasjon \> Oppsett \> Key Vault-parametere**.
1. Velg **Ny** for å opprette en post, og angi følgende felter for den:

    - **Navn** – Angi et navn.
    - **Beskrivelse** – Angi en beskrivelse.
    - **Nettadresse for Key Vault** – Angi standard nettadresse for nøkkelhvelvet.
    - **Key Vault-klient** – Angi den interaktive klient-ID-en til Active Directory-programmet som er tilknyttet et nøkkelhvelv for godkjenning.
    - **Key Vault-hemmelighetsnøkkel** – Angi referansen til referansen til sertifikatet.
    - **Aktivert for forseglet budgivning** – Sett dette alternativet til *Ja*.

![Siden Key Vault-parametere](media/sealed-bidding-key-vault-param.png "Siden Key Vault-parametere")

> [!NOTE]
> Du kan bare aktivere én tastehvelvkonfigurasjon for forseglet budgivning om gangen. Før du deaktiverer en eksisterende nøkkelhvelvkonfigurasjon, må du kontrollere at alle forseglede tilbud som bruker den, ikke er forseglet. Inspiser alle tilfeller for tilbudsforespørseler av typen *Forseglet*, og kontroller at alle svar for den ikke er forseglet.

### <a name="step-6-set-the-key-expiration-time"></a>Trinn 6: Angi utløpstiden for nøkkelen

Følg denne fremgangsmåten for å angi utløpstiden som gjelder nøkkelen som genereres for hvert nytt bud.

1. Gå til **Parametere for innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.
1. Angi antall dager som tilbudsforespørselsperioden skal vare i feltet **Dagers forskyvning** i fanen **Tilbudsforespørsel**. Når en tilbudsforespørsel opprettes, legges antall dager du angir her til systemdatoen for å definere standard utløpsdato for tilbudsforespørselen.
1. I feltet **Forskyving av utløpsdato for krypteringsnøkkel** angir du hvor mange dager hver krypteringsnøkkel skal være gyldig etter at den er utstedt. Når krypteringsnøkkelen er utløpt, kan du vise, redigere eller fjerne det forseglede budet som bruker det.

> [!TIP]
> Verdien til feltet **Forskyving av utløpsdato for krypteringsnøkkel** skal ikke være mindre enn verdien til **Dagers forskyvning**-feltet.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Trinn 7: Angi standard budtype

Hver tilbudsforespørselssak har en budtype. Budtypen definerer om tilbudsforespørselssaken gir åpen eller forseglet bud.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Tilbudsforespørselssaker som ikke har en forespørselstype

Følg denne fremgangsmåten for å angi standard budtype som ikke er tilordnet til nye tilbudsforespørsler som ikke er tilordnet en forespørselstype når de opprettes.

1. Gå til **Parametere for innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.
1. Sett **Budtype**-feltet til **Forseglet** i kategorien *Tilbudsforespørsel*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Tilbudsforespørselssaker som har en forespørselstype

Følg denne fremgangsmåten for å angi standard budtype som er tilordnet til nye tilbudsforespørsler som ikke er tilordnet en forespørselstype når de opprettes.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Tilbudsforespørsel \> Forespørselstype**.
1. Opprett en ny forespørselstype, eller velg en eksisterende forespørselstype der du vil bruke budtypen *Forseglet*.
1. Sett **Budtype**-feltet til *Forseglet*.
1. Gjenta denne fremgangsmåten for hver ekstra forespørselstype der du vil implementere forseglet bud.

> [!TIP]
> En forespørselstype behøver ikke å tilordnes når en ny tilbudsforespørsel opprettes. Hvis det er tilordnet en forespørselstype, kan standard budtype for en tilbudsforespørsel hente den. Ellers kan standard forespørselstype som er definert i Parametere for innkjøp og leverandører, brukes.

## <a name="the-sealed-bidding-process"></a>Den forseglede budgivningsprosessen

Forseglet budgivning følger nesten samme prosess som er beskrevet i [oversikten for tilbudsforespørsler](request-quotations.md). Den viktigste forskjellen er at buddataene og vedleggene beholdes krypteres til forseglingen for budet er opphevet.

> [!IMPORTANT]
> [Spørreskjemaer](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) er ikke kryptert og bør ikke brukes til å samle inn sensitiv informasjon

Her er en oversikt over prosessen:

1. Du oppretter og sender en tilbudsforespørsel til én eller flere leverandører.
1. Leverandører svarer ved å sende inn forseglet tilbud.
1. Du opphever budene etter utløpstiden for budoppføringen.
1. Budene blir synlige, og du kan evaluere og sammenligne dem.
1. Når et bud er godkjent, genererer du en bestilling, genererer en innkjøpsavtale eller oppdaterer en innkjøpsrekvisisjon.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Opprett en tilbudsforespørselssak som bruker forseglet bud

Prosessen med å opprette en tilbudsforespørselssak for forseglet bud er nesten den samme som prosessen for ikke-forseglet bud. Hvis du vil ha informasjon om hvordan du oppretter begge typene tilbudsforespørselssaker, kan du se [Opprett en tilbudsforespørsel](tasks/create-request-quotation.md). Denne delen fremhever et par viktige hensyn når du oppretter en tilbudsforespørsel om forseglet budgivning.

Tilbudsforespørselssaker for forseglet bud må ha **budtypeverdien** *Forseglet*. Det er tre måter å tilordne denne verdien til en tilbudsforespørselssak på:

- Angi verdien direkte i tilbudsforespørselen etter at du har opprettet den.
- Definer forseglet bud som standard budtype for alle tilbudsforespørsler i innkjøps- og leverandørparametere. (Se delen [Angi standard budtype](#set-default-bid-type) tidligere i dette emnet.)
- Når du oppretter en ny tilbudsforespørselssak, velger du en forespørselstype som er definert for forseglet bud. (Se delen [Angi standard budtype](#set-default-bid-type).)

For forseglet bud fastsetter tilbudsforespørselssakens **Utløpsdato og klokkeslett**-verdi når forseglingen på de sendte tilbudene kan oppheves. Verdien for **utløpsdato og tidspunkt** på hver linje vil samsvare med verdien i hodet.

Du kan ikke endre budstypen etter at en tilbudsforespørselssak er sendt.

### <a name="vendors-respond-to-an-rfq"></a>Leverandører svarer på en tilbudsforespørsel

Leverandører som svarer på et forseglet tilbud, bruker samme fremgangsmåte som de bruker til å svare på åpne tilbud, som beskrevet i [Arbeid med tilbud i arbeidsområdet for leverandørbud](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Hvis du vil ha detaljerte instruksjoner om hvordan du arbeider med både åpne bud og forseglede bud, kan du se [Angi og sammenligne tilbudsforespørselsbud og bonuskontrakter](tasks/enter-compare-rfq-bids-award-contracts.md). Den eneste forskjellen mellom behandling av forseglet tilbud og behandling av åpne bud, er at så lenge budperioden er utløpt, kan ikke innkjøpspersonalet åpne et forseglet tilbud fra en leverandør. Bare en kontaktperson for leverandøren kan åpne denne leverandørens forseglet tilbud.

> [!IMPORTANT]
> For forseglet budgivning kan leverandører bare laste opp vedlegg i PDF-format. Ingen andre formater blir godtatt.

Når en registrert leverandørbruker velger **Bud** på en forseglet tilbudsforespørsel, kan de legge inn buddataene, og dataene blir sikret. Leverandører kan lagre arbeidet sitt mens de forbereder et bud, komme tilbake til det så ofte som nødvendig og deretter sende det når det er klart. Leverandører kan også se budet sitt etter at de har sendt det. Hvis leverandørene må endre budet etter at de har sendt det, kan de tilbakekalle det, oppdatere det og sende det på nytt når som helst til budsperioden er utløpt.

Følgende betingelser gjelder under forseglet budgivning:

- Under forseglet budgivning oppretter systemet en journal for *tilbudsforespørsel*.
- Når en leverandør sender et bud, opprettes det en journal for tilbudsforespørsel uten linjer, som har en forseglet pris.
- Når forseglingen for saken oppheves, opprettes det en journal for tilbudsforespørsel som har en pris og et beløp. Du kan få tilgang til denne journalen ved å velge **Journaler for tilbudsforespørsel** på siden **Alle tilbudsforespørsler**.
- Systemet lagrer en logg over hver handling som brukere utfører på et forseglet bud. Disse handlingene omfatter visning, redigering og lagring av budet. Denne loggen er synlig både for leverandøren og for innkjøpspersonalet som har tilgang til budet.
- Etter hvert som budet forløper, kan innkjøpspersonalet vise statusen. Statusen er enten *Leverandør oppdaterer* eller *Rapportert av leverandør*.
- Statusen til linjene i et forseglet bud forblir S *endt* til budet ikke er forseglet.
- Hvis leverandøren velger å avvise et bud, vil budet ha statusen **Svarfremgang** for *Avslått av leverandør*. Denne statusen vil være synlig for innkjøpspersonalet.
- Svar i spørreskjemaer lagres **ikke** i kryptert skjema i databasen. Derfor er de ikke forseglet. De vil imidlertid ikke være synlige i brukergrensesnittet for tilbudsforespørsel før forseglingen for saken er opphevet.

### <a name="all-sealed-bid-activities-are-logged"></a>Alle forseglede budaktiviteter logges

En detaljert logg registrerer alle brukeraktiviteter og handlinger for et bud. Ved hjelp av aktivitetsloggen kan organisasjoner bestemme hvem som oppdaterte et bud i løpet av levetiden, og hvilke oppdateringer som var. Organisasjoner kan også bekrefte at bare autoriserte personer fikk tilgang til et forseglet tilbud. Aktivitetsloggen er tilgjengelig på **aktivitetssiden** for hvert bud.

### <a name="review-rfq-activity"></a>Gå gjennom tilbudsforespørselsaktivitet

All samhandling med budet blir logget og kan vises på **aktivitetssiden**. Illustrasjonen nedenfor viser et eksempel.

![Eksempel på aktivitetssiden](media/sealed-bidding-rfq-activity.png "Eksempel på aktivitetssiden")

Leverandører kan få tilgang til **aktivitetssiden** ved å velge **Aktivitet** på siden **Forseglet bud for tilbudsforespørsel**. Innkjøpspersonalet kan få tilgang til det ved å velge **Aktivitet** på siden **Tilbudsforespørsel**. Aktivitetsloggen gir full oversikt over leverandører og for innkjøpspersonalet som har tilgang til budet. Derfor kan det avsløre enhver uautorisert tilgang.

### <a name="unseal-sealed-bids"></a>Opphev forseglet bud

Når verdien for **utløpsdatoen og klokkeslett** som ble konfigurert for en forseglet bud-tilbudsforespørselssak har passert, blir **Opphev forsegling**-knappen tilgjengelig. Velg **Opphev forsegling** for å oppheve forseglingen for alle budene for den valgte tilbudsforespørselssaken. Deretter blir alle buddataene og vedleggene synlige, slik at svarene på saken kan behandles. I tillegg opprettes det journaler som inneholder de sendte buddataene.

Hendelsen for oppheving av forsegling blir logget og kan vises på **aktivitetssiden**.

### <a name="process-accepted-bids"></a>Behandle godkjente bud

Prosessen med å sammenligne og godkjenne tidligere forseglede bud er den samme som prosessen for åpne bud. Hvis du vil ha informasjon om hvordan du gir poeng, sammenligner, avviser og godtar ikke-forseglede bud, kan du se [Angi og sammenligne tilbudsforespørselsbud og bonuskontrakter](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Aktivitetsloggen for tilbudsforespørsel kan aldri slettes

Ingen, ikke engang administratorer og Microsoft Kundestøtte, kan redigere eller slette aktivitetsloggen for tilbudsforespørselen. Denne begrensningen bidrar til å sikre hvor den forseglede budprosessen er. Det sikrer også at det opprettholdes et nøyaktig revisjonsspor.
