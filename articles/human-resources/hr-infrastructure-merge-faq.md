---
title: Vanlige spørsmål om sammenslåing av Dynamics 365 Human Resources-infrastruktur
description: Denne artikkelen svarer på vanlige spørsmål om sammenslåingen av infrastruktur for Microsoft Dynamics 365 Human Resources og økonomi- og driftsapper.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203207"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Vanlige spørsmål om sammenslåing av Dynamics 365 Human Resources-infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Hva er Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources tilbyr verktøy som hjelper personalgrupper med å øke organisasjonsmessig fleksibilitet, transformere erfaringen til de ansatte og optimalisere personalprogrammer for å skape en arbeidsplass der mennesker og bedrift kan trives. Hvis du vil vite mer om Dynamics 365 Human Resources, kan du se [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformer de ansattes opplevelse.** Behold de beste aktørene ved å gi ledere og ansatte muligheten til å bruke tilkoblede selvbetjeningsopplevelser som driver engasjement og vekst.
- **Optimalisere personalprogrammer.** Reduser driftskostnadene, og opprett programmer for håndtering av permisjon og fravær, arbeidstid, fordeler og kompensasjon med folk i sentrum.
- **Øk den organisasjonsmessige fleksibiliteten.** Sørg for at personalavdelingen kan operere med fleksibiliteten som virksomheten krever, ved å bruke Dataverse og Microsoft Power Platform til å sentralisere persondata og enkelt utvide Dynamics 365 Human Resources.
- **Oppdag innsikt i arbeidsstyrken.** Ta datadrevne beslutninger gjennom evnen til å analysere og visualisere persondata på rike instrumentbord som er tilgjengelige på alle enheter.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Verdi og fordeler ved sammenslåingen av infrastruktur

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hva er sammenslåing av Dynamics 365 Human Resources-infrastruktur?

Det finnes for øyeblikket to separate sett med personalfunksjoner på to ulike infrastrukturer i Dynamics 365:

- **Dynamics 365 Human Resources** – En frittstående app som kjører på en uavhengig infrastruktur. Da denne appen ble lansert, ble infrastrukturen atskilt fra andre Dynamics 365-driftsapper. Kundene våre bruker denne appen til å øke organisasjonsfleksibiliteten, optimalisere personalprogrammer, transformere ansattopplevelsen og få innsikt i arbeidsstyrken.
- **Personalmodul** – Et eldre sett med funksjoner som tidligere var en del av lagerenheten (SKU) for Unified Operations-lisensiering. Personalmodulen kjører på Finance and Operations-infrastrukturen, som er den samme i alle driftsapper. Disse appene omfatter Dynamics 365 Finance, Dynamics 365 Project Operations og Dynamics 365 Supply Chain Management. Kunder mottok personalfunksjonene som en del av Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

I løpet av de siste tre årene har Microsoft ikke lagt til noen nye funksjoner eller forbedringer i personalmodulen. I stedet har veikartinvesteringene våre hatt fokus på Dynamics 365 Human Resources-appen.

Ved å bringe disse to funksjonene inn i samme infrastruktur vil vi hjelpe kundene med å oppnå følgende fordeler:

- Utvidelser som er lagt til i Dynamics 365 Human Resources i løpet av de siste tre årene, inkludert utvidet permisjons- og fraværshåndtering, administrasjon av fordeler og rapportering.
- Forbedret utvidbarhet via Microsoft Power Platform og muligheten til å utvide forretningslogikk for å tilpasse sider.
- Forbedret distribusjon, oppdateringer og vedlikehold som er konsekvent med hensyn til administrasjon av applivssyklus (ALM), Lifecycle Services, geografisk tilgjengelighet og mer.
- Mer teknologisk innovasjon etter hvert som teknikerteamet bruker felles tjenester, verktøy og reduserte plattformkostnader.

Denne overgangen vil påvirke kunder som for øyeblikket bruker Dynamics 365 Human Resources eller den eldre personalmodulen.

## <a name="glossary-of-terms-used-in-this-faq"></a>Ordliste over begreper som brukes i disse vanlige spørsmålene

- **Dynamics 365 Human Resources** – Vårt nåværende og fremtidige produkt som tilbyr personalfunksjoner på markedet.
- **Personalmodul** – Et sett med eldre funksjoner som tidligere var lisensiert med Unified Operations-tilbudet. Funksjonene aktiveres når en kunde eier Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.
- **Finance and Operations-infrastruktur** – Utviklingsarkitekturen som brukes av driftsporteføljen, inkludert Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. Denne infrastrukturen er den som vil bli brukt fremover. I disse vanlige spørsmålene refererer begrepet *sammenslått infrastruktur* til Finance and Operations-miljøet.
- **Human Resources-infrastruktur** – Utviklingsarkitekturen som historisk sett ble brukt for Dynamics 365 Human Resources-appen. Sammenslåingen av infrastrukturen vil bringe Dynamics 365 Human Resources til Finance and Operations-infrastrukturen. Den frittstående infrastrukturen vil bli avviklet.

## <a name="general-questions-about-the-infrastructure-merge"></a>Generelle spørsmål om sammenslåingen av infrastrukturen

### <a name="will-customers-lose-any-features-or-capabilities"></a>Vil kundene miste noen funksjoner eller egenskaper?

Målet vårt er å minimere innvirkningen av denne overgangen for kundene. Vi kommer ikke til å fjerne noen funksjoner eller egenskaper. Det vil være funksjonell paritet mellom Dynamics 365 Human Resources og personalmodulen. I tilfeller der det finnes en funksjon i begge infrastrukturene, brukes Dynamics 365 Human Resources-opplevelsen.

### <a name="will-the-user-experience-change"></a>Vil brukeropplevelsen endres?

