---
title: Hva er nytt eller endret i Dynamics 365 Talent (18. juni 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/18/2019
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
ms.search.validFrom: 2019-06-18
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a8b17fbeba591c20253bc4ec66767ac0dea64e6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528081"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-18-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (18. juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Jobbgodkjenninger vises på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**, som viser jobb-ID, jobbtittel, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringene som er beskrevet i denne delen, gjelder build nummer 8.1.2347.

### <a name="confirmation-of-course-participants-causes-an-error"></a>Bekreftelse av kursdeltakere fører til en feil

Dialogboksen for å skrive ut rapporten om kursdeltakere er fjernet. Denne rapporten støttes ikke i Talent.

### <a name="the-compensation-section-of-the-transfer-worker-page-isnt-available-in-some-scenarios"></a>Kompensasjon-delen på Overfør arbeider-siden er ikke tilgjengelig i enkelte scenarioer

Denne endringen lar brukere angi kompensasjonsdata når de fyller ut **Overfør arbeider**-siden.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkassemiljøer

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**. Forekomsten av typen **Sandkasse** gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidforespørsler

Organisasjoner kan tilby mange typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

Følgende enheter støtter egendefinerte felt: Inntektskode for lønn og Referansepunkt for kompensasjon. 

### <a name="new-common-data-service-entities"></a>Nye enheter for Common Data Service

Årsakskoder-enheten kommer til å bli lagt til i Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Vise prestasjonsinformasjon for direkte underordnede og deres underordnede i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede.

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Ansatte, ledere og Personale kan skrive ut prestasjonsvurderingen for en ansatt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]