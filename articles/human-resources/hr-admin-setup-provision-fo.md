---
title: Klargjøring av Human Resources i infrastrukturen i Finance and Operations
description: Denne artikkelen forklarer prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources i infrastrukturen i Finance and Operations.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221602"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Klargjøring av Human Resources i infrastrukturen i Finance and Operations

_**Gjelder for:** Human Resources i infrastrukturen for økonomi- og driftsapper_ 

> [!NOTE]
> Fra og med juli 2022 kan ikke nye Human Resources-miljøer klargjøres i den frittstående Human Resources-infrastrukturen, og nye Microsoft Dynamics Lifecycle Services-prosjekter (LCS) kan ikke opprettes i den. Kunder kan distribuere Human Resources-miljøer i infrastrukturen i Finance and Operations.

Denne artikkelen forklarer prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources i infrastrukturen i Finance and Operations.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan klargjøre et nytt miljø:

- Du har kjøpt Human Resources via en Cloud Solution Provider (CSP) eller en enterprise architecture (EA)-avtale. Hvis du har en eksisterende Dynamics 365-lisens som allerede inneholder Human Resources-serviceplanen, og du kan ikke fullføre trinnene i denne artikkelen, kan du kontakte kundestøtte.
- Den globale administratoren har logget seg på [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) og opprettet et nytt Finance and Operations-prosjekt.

## <a name="provision-a-human-resources-trial-environment"></a>Klargjøre et Human Resources-prøvemiljø

