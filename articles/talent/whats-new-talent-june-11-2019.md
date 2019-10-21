---
title: Hva er nytt eller endret i Dynamics 365 Talent (11. juni 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b06dc0556bd1461573cd56abed602d72333a3f39
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023936"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (11. juni 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="search-engine-optimization-for-job-posts"></a>Optimalisering av søkemotor for jobbutlysinger

Etter at du har aktivert **Optimalisering av søkemotor** i Dynamics 365 Talent: Attract-administrasjonssenteret, informerer Attract API-et (programmeringsgrensesnittet) for Google-indeksering om foreta et kravlesøk på nettsiden hver gang du aktiverer og posterer en ny jobb eller oppdaterer en eksisterende jobb. På denne måten vises jobben i søkeresultatene for Google og andre søkemotorer.

Likeledes, når du opphever posteringen av en jobb, blir Attract informert av API-et for indeksering slik at den uposterte jobben ikke lenger vises i resultatene.

> [!NOTE]
> Indekseringsroboter har ingen definert tidsramme for kravlesøk på nettsider eller oppdatering av søkeresultater.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Jobbgodkjenninger vises på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**, som viser jobb-ID, jobbtittel, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringene som er beskrevet i denne delen, gjelder build nummer 8.1.2337.

### <a name="platform-update-27-for-finance-and-operations"></a>Platform update 27 for Finance and Operations

Hvis du vil ha mer informasjon om Platform update 27 for Finance and Operations, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 Finance and Operations Platform Update 27 (juni 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Arbeidsområdet for funksjonsbehandling i Talent

Arbeidsområdet **Funksjonsbehandling** i **Systemadministrasjon** lar deg vise, aktivere, deaktivere og planlegge funksjoner som er levert i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet **Funksjonsbehandling** til å aktivere dem og vise dokumentasjonen for dem.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

Enheten Utstedende byrå har nå støtte for egendefinerte felt.

### <a name="new-common-data-service-entities"></a>Nye enheter for Common Data Service

Oppgavegruppe-enheten er lagt til.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkassemiljøer

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er Produksjon eller Sandkasse. Forekomsten av typen Sandkasse gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidforespørsler

Organisasjoner kan tilby mange typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Vise utvidet informasjon om underordnedes prestasjon i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede.

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Ansatte, ledere og Personale kan skrive ut prestasjonsvurderingen for en ansatt.
