---
title: Organisasjonshierarki i Dataverse
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 77625e6e80bfa45add6839df89d9aae27e41d456
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355304"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisasjonshierarki i Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki. Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.

Selv om Dataverse ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter. Som en del av Dataverse-integreringen legges datastrukturen for organisasjonshierarkiet til i Dataverse.

## <a name="data-flow"></a>Dataflyt

Et forretningsøkosystem som består av Finance and Operations-apper og Dataverse, vil fortsatt ha et organisasjonshierarki. Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Dataverse for informasjons- og utvidelsesformål. Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Dataverse, som en énveis dataflyt fra Finance and Operations-apper til Dataverse.

![Bilde av arkitektur.](media/dual-write-data-flow.png)

Tabeltilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Dataverse.

## <a name="templates"></a>Maler

Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene. Som følgende tabell viser opprettes en samling tabelltilordning for å synkronisere produkter og beslektet informasjon.

Finance and Operations-apper | Andre Dynamics 365-apper | beskrivelse
-----------------------|--------------------------------|---
Formål for organisasjonshierarki | msdyn_internalorganizationhierarchypurposes | Denne malen gir enveis synkronisering av formålstabellen for organisasjonshierarkiet.
Type organisasjonshierarki | msdyn_internalorganizationhierarchytypes | Denne malen gir enveis synkronisering av typetabellen for organisasjonshierarkiet.
Organisasjonshierarki – publisert | msdyn_internalorganizationhierarchies | Denne malen gir enveis synkronisering av den publiserte tabellen for organisasjonshierarkiet.
Driftsenhet | msdyn_internalorganizations |
Juridiske enheter | msdyn_internalorganizations |
Juridiske enheter | cdm_companies | Gir toveis synkronisering av informasjon om juridisk enhet (firma).

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Intern organisasjon

Informasjon om intern organisasjon i Dataverse kommer fra to tabeller, **driftsenhet** og **juridiske enheter**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]