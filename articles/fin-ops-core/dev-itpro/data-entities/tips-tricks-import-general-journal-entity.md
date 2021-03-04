---
title: Anbefalte fremgangsmåter for å importere bilag ved hjelp av enheten Økonomijournal
description: Dette emnet inneholder tips for å importere data inn i økonomijournalen ved hjelp av Økonomijournal-enheten.
author: rcarlson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5b36e11bd9ef338334f7ac1b6412edb7754010f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687649"
---
# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Anbefalte fremgangsmåter for å importere bilag ved hjelp av enheten Økonomijournal

[!include [banner](../includes/banner.md)]

Dette emnet inneholder tips for å importere data inn i økonomijournalen ved hjelp av Økonomijournal-enheten.

Du kan bruke Økonomijournal-enheten til å importere bilag som har konto- eller motkontotypen **Finans**, **Kunde**, **Leverandør** eller **Bank**. Bilaget kan angis som én linje, ved hjelp av både **Konto**- og **Motkonto**-feltet, eller som et flerlinjet bilag, der bare **Konto**-feltet brukes (og **Motkonto** er tomt på hver linje). Økonomijournal-enheten støtter ikke alle kontotyper. Andre enheter finnes i stedet for scenarier der det kreves ulike kombinasjoner av kontotyper. Hvis du for eksempel vil importere en prosjekttransaksjon, kan du bruke Prosjektutgiftsjournal-enheten. Hver enhet er utformet for å støtte bestemte scenarier. Dette betyr at tilleggsfelt kan være tilgjengelige i enheter for disse scenariene. Det kan imidlertid hende at flere felt ikke er tilgjengelige i enheter for ulike scenarier.

## <a name="setup"></a>Installasjon
Før du importerer ved hjelp av Økonomijournal-enheten, må du kontrollere følgende oppsett:

- **Oppsett av nummerserie for journalpartinummeret** – Når du importerer ved hjelp av Økonomijournal-enheten, bruker journalpartinummeret nummerserien som er definert i parametere for økonomimodul. Hvis du har satt nummerserien for journalpartinummeret til **Manuelt**, brukes ikke et standardnummer. Dette oppsettet støttes ikke.
- **Konfigurasjon av finansdimensjoner** – Alle organisasjoner må definere rekkefølgen til finansdimensjoner når enheter brukes til å importere transaksjoner. Ordren er definert for formatet **Integrering av finansdimensjoner** på **Økonomimodul** &gt; **Kontoplan** &gt; **Dimensjoner** &gt; **Konfigurasjon av finansdimensjoner for programintegrering** &gt; **Velg dataenheter**. Segmentene til finanskontoen som importeres, må ha samme rekkefølge. Hvis ikke, vil det oppstå en feil under import.

## <a name="general-journal-entity-setup"></a>Oppsett av Økonomijournal-enhet
To innstillinger i databehandling påvirker hvordan standard journalpartinummer eller bilagsnummer brukes:

- **Settbasert behandling** (på dataenhet)
- **Automatisk generert** (på felttilordning)

Følgende deler beskriver effekten av disse innstillingene. De forklarer også hvordan systemet genererer partinumre for journaler og bilagsnumre.

### <a name="journal-batch-number"></a>Journalpartinummer

- Innstillingen **Settbasert behandling** på Økonomijournal-enheten påvirker ikke hvordan journalpartinumre genereres.
- Hvis feltet **Journalpartinummer** er satt til **Automatisk generert**, opprettes et nytt journalpartinummer for hver linje som importeres. Denne virkemåten anbefales. Innstillingen **Automatisk generert** finner du på importprosjektet under **Vis kart** i kategorien til **Tilordningsdetaljer**.
- Hvis feltet **Journalpartinummer** ikke er satt til **Automatisk generert**, opprettes journalpartinummeret slik:

    - Hvis journalpartinummeret som er definert i den importerte filen, samsvarer med en eksisterende, upostert daglig journal i, importeres alle linjer som har et tilsvarende journalpartinummer til den eksisterende journalen. Linjene importeres aldri til partinummeret for en postert journal. I stedet opprettes det et nytt nummer.
    - Hvis journalpartinummeret som er definert i den importerte filen, ikke samsvarer med en eksisterende, upostert daglig journal, grupperes alle linjer som har et samme journalpartinummer under en ny journal. Alle linjer som for eksempel har journalpartinummer 1, importeres til en ny journal, og alle linjer som har journalpartinummer 2, importeres til en annen ny journal. Partinummeret for journalen opprettes ved hjelp av nummerserien som er definert i Økonomiparametere.

### <a name="voucher-number"></a>Bilagsnummer

- Når du bruker innstillingen **Settbasert behandling** for Økonomijournal-enheten, må bilagsnummeret angis i den importerte filen. Hver transaksjon i økonomijournalen tilordnes bilagsnummeret som er angitt i den importerte filen, selv om bilaget ikke er balansert. Merk følgende punkt hvis du vil bruke settbasert behandling, men du også vil bruke nummerserien som er definert for bilagsnumre.

    - Hvis du vil aktivere denne funksjonaliteten for journalnavnet som brukes for importer, kan du sette **Nummertilordning ved postering** til **Ja**.
    - Et bilagsnummer må fortsatt være definert i den importerte filen. Dette nummeret er imidlertid midlertidig og blir overskrevet av bilagsnummeret når journalen posteres. Du må kontrollere at linjene i journalen er gruppert på riktig måte etter midlertidig bilagsnummer. Under postering finnes for eksempel tre linjer som har det midlertidige bilagsnummeret 1. Det midlertidige bilagsnummeret for alle tre linjene blir overskrevet av det neste nummeret i nummerserien. Hvis disse tre linjene ikke er balanserte oppføringer, posteres ikke bilaget. Hvis det finnes linjer som har det midlertidige bilagsnummeret 2, overskrives dette nummeret av neste bilagsnummer i nummerserien og så videre.

- Når du ikke bruker innstillingen **Settbasert behandling** , behøver du ikke å angi et bilagsnummer i den importerte filen. Bilagsnumrene opprettes under import, basert på oppsettet for journalnavnet (**Bare ett bilag**, **I forbindelse med saldo** og så videre). Hvis journalnavnet for eksempel er definert som **I forbindelse med saldo**, mottar den første linjen et nytt standard bilagsnummer. Systemet evaluerer deretter linjen for å finne ut om debetbeløpene samsvarer med kreditbeløpene. Hvis det finnes en motkonto på linjen, mottar den neste linjen som importeres et nytt bilagsnummer. Hvis det ikke finnes noen motkonto, evaluerer systemet om debetbeløpene samsvarer med kreditbeløpene når hver nye linje importeres.
- Hvis feltet **Bilagsnummer** er satt til **Automatisk generert**, kan ikke importen fullføres. Innstillingen **Automatisk generert** for feltet **Bilagsnummer** støttes ikke.

Økonomijournal-enheten bruker settbasert behandling som standard. Når du evaluerer forretningskravene for organisasjonen, kan du endre innstillingen **Settbasert behandling** ved å klikke **Dataenheter** i arbeidsområdet **Databehandling**. Settbasert behandling brukes til å øke hastigheten på importprosessen. Hvis du ikke bruker settbasert behandling, vil import av Økonomijournal-enheten være langsommere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]