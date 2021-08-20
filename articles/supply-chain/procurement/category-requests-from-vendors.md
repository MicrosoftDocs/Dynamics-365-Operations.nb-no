---
title: Kategoriforespørsler fra leverandører
description: Dette emnet beskriver hvordan leverandører kan be om innkjøpskategorier for kontoen. Det beskriver også godkjenningsprosessen som er fullført av innkjøpsagenter.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f73e163084ec2870d01cc063c63246a4480fd3a056d04617771b955477325671
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782497"
---
# <a name="category-requests-from-vendors"></a>Kategoriforespørsler fra leverandører

[!include [banner](../includes/banner.md)]

Ved hjelp av kategoriforespørselsprosessen kan leverandører be om at nye innkjøpskategorier blir tilknyttet kontoen. Disse innkjøpskategoriene kan deretter brukes av de relaterte innkjøps- og leverandørprosessene. (Hvis du vil ha mer informasjon, kan du se [Oversikt over innkjøpskataloger](procurement-catalogs.md).)

Kategoriforespørsler startes av leverandører i arbeidsområdet **Leverandøropplysninger**. De sendes deretter til byrået for gjennomgang og godkjenning. Godkjente kategorier legges til i listen over innkjøpskategorier for leverandørens konto.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funksjonen i systemet

Hvis systemet ikke allerede inneholder funksjonen som er beskrevet i dette emnet, kan du gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Tillat leverandører å søke etter innkjøpskategorier gjennom leverandørsamarbeidsfunksjonen*.

