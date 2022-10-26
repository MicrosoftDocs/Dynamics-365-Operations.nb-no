---
title: Startside for sensordataintelligens
description: Denne artikkelen inneholder en oversikt over sensordataintelligens. Organisasjoner kan bruke denne funksjonen til å drive forretningsprosesser i Microsoft Dynamics 365 Supply Chain Management, basert på IoT-signaler (Tingenes Internett) fra maskiner og utstyr på produksjonsgulvet.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689864"
---
# <a name="sensor-data-intelligence-home-page"></a>Startside for sensordataintelligens

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Med sensordataintelligens for Microsoft Dynamics 365 Supply Chain Management kan organisasjonerr drive forretningsprosesser i Supply Chain Management, basert på IoT-signaler (Tingenes Internett) fra maskiner og utstyr på produksjonsgulvet. Det er en oppdatert versjon av funksjonen *IoT-intelligens*, med nytt navn, som tidligere var tilgjengelig for Supply Chain Management.

Med sensordataintelligens kan du utføre følgende oppgaver:

- Samle inn detaljer fra maskiner og utstyr for å oppdatere tellerverdier for objekter i Supply Chain Management og drive prediktivt vedlikehold.
- Konfigurer løsningen ved å bruke en enkel pålastingsveiviser i stedet for å installere og konfigurere komponenter manuelt i Microsoft Dynamics Lifecycle Services (LCS).
- Distribuer komponenter på ditt eget abonnement, slik at du har mer fleksibilitet til å administrere Azure-komponenter.
- Konfigurer, skaler og utvid løsningen som forretningslogikk som kjører på Azure-komponenter. Disse komponentene administreres nå på ditt eget abonnement. Derfor kan du tilpasse dem etter behov for å oppfylle dine unike forretningsbehov.

## <a name="business-scenarios"></a>Foretningsscenarioer

Sensordataintelligens muliggjør flere typer funksjonalitet, der hver type representeres av et bestemt *scenario* i systemet. Hvert scenario inneholder et spesialisert sett med konfigurasjonsalternativer i systemet, slik det vises i tabellen nedenfor.

| Scenario | Beskrivelse |
|---|---|
| [Aktivumnedetid](sdi-scenario-asset-downtime.md) | Nøyaktig spore effektiviteten til maskinressurser ved å bruke data for å spore maskinens nedetid. |
| [Vedlikehold av objekt](sdi-scenario-asset-maintenance.md) | Minimer vedlikeholdskostnadene og forleng levetiden for ressurser ved å forbedre vedlikeholdsplaner basert på sensoravlesninger av kritiske kontrollpunkter for maskinressurser. |
| [Maskinstatus](sdi-scenario-equipment-downtime.md) | Sørg for effektivitet når operasjonen utføres, ved å bruke sensoravlesninger til å varsle planleggere om maskinavbrudd, og tilby alternativer for å redusere potensielle forsinkelser. |
| [Produktkvalitet](sdi-scenario-product-quality.md) | Sikre kvaliteten på produktpartier ved å sammenligne sensoravlesninger med faktiske egenskaper til hvert produktparti, for eksempel fuktighet, temperatur eller egendefinerte kvalitetsmålinger. Systemet vil varsle brukere når avvik oppstår. |
| [Produksjonsforsinkelser](sdi-scenario-production-delays.md) | Bruk sensoravlesninger til å sammenligne faktisk syklustid med planlagt syklustid, og til å varsle arbeidsledere når produksjonen ikke går etter planen. Arbeidsledere kan deretter gripe inn etter behov for å oppnå maksimal driftseffektivitet. |

## <a name="architecture"></a>Arkitektur

Arkitekturdiagrammet nedenfor gir en oversikt over løsningen og komponentene.

![Arkitekturdiagram for sensordataintelligens.](media/sdi-architecture.png "Arkitekturdiagram for sensordataintelligens")
