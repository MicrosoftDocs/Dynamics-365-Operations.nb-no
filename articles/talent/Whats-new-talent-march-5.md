---
title: Hva er nytt eller endret i Dynamics 365 Talent (5. mars 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 561b6fad0facad86e9a7bc8f36218ab98fcec73c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773271"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (5. mars 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="extending-option-sets-in-attract"></a>Utvide alternativsett i Attract

I Attract finnes det flere felt som er alternativsett i Common Data Service. Nye funksjoner er lansert for å utvide alternativsettene og begynner med **Avslag**-årsaksfeltet, **Ansettelsestype**-feltet og **Ansiennitetstype**-feltet.

> [!IMPORTANT]
> Jobbposteringen til LinkedIn-funksjonaliteten krever bruk av feltene **Ansettelsestype** og **Ansiennitetstype** på siden **Jobbdetaljer**. Standardverdiene i disse feltene støttes av LinkedIn og vises når jobben posteres. Hvis du posterer jobber i LinkedIn og endrer de eksisterende alternativsettverdiene for disse feltene, vil jobben fortsatt posteres, men LinkedIn vil ikke vise de egendefinerte **Ansettelsestype**- og **Ansiennitetstype**-verdiene.

## <a name="changes-in-onboarding"></a>Endringer i jobbintroduksjon

### <a name="private-preview-for-onboard-teams"></a>Privat forhåndsvisning for jobbintroduksjonsteam
Du kan nå enkelt dele og samarbeide om maler på tvers av hele organisasjonen. Hvis du vil ha mer informasjon, se [Dele gode fremgangsmåter i hele organisasjonen ved hjelp av jobbintroduksjonsteam](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Privat forhåndsvisning for tilordnetplassholdere
Du kan berike malene ved å tilordne aktiviteter til roller i stedet for enkeltpersoner. Roller tilordnes deretter til enkeltpersoner ved oppretting av veiledningen. Hvis du vil ha mer informasjon, se [Strømlinjeforme veiledningsadministrasjon ved å tilordne aktiviteter til roller](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Endringer i Core HR
**Build 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Konfigurere arbeidsflyt til å automatisk godkjenne eller følge arbeidsflyten når en HR- eller linjeleder sender eller oppdaterer fraværsforespørsler
Nye arbeidsflytbetingelser er lagt til for å tillate automatisk godkjenning av fraværsforespørsler hvis de sendes av en ansatts leder eller HR. Én måte å oppnå denne automatiske godkjenningen i en arbeidsflyt på, er å aktivere en automatisk handling i arbeidsflyten for godkjenning.

Betingelsene som er lagt til, inkluderer:

- Sendt av – Brukes til å evaluere systembruker-IDen til brukeren som sendte forespørselen til arbeidsflyten.
- Sendt på vegne av – Brukes til å evaluere hvis fraværsforespørselen ble sendt på vegne av arbeideren som er knyttet til forespørselen.
- Sendt av personal – Brukes til å evaluere hvis systembrukeren som sendte forespørselen til arbeidsflyt, har en HR-rolle.
- Sendt av leder – Brukes til å evaluere hvis brukeren som sendte fraværsforespørselen til arbeidsflyten, er en linjehierarkileder for arbeideren som er knyttet til forespørselen.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Aktivere fast kompensasjon for ansatte for fremtidige stillingstilordninger
Det er vanlig for ansatte å delta i en organisasjon med en fremtidig startdato. Med denne endringen er det mulig å definere fast kompensasjon for ansatte med fremtidige stillingstilordninger.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Lønnsfeltene for stillingen er tomme når plasseringen redigeres
Med denne endringen, når du ber om endringer i eksisterende stillinger, vil lønnsfeltene nå som standard gå til gjeldende verdier.

### <a name="other-miscellaneous-bug-fixes"></a>Andre feilrettinger
Andre mindre feilrettinger er inkludert i denne utgivelsen.

### <a name="upgrade-to-common-data-service"></a>Oppgradere til Common Data Service
Tidsfrister for å oppgradere til Common Data Service nærmer deg raskt. Logg på Power Apps-administrasjonssenteret for å bestemme om databasen må oppgraderes. Hvis du vil ha mer informasjon om tidsfrister og de nødvendige trinnene for å oppgradere, kan du se [Oppgradere til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)
I mange organisasjoner har kompensasjons- og fordelsansvarlige bare tilgang til bestemte kompensasjonsposter, for eksempel poster for ledere eller regionsbaserte ansatte. Med denne endringen kan du administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter. Bare rollene som har den rette tilgangen, vil kunne behandle kompensasjon for disse ansatte.

###  <a name="platform-update-24-for-finance-and-operations"></a>Platform update 24 for Finance and Operations
Hvis du vil ha mer informasjon om Platform update 24 for Finance and Operations, kan du se [Hva er nytt eller endret i Platform update 24 for Finance and Operations (mars 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
