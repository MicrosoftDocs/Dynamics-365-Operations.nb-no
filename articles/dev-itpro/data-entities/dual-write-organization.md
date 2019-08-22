---
title: Organisasjonshierarki i Common Data Service
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789228"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organisasjonshierarki i Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Fordi Microsoft Dynamics 365 for Finance and Operations er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki. Forretningsøkonomi og -operasjoner kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.

Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter. Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.

## <a name="data-flow"></a>Dataflyt

Et forretningsøkosystem som består av Finance and Operations og Common Data Service, vil fortsatt ha et organisasjonshierarki. Dette organisasjonshierarkiet er bygd på Finance and Operations, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål. Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations til Common Data Service.

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a>Maler

Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations til Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Formålet med internt organisasjonshierarki

Denne malen gir enveissynkronisering av formålsenheten for organisasjonshierarkiet fra Finance and Operations til Dynamics 365 for Customer Engagement.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Intern organisasjonshierarkitype

Denne malen gir enveissynkronisering av typeenheten for organisasjonshierarkiet fra Finance and Operations til Customer Engagement.

<!-- ![architecture image](media/dual-write-type.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Internt organisasjonshierarki

Denne malen gir enveissynkronisering av den publiserte enheten for organisasjonshierarkiet fra Finance and Operations til Customer Engagement.

<!-- ![architecture image](media/dual-write-organization.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Intern organisasjon

Informasjon om intern organisasjon i Common Data Service kommer fra to Finance and Operations-enheter, **driftsenhet** og **juridiske enheter**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Driftsenhet

Kildefelt | Tilordningstype | Målfelt
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NAVN | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Juridisk enhet

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NAVN | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
none | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Bedrift

Gir toveissynkronisering av informasjon om juridisk enhet (firma) mellom Finance and Operations og Customer Engagement.

<!-- ![architecture image](media/dual-write-company.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
