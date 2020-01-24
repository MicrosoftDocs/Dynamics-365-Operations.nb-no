---
title: Hva er nytt eller endret i Dynamics 365 for Talent (27. august 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899249"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (27. august 2019)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2447. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkasseforekomster

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er Produksjon eller Sandkasse. Forekomster av typen Sandkasse gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til Produksjon-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen Sandkasse, kan du kontakte kundestøtten for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Vise utvidet informasjon for prestasjon i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Sletting av juridiske enheter er ikke tillatt hvis det finnes ansatte i firmaet (339849)

Med denne endringen kan du ikke fjerne eller slette firmaer hvis ansatte og andre relaterte data finnes for den juridiske enheten.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Business Intelligence Analytics for kompensasjonsstyring samsvarer ikke i kompensasjonsarbeidsområdet (322493)

I denne versjonen er kompensasjonsanalyse blitt justert slik at den gjenspeiler planene som er tilordnet ansatte, nøyaktig.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Arbeidsflytplassholder %company% viser DAT når ansatte ansettes gjennom arbeidsflyt (343905)

Med denne versjonen viser firmaplassholderen den juridiske enheten som er knyttet til ansettelsen av den nyansatte.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>CDSJobPosition-enheten viser en feil når gyldig til-dato er angitt (349387)

I denne versjonen tillater datakildene **Stillingsdetaljer** og **Stillingsvarighet** på **CDSJobPosition**-enheten redigeringer fra Common Data Service til **Gyldig dato**-feltene. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>For ansattavslutning er siste arbeidsdag fylt ut i Sluttdato for tilordning (332496)

Denne endringen setter nå som standard **Sluttdato for tilordning** for stillingen til **Sluttdato for ansettelse**. Du kan endre disse standardene når du angir data.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Juridiske enheter er ikke begrenset til ansettelse (338871)
 
Denne endringen begrenser ansettelsesprosessen slik at den bare viser de juridiske enhetene som brukeren har tilgang til.  

## <a name="in-preview"></a>I forhåndsvisning

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinjeformet ansattoppføring og navigasjon

Denne funksjonaliteten er nå tilgjengelig i sandkasse- og prøvemiljøer. Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon > Koblinger > Oppsett > Systemparametere> Forhåndsvisningsfunksjoner**. Velg **Utvidet arbeiderskjema og navigering**. Dette aktiverer disse endringene for alle brukere. Du kan når som helst deaktivere dette alternativet.

Hvis du vil ha mer informasjon, se [Strømlinjeformet ansattoppføring og navigasjon](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-29"></a>Plattform update 29

Hvis du vil ha mer informasjon om Platform update 29, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 for Finance and Operations Platform Update 29 (oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
