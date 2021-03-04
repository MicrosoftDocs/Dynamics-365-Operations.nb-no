---
title: Hva er nytt eller endret i Dynamics 365 Talent (23. juli 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 360574d3c8e0b349119e0987f2453a5d5be21e90
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528153"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (23. juli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="pdf-renderer-for-candidate-documents"></a>PDF-gjengivelse for kandidatdokumenter

Attract-brukere kan nå vise PDF-vedlegg for kandidater i dokumentvisningen i stedet for å laste ned vedleggene.

### <a name="signing-up-for-attract-user-research-group"></a>Registrering for Attract-brukerundersøkelsesgruppe 

Når vi planlegger nye produktfunksjoner eller leverer forhåndsvisningsfunksjoner, ser vi etter brukere som kan være med å styre oss i riktig retning. Interesserte brukere kan nå registrere seg for å være med i vår brukerundersøkelsesgruppe ved å bruke registreringskoblingen i appen vår.

### <a name="job-approvals-appear-on-the-home-page"></a>Jobbgodkjenninger vises på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**, som viser jobb-ID, jobbtittel, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2394.

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Enhetsstøtte for egendefinerte felt i Common Data Service 

I denne utgaven støtter nå **Arbeidskalender** og **Arbeidskalender** dag egendefinerte i Common Data Service.

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidsforespørsler

Organisasjoner kan tilby mange forskjellige typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkasseforekomster

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**. Forekomster av typen **Sandkasse** gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Vise utvidet informasjon for prestasjon i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger, som deres ansatte behandler sammen med dem. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede. 

## <a name="coming-soon"></a>Kommer snart

### <a name="region-support-for-canada-and-southeast-asia"></a>Områdestøtte for Canada og Sørøst-Asia

Vi er glad for å annonsere at områdene Canada og Sørøst-Asia er tilgjengelige for Talent 1. august 2019. Med denne endringen kan du opprette miljøer i de kanadiske og asiatiske områdene, og alle Talent-data vil bli oppbevart kun innenfor disse stedene. Du kan opprette et miljø i disse nye områdene ved å velge plasseringen i dialogboksen Nytt miljø og bruke dette miljøet til å klargjøre Talent i LCS som beskrevet her [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Dataoverføring av eksisterende prosjekter fra andre områder til de kanadiske og asiatiske områdene støttes ikke. Bare nye prosjekter kan klargjøres for de nye områdene som støttes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]