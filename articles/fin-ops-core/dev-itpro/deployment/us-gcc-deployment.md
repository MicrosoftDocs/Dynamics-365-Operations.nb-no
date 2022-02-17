---
title: Dynamics 365 Finance og Dynamics 365 Supply Chain Management i US Government Community Cloud (GCC)
description: Dette emnet gir informasjon om Microsoft Dynamics 365 US Government-produkter som er tilgjengelige for kvalifiserte myndigheter og private enheter.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062292"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance og Dynamics 365 Supply Chain Management i US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]



Utvalgte Microsoft Dynamics 365 United States (US) Government-produkter er tilgjengelige for kvalifiserte myndigheter og private enheter. Disse enhetene er begrenset til følgende typer:

- Føderale, statlige, lokale, tribale og territorialmyndigheter
- Private enheter som bruker Dynamics 365 US Government til å levere løsninger til myndighetene eller kvalifiserte medlemmer av skymiljøet
- Private enheter som har kundedata som er underlagt bestemmelser fra myndighetene, og Dynamics 365 US Government er den rette tjenesten for å møte de forskriftsmessige kravene.

Hvis du vil ha mer informasjon, kan du se [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Innføring

Hvis du vil fullføre innledende innføringen for et implementeringsprosjekt i Microsoft Dynamics Lifecycle Services (LCS), følger du instruksjonene i [Jobbintroduksjon for et implementeringsprosjekt](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Bruk imidlertid ikke koblingen til offentlige LCS som følger med i disse instruksjonene. I stedet bruker du følgende URL-adresse til å åpne LCS for US Government Community Cloud (GCC): <https://gov.lcs.microsoftdynamics.us>.

Når den innledende innføringen er fullført, følger du instruksjonene i [Prosjektinnføring](../lifecycle-services/project-onboarding.md). Igjen bruker du [LCS for GCC](https://gov.lcs.microsoftdynamics.us) i stedet for offentlig LCS.

## <a name="environment-deployment"></a>Distribuere miljøet

Når du har fullført prosjektinnføring, kan du se gjennom tilleggsfunksjonene i LCS som beskrives i [Lifecycle Services (LCS) for Finance og Operations-appkunder](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Deretter kan du gå videre til miljødistribusjon.

- Hvis du vil distribuere Microsoft-administrerte miljøer via LCS, følger du instruksjonene i [Lifecycle Services (LCS) for Finance og Operations-appkunder](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- For skybaserte miljøer kan du se [Distribuere og få tilgang til utviklingsmiljøer](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Du må også fullføre Resource Manager-innføringsprosessen for koblingene dine, som beskrevet i [Fullfør jobbintroduksjonsprosessen for Azure Resource Manager for Lifecycle Services-prosjekter for amerikanske myndigheter](arm-onbarding-us-goverment.md).

> [!NOTE]
> For amerikanske myndigheters LCS-prosjekter støttes bare Azure Government-spesifikke Azure-abonnementer.

## <a name="features-that-arent-available"></a>Funksjoner som ikke er tilgjengelige

Enkelte funksjoner er ikke tilgjengelige for distribusjon i GCC, eller de er ikke tilgjengelige for bruk med Dynamics 365 i GCC. For eksempel vil Azure DevOps-tjenester ikke være tilgjengelige i GCC. Lokale Azure DevOps eller offentlige Azure DevOps-tjenester kan imidlertid brukes. Hvis du vil ha detaljert informasjon om funksjonstilgjengelighet, kan du se [Tilgjengelighet av Business Applications-funksjonen for amerikanske myndigheter](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Støttes Dynamics 365 Finance og Dynamics 365 Supply Chain Management i GCC-High?

Nei Dynamics 365 Finance og Dynamics 365 Supply Chain Management støttes bare i GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kan jeg bruke offentlig Azure DevOps med Finans og Supply Chain Management i GCC?

Ja, du kan bruke offentlige Azure DevOps-tjenester hvis du ikke har krav på en løsning som er sertfisert av Federal Risk and Authorization Management Program (FEDRAMP). Alternativt kan du bruke Azure DevOps server.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kan jeg distribuere et skybasert miljø lag-1-utviklingsmiljø på et Azure Commercial-abonnement?

Nei I [LCS for GCC](https://gov.lcs.microsoftdynamics.us) må du bruke et Azure Government-abonnement til å distribuere et skybasert miljø.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Hva kan jeg gjøre hvis jeg trenger en pakke fra Delt aktiva-biblioteket, men det er ikke tilgjengelig i LCS for GCC?

Du kan laste ned den samme pakken fra Delt aktiva-biblioteket i [offentlig LCS](https://lcs.dynamics.com). Eventuelt kan partneren din hjelpe deg med å laste ned pakken.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Er verktøyet for kodeoppgradering tilgjengelig i GCC?

Nei, kodeoppgraderingsverktøyet er for øyeblikket ikke tilgjengelig i GCC. Du kan imidlertid opprette et kundeemneprosjekt i [offentlig LCS](https://lcs.dynamics.com) og bruke verktøyet for kodeoppgradering. Vær oppmerksom på at du ikke kan distribuere miljøer i kundeemneprosjekter.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kan partneren min åpne en støtteforespørsel på mine vegne?

Ja. Hvis partneren din imidlertid bruker en ikke-GCC-identitet, sendes støtteforespørselen til den offentlige støttekøen. Vi anbefaler at du bruker kunde-GCC-rettighet i LCS til å åpne støtteforespørsler.

## <a name="see-also"></a>Se også

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Tilgjengelighet av Business Applications-funksjonen for amerikanske myndigheter](https://aka.ms/BAPFunctionalParity).
- [Brukerveiledning for Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Oversikt over skydistribusjon](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
