---
title: Reparasjonsstyring
description: Grupper problemer systematisk for å bidra med løsningsforslag som har hjulpet tidligere.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32372a6a54e2adfbf511e2247be4a9baa28b4b53
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015208"
---
# <a name="repair-management"></a>Reparasjonsstyring       

[!include [banner](../includes/banner.md)]


For reparasjonsstyring kan du gruppere problemer systematisk. Dette er for å bidra med løsningsforslag som har hjulpet tidligere.

Du definerer innstillinger for symptomer, diagnose og løsning. Alle disse kan senere brukes når du får en lignende vare til reparasjon. Du kan også definere reparasjonsstadier som kan følge fremdriften på en reparasjon.

## <a name="setting-up-repair-management"></a>Definere reparasjonsadministrasjon

Bruk de følgende oppsettskjemaene til å angi informasjon som skal brukes til å angi symptomene, diagnosen og løsningen for reparasjonen.

- **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Betingelser**.
- **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Symptomområder**.
-  **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Diagnoseområder**.
- **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Løsninger**.
- **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Reparasjonsstadier**.

## <a name="symptoms-and-conditions"></a>Symptomer og forhold

Symptomer er kundens beskrivelse av problemet. Symptomene omfatter kundens observasjoner om behovet for reparasjon.

Du kan definere symptomområder, symptomkoder og forhold. Symptomområdet dekker området med feilen, og symptomkoden dekker symptomet på feilen. Forholdet beskriver situasjonen eller miljøet som er til stede når problemet oppstår.

**Eksempel**

En datamaskin sendes til reparasjon fordi harddisken mislykkes etter bruk lengre. Harddiskfeilen fører til en blå skjerm-feil. Teknikeren som mottar datamaskinen angir følgende symptomer og forhold:

1.  Symptomområdet er harddisken

2.  Symptomkoden er blå skjerm-feil

3.  Forhldet er at harddisken feiler etter utvidet bruk

## <a name="diagnosis-and-resolutions"></a>Diagnose og løsninger

Diagnose- og løsningfeltene er informasjon fra reparasjonssiden. Dette er fremgangsmåten en tekniker har gjennomgått for å undersøke problemet.

Diagnoseområdet dekker hva som må gjøres for å løse problemet. Diagnosekoden er hvordan problemet ble håndtert, og løsningen kan være at varen ble reparert, byttet ut, eller bestillingen ble annullert av kunden. Hvis for eksempel datamaskinen er reparert, kan diagnoseområdet være "defekt del", diagnosekoden kan være "nytt skjermkort installert", og løsningen kan være "byttet ut".

## <a name="repair-stages"></a>Reparasjonsstadier

Reparasjonsstadier beskriver fremdriften på reparasjonsprosessen. Reparasjonsstadiet inneholder godkjenningsparameteren **Fullført**, som angir at reparasjonslinjen er fullført og at fullføringsdato- og tidspunkt er registrert.

## <a name="applying-repair-management"></a>Bruk reparasjonsstyring

Før du kan bruke reparasjonsstyring på en vare, må varen defineres med en serviceobjektrelasjon på en serviceordre. Fra serviceordren kan du deretter opprette en reparasjonslinje med informasjon om det aktuelle problemet. På reparasjonslinjen kan du definere serviceobjektet som er til reparasjon og informasjon om symptomer, diagnose og utføreselse. Du kan også opprette et notat for reparasjonslinjen.

Du kan opprette reparasjonslinjer for hvert trinn i reparasjonsprosessen.

## <a name="create-a-repair-line-on-a-service-order"></a>Opprette en reparasjonslinje på en serviceordre

1.  Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

2.  Velg serviceordren med serviceobjektet som skal repareres.

3.  Velg **Reparasjon** \> **Reparasjonslinjer** for å åpne skjemaet **Reparasjonslinjer**.

4.  Velg **Ny** for å opprette en ny linje.

5.  Velg et serviceobjekt. Du velge et hvilket som helst objekt som er definert med en objektrelasjon på serviceordren.

6.  Velg de aktuelle forhåndsdefinerte symptom-, diagnose- og utførelsesverdiene på reparasjonslinjen, og velg deretter fanen **Notat** for å opprette et notat på reparasjonslinjen.

7.  Velg **Lagre** for å lagre den nye reparasjonslinjen. Feltet **Opprettet dato og klokkeslett** i fanen **Generelt** i skjemaet **Reparasjonslinjer** oppdateres med tidspunktet for lagringen.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Spore fremdrift og løse et reparasjonsproblem

Du kan definere reparasjonsstadiene for en reparasjonslinje for å spore fremdriften til en reparasjon.

Når reparasjonen er fullført, kan du lukke reparasjonslinjen. Set reparasjonsstadiet til et stadium med en **Fullført**-egenskap aktivert. Gjeldende dato og tidspunkt registreres som fullføringstidspunktet på linjen.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Lukke en reparasjonslinje for en fullført reparasjon

1.  Åpne skjemaet **Reparasjonslinjer**. Følg fremgangsmåten for å opprette en reparasjonslinje tidligere i denne artikkelen.

2.  Velg reparasjonslinjen med reparasjonen du ønsker å lukke.

3.  I feltet **Reparasjonsstadium** velger du et stadium der egenskapen **Fullført** er aktivert.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]