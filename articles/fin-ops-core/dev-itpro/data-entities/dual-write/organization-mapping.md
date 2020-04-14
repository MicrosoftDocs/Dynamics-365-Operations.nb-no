---
title: Organisasjonshierarki i Common Data Service
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations-apper og Common Data Service.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173160"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organisasjonshierarki i Common Data Service

[!include [banner](../../includes/banner.md)]



Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki. Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.

Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter. Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.

## <a name="data-flow"></a>Dataflyt

Et forretningsøkosystem som består av Finance and Operations-apper og Common Data Service, vil fortsatt ha et organisasjonshierarki. Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål. Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations-apper til Common Data Service.

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a>Maler

Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Common Data Service.

## <a name="templates"></a>Maler

Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene. Som følgende tabell viser opprettes en samling enhetstilordning for å synkronisere produkter og beslektet informasjon.

Finance and Operations-apper | Andre Dynamics 365-apper | beskrivelse
-----------------------|--------------------------------|---
Formål for organisasjonshierarki | msdyn_internalorganizationhierarchypurposes | Denne malen gir enveis synkronisering av formålsenheten for organisasjonshierarkiet.
Type organisasjonshierarki | msdyn_internalorganizationhierarchytypes | Denne malen gir enveis synkronisering av typeenheten for organisasjonshierarkiet.
Organisasjonshierarki - publisert | msdyn_internalorganizationhierarchies | Denne malen gir enveis synkronisering av den publiserte enheten for organisasjonshierarkiet.
Driftsenhet | msdyn_internalorganizations | 
Juridiske enheter | msdyn_internalorganizations | 
Juridiske enheter | cdm_companies | Gir toveis synkronisering av informasjon om juridisk enhet (firma).


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Intern organisasjon

Informasjon om intern organisasjon i Common Data Service kommer fra to enheter, **driftsenhet** og **juridiske enheter**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

