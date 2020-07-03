---
title: Ferdigmelde fra jobbkortenheten
description: Dette emnet beskriver hvordan du konfigurerer systemet slik at brukere av en jobbkortenhet kan rapportere ferdige produkter fra en produksjonsordre til beholdning.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
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
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403268"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Ferdigmelde fra jobbkortenheten

[!include [banner](../includes/banner.md)]

Arbeidere bruker **Rapporter fremdrift**-siden på jobbkortenheten til å rapportere antallet som er fullført for en produksjonsjobb.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontrollere om antallene som ferdigmeldes, blir lagt til i beholdningen

Følg denne fremgangsmåten for å kontrollere hvorvidt og hvordan antallene som er rapportert som fullført for den siste operasjonen, skal legges til i beholdningen.

1. Gå til **Produktkontroll \> Oppsett \> Produksjonsutførelse \> Standarder for produksjonsordre**.
1. I **Ferdigmeld**-kategorien angir du en av følgende verdier for **Oppdater ferdig rapport online**-feltet:

    - **Nei** – ingen antall blir lagt til i beholdningen når antallene rapporteres ved siste operasjon. Statusen for produksjonsordren endres aldri.
    - **Status + Antall** – Statusen for produksjonsordren endres til *Ferdigmeldt*, og antallet ferdigmeldes til beholdningen.
    - **Antall** – Antallet rapporteres som fullført til beholdningen, men status for produksjonsordren endres aldri.
    - **Status** – Bare statusen for produksjonsordren endres. Ingen antall blir lagt til i beholdningen når antallene rapporteres ved siste operasjon.

> [!NOTE]
> Antall spores ikke i beholdningen hvis operasjonene de ferdigmeldes for, ikke er definert som siste operasjon. Disse antallene kan imidlertid brukes til å vise fremdriften. De kan også inkluderes i regler som kontrollerer om arbeidere kan starte neste operasjon før en definert terskel for rapporterte antall i den forrige operasjonen nås. Du kan definere disse reglene i **Antallsvalidering**-kategorien på **Standarder for produksjonsordre**-siden.