> [!NOTE]
> Fra og med april 2022 vil ikke Human Resources-prøvemiljøene være tilgjengelige i den frittstående appen. Potensielle kunder som er interessert i å evaluere Human Resources-funksjonene i økonomi- og driftsapper, kan gjøre dette ved hjelp av den gratis 30-dagers prøveversjonen sammen med demodataene. Dynamics 365 Finance inneholder Human Resources-funksjonene som er innlemmet i Finance-infrastrukturen gjennom sammenslåingen av den frittstående appen. Hvis du vil ha mer informasjon, kan du se [Sammenslåing av HR-tilbud sammenfatter funksjoner for kunder](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Hvis du vil ha mer informasjon om Dynamics 365 Finance-prøveversjoner, kan du se den [trinnvise veiledningen](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Planlegge Human Resources-miljøer

Før du oppretter ditt første Human Resources-miljø, bør du nøye planlegge miljøbehovene for prosjektet. Et basisabonnement på Human Resources omfatter to miljøer: et produksjonsmiljø og et standardmiljø for aksepttest (sandkassemiljø). Du kan kjøpe flere miljøer for å støtte prosjektaktiviteter, avhengig av kompleksiteten i prosjektet.

Her vises noen hensyn for valgfrie tilleggsmiljøer:

- **Dataoverføring**: Datamigreringsaktiviteter gjør at sandkassemiljøet kan brukes til testeformål gjennom hele prosjektet. Når du har et ekstra miljø, kan aktiviteter for migrering av data fortsette mens testing og konfigurasjon skjer samtidig i et annet miljø.
- **Integrering** – Konfigurer og test integreringer, som kan inkludere opprinnelige integrasjoner eller egendefinerte integrasjoner, for eksempel integreringer av lønn, søkersporingssystemer eller fordelssystemer og -leverandører.
- **Opplæring**: Du trenger kanskje et eget miljø som er konfigurert med et sett med opplæringsdata, slik at du kan lære opp de ansatte i bruken av det nye systemet. 
- **Prosjekt med flere faser** – Du trenger kanskje et tilleggsmiljø for å støtte konfigurasjon, dataoverføring, testing eller andre aktiviteter i en prosjektfase som er planlagt etter den innledende aktiveringen av prosjektet.
- **Utvikling** – I Finance and Operations-infrastrukturen kan du nå utvide løsningen og utvikle dine egne tilpasninger. Hver utvikler må bruke sitt eget utviklingsmiljø. For mer informasjon kan du se [Distribuere og få tilgang til utviklingsmiljøer](../fin-ops-core/dev-itpro/dev-tools/access-instances.md).
- **GOLD** – For nye distribusjoner er det en vanlig praksis å bruke et eget GOLD-miljø som holdes atskilt for konfigurasjon og datamigrering. Dette miljøet kan brukes gjennom implementeringen for å oppdatere andre miljøer. Det vil bli brukt til å opprette det nye produksjonsmiljøet som har basiskonfigurasjonen og dataoverføringen. Du kan ikke distribuere et produksjonsmiljø i Finance and Operations-infrastrukturen før du har fullført klargjøringsprosessen for aktivering. Hvis du vil ha mer informasjon, kan du se [Klargjør for aktivering](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Når du vurderer miljøene, anbefaler vi følgende tilnærming:
>
> - Bruk standardmiljøet for godkjenningstest (tidligere sandkassemiljøet) eller et annet miljø for å utføre en testovergangen før du aktiverer.
> - Lag en detaljert kontrolliste for overgang som inneholder hver datapakke som kreves for å migrere de siste dataene til produksjonsmiljøet under overgangen til aktivering. Denne anbefalingen er spesielt viktig hvis du ikke har et eget GOLD-miljø der du kan lagre konfigurasjonene.
> - Bruk standard godkjenningstestmiljø (tidligere sandkasse) eller et annet miljø på nivå 2 eller høyere som TEST-miljøet i hele prosjektet. Hvis du trenger flere miljøer, kan organisasjonen kjøpe dem for en ekstra kostnad.

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt

Hvis du vil bruke LCS til å administrere Human Resources-miljøene dine, må du først opprette et LCS-prosjekt. Hvis du migrerer Human Resources-miljøet til Finance and Operations-infrastrukturen, må du opprette et nytt LCS-prosjekt for økonomi- og driftsapper. Hvis du allerede har et LCS-prosjekt for andre økonomi- og driftsapper, kan du aktivere Human Resources-funksjoner i arbeidsområdet **Funksjonsbehandling**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Når en ny kunde registrerer seg for Human Resources, inkluderer abonnementet et arbeidsområde for implementeringsprosjekt. Når kunden har aktivert tjenesten, må leieradministratoren logge seg på <https://lcs.dynamics.com> ved å bruke leierkontoen. Prosjektarbeidsområdet opprettes automatisk for organisasjonen. Hvis du vil ha mer informasjon, kan du se [Lifecycle Services (LCS) for kunder med økonomi- og driftsapper](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md).

> [!NOTE]
> For å sikre en vellykket klargjøring må kontoen du bruker til klargjøring av Human Resources-miljøet, være tilordnet enten rollen **Systemadministrator** eller rollen **Systemtilpasser** i Power Apps-miljøet som er knyttet til Human Resources-miljøet. Hvis du vil ha mer informasjon om tilordning av sikkerhetsroller til brukere i Microsoft Power Platform, kan du se [Konfigurere brukersikkerhet på ressurser](/power-platform/admin/database-security).

Du må fullføre pålastingsprosessen for LCS-prosjekter før du kan begynne å distribuere miljøer. Hvis du vil ha mer informasjon, kan du se [Prosjektinnføring](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md). Hvis du vil ha mer informasjon om hvordan du bruker LCS, kan du se [Brukerveiledning for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md).

## <a name="deploy-human-resources-environments"></a>Distribuer Human Resources-miljøer

Distribusjon av økonomi- og driftsapper, inkludert Human Resources, i skyen krever at du forstår miljøet og abonnementet du distribuerer til, hvem som kan utføre hvilke oppgaver, og hvilke data og tilpasninger du må administrere. Vi anbefaler at du bruker en tjenestekonto i stedet for en navngitt bruker når du distribuerer nye miljøer. Hvis du vil ha mer informasjon om hvordan du distribuerer miljøer i Finance and Operations-infrastrukturen, kan du se [Oversikt over skydistribusjon](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Hvis du vil distribuere et produksjonsmiljø for Human Resources i Finance and Operations-infrastrukturen, må du fullføre klargjøringsprosessen for aktivering. Hvis du vil ha mer informasjon, kan du se [Klargjør for aktivering](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md). Denne prosessen omfatter abonnementsberegneren i LCS. Hvis du vil ha mer informasjon, kan du se [Abonnementsberegner](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integrer Microsoft Power Platform med Human Resources

Microsoft Power Platform inneholder en pakke med funksjoner for Dynamics 365-apper via Power Platform-administrasjonssenteret. Du kan integrere og utvide bruken av Human Resources-data ved hjelp av Microsoft Power Platform. Hvis du vil ha informasjon om hvordan du integrerer Human Resources med Microsoft Power Platform, kan du se [Microsoft Power Platform-integrering med økonomi- og driftsapper](../fin-ops-core/dev-itpro/power-platform/overview.md).

## <a name="supported-geographies"></a>Geografier som støttes

Hvis du vil ha informasjon om språkene og geografiene som støttes for Human Resources, kan du se [Global som standard: lær om land og språk som støttes](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet

Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Du må eksplisitt gi tilgang til flere programbrukere. Du må legge til brukere og tilordne de riktige rollene til dem i Human Resources-miljøet. Hvis du vil ha mer informasjon, se [Opprette nye brukere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tilordne brukere til sikkerhetsroller](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Tilleggsressurser
Du kan lære mer om hvordan du bruker og administrerer prosjekter i LCS i Finance and Operations-infrastrukturen ved å bruke følgende ressurser:

- [Ressurser for Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Brukerveiledning for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Oversikt over distribusjon av selvbetjening](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Startsiden for databaseflyttingsoperasjoner](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
