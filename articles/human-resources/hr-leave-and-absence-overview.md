---
title: Oversikt
description: I Dynamics 365 Human Resources gir arbeidsområdet Permisjon og fravær et fleksibelt rammeverk for å opprette nye permisjonsplaner, arbeidsflyter for behandling av forespørsler og en intuitiv, selvbetjent side der ansatte kan be om avspasering.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428973"
---
# <a name="overview"></a>Oversikt

Dynamics 365 Human Resources hjelper deg med å gi arbeiderne flotte fordeler. Arbeidsområdet **Permisjon og fravær** gir et fleksibelt rammeverk for å opprette nye permisjonsplaner, arbeidsflyter for behandling av forespørsler og en intuitiv, selvbetjent side der ansatte kan be om avspasering. Analyse hjelper organisasjonen din med å måle og overvåke permisjonssaldoer og forbruk for permisjonsplaner.

## <a name="set-up-leave-and-absence"></a>Konfigurere permisjon og fravær

Før du kan opprette permisjonsplaner for de ansatte, må du utføre noen få konfigurasjonstrinn:

- [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md)
- [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Opprette en arbeidsflyt for permisjonsforespørsel](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Opprette og administrere permisjonsplaner

Før du oppretter permisjonsplaner for arbeiderne, må du opprette permisjons- og fraværstyper. Når du har opprettet en permisjonsplan, kan du deretter registrere arbeidere i planen. Du kan også kjøre avsetningsprosessen, opprette varsler og vise analyse for planene dine.

- [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)
- [Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
- [Tilordne arbeidere til en permisjonsplan](hr-leave-and-absence-enroll.md)
- [Avsette permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)
- [Vise analyse for permisjon og fravær](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Be om avspasering og administrere forespørsler

De ansatte kan sende inn avspaseringsforespørsler, og du kan behandle dem i arbeidsområdet **Ansattselvbetjening**.

- [Be om fritid](hr-employee-self-service-request-time-off.md)
- [Administrere forespørsler om permisjon og fravær](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Kjente problemer med permisjon og fravær

### <a name="rounding-precision"></a>Avrundingspresisjon

Du kan ikke angi **Avrundingspresisjon** når du angir **Avrundingstype**. Du kan bare angi **Avrundingspresisjon** ved hjelp av enheten **Permisjons- og fraværstype**. 

1. Fra **Permisjons- og fraværstyper** velger du **Åpne i Excel** for å åpne neheten **Permisjons- og fraværstype**.

2. Når filen er åpnet og er aktivert, velger du **Utforming**.

3. I tabellen **Permisjons- og fraværstype** velger du blyantalternativet for å redigere.

4. Velg **Avrundingspresisjon** og **Avrundingstype**, og velg deretter **Legg til** for å legge dette til i listen over felt.

5. Velg **Oppdater**, og velg deretter **Ferdig**.

6. Angi eller velg **Avrundingstype** for hver permisjonstype hvis de ikke allerede er angitt. 

7. Angi **Avrundingspresisjon** for de aktuelle typene.

8. Velg **Publiser** for å sende endringene til Human Resources.

## <a name="leave-and-absence-preview-features"></a>Forhåndsversjonsfunksjoner for permisjon og fravær

Du kan prøve ut nye forhåndsversjonsfunksjoner for permisjon og fravær i et **sandkassemiljø**. Hvis du vil ha informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Forhåndsversjonsfunksjonene omfatter:

- **Permisjonsavsetning per firma eller plan** – du kan kjøre avsetningsprosessen enten for alle firmaer eller for ett enkelt firma. Du kan også kjøre avsetningsprosessen for en bestemt permisjons- og fraværsplan for et bestemt firma. 

- **Kjøp permisjon** – du kan aktivere og opprette policyer for kjøp av permisjon slik at ansatte kan sende kjøpsforespørsler. Ansatte kan sende inn kjøpsforespørsler og få saldoene sine automatisk oppdatert slik at de gjenspeiler forespørselen.  

- **Legge til vedlegg i godkjente permisjonsforespørsler** – du kan legge til et vedlegg i en permisjonsforespørsel som allerede er godkjent. 