Hvis du vil ha mer informasjon om hvordan du arbeider med **Standarder for produksjonsordre**-siden, kan du se [Produksjonsparametere i Produksjonsutførelse](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Rapporter ferdigstillelse av partistyrte varer

Jobbkortenheten støtter tre scenarier for rapportering av partivise varer. Disse scenariene gjelder både for varer som er aktivert for avanserte lagerprosesser, og for varer som ikke er aktivert for avanserte lagerprosesser.

- **Manuelt tilordnede partinumre:** Arbeidere angir et egendefinert partinummer. Dette partinummeret kan komme fra en ekstern kilde som ikke er kjent for systemet.
- **Forhåndsdefinerte partinumre:** Arbeidere velger et partinummer fra en liste over partinumre som systemet automatisk genererer før produksjonsordren frigis til jobbkortenheten.
- **Faste partinumre:** Arbeidere verken angir eller velger et partinummer. I stedet tilordner systemet automatisk et partinummer til produksjonsordren før den frigis.

Følg denne fremgangsmåten for å aktivere hvert enkelt scenario.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet du vil konfigurere.
1. I **Administrer lager**-hurtigkategorien, i **Partinummergruppe**-feltet velger du sporingsnummergruppen som er definert til å støtte scenariet.

> [!NOTE]
> Hvis ingen partinummergruppe er tilordnet et partistyrt produkt, inneholder jobbkortenheten en standardløsning for manuell registrering av partinummer under ferdigmelding.

Underdelene nedenfor beskriver hvordan du definerer sporingsnummergrupper for å støtte alle de tre scenariene for rapportering av partivise varer.

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a>Aktivere rapportering av partinummer på jobbkortenheten

Hvis du vil at jobbkortenhetene skal godta et partinummer under ferdigmelding, må du bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere følgende funksjoner (i denne rekkefølgen):

1. Forbedret brukeropplevelse for dialogboksen Rapportfremdrift i jobbkortenheten.
1. Aktiver angivelse av parti- og serienumre under ferdigrapportering fra jobbkortenheten (forhåndsvisning)

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Konfigurere en sporingsnummergruppe som gjør at arbeiderne kan tilordne et partinummer manuelt

For å tillate manuelt tilordne partinumre følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.

1. Gå til **Lagerstyring \> Oppsett \> Dimensjoner \> Sporingsnummergrupper**.
1. Opprette eller velge sporingsnummergruppen som skal konfigureres.
1. På **Generelt**-hurtigfanen angir du **Manuelt**-alternativet til **Ja**.

    ![Siden med sporingsnummergrupper](media/tracking-number-group-manual.png "Siden med sporingsnummergrupper")

1. Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.

Når du bruker dette scenariet, er **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en tekstboks der arbeidere kan angi en hvilken som helst verdi.

![Side med fremdriftsrapport med et felt for manuelle partinumre](media/job-card-device-batch-manual.png "Side med fremdriftsrapport med et felt for manuelle partinumre")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Konfigurere en sporingsnummergruppe som gir en liste over forhåndsdefinerte partinumre

For å generere en liste over forhåndsdefinerte partinumre følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.

1. Gå til **Lagerstyring \> Oppsett > Dimensjoner \> Sporingsnummergrupper**.
1. Opprette eller velge sporingsnummergruppen som skal konfigureres.
1. På **Generelt**-hurtigfanen angir du **Bare for lagertransaksjoner**-alternativet til **Ja**.
1. Bruk **Per antall**-feltet til å dele opp partinumre etter antall, basert på verdien du angir. Tenk deg at du har en produksjonsordre på ti stykker, og at **Per antall**-feltet er satt til *2*. I dette tilfellet blir fem partinumre tilordnet produksjonsordren når den opprettes.

    ![Siden med sporingsnummergrupper](media/tracking-number-group-predefined.png "Siden med sporingsnummergrupper")

1. Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.

Når du bruker dette scenariet, er **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en rullegardinliste der arbeidere må velge en forhåndsdefinert verdi.

![Side med fremdriftsrapport med en liste over forhåndsdefinerte partinumre](media/job-card-device-batch-predefined.png "Side med fremdriftsrapport med en liste over forhåndsdefinerte partinumre")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Konfigurere en sporingsnummergruppe som automatisk tilordner partinumre

Hvis partinumre skal tilordnes automatisk uten inndata fra ansatte, følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.

1. Gå til **Lagerstyring \> Oppsett \> Dimensjoner \> Sporingsnummergrupper**.
1. Opprette eller velge sporingsnummergruppen som skal konfigureres.
1. På **Generelt**-hurtigfanen angir du **Bare for lagertransaksjoner**-alternativet til **Nei**.
1. Angi **Manuelt**-alternativet til **Nei**.

    ![Siden med sporingsnummergrupper](media/tracking-number-group-fixed.png "Siden med sporingsnummergrupper")

1. Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.

Når du bruker dette scenariet, viser **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en verdi, men arbeiderne kan ikke redigere den.

![Side med fremdriftsrapport med et fastsatt partinummer](media/job-card-device-batch-fixed.png "Side med fremdriftsrapport med et fastsatt partinummer")

## <a name="report-as-finished-to-a-license-plate"></a>Ferdigmeld til et nummerskilt

Avanserte lagerprosesser kan bruke nummerskiltdimensjonen til å spore beholdning på lagerlokasjoner som er definert for dette formålet. I dette tilfellet kreves skiltnummeret når en arbeider rapporterer antall som ferdigmeldt.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Aktivere nummerskiltrapportering og etikettutskrifter

Hvis du vil bruke funksjonene som beskrives i denne delen, må du bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere følgende funksjoner (i denne rekkefølgen):

1. Nummerskilt for ferdigmelding lagt til i jobbkortenheten
1. Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten
1. Skriv ut etikett fra jobbkortenhet

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Konfigurere ferdigmelding til et nummerskilt

Følg denne fremgangsmåten for å kontrollere om arbeidere bør gjenbruke et eksisterende nummerskilt eller generere et nytt nummerskilt når de ferdigmelder antall.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurer jobbkort for enheter**.
2. Angi følgende alternativer for hver enhet:

    - **Generer nummerskilt** – sett dette alternativet til **Ja** for å generere et nytt nummerskilt for hver rapport som fullføres. Angi **Nei** hvis det skal brukes et eksisterende nummerskilt for hver ferdigmelding.
    - **Skriv ut etikett** – sett dette alternativet til **Ja** hvis arbeideren må skrive ut en nummerskiltetikett for hver ferdigmelding. Angi **Nei** hvis det ikke kreves etiketter. 

![Side for konfigurasjon av jobbkort for enheter](media/config-job-card-raf.png "Side for konfigurasjon av jobbkort for enheter")

> [!NOTE]
> For å konfigurere etiketten går du til **Lagerstyring \> Oppsett \> Dokumentruting \> Dokumentruting**. Hvis du vil ha mer informasjon, kan du se [Aktivere utskrift av nummerskiltetiketter](../warehousing/tasks/license-plate-label-printing.md).
