---
title: Reparasjonsstyring
description: "Grupper problemer systematisk for å bidra med løsningsforslag som har hjulpet tidligere."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a>Reparasjonsstyring       

[!include [banner](../includes/banner.md)]


For reparasjonsstyring kan du gruppere problemer systematisk. Dette er for å bidra med løsningsforslag som har hjulpet tidligere.

Du definerer innstillinger for symptomer, diagnose og løsning. Alle disse kan senere brukes når du får en lignende vare til reparasjon. Du kan også definere reparasjonsstadier som kan følge fremdriften på en reparasjon.

## <a name="setting-up-repair-management"></a>Definere reparasjonsadministrasjon

Bruk de følgende oppsettskjemaene til å angi informasjon som skal brukes til å angi symptomene, diagnosen og løsningen for reparasjonen.

1.  Klikk **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Betingelser**.

2.  Klikk **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Symptomområder**.

3.  Klikk **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Diagnoseområder**.

4.  Klikk **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Løsninger**.

5.  Klikk **Servicestyring** \> **Oppsett** \> **Reparasjon** \> **Reparasjonsstadier**.

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

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Velg serviceordren med serviceobjektet som skal repareres.

3.  Klikk **Reparasjon** \> **Reparasjonslinjer** for å åpne **Reparasjonslinjer**-skjemaet.

4.  Trykk CTRL+N for å opprette en ny linje.

5.  Velg et serviceobjekt. Du velge et hvilket som helst objekt som er definert med en objektrelasjon på serviceordren.

6.  Velg de aktuelle forhåndsdefinerte symptom-, diagnose- og utførelsesverdiene på reparasjonslinjen, og klikk om nødvendig kategorien **Notat** for å opprette et notat på reparasjonslinjen.

7.  Trykk CTRL+S for å lagre den nye reparasjonslinjen. Feltet **Opprettet dato og klokkeslett** i kategorien **Generelt** i skjemaet **Reparasjonslinjer** oppdateres med tidspunktet for lagringen.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Spore fremdrift og løse et reparasjonsproblem

Du kan definere reparasjonsstadiene for en reparasjonslinje for å spore fremdriften til en reparasjon.

Når reparasjonen er fullført, kan du lukke reparasjonslinjen. Set reparasjonsstadiet til et stadium med en **Fullført**-egenskap aktivert. Gjeldende dato og tidspunkt registreres som fullføringstidspunktet på linjen.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Lukke en reparasjonslinje for en fullført reparasjon

1.  Åpne skjemaet **Reparasjonslinjer**. Følg fremgangsmåten for å opprette en reparasjonslinje tidligere i dette emnet.

2.  Velg reparasjonslinjen med reparasjonen du ønsker å lukke.

3.  I feltet **Reparasjonsstadium** velger du et stadium der egenskapen **Fullført** er aktivert.

  



