---
title: Vanlige spørsmål om sammenslåing av Dynamics 365 Human Resources-infrastruktur
description: Dette emnet svarer på vanlige spørsmål om sammenslåingen av infrastruktur for Microsoft Dynamics 365 Human Resources og økonomi- og driftsapper.
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
ms.openlocfilehash: 766ee49c17749841d8acac6637a0262e87e52e92
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809620"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Vanlige spørsmål om sammenslåing av Dynamics 365 Human Resources-infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dette emnet svarer på vanlige spørsmål om sammenslåingen av infrastruktur for Microsoft Dynamics 365 Human Resources og økonomi- og driftsapper.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hva er sammenslåing av Dynamics 365 Human Resources-infrastruktur?

Dynamics 365 Human Resources er en frittstående app som bruker en annen infrastruktur enn andre økonomi- og driftsapper, for eksempel Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations. Sammenslåingen av infrastrukturen vil føre Dynamics 365 Human Resources til den samme infrastrukturen som andre økonomi- og driftsapper.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Verdi og fordeler ved sammenslåingen av infrastruktur

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Organisasjonen bruker Dynamics 365 Human Resources til å administrere personaloperasjonene. Hvilke fordeler får vi se ut av disse endringene?

- Disse endringene tar bort forvirringen forårsaket av flere sett med personalfunksjoner i Dynamics 365.
- De gir både Microsoft Power Platform utvidbarhet og en måte å utvide forretningslogikk og funksjonsalternativer på.
- De gir konsistens mellom Dynamics 365 Human Resources og andre økonomi- og driftsapper når det gjelder håndtering av applivssyklus, (ALM), Microsoft Dynamics Lifecycle Services (LCS), geografisk tilgjengelighet, utvidbarhet og mer.
- De lar deg dra nytte av fellestjenester og verktøy, og bidra til å redusere kostnader.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Organisasjonen min bruker Human Resources-modulen i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Hvilke fordeler får vi se ut av disse endringene?

Funksjonene og investeringene som er gjort i Dynamics 365 Human Resources, vil nå være tilgjengelige for kunder som bruker personalmodulen i Dynamics 365 Finance. Noen av disse funksjonene omfatter permisjons- og fraværsstyring, fordelsadministrasjon og oppgavebehandling.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Vil jeg miste noen funksjoner eller funksjoner som jeg bruker for øyeblikket?

Det vil være funksjonell paritet mellom Dynamics 365 Human Resources og personalmodulen i økonomi- og driftsapper. Dynamics 365 Human Resources vil ha prioritet for like funksjoner. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Vil opplevelsen endres for brukerne?

De nye personalfunksjonene administreres gjennom funksjonsadministrasjon. Kundene vil bestemme om de vil implementere dem. I noen tilfeller kan funksjoner endres. I slike tilfeller vil dokumentasjonen bli gitt.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Hvordan påvirker denne endringen meg hvis jeg blir en eksisterende kunde, og jeg bruker både personalmodulen i økonomi- og driftsinfrastrukturen og Dynamics 365 Human Resources gjennom egendefinerte integrasjoner?

Det vil ikke lenger være nødvendig med egendefinerte integrasjoner mellom Dynamics 365 Human Resources og personalmodulen i Dynamics 365 Finance. Alle personaldata ligger i samme database som andre økonomi- og driftsapper.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migrering fra Dynamics 365 Human Resources til økonomi- og driftsapper

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisasjonen bruker Dynamics 365 Human Resources til å administrere personaloperasjonene. Hva må vi planlegge for å migrere til den nye erfaringen?

Hvis organisasjonen bruker Dynamics 365 Human Resources, men ikke bruker andre økonomi- og driftsapper, blir Human Resources-miljøet migrert til den nye infrastrukturen. Mye av denne migreringsprosessen vil være automatisert. Prosessene vil være på plass for å migrere databasen og synkronisere den med den nye infrastrukturen.

I tillegg vil verktøy være på plass slik at du kan teste migreringsprosessen og validere data og erfaring før du migrerer produksjonsmiljøet.

