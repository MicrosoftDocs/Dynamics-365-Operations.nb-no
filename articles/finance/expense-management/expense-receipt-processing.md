---
title: Behandling av utgiftskvitteringer
description: Dette emnet inneholder informasjon om OCR-behandling (optisk tegngjenkjenning) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når utgiftsrapporter opprettes i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: efba2faf9428d9b556d74273bc7daadba7211c48
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248969"
---
# <a name="expense-receipt-processing"></a>Behandling av utgiftsmottak

[!include [banner](../includes/banner.md)]

Utgiftsoppføring er forbedret gjennom innføringen av OCR-behandling (optisk tegngjenkjenning) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når utgiftsrapporter opprettes.

## <a name="key-features"></a>Hovedfunksjoner

- Forhandlerens navn, dato og totalt beløp trekkes fra kvitteringer.
- Funksjonen prøver å matche ikke-tilknyttede kvitteringer med ikke-tilknyttede utgiftstransaksjoner.
- Brukere kan opprette manuelt angitte utgiftstransaksjoner fra kvitteringer.

## <a name="usage-examples"></a>Eksempler på bruk

- **Legg automatisk til kvitteringer som inkluderer kredittkorttransaksjoner, når en utgiftsrapport opprettes.**

    1. Åpne **Utgiftsadministrering**-arbeidsområdet.
    2. I **Kvitteringer**-fanen verifiserer du at det ikke finnes tilknyttede kvitteringer. Du kan også laste opp kvitteringer i **Kvitteringer**-fanen.
    3. I **Utgifter**-fanen verifiserer du at det ikke finnes tilknyttede utgifter. Vanligvis importerer utgiftsadministratoren disse utgiftene fra kredittkortleverandøren.
    4. Velg **Ny utgiftsrapport**. Vær oppmerksom på at du kan inkludere utgifter og kvitteringer, nå også, når du oppretter en utgiftsrapport. Hvis du legger til både utgifter og kvitteringer, utløses automatisk matching av kvitteringene med utgiftene.

- **Opprett en utgift, eller match en utgift fra en kvittering.**

    1. På en utgiftsrapport går du til **Kvitteringer**-fane og legger ved en kvittering ved å velge **Legg til kvitteringer**.
    2. Under det opplastede bildet av kvitteringen, legger du merke til alternativene **Opprett** og **Match**.

        - Velg **Opprett** hvis du vil opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som hentes fra kvitteringen.
        - Hvis du velger **Match**, prøver systemet å matche en eksisterende utgift med kvitteringen.

## <a name="installation"></a>Installasjon

Denne funksjonen fungerer i kombinasjon med **Utgiftsrapporter avbildet på nytt**-funksjonen for å forenkle utgiftsopplevelsen.

For å kunne bruke disse avanserte utgiftsfunksjonene må du installere Expense Management Service-tillegget for Microsoft Dynamics 365 Finance, og aktivere funksjonene i forekomsten. Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).

1. Logg på LCS, og åpne ønsket miljø.
2. Gå til **Detaljerte opplysninger**.
3. Velg **Vedlikehold**, eller rull ned til hurtigfanen **Miljøtillegg**.
4. Velg **Installer et nytt tillegg**.
5. Velg **Utgiftsadministreringstjeneste**.
6. Følg installasjonsveiledningen, og godta vilkårene.
7. Velg **Installer**.

I **Funksjonsadministrering**-arbeidsområde aktiverer du følgende funksjoner:

- Ny utforming av utgiftsrapporter
- Samsvar og opprett utgift automatisk fra mottak

Når du aktiverer disse funksjonene, finner følgende handlinger sted:

- Det eksisterende **Utgiftsadministrering**-arbeidsområdet erstattes med det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet av reiseregningsfelt.
- Du kan fremdeles åpne forrige **Utgiftsrapporter**-side ved å gå til **Utgiftsadministrering > Mine utgifter > Utgiftsrapporter**.
- Arbeidsflyter og alle godkjenninger fører deg fortsatt til den eksisterende reiseregningssiden.
- Kvitteringer behandles gjennom Microsoft Azure Cognitive Services, og metadata pakkes ut og legges til.
- Det legges til et alternativ der du kan opprette en utgiftsrapport som inneholder matchede ikke-tilknyttede kvitteringer.
- Et alternativ som legges til i utgiftsrapporter, lar deg opprette en utgiftslinje fra en kvittering, eller forsøke å matche en eksisterende kvittering med en eksisterende utgiftslinje.

Hvis du vil ha mer informasjon om funksjonen for gjentatt avbildning av utgiftsrapporter, kan du se [Gjentatt avbildning av utgiftsrapporter](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

**Bruker Microsoft dataene mine til sine modeller?**

Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for kvitteringsbehandling. Denne modellen er ikke basert på kvitteringene som du laster opp.

**Hvor er denne funksjonen tilgjengelig, og hvor behandles den?**

For øyeblikket støttes USA.

**Hvor ender kvitteringen mine opp?**

Finans kontakter Cognitive Services for å trekke ut feltdataene. Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandling utføres. Når behandlingen er fullført, fjerner Cognitive Services kvitteringen. Kvitteringer lagres fremdeles i Finans.

Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonaliteten til skjemagjenkjenner](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
