---
title: Konfigurer jobbkort for enheter
description: Dette emnet beskriver de ulike alternativene for konfigurasjon av jobbkortenheten.
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: fc698ac7e0cfc8d6b196abf35658688ad1bc8bc7
ms.sourcegitcommit: 6319a07ee6c36ebb28acaf205bc79d2fd8f7dd5d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/30/2020
ms.locfileid: "3413176"
---
# <a name="configure-job-card-for-devices"></a>Konfigurer jobbkort for enheter

[!include [banner](../includes/banner.md)]

Jobbkortenheten brukes av butikkansatte til å registrere det daglige arbeidet deres – for eksempel når de begynner på jobber – rapportere tilbakemeldinger om jobber, registrere indirekte aktiviteter og rapportere fravær. Disse registreringene er grunnlaget for sporing av fremdriften og kostnaden av produksjonsordrer, samt for beregning av grunnlaget for arbeidernes lønn. Dette emnet beskriver de ulike alternativene for konfigurasjon av jobbkortenheter.

## <a name="enable-new-features-in-feature-management"></a>Aktivere nye funksjoner i funksjonsbehandling

Noen få av innstillingene som er beskrevet i dette emnet, må være aktivert i systemet før de blir tilgjengelige for deg. Bruk [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-siden for å aktivere noen av eller alle de følgende funksjonene ved behov.

### <a name="generate-license-plate"></a>Generer nummerskilt

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. Nummerskilt for ferdigmelding lagt til i jobbkortenheten
1. Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten

### <a name="print-label"></a>Skriv ut etikett

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. Nummerskilt for ferdigmelding lagt til i jobbkortenheten
1. Skriv ut etikett fra jobbkortenhet

### <a name="allow-locking-of-touch-screen"></a>Tillate låsing av berøringsskjerm

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Forhåndsversjon) Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres.

## <a name="manage-your-device-configurations"></a>Administrere enhetskonfigurasjoner

For å konfigurere enhetskonfigurasjoner går du til **Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter**. Siden **Konfigurer jobbkort for enheter** åpnes, og viser en liste over eksisterende konfigurasjoner. Herfra kan du gjøre følgende: 

- Velg en hvilken som helst enhetskonfigurasjon som er oppført i venstre kolonne, for å vise og redigere den.
- Velg **Ny** i handlingsruten for å legge til en ny enhetskonfigurasjon i listen. Deretter angir du et navn i **Konfigurasjon**-feltet slik at du kan identifisere den nye konfigurasjonen. Verdien du angir her, må være unik blant alle enhetskonfigurasjoner, og du vil ikke kunne redigere den senere.

Se delene nedenfor for mer informasjon om hver av innstillingene for konfigurering av jobbkortenheter.

## <a name="general-settings"></a>Generelle innstillinger

I **Generelt**-hurtigkategorien kan du konfigurere hvert av de ulike alternativene som er tilgjengelige for den valgte enhetskonfigurasjonen. Følgende innstillinger er tilgjengelige:

