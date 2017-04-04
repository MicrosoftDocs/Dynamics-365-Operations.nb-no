---
title: "Gode fremgangsmåter for å importere bilagene ved hjelp av den generelle journal-enheten"
description: "Dette emnet inneholder tips for å importere data inn i den generelle journalen ved hjelp av Generelt journalen enhet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Gode fremgangsmåter for å importere bilagene ved hjelp av den generelle journal-enheten

Dette emnet inneholder tips for å importere data inn i den generelle journalen ved hjelp av Generelt journalen enhet.  

Du kan bruke den generelle journal-enheten til å importere bilag som har en konto eller motkonto-kontotype **finans, kunde, leverandør eller Bank**. Bilaget kan angis som én linje, ved hjelp av både **konto** feltet og **motkonto** felt, eller som en flerlinjet bilag, der bare den **konto** feltet brukes (og **motkonto** er tom på hver linje). Finanskladd-enheten støtter ikke hver kontotype. Andre enheter finnes i stedet for scenarier der det kreves ulike kombinasjoner av kontotyper. Hvis du vil importere en project-transaksjon, kan du for eksempel bruke Project utgifter journal enhet. Hver enhet er utformet for å støtte bestemte scenarier, noe som betyr flere felt kan være tilgjengelige i enheter for scenarier, men ikke i enheter for et annet scenario.

## <a name="setup"></a>Konfigurer
Før du importerer ved hjelp av den generelle journal-enheten, må du kontrollere følgende oppsett:

-   **Nummerserieoppsettet for partinummeret journal** - som standard, når du importerer ved hjelp av finanskladd-enhet, journal satsvise nummeret bruker nummerserien som er definert i Økonomiparametere. Hvis du har satt nummerserien for journalpartinummeret til **Manuelt**, brukes ikke et standardnummer. Dette oppsettet støttes ikke.
-   **Finansdimensjon-konfigurasjon** -hver organisasjon må definere rekkefølgen på økonomiske dimensjoner når enheter brukes til å importere transaksjonene. Ordren er definert for den **Finans dimensjoner integrasjon** format, på **Økonomi**&gt;**kontoplanen**&gt;**dimensjoner**&gt;**finansdimensjon konfigurasjon for å integrere programmer**&gt;**velge data enheter**. Segmentene til finanskontoen som importeres, må ha samme rekkefølge. Hvis ikke, vil det oppstå en feil under import.

## <a name="general-journal-entity-setup"></a>Oppsett av Økonomijournal-enhet
To innstillinger i databehandling påvirker hvordan standard-journalbatchnummer eller bilagsnummer brukes:

-   **Set-basert behandling** (på data-enhet)
-   **Automatisk generert** (på felttilordning)

Avsnittene nedenfor beskriver virkningen av disse innstillingene, og beskriver også hvordan journalpartinumre og bilagsnumre genereres.

### <a name="journal-batch-number"></a>Journalpartinummer

-   Innstillingen **Settbasert behandling** på Økonomijournal-enheten påvirker ikke hvordan journalpartinumre genereres.
-   Hvis feltet **Journalpartinummer** er satt til **Automatisk generert**, opprettes et nytt journalpartinummer for hver linje som importeres. Denne virkemåten anbefales. Innstillingen **Automatisk generert** finner du på importprosjektet under **Vis kart** i kategorien til **Tilordningsdetaljer**.
-   Hvis feltet **Journalpartinummer** ikke er satt til **Automatisk generert**, opprettes journalpartinummeret slik:
    -   Hvis journalbatchnummer som er definert i den importerte filen samsvarer med en eksisterende, ikke-posterte daglige journalen i Microsoft Dynamics 365 for operasjoner, importeres alle linjer som har en tilsvarende journalbatchnummer til eksisterende journal. Linjene importeres aldri til partinummeret for en postert journal. I stedet opprettes det et nytt nummer.
    -   Hvis journalbatchnummer som er definert i den importerte filen ikke samsvarer med en eksisterende, ikke-posterte daglige journalen i Dynamics 365 for operasjoner, grupperes alle linjer som har samme journalbatchnummer under en ny journal. Alle linjer som for eksempel har journalpartinummer 1, importeres til en ny journal, og alle linjer som har journalpartinummer 2, importeres til en annen ny journal. Partinummeret for journalen opprettes ved hjelp av nummerserien som er definert i Økonomiparametere.

### <a name="voucher-number"></a>Bilagsnummer

-   Når du bruker innstillingen **Settbasert behandling** for Økonomijournal-enheten, må bilagsnummeret angis i den importerte filen. Hver transaksjon i økonomijournalen tilordnes bilagsnummeret som er angitt i den importerte filen, selv om bilaget ikke er balansert. Hvis du vil bruke set-basert behandling, men du også ønsker å bruke nummerserien som er definert for bilagsnumre i Dynamics 365 for operasjoner, en hurtigreparasjon er tilgjengelig for utgitt i februar 2016. Hurtigreparasjonsnummeret er 3170316 og er tilgjengelig for nedlasting fra Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Laste ned hurtigreparasjoner fra Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Hvis du vil aktivere denne funksjonaliteten for journalnavnet som brukes for Importer i Dynamics 365 for operasjoner, kan du angi **nummer fordeling ved postering** til **Ja**.
    -   Et bilagsnummer må fortsatt være definert i den importerte filen. Dette nummeret er midlertidig, og blir overskrevet av Dynamics-365 for operasjoner bilagsnummer når journalen posteres. Du må kontrollere at linjene i journalen er gruppert på riktig måte etter midlertidig bilagsnummer. For eksempel under postering finnes tre linjer som har en midlertidig bilagsnummeret til 1. Midlertidige bilagsnummeret for alle tre linjene blir overskrevet av neste nummer i nummerserien. Hvis disse tre linjene ikke er balanserte oppføringer, posteres ikke bilaget. Hvis det finnes linjer som har det midlertidige bilagsnummeret 2, overskrives dette nummeret av neste bilagsnummer i nummerserien og så videre.

<!-- -->

-   Når du ikke bruker den **sett-basert behandling** innstilling, trenger du ikke å angi et bilagsnummer i den importerte filen. Bilagsnumrene opprettes under import, basert på oppsettet for journalnavnet (**Bare ett bilag**, **I forbindelse med saldo** og så videre). Hvis journalnavnet for eksempel er definert som **I forbindelse med saldo**, mottar den første linjen et nytt standard bilagsnummer. Systemet evaluerer deretter linjen for å finne ut om debetbeløpene samsvarer med kreditbeløpene. Hvis det finnes en motkonto på linjen, mottar den neste linjen som importeres et nytt bilagsnummer. Hvis det ikke finnes noen motkonto, evaluerer systemet om debetbeløpene samsvarer med kreditbeløpene når hver nye linje importeres.
-   Hvis feltet **Bilagsnummer** er satt til **Automatisk generert**, kan ikke importen fullføres. Innstillingen **Automatisk generert** for feltet **Bilagsnummer** støttes ikke.

Økonomijournal-enheten bruker settbasert behandling som standard. Når du evaluerer forretningskravene for organisasjonen, kan du endre innstillingen **Settbasert behandling** ved å klikke **Dataenheter** i arbeidsområdet **Databehandling**. Settbasert behandling brukes til å øke hastigheten på importprosessen. Hvis du ikke bruker settbasert behandling, vil import av Økonomijournal-enheten være langsommere.