Hvis organisasjonen bruker både Dynamics 365 Human Resources og andre økonomi- og driftsapper, bør du planlegge mer tid for validering for å sikre at dataene er riktig migrert til det nye miljøet. Migrering til den nye infrastrukturen vil flette dataene fra Human Resources-miljøet med økonomi- og driftsmiljøet ditt. Data i konflikt vil imidlertid kreve at brukere angir inndata for å avgjøre hvordan konflikten skal løses. Brukere og administratorer må administrere datatilordningene der det er konflikter, og teste migrering i sandkassemiljøer før migreringen av produksjonsmiljøer migreres.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisasjonen min bruker Human Resources-modulen i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Hva må vi planlegge for å migrere til den nye erfaringen?

For organisasjoner som bruker personalmodulen i økonomi- og driftsapper, blir den nye funksjonsfunksjonaliteten fra Dynamics 365 Human Resources brukt i miljøet gjennom standardprosessen for én versjonsoppdatering. Du kan forvente å se den nye funksjonaliteten i miljøet ditt etter hvert som den blir tilgjengelig i hver oppdatering. Du kan bruke Funksjonsbehandling til å aktivere nye funksjoner, men du bør planlegge å validere disse funksjonene. Følg prosessene du har på plass for å validere andre oppdateringer i miljøet. Hvis du vil ha mer informasjon om hvordan oppdateringer brukes på økonomi- og driftsapper, kan du se [Oversikt over én versjon](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Når blir organisasjonen migrert?

Migrering for hver organisasjon vil avhenge av den gjeldende konfigurasjonen og beredskapen for å migrere til den nye infrastrukturen. Disse datoene kan endres.

- Organisasjoner som bruker personalmodulen i økonomi- og driftsapper, vil motta personalfunksjonaliteten for Dynamics 365 Human Resources som en del av den vanlige oppdateringsprosessen for én versjon. Nye funksjoner skal vanligvis være tilgjengelige fra og med januar 2022.
- Organisasjoner som bare bruker Dynamics 365 Human Resources, vil ha tilgang til verktøy for migrering, slik at de kan begynne å teste og starte migreringen fra midten av 2022. Datoen da migreringen til den nye infrastrukturen må fullføres innen, er ennå ikke bestemt. Det vil imidlertid være minst ett år etter datoen da migreringsverktøy blir tilgjengelig.
- Organisasjoner som bruker både Dynamics 365 Human Resources og andre økonomi- og driftsapper, vil ha tilgang til verktøy for migrering, slik at de kan begynne å teste og starte migreringen fra sent i 2022. Datoen da migreringen til den nye infrastrukturen må fullføres innen, er ennå ikke bestemt. Det vil imidlertid være minst ett år etter datoen da migreringsverktøy blir tilgjengelig.

Hvis du vil ha mer informasjon om de nye funksjonene for Dynamics 365 Human Resources, kan du se [Nyheter eller endringer i Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Organisasjonen min er fortsatt ikke aktivert i Dynamics 365 Human Resources. Skal vi aktivere Human Resources-modulen i økonomi- og driftsappene eller med Dynamics 365 Human Resources-appen i den eldre infrastrukturen?

Viktige elementer du må vurdere er hvilke personalfunksjoner som er nødvendige, og når denne funksjonaliteten vil være tilgjengelig på den nye infrastrukturen. Hvis organisasjonen trenger kjernefunksjonaliteten for personaladministrasjon, er den for øyeblikket tilgjengelig i personalmodulen med økonomi- og driftsappene for den nye infrastrukturen. Funksjonsparitet mellom personalmodulen i økonomi- og driftsappene og Dynamics 365 Human Resources-appen er forventet i 10.0.25-versjonen, som er planlagt å være tilgjengelig i mars 2022. Integreringsfunksjoner som Teams-appen og Dataverse-enhetsintegrasjonene, vil være tilgjengelige i senere versjoner.

Hvis personalfunksjonaliteten for organisasjonen må være tilgjengelig i den nye infrastrukturen innen tidsrammen organisasjonen vil gå live i, kan det være enklere å gå live i Human Resources-modulen i økonomi- og driftsappene. Dette vil føre til en enklere migrering, fordi det vil være en standard appoppgradering til Dynamics 365 Human Resources-appen, og kunden vil allerede være i den nye infrastrukturen. Hvis organisasjonen bestemmer seg for å aktivere Dynamics 365 Human Resources-appen i den eldre infrastrukturen, kreves det en migrering av miljøet for å flytte til den nye infrastrukturen. Du kan unngå dette ved å aktivere i den nye infrastrukturen.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Jeg bruker nye funksjoner som bare er tilgjengelige i Dynamics 365 Human Resources (som **Permisjon og fravær** og **Fordelsadministrasjon**). Vil disse funksjonene nå være tilgjengelige i Human Resources-modulen i økonomi- og driftsinfrastrukturen også?

Ja, alle modulene fra Dynamics 365 Human Resources fungerer som i økonomi- og driftsapper, og det er 100 prosent funksjonsparitet. Som en del av den overordnede migreringsstrategien for kunder som for øyeblikket bruker disse funksjonene i Human Resources, vil kundedata migreres slik at de fortsetter å arbeide med økonomi- og driftsinfrastrukturen.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Jeg bruker de nye Dynamics 365 Human Resources-fordelsadministrasjonsfunksjonene. Jeg har bygd egendefinerte integrasjoner med personalmodulen på økonomi- og driftsinfrastrukturen slik at jeg kan dra nytte av lønnsfunksjonene ved å bruke fordelsdata. Vil disse egendefinerte integrasjonene være nødvendige fremover?

Som en del av infrastrukturflettingen blir personaldata hentet inn i den samme databasen som andre økonomi- og driftsapper. Integrering mellom moduler i økonomi- og driftsapper er ikke lenger påkrevd.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Organisasjonen min bruker én eller flere ISV-løsninger med Dynamics 365 Human Resources. Vil ISV-løsningene våre migreres automatisk?

Migreringserfaringen for hver uavhengige programvareleverandørløsning (ISV) vil variere, avhengig av integreringsmetoden for løsningen. Microsoft vil arbeide nøye med ISV-er for å sikre en problemfri overgang til den nye infrastrukturen.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisasjonen min bruker LinkedIn Talent Hub-integrering med Dynamics 365 Human Resources. Vil denne integreringen fortsette å fungere etter at infrastrukturendringen er fullført?

Nei, LinkedIn Talent Hub-integreringen vil ikke fungere etter migreringen til den nye infrastrukturen. Tjenesten for LinkedIn Talent Hub-integreringen vil bli trukket tilbake med den eldre Dynamics 365 Human Resources-infrastrukturen.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisasjonen min bruker Human Resources-appen for Teams. Vil appen fortsette å fungere etter at infrastrukturendringen er fullført?

Ja, Human Resources-appen for Teams fortsetter å fungere etter migreringen til den nye infrastrukturen.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Organisasjonen min har konfigurert egendefinert sikkerhet i Dynamics 365 Human Resources. Vil tilpasset sikkerhet fortsatt brukes etter at infrastrukturendringen er fullført?

Ja, egendefinerte sikkerhetskonfigurasjoner blir inkludert i dataoverføringen til den nye infrastrukturen.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Vi bruker dataintegrator til å flytte data mellom Dynamics 365 Human Resources og økonomi- og driftsapper. Hvordan berøres dataene som integreres i øyeblikket?

Personaldata som for øyeblikket er i Dynamics 365 Human Resources, synkroniseres med Dataverse. Dataintegrator kan deretter brukes til enveis synkronisering med økonomi- og driftsapper. Etter migrering til den nye infrastrukturen, vil personaldata være integrert i økonomi- og driftsappene. Dataintegratoren vil ikke lenger være nødvendig for å synkronisere dataene mellom økonomi- og driftsapper og Human Resources.

De gjeldende interne Dataverse-tabellene for Human Resources vil fortsette å synkronisere dataene fra miljøet på den nye infrastrukturen. Enhetene vil bli konvertert til å støtte dobbel skriving. Alle andre dataintegreringer som konfigureres via Dataintegrator mot disse tabellene for andre Dynamics 365-apper, vil fortsette å fungere slik de er konfigurert for øyeblikket.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Vi bruker dobbel skriving til å flytte personaldata mellom Dataverse og andre økonomi- og driftsapper. Hvordan påvirkes dataene som blir integrert i øyeblikket av migrering til den nye infrastrukturen?

Personaldata blir integrert i økonomi- og driftsapper i miljøet i den nye infrastrukturen. Dobbel skriving vil brukes til å flytte personaldata mellom det nye miljøet og Dataverse-miljøet.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Vi har bygd egendefinerte integrasjoner fra Dynamics 365 Human Resources til én eller flere eksterne systemer. Må vi utvikle nye integreringer etter at infrastrukturendringen er fullført?

Det avhenger av integreringens sluttpunkt. Hvis du vil ha mer informasjon om integreringsteknologi som er tilgjengelig i økonomi- og driftsapper, og hvordan du velger den beste integreringsteknologien, kan du se [Integreringsoversikt](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Vi har utvidet Dataverse for Dynamics 365 Human Resources. Vil disse utvidelsene migreres automatisk?

Hvis Dynamics 365 Human Resources og økonomi- og driftsmiljøer som skal sammenkobles i miljøet i den nye infrastrukturen, er koblet til det samme Dataverse-miljøet, vil de to appene fortsette å være koblet til det samme Dataverse-miljøet etter migreringen. Ingen migrering kreves for Dataverse-utvidelser.

Hvis derimot Dynamics 365 Human Resources og økonomi- og driftsmiljøer for øyeblikket er koblet til separate Dataverse-miljøer, må de to Dataverse-miljøene kombineres slik at de er koblet til ett enkelt miljø i den nye infrastrukturen. For denne Dataverse-migreringen kan Dataverse-tabellene som er standard i Human Resources-løsningene, kobles til og synkroniseres på nytt med det nye Dataverse-miljøet. Eventuelle utvidelser i Dataverse-miljøet vil ikke migreres automatisk, men må legges til i det nye miljøet på nytt. Vi anbefaler at du bruker administrerte løsninger til å administrere Dataverse-tilleggene. Hvis du vil ha mer informasjon, kan du se [Innføring i løsninger](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>Vi har brukt funksjonaliteten for egendefinerte felt i Dynamics 365 Human Resources, vil disse egendefinerte feltene migrere automatisk?
Ja, de egendefinerte feltene som er lagt til, vil migrere til den nye infrastrukturen.

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Vi har konfigurert Microsoft Power Automate-flyter og/eller Microsoft Power Apps til å fungere med Dynamics 365 Human Resources. Vil disse Microsoft Power Platform-komponentene migreres og fungere automatisk etter at infrastrukturendringen er fullført?

Power Apps, Power Automate-flyter og andre Microsoft Power Platform-tilpasninger ligner på Dataverse-utvidelser. Om de fungerer automatisk etter migrering til den nye infrastrukturen, avhenger av om Human Resources -appen og økonomi- og driftsappene er koblet til det samme Power Apps-miljøet før migreringen.

Hvis appene for øyeblikket er koblet til det samme Power Apps-miljøet, vil de fortsette å være koblet til det Power Apps-miljøet etter migreringen til den nye infrastrukturen. I dette tilfellet vil Power Apps, Power Automate-flyter og andre Microsoft Power Platform-tilpasninger fortsette å fungere uten tilleggskonfigurasjoner. Vi anbefaler at du bruker administrerte løsninger til å administrere programtilleggene på Dataverse. Hvis du vil ha mer informasjon, kan du se [Innføring i løsninger](/powerapps/developer/data-platform/introduction-solutions).

Hvis imidlertid Human Resources-appen og økonomi- og driftsappene er koblet til separate Power Apps-miljøer, må de kombineres som en del av migreringen. Denne oppgaven krever at alle Power Apps- og andre tilpasninger blir publisert på nytt i det nye miljøet.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Vi har aktivert virtuelle Dataverse-tabeller for Dynamics 365 Human Resources. Hva vil skje med disse tabellene under migrering?

Etter migreringen, hvis miljøet på den nye infrastrukturen fortsatt er koblet til Dataverse-miljøet som for øyeblikket er koblet til Dynamics 365 Human Resources, vil virtuelle Dataverse-tabeller som er generert i det miljøet, fortsatt fungere uten tilleggskonfigurasjon.

Hvis miljøet på den nye infrastrukturen er koblet til et annet Dataverse-miljø etter migreringen, må imidlertid de virtuelle tabellene genereres på nytt i det nye Dataverse-miljøet.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Vi har utviklet en integrasjon ved hjelp av søkersporingssystemet (AST), API, Lønns-API, virtuelle Dataverse-tabeller for Dynamics 365 Human Resources, eller andre enheter i Dataverse-web-APIen. Vil disse integreringene fortsette å fungere etter at infrastrukturendringen er fullført?

Etter migreringen, hvis miljøet på den nye infrastrukturen fortsatt er koblet til Dataverse-miljøet som for øyeblikket er koblet til Dynamics 365 Human Resources, vil integreringer som er utviklet mot Dataverse-web-API, fortsatt fungere etter at migreringen er fullført.

Hvis miljøet på den nye infrastrukturen er koblet til et annet Dataverse-miljø etter migrering, må integreringer som er utviklet mot Dataverse-web-API, konfigureres slik at de kobler til det nye Dataverse-miljøet.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Har det innvirkning på Azure-området når miljøet mitt migreres?

Det forventes at Human Resources-miljøet vanligvis vil forbli i det samme Azure-området under migreringen. Det eneste unntaket er hvis Human Resources-miljøet blir flettet med et økonomi- og driftsmiljø som er i et annet område. I dette tilfellet blir Human Resources-miljøet migrert til Azure-området for økonomi- og driftsmiljøet.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Organisasjonen min avhenger av arbeidsflyt i Dynamics 365 Human Resources for ett eller flere forretningsprosesser. Vil disse arbeidsflytetene migreres automatisk?

Ja, arbeidsflytkonfigurasjoner, arbeidsflytlogg og gjeldende arbeidsflyter i arbeid blir migrert.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Hvilke opplæring og ressurser vil være tilgjengelige for å hjelpe til med migreringsprosessen?

Du finner fullstendig dokumentasjon for å beskrive hvert trinn i migreringsprosessen i detalj. Tilleggsressurser for opplæring, for eksempel opplæring og workshops, kan også være tilgjengelige, avhengig av behovet.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Organisasjonen min har opprettet lagrede visninger i Dynamics 365 Human Resources for å forbedre grensesnittets anvendelighet. Vil disse lagrede visningene migreres automatisk?

Ja, lagrede visninger migreres til den nye infrastrukturen.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Vi bruker Ceridian med Dynamics 365 Human Resources. Vil Ceridian-integreringen være tilgjengelig etter at infrastrukturendringen er fullført? 

Integreringen med Ceridian vil bli migrert til lønns-API-basert integrering. Den filbaserte integreringen som for øyeblikket finnes i Dynamics 365 Human Resources, vil ikke bli migrert til økonomi- og driftsinfrastrukturen. Hvis du vil ha mer informasjon, kan du se [Innføring i lønns-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Hvordan vil migreringen påvirke oppdateringsprosessen for service?

Etter migreringen vil kundene ha mye mer fleksibilitet når det gjelder ALM- og serviceoppdateringer. Serviceoppdateringer brukes ikke lenger automatisk i Human Resources-miljøer. I stedet vil tjenesten følge prosesser og funksjonalitet for oppdatering av én versjonstjeneste. Derfor vil konfigurasjonsalternativer for oppdateringer bli tilgjengelige via LCS. Hvis du vil ha mer informasjon, kan du se [Oversikt over én versjon](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Hvordan påvirker migreringene LCS-prosjektet for Dynamics 365 Human Resources?

Migrering til den nye infrastrukturen vil flytte styringen av Dynamics 365 Human Resources-miljøene dine til et implementeringsprosjekt av økonomi og drift i LCS. Hvis migreringen fletter Dynamics 365 Human Resources med et eksisterende økonomi- og driftsmiljø, vil Human Resources LCS-prosjektet flettes til LCS-implementeringsprosjektet for økonomi- og driftsappen. Hvis du for øyeblikket bare bruker Dynamics 365 Human Resources, opprettes det et nytt LCS-implementeringsprosjekt, og det eksisterende Human Resources LCS-prosjektet vil bli migrert til det nye prosjektet.

Det nye prosjektet vil være av samme type prosjekt som økonomi- og driftsapper bruker. Det vil ha de samme funksjonene og funksjonaliteten for miljøadministrasjon. Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Vi har koblet oppgaveregistreringene til forretningsprosessmodellereren i Human Resources. Hvordan migreres og flettes forretningsprosessmodellereren inn i LCS?

Forretningsprosessbibliotek for LCS-prosjektet vil bli migrert til det nye LCS-prosjektet for Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Organisasjonen bruker i øyeblikket bare Dynamics 365 Human Resources. Hvilke ressurser er tilgjengelige slik at vi kan lære mer om utviklingsfunksjonene etter at infrastrukturendringen er fullført?

Både Microsoft Power Platform-utvidbarhetsalternativer og utvidbarhetsalternativer for økonomi og drift vil være tilgjengelige, og kan brukes i utvikling. Hvis du vil ha mer informasjon, kan du se [Utvikle og tilpasse hjemmesiden](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Vi har aktivert funksjoner i Dynamics 365 Human Resources. Vil disse funksjonene aktiveres automatisk under migrering?

Om en funksjon aktiveres automatisk i den nye infrastrukturen, bestemmes enkeltvis for hver funksjon. Denne informasjonen vil bli inkludert i dokumentasjonen til funksjonen.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Hva skjer med BYOD-databasen min under migrering?

Importer og eksporter konfigurasjoner for å ta med din egen database (BYOD) vil bli migrert til den nye infrastrukturen.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Hva skjer med Azure Data Lake under migrering?

Enhver eksport som for øyeblikket er konfigurert for Azure Data Lake Storage i økonomi- og driftsapper, vil opprettholde samme konfigurasjon etter migrering.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Vi bruker Dynamics AX 2012 for øyeblikket. Vil oppgraderingsverktøyene som for øyeblikket er tilgjengelige, brukes til å oppgradere HR-modulen i AX 2012 til Dynamics 365 Human Resources?

Ja. Dynamics 365 Human Resources vil bli inkludert i den flettede kodebasen og infrastrukturen for økonomi- og driftsapper. En oppgradering fra Dynamics AX 2012 til Dynamics 365 Human Resources vil bruke den samme oppgraderingsbanen og det samme verktøyet som brukes til å oppgradere til den nyeste versjonen av økonomi- og driftsapper.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Vi bruker dokumentbehandling med Dynamics 365 Human Resources. Hva vil skje med dokumentene under migrering?

Dokumentene vil fortsatt være i den eksisterende dokumentlagringen. De vil bli tilordnet på nytt til miljøet i den nye infrastrukturen.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Hva skjer med de satsvise jobbene vi har konfigurert i Dynamics 365 Human Resources etter migrering?

Gjeldende satsvise jobber blir migrert automatisk til den nye infrastrukturen.

## <a name="licensing-impact"></a>Lisensieringseffekt

Denne dokumentasjonen erstatter ikke noe av den juridiske dokumentasjonen som dekker bruksrettigheter.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Organisasjonen bruker Dynamics 365 Human Resources til å administrere personaloperasjonene. Endres lisensene eller kostnadene våre?

Kunder som har kjøpt Dynamics 365 Human Resources-lisenser, berøres ikke. Det er ingen lisensieringsoverføring for disse kundene. Den ekstra SKU-enheten (sandbox stock keeping unit) som var spesifikk for Human Resources, vil ikke lenger være tilgjengelig. I stedet kan kundene velge å kjøpe et sandkassemiljø for økonomi og drift med lag 2 til en litt lavere pris. Eksisterende kunder som har kjøpt en Human Resources-sandkasse, blir migrert til et sandkassemiljø for økonomi og drift med lag 2 uten ekstra kostnad.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Organisasjonen min bruker Human Resources-modulen i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Endres lisensene eller kostnadene mine?

Eksisterende brukere av Dynamics 365-apper og brukere av frittstående Dynamics 365 Finance, Supply Chain Management, Commerce og Project Operations kan få tilgang til Human Resources som en del av disse lisensene frem til februar 2025 eller inntil den gjeldende lisensavtalen utløper, avhengig av hvilken som er tidligere. Du kan velge å flytte til Human Resources-lisenser tidligere hvis det hjelper deg med å oppnå bedre kostnadsspareringer. Fra og med februar 2025 må alle eksisterende CSP- og EA-kunder rulle av Human Resources-modulen og kjøpe Human Resources-lisenser for å dra nytte av de nye funksjonene som blir hentet til økonomi- og driftsappene.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Organisasjonen min brukes direkte med Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Er vi pålagt å kjøpe et tilleggsmiljø for å støtte sammenslåing av infrastruktur?

Tilleggsmiljøer kreves ikke for å støtte infrastrukturendring.

