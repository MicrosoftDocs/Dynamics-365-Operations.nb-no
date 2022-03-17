---
title: Organisasjonshierarki i Dataverse
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9174612743c68595d12dd223f0932ace1857c0fb
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358370"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisasjonshierarki i Dataverse

[!include [banner](../../includes/banner.md)]



Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki. Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.

Selv om Dataverse ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter. Som en del av Dataverse-integreringen legges datastrukturen for organisasjonshierarkiet til i Dataverse.

## <a name="data-flow"></a>Dataflyt

Et forretningsøkosystem som består av Finance and Operations-apper og Dataverse, vil fortsatt ha et organisasjonshierarki. Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Dataverse for informasjons- og utvidelsesformål. Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Dataverse, som en énveis dataflyt fra Finance and Operations-apper til Dataverse.

![Bilde av arkitektur.](media/dual-write-data-flow.png)

Tabelltilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra økonomi- og driftsapper til Dataverse.

## <a name="templates"></a>Maler

En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten. Du kan definere følgende typer interne organisasjoner: juridiske enheter, driftsenheter og team. Som tabellen nedenfor viser opprettes det en samling tabelltilordninger for å synkronisere juridiske enheter, driftsenheter og relatert informasjon om organisasjonshierarki.

Finance and Operations-apper | Kundeengasjementsapper     | Beskrivelse
-----------------------|--------------------------------|---
[Juridiske enheter](mapping-reference.md#102) | cdm_companies | 
[Juridiske enheter](mapping-reference.md#142) | msdyn_internalorganizations |
[Driftsenhet](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisasjonshierarki – publisert](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Denne malen gir enveis synkronisering av den publiserte tabellen for organisasjonshierarkiet.
[Formål for organisasjonshierarki](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Denne malen gir enveis synkronisering av formålstabellen for organisasjonshierarkiet.
[Type organisasjonshierarki](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Denne malen gir enveis synkronisering av typetabellen for organisasjonshierarkiet.

## <a name="internal-organization"></a>Intern organisasjon

Informasjon om intern organisasjon i Dataverse kommer fra to tabeller, **driftsenhet** og **juridiske enheter**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