Brukeropplevelsen vil være konsekvent med standardopplevelsen på Dynamics 365-plattformen. Selv om den generelle opplevelsen for instrumentbordet og menyene vil være lik, vil den bli samkjørt med standardopplevelsen for Dynamics 365 Finance-apper. Navigeringen vil omfatte både moduler og arbeidsområder, gjøre det mulig å ha favoritter og mer. Dynamics 365 Human Resources-arbeidsområdene, for eksempel **Personaladministrasjon** og **Personer**, vil flettes inn i Finance and Operations-infrastrukturen. I fremtiden vil nye funksjoner leveres gjennom Funksjonsbehandling, som lar kundene vise nye funksjoner og bestemme hvilke de vil bruke. For mer informasjon, se [Oversikt over funksjonsbehandling](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og [Dokumentasjon for brukergrensesnittet](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Når er sammenslåingen av Dynamics 365 Human Resources-infrastrukturen ferdig?

Sammenslåingen av infrastrukturen rulles ut i faser for å gi kundene tid til å planlegge og fullføre de nødvendige trinnene. Vi begynte å rulle ut funksjoner i lanseringsbølge 2 for Dynamics i 2021. Vi planlegger å fullføre all produktutviklingsinnsats for dette prosjektet innen slutten av lanseringsbølge 2 i 2022. Legg merke til at tidslinjene kan endres. For den mest oppdaterte informasjonen, se [lanseringsplanene](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Hvilke opplæringer og ressurser vil være tilgjengelige for å hjelpe til med sammenslåingen av infrastrukturen?

Vi vil oppgi dokumentasjon som beskriver hvert trinn i sammenslåingen av infrastrukturen i detalj. Vi tilbyr ytterligere opplæringsressurser, for eksempel videoer og seminarer, etter behov for å hjelpe kunder og partnere med en problemfri overgang.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Kommer det til å bli endringer i utviklingsfunksjoner etter at sammenslåingen av infrastrukturen er fullført?

Hvis du vil lære mer om utviklingsfunksjoner, kan du se [Utvikle og tilpasse hjemmesiden](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Spørsmål om funksjonstilgjengelighet

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Vil LinkedIn Talent Hub-integreringen ikke fungere i Finance and Operations-infrastrukturen?

Nei, LinkedIn Talent Hub-integreringen vil ikke være en del av den sammenslåtte infrastrukturen. Offentlige API-er (grensesnitt for programmering av apper) er tilgjengelige for å bygge løsninger for rekruttering og søkersporing. Kunder som planlegger å bruke LinkedIn Talent Hub, bør samarbeide med Microsoft-partneren sin for å integrere ved hjelp av de medfølgende API-ene. Hvis du vil ha mer informasjon om API-er for ATS-integrering (søkersporingssystem), kan du se [Innføring i API for søkersporingssystemintegrering](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Vil funksjonene som for øyeblikket bare er tilgjengelige i Dynamics 365 Human Resources (for eksempel permisjonsadministrasjon og fordelsadministrasjon), være tilgjengelige etter at sammenslåingen er fullført?

Ja. Alle Dynamics 365 Human Resources-appfunksjoner tas med over til Finance and Operations-infrastrukturen. Funksjonene vil bli gjort tilgjengelige i en gradvis tilnærming. Hvis du vil ha oppdatert informasjon om funksjonstilgjengelighet for den sammenslåtte infrastrukturen, bør du regelmessig se gjennom [lanseringsplanene](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Vil Ceridian-integreringer med Dynamics 365 Human Resources være tilgjengelige etter at sammenslåingen av infrastrukturen er fullført?

Ceridian er i ferd med å opprette en V2-integrasjon med Dynamics 365 Human Resources som drar nytte av API-ene for lønn. Den filbaserte integreringen som for øyeblikket finnes i Dynamics 365 Human Resources, vil ikke bli migrert til Finance and Operations-infrastrukturen. Hvis du vil ha mer informasjon, kan du se [Innføring i lønns-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Vil søkersporing eller pålasting/avlasting av den ansattes funksjonalitet være inkludert?

I tidligere versjoner opprettet vi API-en for ATS-integrering for å gjøre det mulig for partnere og kunder å opprette ATS-integreringer med Human Resources. Ekstra ATS-relatert funksjonalitet ble tilgjengelig i bølge 1 i 2022. Vi vil fortsette å forbedre disse API-ene i fremtidige versjoner.

Personalefunksjonaliteten som for øyeblikket finnes i Finance and Operations-infrastrukturen, omfatter litt rekrutteringsstyringsfunksjonalitet som ikke finnes i Dynamics 365 Human Resources. Når sammenslåingen av infrastrukturen er fullført, vil denne funksjonaliteten være tilgjengelig for alle Human Resources-kunder. Denne funksjonaliteten gir enkel ATS-funksjonalitet. Vi planlegger imidlertid ikke å utvide denne funksjonaliteten i fremtiden. Kunder som trenger mer avansert funksjonalitet, kan benytte seg av ATS-integrasjoner for partnere. Hvis du vil ha mer informasjon om API-er for ATS-integrering, kan du se [Innføring i API for søkersporingssystemintegrering](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Vil Dynamics AX 2012-oppgraderingsverktøyene brukes til å oppgradere personalmodulen i AX 2012 til Dynamics 365 Human Resources-appen?

Ja. Oppgraderingen fra Dynamics AX 2012 til Dynamics 365 Human Resources vil følge den samme oppgraderingsbanen og det samme verktøyet som brukes til å oppgradere til den nyeste versjonen andre Dynamics 365-driftsapper, for eksempel Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

Hvis du vil ha mer informasjon om migreringen til Finance and Operations-infrastrukturen, kan du se [Vanlige spørsmål om migrering av Human Resource-kunder](./customer-migration.md).
