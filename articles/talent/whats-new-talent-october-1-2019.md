---
title: Hva er nytt eller endret i Dynamics 365 Talent (1. oktober 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529666"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (1. oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2509. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinjeformet ansattoppføring og navigasjon

Denne funksjonaliteten er nå tilgjengelig i alle sandkassemiljøer. Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon > Koblinger > Oppsett > Systemparametere> Forhåndsvisningsfunksjoner**. Velg **Utvidet arbeiderskjema og navigering**. Dette aktiverer disse endringene for alle brukere. Du kan når som helst deaktivere dette alternativet.

Hvis du vil ha mer informasjon, se [Strømlinjeformet ansattoppføring og navigasjon](./streamlined-employee-entry.md). Hvis du vil se en video om disse endringene, kan du se [Oversikt over Dynamics 365 for Talent 2019-utgivelsen Wave 2](https://aka.ms/ROGT19RW2ROV).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Du kan aktivere forhåndsvisningsfunksjoner i sandkasse- og prøvemiljøer

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er Produksjon eller Sandkasse. Forekomster av typen Sandkasse gjør at nye funksjoner kan testes tidlig. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen Sandkasse, kan du kontakte kundestøtten for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Kompensasjonsdato er som standard en annen dato enn stillingstilordningen (337694)

Med denne endringen er standard kompensasjonsdato startdatoen for tillingstilordningen.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Kan ikke avslutte kompensasjon sammen med stillingstilordningen (328993)

Med denne endringen kan du avslutte kompensasjonen når du avslutter stillingstilordningen ved hjelp av **Avslutt tilordning** på siden **Tilordninger for arbeiderstilling** med personalhandlinger aktivert.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Validering av bankkonto krever registrerings- og kontonumre på alle lokasjoner (340403)

I denne ukens endringer er det lagt til et nytt konfigurasjonsalternativ for å deaktivere obligatorisk validering for **Registreringsnummer** og **Kontonummer**. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>Vedlegg er ikke aktivert i MSS-ytelses journaler for tilbakemelding om resultat (341794)

Med denne uke utgivelse aktiveres vedlegg for tilbakemeldingselementer på siden for ytelsesjournal.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Detaljer for fraværsforespørsel synkroniseres ikke fra Common Data Service til Talent (369608)

Med disse endringene vil detaljer for fraværsforespørsel som oppdateres i Common Data Service, synkroniseres tilbake til Talent.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Jobbeskrivelse vises ikke for jobben på sien Kompetansegapanalyse (369398)

I denne ukens bygg vises beskrivelsen når du velger jobben på siden **Kompetansegapanalyse**.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Ansatte, ledere og personaleksperter kan skrive ut prestasjonsvurderingen for en ansatt.
