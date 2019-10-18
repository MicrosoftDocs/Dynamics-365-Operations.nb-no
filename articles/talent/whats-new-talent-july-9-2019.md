---
title: Hva er nytt eller endret i Dynamics 365 Talent (9. juli 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b3eb53943546166eee845749a070ed2fca1a03b8
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023959"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (9. juli 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Kommer snart i Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Jobbgodkjenninger vises på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**, som viser jobb-ID, jobbtittel, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Platform update 28 for Finance and Operations

Hvis du vil ha mer informasjon om Platform update 28 for Finance and Operations, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 Finance and Operations Platform Update 28 (juli 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Enhetsstøtte for egendefinerte felt i Common Data Service 

Følgende enheter støtter egendefinerte felt: 

- **Fast plan for kompensasjon**
- **Oppsett av referansepunkt for kompensasjon**
- **Oppsettslinje for referansepunkt for kompensasjon**
- **Inntektskode for lønn**
- **Lønnsperiode**
- **Fast kompensasjonshendelse**
- **Kompensasjonsrutenett**

Slik viser du alle oppdaterte enheter i Talent:

1. Velg **Systemadministrasjon**, velg **Koblinger**, og velg deretter **Common data service-konfigurasjon**.
2. Velg rullegardinmenyen **CDS-enhetsnavn**. Alle oppførte enheter er på den siste versjonen. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Fullt navn lagt til arbeiderenhet i Common Data Service

Feltet **Fullt navn** er lagt til **Arbeider**-enheten.

### <a name="full-time-equivalent-higher-than-10"></a>Fulltidsekvivalent høyere enn 1,0

En advarsel vises nå hvis en verdi som er større enn 1,0, angis for en heltidsansatt i en stilling. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>En advarsel vises ikke lenger på arbeidersiden når det ikke er noen fremtidig datert ansettelse

Du vil ikke lenger motta en melding som angir at det finnes en fremtidig ansettelse når du navigerer til **Arbeider**-siden fra listen for **Ansatte som slutter** i arbeidsområdet **Personal administrasjon**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Kan ikke slette en forretningsprosess i Talent

Du kan nå slette forretningsprosesser i arbeidsområdet **Forretningsprosess**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Permisjonssaldo viser ikke lenger null for planer uten avsetninger ved bruk av Saldo per avsetningsperiode

Planer som er definert uten avsetninger, kan nå vise en saldo.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkasseforekomster

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**. Forekomster av typen **Sandkasse** gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidsforespørsler

Organisasjoner kan tilby mange forskjellige typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Vise utvidet informasjon for prestasjon i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger, som deres ansatte behandler sammen med dem. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede. 

### <a name="entities-supporting-custom-fields"></a>Enheter som støtter egendefinerte felt

Følgende enheter vil bli aktivert for egendefinerte felt i Common Data Service: 

- **Permisjonstype**
- **Bankkonto for arbeider**
- **Arbeidskalender**
