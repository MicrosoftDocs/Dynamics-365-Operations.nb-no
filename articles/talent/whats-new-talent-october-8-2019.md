---
title: Hva er nytt eller endret i Dynamics 365 Talent (8. oktober 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529486"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (8. oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringene som er beskrevet i denne delen, gjelder build nummer 8.1.2542. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Fjerne åpen registrering for fordeler fra offentlig forhåndsvisning

I forbindelse med vår kunngjøring i blogginnlegget [Strategiske investeringene i Core HR gir til store driftsfordeler](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) fjerner Microsoft funksjonen for åpen registrering av fordeler fra den offentlige forhåndsvisningen 18. oktober 2019. I stedet vil ny funksjonalitet bli utgitt i fremtiden. Produksjonsbruk av funksjonen for åpen registrering av fordeler som for øyeblikket er i den offentlige forhåndsvisningen, støttes ikke. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service-integrering er nå deaktivert som standard i nye klargjøringer (343675)
 
Når nye miljøer klargjøres, er Common Data Service-integrasjonen nå deaktivert. Hvis du vil ha mer informasjon, kan du se [Konfigurere Common Data Service-integrasjon](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinjeformet ansattoppføring og navigasjon

Funksjonaliteten for ansattoppføring og navigasjon er nå tilgjengelig i alle miljøer. Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon \> Koblinger \> Oppsett \> Systemparametere \> Forhåndsvisningsfunksjoner**, og deretter velger du **Utvidet arbeiderskjema og navigering**. Funksjonen aktiveres da for alle brukere. Du kan når som helst deaktivere dette alternativet.

Hvis du vil ha mer informasjon, se [Strømlinjeformet ansattoppføring og navigasjon](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) i Dynamics 365: 2019-frigivelsesbølge 2-planen.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract og Onboard oppretter inaktive arbeidere i Core HR (380517)

Frigivelsen denne uken retter opp et problem der Attract og Onboard oppretter inaktive arbeidere i Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Arbeidsflyten mislykkes når lederen er logget på et annet firma under avslutning av en ansatt (346852)

Arbeidsflyten mislykkes ikke lenger basert på den juridiske enheten som lederen er logget på.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Mangler informasjon for HcmOnboardingWorkerChecklistTaskEntity (349591)

Denne versjonen inneholder tilleggsinformasjon om **HcmOnboardingWorkerChecklistTaskEntity**. Her er noen eksempler:

- **Gruppenavn** når den tilordnede typen er **gruppe**
- **Ansattnavn** når den tilordnede typen er **ansatt**
- **Ledernavn** når den tilordnede typen er **leder**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Enheter vises ikke i alfabetisk rekkefølge i Common Data Service-administrasjon (377414)

Enheter vises nå i alfabetisk rekkefølge på siden **CDS-administrasjon**.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Hvis du endrer ansettelsestypen med en fremtidig dato, tillates ikke en stillingstilordning (339958)

Denne endringen tillater stillingstilordninger når arbeidertyper endres (for eksempel fra ansatt til oppdragstaker).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Oppdatering av enheten for permisjonsbanktransaksjonen for Common Data Service oppretter en ny post i Talent (352938)

Permisjonstransaksjonen er nå oppdatert når det gjøres en oppdatering for Common Data Service for permisjonsbanktransaksjoner.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Tittelen på vedlegg for tilbakemeldingselementer viser beskrivelsen av tilbakemeldingen (343765)

Beskrivelsen av tilbakemeldingen vises ikke lenger i vedleggstittelen.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Kommentarfeltet for kompensasjonsarbeidsflyt viser feil innhold (339297)

Denne endringen viser innholdet i feltet **%HcmActionState.HcmWorkerActionComment.Comments%** field.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity og WorkCalendarDayEntity er ikke eksponert via OData (376329)

I denne versjonen er **WorkCalendarEntity** og **WorkCalendarDayEntity** nå tilgjengelige via Open Data Protocol (OData).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity er treg når OData brukes (375221)

Endringer forbedrer ytelsen til **HCMWorkerEntity** når Microsoft Excel-arbeidsbokutformingen brukes.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Journaloppføring for lederytelse viser en feil etter sletting av en ytelsesjournal og oppretting av en ny (336061)

Denne versjonen retter opp et problem som oppstår etter at én ytelseslogg er slettet og en ny opprettes umiddelbart etterpå. Denne korrigeringen endrer virkemåten i lederens selvbetjening.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.