- **Rapporter antall ved utstempling** – sett dette til **Ja** for å be arbeiderne om å rapportere tilbakemelding om jobber som pågår ved utstempling. Når **Nei** er valgt, blir ikke arbeiderne spurt om dette.
- **Lås ansatt** – Når dette alternativet er satt til **Nei**, logges hver arbeider av umiddelbart etter at de har gjort en registrering (for eksempel en ny jobb), og deretter går enheten tilbake til påloggingssiden. Når dette alternativet er satt til **Ja**, vil hver arbeider forbli logget på jobbkortenheten. Arbeideren vil likevel kunne logge seg av manuelt for å tillate at en annen arbeider logger seg på mens jobbkortenheten fortsatt kjører med samme systembrukerkonto. Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](#assigned-users).
- **Strekkodeskanner** – sett dette til **Ja** for å angi et alternativ på jobbkortenheten som lar arbeiderne registrere at en ny jobb har startet, ved å skanne en strekkode.
- **Bruk det faktiske registreringstidspunktet** – Velg **Ja** for å angi at tidspunktet for hver nye registrering skal være likt det nøyaktige tidspunktet da registreringen ble sendt av en arbeider. Angi **Nei** for å bruke påloggingstiden i stedet. Du bør normalt velge **Ja** hvis du har aktivert **Lås ansatt**- og/eller **Én arbeider**-alternativene, ettersom arbeiderne ofte er logget på i lengre perioder.
- **Én arbeider** – Velg **Ja** hvis bare én arbeider bruker hver jobbkortenhet der denne konfigurasjonen er aktiv. Når alternativet er valgt, er **Lås ansatt**-alternativet automatisk satt til **Ja**. I tillegg fjerner dette alternativet behovet (og muligheten) for at arbeideren kan logge på med en kort-ID (eller lignende). I stedet logger arbeideren seg på Supply Chain Management ved hjelp av en systembrukerkonto som er koblet til et *tidsregistrert arbeider* (fra *arbeidere*-tabellen), og blir samtidig logget på jobbkortenheten som den aktuelle arbeideren  Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](#assigned-users).
- **Tillat at arbeidere kan angi personlige filtre** – Velg **Ja** for å tillate at arbeidere kan filtrere jobbene de ser på enheten. Arbeideren kan endre verdier for ett av de tre filterkriteriene: **Produksjonsenhet**, **Ressursgruppe** og **Ressurs**. Bare jobber som er planlagt på ressurser som samsvarer med de valgte filterkriteriene, vises på enheten. Du kan også tilordne standardverdier for enkelte av eller alle disse kriteriene, og de vil gjelde selv når dette alternativet ikke er valgt.
- **Tillat låsing av berøringsskjermen** – Velg **Ja** for å tillate at arbeiderne kan låse berøringsskjermen for jobbkortenheten slik at de kan rengjøre den. Når den er aktivert, legges det til en **Lås skjerm for rengjøring** -knapp på påloggingssiden for enheten. Når en arbeider velger denne knappen, låses berøringsskjermen midlertidig for å hindre uønskede inndata, og en nedtellingstidtaker vises. Arbeideren kan nå trygt rengjøre enheten og skjermen. Når nedtellingen er fullført, låses berøringsskjermen automatisk opp igjen.
- **Varighet for skjermlås** – når alternativet **Tillat låsing av berøringsskjerm** er aktivert, bruker du dette alternativet til å angi antall sekunder berøringsskjermen skal være låst for rengjøring. Varigheten må være mellom 5 og 120 sekunder.
- **Produksjonsenhet** – Velg en produksjonsenhet som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider. Bare jobber som er planlagt på ressursgrupper under den valgte produksjonsenheten, vises i utgangspunktet av enheten. Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.
- **Ressursgruppe** – Velg en ressursgruppe som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider. Bare jobber som er planlagt på ressursgrupper under den valgte ressursgruppen, vises i utgangspunktet av enheten. Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.
- **Ressurs** – Velg en ressurs som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider. Bare jobber som er planlagt på den valgte ressursen, vises i utgangspunktet av enheten. Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.
- **Generer nummerskilt** – sett dette alternativet til **Ja** for å generere et nytt nummerskilt hver gang en arbeider bruker en jobbkortenhet for å ferdigmelde. Skiltnummeret genereres fra en nummerserie som er definert på **Parametere for lagerstyring**-siden. Når den er satt til **Nei**, må arbeiderne angi et eksisterende nummerskilt når de ferdigmelder seg.
- **Skriv ut etikett** – sett dette alternativet til **Ja** for å skrive ut en nummerskiltetikett når en arbeider bruker jobbkortenheten til å ferdigmelde. Konfigurasjonen av etiketten defineres i dokumentruting, som beskrevet i [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Tilordnede brukere

Bruk **Tilordnede brukere**-hurtigkategorien for å knytte én eller flere systembrukere til den gjeldende enhetskonfigurasjonen. Hver systembruker kan bare tilordnes én jobbenhetskonfigurasjon.

Når du konfigurerer en enhet, logger en IT-arbeider vanligvis på Supply Chain Management ved hjelp av en systembrukerkonto. Deretter gjelder jobbenhetskonfigurasjonen som er tilknyttet systembrukeren, så lenge den systembrukeren fortsatt er logget på. Disse systembrukerkontoene er vanligvis begrenset til bare å tillate tilgang til enhetssiden for jobbkort og ingen annen del av Supply Chain Management.

Når systembrukeren er logget på, og jobbenhetskonfigurasjonen er lastet inn, kan vedkommende deretter logge på jobbkortenheten ved å bruke den *tidsregistrerte arbeider*-kontoen (for eksempel ved å skanne en strekkode på kortet), slik at de kan starte nye jobber og utføre andre typer registreringer. Ulike arbeidere kan logge på og av i løpet av dagen, men den samme enhetskonfigurasjonen forblir aktivert på den aktuelle maskinen fordi systembrukeren fortsatt er logget på Supply Chain Management for dagen.

Men som nevnt tidligere, når du for eksempel bruker en enhetskonfigurasjon med alternativet **Én arbeider**, logger arbeiderne seg vanligvis på Supply Chain Management ved hjelp av en systembruker som er koblet til deres egen *tidsregistrert arbeider*-konto, slik at de laster inn enhetskonfigurasjonen og logger på som en arbeider på jobbkortenheten samtidig.

## <a name="additional-resources"></a>Tilleggsressurser

[Ferdigmeld fra den jobbkortenheten.](report-finished-job-device.md)