Når funksjonen er aktivert, kan du fremdeles legge til innkjøpskategorier manuelt i leverandørkontoer. Hvis du vil ha mer informasjon, kan du se [Godkjenne leverandører for spesifikke innkjøpskategorier](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Krav til leverandørsamarbeid

Før en leverandør kan samhandle med kategoriforespørsler, må det konfigureres for leverandørsamarbeid.

Leverandøren må ha minst én bruker for leverandørsamarbeid. Bare leverandørbrukere med sikkerhetsrollen *Leverandøradministrasjon (ekstern)* kan opprette og sende kategoriforespørsler.

Hvis du vil ha mer informasjon, se [Definere og vedlikeholde leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Definere arbeidsflyten for leverandørkategoriforespørsel

Arbeidsflyten for *Leverandørkategoriforespørsel* må defineres i innkjøps- og leverandørarbeidsflytene. Leverandører sender nye kategoriforespørsler som du kan se gjennom og godkjenne. Forespurte innkjøpskategorier legges til i en leverandørkonto etter at en kategoriforespørsel er godkjent.

Følgende eksempel viser hvordan du konfigurerer en enkel arbeidsflyt for *Leverandørkategoriforespørsel* som har én enkelt godkjenner. Du må gå gjennom de interne prosessene for å finne riktig arbeidsflytoppsett for byrået.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Arbeidsflyter for innkjøp og leverandører**.
1. Velg **Ny** i handlingsruten.
1. I dialogboksen velger du **arbeidsflyten for leverandørkategoriforespørsel** for å åpne arbeidsflytredigeringsprogrammet.
1. Logg deg på arbeidsflytredigeringsprogrammet.
1. I handlingsruten velger du **Egenskaper**.
1. Angi instruksjonstekst i feltet **Sendeinstruksjoner** på **Egenskaper**-siden for arbeidsflyten. Instruksjonene blir synlige for leverandører når de sender en kategoriforespørsel.
1. Lukk **Egenskaper**-siden.
1. Dra arbeidsflytelementet **Godkjenn ny kategoriforespørsel** til lerretet.
1. Dra en kobling fra arbeidsflytelementet **Start** til arbeidsflytelementet **Godkjenn ny kategoriforespørsel**.
1. Dra en kobling fra arbeidsflytelementet **Godkjenn ny kategoriforespørsel** til arbeidsflytelementet **Slutt**.
1. Dobbelttapp (eller dobbeltklikk) arbeidsflytelementet **Godkjenn ny kategoriforespørsel**.
1. Velg og hold nede (eller høyreklikk) arbeidsflytelementet **Trinn 1**, og velg deretter **Egenskaper**.
1. Angi emnetekst i feltet **Emne for arbeidselement** på **Egenskaper**-siden for arbeidsflytelementet. Denne teksten vises som verdien i feltet **Emne** på siden **Arbeidselementer som er tilordnet til meg**.
1. I **Instruksjoner for arbeidselement**-feltet angir du instruksjonsteksten. Instruksjonene vises for godkjennere når de velger **Arbeidsflyt** i handlingsruten for en kategoriforespørsel.
1. I den venstre ruten velger du **Tilordning**.
1. I kategorien **Tilordningstype** angir du **Tilordne brukere til dette arbeidsflytelementet** til *Bruker*.
1. Velg en godkjenner i listen **Tilgjengelige brukere** i kategorien **Bruker**. Velg for eksempel en bruker i innkjøpsavdelingen.
1. Velg Pil høyre-knappen (**\>**) for å flytte godkjenneren til listen **Valgte brukere**.
1. Lukk **Egenskaper**-siden.
1. Velg **Lagre og lukk**.
1. Skriv inn merknader om arbeidsflyten i feltet **Versjonsmerknader**.
1. Velg **OK** for å lagre arbeidsflyten.
1. Hvis du er klar til å starte å teste arbeidsflyten, velger du **Aktiver den nye versjonen**. Hvis ikke velger du **Ikke aktiver den nye versjonen**.
1. Velg **OK** for å fullføre ny arbeidsflytoppsettet.

> [!TIP]
> Hvis byrået ikke krever godkjenning av kategoriforespørsler, bør du konfigurere arbeidsflyten for automatisk godkjenning.

Hvis du vil ha mer informasjon om konfigurasjon av arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Opprette og sende en kategoriforespørsel

Denne delen beskriver hvordan leverandører kan bruke arbeidsområdet for **Leverandøropplysninger** til å opprette, redigere, vise og sende kategoriforespørsler.

### <a name="start-a-new-request"></a>Starte en ny forespørsel

Følg denne fremgangsmåten for å starte en ny kategoriforespørsel.

1. Velg flisen for **Kategoriforespørsler** i arbeidsområdet for **Leverandøropplysninger**.
1. Velg **Ny kategoriforespørsel** i handlingsruten på **Kategoriforespørsler**-siden.
1. I dialogboksen **Ny kategoriforespørsel** finner du kategorien du vil søke etter, ved å navigere i treet og/eller ved hjelp av filteret øverst i listen. Merk av for hver relevante kategori.

    Merk følgende punkt:

    - Kategorier som for øyeblikket er aktive på leverandørkontoen din, vises som valgte og kan ikke fjernes.
    - Du kan be om flere innkjøpskategorier i én enkelt kategoriforespørsel.

1. Velg **OK** for å opprette utkastforespørselen.

    Den nye utkastforespørselen vises nå på **Kategoriforespørsler**-siden.

1. Åpne den nye utkastforespørselen for å gjennomgå og redigere den etter behov.

    - Hvis du vil vise en liste over kategorier som for øyeblikket er inkludert i forespørselen, velger du hurtigkategoriene **Forespurte kategorier**.
    - Hvis du vil vise de aktive kategoriene, åpner du **Aktive kategorier**-faktaboksen til høyre på siden.
    - Hvis du vil legge til en kategori i forespørselen, velger du **Legg til** på verktøylinjen i hurtigkategorien **Forespurte kategorier**.
    - Hvis du vil fjerne en kategori fra forespørselen, velger du kategorien i hurtigkategorien **Forespurte kategorier**, og deretter velger du **Fjern** på verktøylinjen.
    - Hvis du vil legge ved et dokument i forespørselen, velger du **Vedlegg** i handlingsruten. Tilknyttede dokumenter vil være tilgjengelige for godkjennere når de går gjennom kategoriforespørselen.
    - Hvis du vil fjerne et vedlagt dokument fra forespørselen, velger du **Vedlegg** i handlingsruten. Velg dokumentet du vil fjerne, og velg deretter **Slett** i handlingsruten.

1. Hvis du er klar til å sende forespørselen, velger du **Send** i handlingsruten. Ellers kan du bare lukke siden og hoppe over de gjenværende trinnene i denne fremgangsmåten. Du kan deretter gå tilbake til forespørselen senere.
1. Les eventuelle innsendingsinstruksjoner som vises, og velg deretter **Send**.
1. I boksen **Kommentar** angir du eventuell tilleggsinformasjon som kreves. Velg deretter **Send** for å fullføre forespørselen.

### <a name="edit-a-draft-or-recalled-request"></a>Redigere en kladd eller en tilbakekalt forespørsel

Følg denne fremgangsmåten for å redigere et kladd eller en tilbakekalt kategoriforespørsel.

1. Velg flisen for **Kategoriforespørsler** i arbeidsområdet for **Leverandøropplysninger**.
1. Velg utkastet eller den tilbakekalte forespørselen for å åpne den.
1. Rediger forespørselen etter behov, og lukk den deretter eller send den som beskrevet i forrige fremgangsmåte.

### <a name="submit-a-draft-or-recalled-request"></a>Sende en kladd eller en tilbakekalt forespørsel

Følg denne fremgangsmåten for å sende et kladd eller en tilbakekalt kategoriforespørsel.

1. Velg flisen for **Kategoriforespørsler** i arbeidsområdet for **Leverandøropplysninger**.
1. Velg utkastet eller den tilbakekalte forespørselen du vil sende.
1. I handlingsruten velger du **Send**.
1. Les eventuelle innsendingsinstruksjoner som vises, og velg deretter **Send**.
1. I boksen **Kommentar** angir du eventuell tilleggsinformasjon som kreves. Velg deretter **Send** for å fullføre forespørselen.

    Statusen til kategoriforespørselen endres til en av følgende verdier:

    - _Venter på gjennomgang_ – Forespørselen er i arbeidsflyten.
    - _Venter på godkjenning_ – Godkjenning er nødvendig.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Tilbakekalle en sendt forespørsel som ennå ikke er godkjent

Følg denne fremgangsmåten for å tilbakekalle en kategoriforespørsel som er sendt, men som ennå ikke er godkjent.

1. Velg flisen for **Kategoriforespørsler** i arbeidsområdet for **Leverandøropplysninger**.
1. Velg den ventende forespørselen du vil tilbakekalle.
1. I handlingsruten velger du **Tilbakekall**.
1. I boksen **Angi en kommentar** angir du eventuell tilleggsinformasjon som kreves. Velg deretter **Send** for å fullføre forespørselen.

    Statusen for kategoriforespørselen endres til _Annullert_. Forespørselen vil fortsatt ha denne statusen til du sletter eller sender den på nytt.

### <a name="delete-a-draft-or-recalled-request"></a>Slette en kladd eller en tilbakekalt forespørsel

Følg denne fremgangsmåten for å slette et kladd eller en tilbakekalt kategoriforespørsel.

1. Velg flisen for **Kategoriforespørsler** i arbeidsområdet for **Leverandøropplysninger**.
1. Velg utkastet eller den tilbakekalte forespørselen du vil slette.
1. Velg deretter **Slett** i handlingsruten.
1. Velg **Ja** for å bekrefte slettingen.

### <a name="view-completed-requests"></a>Vise fullførte forespørsler

Hvis du vil vise fullførte forespørsler, åpner du arbeidsområdet **Leverandøropplysninger** og velger fanen **Kategoriforespørsler**. Kategoriforespørsler som er fullført, vil ha en av følgende statuser:

- _Godkjent_ –Forespørselen er godkjent. Hvis du vil vise kategoriene som nylig er lagt til, kan du gå tilbake til arbeidsområdet for **Leverandørinformasjon**, åpne rullegardinlisten **Flere detaljer** i venstre rute og deretter velge **Kategorier**.
- _Avvist_ – Forespørselen ble avvist. Du kan opprette en ny kategoriforespørsel etter behov.

## <a name="review-category-requests"></a>Gå gjennom kategoriforespørsler

Denne delen beskriver hvordan du godkjenner, avviser og delegerer kategoriforespørsler som leverandører har sendt, og hvordan du viser fullførte forespørsler. Disse arbeidsflythandlingene er for hele kategoriforespørselen.

### <a name="view-category-requests"></a>Vise kategoriforespørsler

Følg denne fremgangsmåten for å vise kategoriforespørsler.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Leverandørsamarbeidsforespørsler \> Kategoriforespørsler**.

    Siden **Kategoriforespørsler** vises. Standardsidevisningen viser kategoriforespørsler som har statusen *Ventende handling*.

1. Hvis du vil vise alle forespørslene, velger du *Alle* i **Vis forespørsler**-feltet.
1. Åpne en forespørsel for å gå gjennom og redigere den etter behov.

    - Hvis du vil vise en liste over kategorier som for øyeblikket er inkludert i forespørselen, velger du hurtigkategoriene **Forespurte kategorier**.
    - Hvis du vil vise de aktive kategoriene, åpner du **Aktive kategorier**-faktaboksen til høyre på siden.
    - Hvis dokumenter er sendt, viser knappen **Vedlegg** (papirklipp) i handlingsruten et antall for tilknyttede dokumenter. Hvis du vil vise tilknyttede dokumenter, velger du **Vedlegg**-knappen. Deretter velger du dokumentet du vil vise, og velger **Åpne** for å vise det.
    - Hvis du vil legge ved et dokument i forespørselen, velger du **Vedlegg** i handlingsruten. Tilknyttede dokumenter vil være tilgjengelige for godkjennere når de går gjennom kategoriforespørselen.
    - Hvis du vil fjerne et vedlagt dokument fra forespørselen, velger du **Vedlegg** i handlingsruten. Velg dokumentet du vil fjerne, og velg deretter **Slett** i handlingsruten.
    - Hvis du vil vise arbeidsflytloggen, velger du **Arbeidsflyt** i handlingsruten. I arbeidsflytalternativene velger du **Mer** og deretter **Arbeidsflytlogg**. Siden **Arbeidslogg** vises.

### <a name="approve-a-pending-category-request"></a>Godkjenne en ventende kategoriforespørsel

Følg denne fremgangsmåten for å godkjenne en ventende kategoriforespørsel.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Leverandørsamarbeidsforespørsler \> Kategoriforespørsler**.
1. Velg den ventende forespørselen om å godkjenne.
1. Gå gjennom kategoriforespørslene.
1. Valgfritt: Velg en årsakskode i feltet **Årsakskode** i hurtigfanen **Generelt**. Skriv deretter inn en kommentar til årsakskoden i **Årsakskommentar**.
1. Velg **Arbeidsflyt** i handlingsruten.
1. Velg **Godkjenn** i arbeidsflytalternativene.
1. I feltet **Kommentar** angir du eventuell tilleggsinformasjon som kreves. Velg deretter **Godkjenn** for å fullføre forespørselen.

    Statusen til kategoriforespørselen endres til _Godkjent_, og innkjøpskategoriene legges til i leverandørkontoen.

### <a name="reject-a-pending-category-request"></a>Avvise en ventende kategoriforespørsel

Følg denne fremgangsmåten for å avvise en ventende kategoriforespørsel.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Leverandørsamarbeidsforespørsler \> Kategoriforespørsler**.
1. Velg den ventende forespørselen om å avvise.
1. Gå gjennom kategoriforespørslene.
1. I handlingsruten velger du **Rediger**.
1. Velg en årsakskode i feltet **Årsakskode** i hurtigfanen **Generelt**. Skriv deretter inn en kommentar til årsakskoden i **Årsakskommentar**.
1. Velg **Lagre** i handlingsruten.
1. Velg **Arbeidsflyt** i handlingsruten.
1. I arbeidsflytalternativene velger du **Mer** og deretter **Avvis**.
1. I feltet **Kommentar** angir du eventuell tilleggsinformasjon som kreves. Velg deretter **Avvis** for å fullføre forespørselen.

    Statusen for kategoriforespørselen endres til _Avvist_. På dette tidspunktet kan leverandøren opprette en ny kategoriforespørsel etter behov.

### <a name="delegate-a-pending-category-request"></a>Delegere en ventende kategoriforespørsel

Følg denne fremgangsmåten for å delegere en ventende kategoriforespørsel til en annen bruker.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Leverandørsamarbeidsforespørsler \> Kategoriforespørsler**.
1. Velg den ventende forespørselen du vil godkjenne.
1. Velg **Arbeidsflyt** i handlingsruten.
1. I arbeidsflytalternativene velger du **Mer** og deretter **Deleger**.
1. I **Bruker**-feltet velger du brukeren du vil tilordne kategoriforespørselen for gjennomgang.
1. I feltet **Kommentar** angir du eventuell tilleggsinformasjon som kreves.
1. Velg **Deleger** for å fullføre ny delegering. Den valgte brukeren kan nå se gjennom kategoriforespørselen.

### <a name="view-procurement-categories-for-a-vendor"></a>Vise innkjøpskategorier for en leverandør

For å vise innkjøpskategorier for en leverandør etter at en kategoriforespørsel er godkjent, følger du disse trinnene.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**.
1. På siden **Alle leverandører** velger du leverandøren du vil vise innkjøpskategorier for.
1. Åpne fanen **Generelt** i handlingsruten, og gå til **Oppsett**-gruppen og velg **Kategorier**.

    Siden **Kategorier** vises. Hurtigkategori **Innkjøp** viser innkjøpskategorier som ble lagt til via kategoriforespørselen.

1. I hurtigkategorien **Innkjøp** kan du gjøre endringer om nødvendig. Du kan for eksempel sette **Status for leverandørkategori** til _Foretrukket_.
