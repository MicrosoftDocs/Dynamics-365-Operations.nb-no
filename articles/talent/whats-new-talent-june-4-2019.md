---
title: Hva er nytt eller endret i Dynamics 365 for Talent (4. juni 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a93ad140fb9116ffb0c486b7f3175f90859f125
ms.sourcegitcommit: 7b5ff31c0a82809641beb681510201b942932c74
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621868"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (4. juni 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 for Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-the-home-page"></a>Jobbgodkjenninger på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**. Denne delen viser jobb-ID-en, tittelen, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene sine under **Forespurt av deg**. Denne delen viser godkjennerne som må godkjenne den innsendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 for Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringene som er beskrevet i denne delen, gjelder build nummer 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side for å validere stillingshierarkidata

Personalansatte (HR) og administratorer kan validere lederhierarkiet for eventuelle sirkelreferanser som ble importert ved en feiltakelse. Du kan få tilgang til den nye siden i **Organisasjonsstyring \> Koblinger \> Stillinger \> Validering av stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angi årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav. Du kan angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Angi en transaksjonsliste for permisjon og fravær for HR

Muligheten til å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men garanterer også nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak fridagssaldoer.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Hvis du sletter en post fra Talent, fjernes ikke posten fra Common Data Service

Poster som fjernes fra Talent Core HR, blir nå også fjernet fra Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Gyldige fra-/til-datoer for variabel kompensasjonsplan blir ikke innfridd

I denne versjonen kan du ikke registrere en ansatt i en variabel kompensasjonsplan hvis startdatoen er før planens startdato eller sluttdatoen er etter planens sluttdato. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Kommentarer vedrørende prestasjonsvurdering fjernes når brukere velger Avbryt

Denne versjonen løser et problem der vurderingskommentarer fjernes hvis en bruker begynner å endre en kommentar, men deretter velger **Avbryt**. 

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkasseforekomster

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**. Forekomster av typen **Sandkasse** gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidsforespørsler

Organisasjoner kan tilby mange forskjellige typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Vise utvidet informasjon for prestasjon i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger, som deres ansatte behandler sammen med dem. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede. 

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Ansatte, ledere og Personale kan skrive ut prestasjonsvurderingen for en ansatt.
