---
title: Prøv storskalaenheter i en distribuert hybridtopologi
description: Dette emnet inneholder informasjon om hvordan du prøver sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376247"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Prøv storskalaenheter i en distribuert hybridtopologi

[!include [banner](../includes/banner.md)]

Fremgangsmåten for å prøve den distribuerte hybridtopologien er enkel. I det første stadiet validerer du tilpasninger for å sikre at de fungerer i den distribuerte topologien. Du har to alternativer.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Alternativ 1: Evaluer tilpasninger i utviklingsmiljøer

Før du begynner å innføre sandkassemiljøene, anbefaler vi at du utforsker storskalaenheter i et utviklingsoppsett, for eksempel et miljø med én boks, slik at du kan validere prosesser, tilpasninger og løsninger. I løpet av dette stadiet blir data og tilpasninger brukt i miljøene med én boks. Du kan kjøre i ett miljø, som kan fungere som både bedriftssenteret og storskalaenheten. Du kan alternativt ha to utviklingsmiljøer der det ene fungerer som senteret og det andre som en storskalaenhet. Dette oppsettet gir den beste måten å identifisere og løse problemer på. Den nyeste [builden for tidlig tilgang (PEAP)](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u) kan også brukes til å fullføre dette stadiet.

Du bør bruke [distribusjonsverktøy for storskalaenheter for utviklingsmiljøer med én boks](https://github.com/microsoft/SCMScaleUnitDevTools) til å installere og vedlikeholde miljøene. Med disse verktøyene kan du konfigurere senteret og storskalaenheter i ett eller to miljøer med én boks. Verktøyene leveres som både som en binær versjon og i kildekode på GitHub. Studer wiki-en til prosjektet, som omfatter en [trinnvis bruksveiledning](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) som beskriver hvordan du bruker verktøyene. Hvis du [distribuerer kantskalaenheter på egendefinert maskinvare ved å bruke lokale forretningsdata](cloud-edge-edge-scale-units-lbd.md), må du følge en annen fremgangsmåte.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Alternativ 2: Skaff tilleggsprogrammer, og distribuer dem i sandkassemiljøene

For å kunne prøve den distribuerte hybridtopologien, må du ha to sandkassemiljøer (lag 2) der det ene har dataene (bedriftssenteret) og det andre er for storskalaenheten og har «tomme data».

Du må skaffe tilleggsprogrammer for minst én sky- eller kantskalaenhet. Tilsvarende prosjekt- og miljøplasser blir deretter gitt i [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), slik at storskalaenhetsmiljøene kan distribueres ved hjelp av [Scale Unit Manager-portalen](https://aka.ms/SCMSUM).

Kontakt Microsoft Kundestøtte for å be om at sandkassemiljøene aktiveres.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]