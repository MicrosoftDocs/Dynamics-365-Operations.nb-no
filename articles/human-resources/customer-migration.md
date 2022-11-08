---
title: Vanlige spørsmål om kundeoverføring i Human Resources
description: Denne artikkelen svarer på vanlige spørsmål om overføringen av Microsoft Dynamics 365 Human Resources til den sammenslåtte infrastrukturen i Finance and Operations.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734365"
---
# <a name="human-resources-customer-migration"></a>Kundeoverføring i Human Resources

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Hvordan skal Dynamics 365 Human Resources-kunder planlegge å flytte til infrastrukturen i Finance and Operations?

To kategorier av Microsoft Dynamics 365 Human Resources-kunder blir påvirket og må foreta endringer for å sikre at de får den siste Finance and Operations-infrastrukturen:

- Kunder som bruker Dynamics 365 Human Resources og ikke har noen andre driftsapper fra Dynamics 365
- Kunder som bruker både Dynamics 365 Human Resources og Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce eller Dynamics 365 Project Operations

Uansett hvilken kategori de tilhører, må kundene flytte data til et nyopprettet miljø i Finance and Operations-infrastrukturen og validere at sammenslåingen er fullført.

Fremover vil Dynamics 365 Human Resources-appen ha sitt eget Finance and Operations-miljø som er atskilt fra andre driftsapper. På denne måten kan kunder dra nytte av alternativer for utvidbarhet uten å måtte slå sammen gjeldende data. Microsoft vil tilby verktøy og et sandkassemiljø som kunder kan bruke til å teste og validere dataoverføringen, før de flytter til et produksjonsmiljø. Verktøyene vil aktivere en tilnærmet automatisert prosess, og vil være tilgjengelig mellom august og november 2022.

Kunder som bruker andre apper i Finance and Operations-infrastrukturen, kan slå sammen Human Resources-dataene med et eksisterende miljø. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Når blir kunder flyttet til infrastrukturen i Finance and Operations?

Overgangen for hvert firma er avhengig av firmaets gjeldende konfigurasjon og beredskap for å flytte til Finance and Operations-infrastrukturen. Vi anbefaler at kundene samarbeider med Microsoft-partneren for å finne den beste banen fremover.

- Organisasjoner som bruker **Human Resources**-modulen i Dynamics 365 Finance, kan aktivere nye funksjoner fra Dynamics 365 Human Resources som en del av den vanlige oppdateringsprosessen for én versjon. Nye funksjoner skal vanligvis være tilgjengelige fra og med januar 2022.
- Organisasjoner som bruker Dynamics 365 Human Resources, har tilgang til verktøy som de kan bruke til å fullføre sammenslåingen av infrastrukturen. Microsoft vil samarbeide med kunder om overgangen for å forhindre avbrudd i tjenesten. Kundene får 12 måneder på seg til å foreta overgangen, fra tidspunktet da overføringsverktøyet blir tilgjengelig.
- Organisasjoner som bruker både Dynamics 365 Human Resources og **Human Resources**-modulen, kan flytte sin frittstående Human Resources-infrastruktur til Finance and Operations-infrastrukturen. Et annet alternativ er å bruke sammenslåingsverktøyene til å bringe miljøer inn i et enkelt miljø. Det er ingen krav eller tidsramme for sammenslåing av de to miljøene.

Hvis du vil ha oppdatert informasjon, kan du kontrollere [lanseringsplanene](/dynamics365/release-plans/) regelmessig.

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Trenger kundene fortsatt egendefinerte integrasjoner mellom Dynamics 365 Human Resources og Human Resources-modulen?

- Kunder som har både Dynamics 365 Human Resources og andre Finance and Operations-infrastrukturmiljøer som for øyeblikket er integrert , må fortsette å integrere de to miljøene etter sammenslåingen.
- Kunder som velger å holde Dynamics 365 Human Resources-miljøet atskilt fra sitt eksisterende miljø for økonomi- og driftsapper, må fortsette å integrere miljøene for å gjøre dataene tilgjengelige i begge miljøene.
- Kunder kan fortsette å bruke dataintegratoren til å kopiere data mellom de to miljøene. Kunder som slår sammen data i ett enkelt miljø etter migrering, trenger ikke lenger å integrere dataene, fordi alle dataene vil være i én enkelt database.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Vil kundenes ISV-løsninger migreres automatisk?

Migreringserfaringen for hver uavhengige programvareleverandørløsning (ISV) vil variere, avhengig av integreringsmetoden for løsningen. Microsoft vil arbeide nøye med ISV-er for å sikre en problemfri overgang til Finance and Operations-infrastrukturen. Mange ISV-løsninger er bygd på Dataverse ved hjelp av funksjoner i Microsoft Power Platform. Disse løsningene avhenger av Dataverse-integreringen mellom Dynamics 365 Human Resources-miljøet og Dataverse-miljøet. Dataverse-integreringen er i ferd med å avskrives som en del av sammenslåingen av infrastrukturen. I Finance and Operations-infrastrukturen planlegges det at nye tilordninger for dobbel skriving skal erstatte funksjonaliteten til Dataverse-integreringen.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Hvordan påvirkes dataintegreringen som flytter data mellom Dynamics 365 Human Resources og andre Dynamics 365-apper?

Når kundene har flyttet til Finance and Operations-infrastrukturen, må de fortsette å integrere data mellom de to miljøene. Kundene kan fortsette å bruke dataintegratoren til å utføre disse datamigreringsoppgavene. Kunder som planlegger å holde Dynamics 365 Human Resources-miljøet atskilt fra sitt eksisterende miljø for økonomi- og driftsapper, må fortsette å integrere data mellom de to miljøene. For kunder som slår sammen de to miljøene til ett enkelt miljø, er det ikke lenger nødvendig å integrere mellom de to miljøene.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Hvoradn blir data flyttet mellom Dynamics 365 Human Resources i Finance and Operations-infrastrukture og Dataverse etter migreringen?

Den nåværende Dataverse-integreringen mellom Dynamics 365 Human Resources og Dataverse blir avskrevet som en del av Finance and Operations-infrastrukturen. Det finnes planer om å introdusere tilordninger av dobbel skriving for å tilordne økonomi- og driftsenhetene til Dataverse-tabellene. Kundene må bestemme hvilke tilordninger for dobbel skriving som kreves for implementeringen. Vi anbefaler at virtuelle tabeller brukes til integreringer og ISV-løsninger, med mindre det fines et bestemt forretningsmessig behov for at dataene må dupliseres i Dataverse for å kjøre forretningslogikk.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Hvordan påvirker migreringen Dataverse -utvidelser for Dynamics 365 Human Resources?

Kunder må migrere til et sandkassemiljø før de migrerer produksjonsmiljøet. Når kunder migrerer sandkassemiljøet, må de lage en kopi av Dataverse-miljøet for å koble seg til det nye overførte Finance and Operations-miljøet. Vi anbefaler at en kunde kopierer både dataene og løsningene for miljøet, slik at de samsvarer med kundens gjeldende produksjonsmiljø.

Når kunder er klare til å migrere Dynamics 365 Human Resources-produksjonsmiljøet, migrerer Microsoft automatisk databasen og Azure Blob Storage. Den migrerte databasen og lagringen vil peke det nye miljøet i Finance and Operations-infrastrukturen til det samme Dataverse-produksjonsmiljøet. Før dataene kan fortsette å kopieres til Dataverse, må kundene aktivere alle tilordninger av dobbel skriving som kreves for integreringene, tilleggene og ISV-løsningene som er bygd på Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Vil Microsoft Power Platform-komponenter som er utviklet for Dynamics 365 Human Resources, automatisk fungere etter at migreringen av infrastrukturen er fullført?

Apper som opprettes i Power Apps, flyter som opprettes i Power Automate, og andre Microsoft Power Platform-tilpasninger, er som Dataverse-utvidelser. Under migreringen av kundeproduksjonsmiljøer har det ingen innvirkning på Dataverse-miljøer, inkludert eventuelle utvidelser. Apper, flyter og andre Microsoft Power Platform-tilpasninger skal fortsette å fungere uten at det kreves tilleggskonfigurasjon.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Hva vil skje med virtuelle Dataverse-tabellenheter for Dynamics 365 Human Resources under migreringen?

Når kunder migrerer Dynamics 365 Human Resources-miljøet sitt til Finance and Operations-infrastrukturen, vil miljøet forbli koblet til Dataverse-miljøet som for øyeblikket er koblet til Dynamics 365 Human Resources. De virtuelle Dataverse-tabellene som er generert i miljøet, vil fortsette å fungere uten at det kreves noen tilleggskonfigurasjon. Det kan hende at de virtuelle tabellene må genereres på nytt i Dataverse-miljøet som er koblet til kundens eksisterende Finance and Operations-miljø.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Hvordan vil en integrering som bruker API-en for Applicant Tracking System (ATS), API-en for Payroll, virtuelle Dataverse-tabeller for Dynamics 365 Human Resources eller andre enheter i web-API-en for Dataverse, fungere etter at sammenslåingen av infrastrukturen er fullført?

Når kunder migrerer Dynamics 365 Human Resources-miljøet sitt til Finance and Operations-infrastrukturen, vil miljøet forbli koblet til Dataverse-miljøet som for øyeblikket er koblet til Dynamics 365 Human Resources. Alle integrasjoner som ble utviklet mot web-API-en for Dataverse, vil fortsette å fungere etter at migreringen er fullført.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Organisasjonen vår har konfigurert egendefinert sikkerhet i Dynamics 365 Human Resources. Vil dette fortsatt brukes etter at infrastrukturmigreringen er fullført?

Ja, egendefinerte sikkerhetskonfigurasjoner blir inkludert i dataoverføringen.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vil arbeidsflyter i Dynamics 365 Human Resources migreres automatisk?

Ja, arbeidsflytkonfigurasjoner, arbeidsflytlogg og gjeldende arbeidsflyter i arbeid blir migrert til den sammenslåtte infrastrukturen.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vil lagrede visninger i Dynamics 365 Human Resources migreres automatisk?

Ja, lagrede visninger migreres til den sammenslåtte infrastrukturen.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Vil funksjoner som er aktivert i Dynamics 365 Human Resources automatisk, være tilgjengelige etter sammenslåingen av infrastrukturen?

- For kunder som bruker **Human Resources**-modulen, vil funksjoner som bare er tilgjengelige i Dynamics 365 Human Resources, administreres gjennom funksjonsadministrasjon. Vanligvis blir ikke disse funksjonene aktivert som standard. Alle funksjoner som må aktiveres som standard, vil bli dokumentert.
- For kunder som bruker Dynamics 365 Human Resources, vil funksjoner være tilgjengelige i infrastrukturen. Alle funksjoner som ikke er tilgjengelige, vil bli dokumentert. Hver funksjonsbehandlingsnøkkel som er aktivert i det gjeldende Dynamics 365 Human Resources-miljøet, blir aktivert i den sammenslåtte infrastrukturen. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Hva skjer med BYOD-databaser under migreringen?

Importer og eksporter konfigurasjoner for å ta med din egen database (BYOD) vil bli migrert til Finance and Operations-infrastrukturen.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Har det innvirkning på Azure-området når kundemiljøet migreres?

Dynamics 365 Human Resources-miljøet vil forbli i det samme Azure-området for migreringen. Hvis det er et krav om å flytte et miljø til et annet Azure-område, må kundene følge standardtrinnene for å migrere til et nytt område etter at migreringen er fullført.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Hva skjer med Azure-datasjøer under migreringen?

Enhver eksport som for øyeblikket er konfigurert for Azure Data Lake i økonomi- og driftsapper, vil opprettholde samme konfigurasjon etter migrering.

> [!NOTE]
> Tilordninger for dobbel skriving må være aktivert for å fortsette å skrive data fra Human Resourece-miljøet til Dataverse.

Kunder som ønsker å eksportere Human Resources-data til datasjøen, kan aktivere denne funksjonen etter at migreringen til Finance and Operations-infrastrukturen er fullført. Hvis du vil ha mer informasjon, kan du se [Datasjøer - Azures arkitektursenter](/azure/architecture/data-guide/scenarios/data-lake).

Kunder kan koble flere Finance and Operations-miljøer til samme datasjø. Hvert miljø vil imidlertid peke til en annen mappe og beholder. Kunder som planlegger å slå sammen miljøer senere, bør planlegge tilnærmingen nøye.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Hvilken migrering vil være nødvendig hvis en kunde for tiden bruker Human Resources-modulen?

Kunder som bruker **Human Resources**-modulen, vil få den nye funksjonaliteten fra Dynamics 365 Human Resources brukt i miljøet sitt gjennom standardprosessen for én versjonsoppdatering. Kundene kan forvente å se den nye funksjonaliteten i miljøet sitt etter hvert som den blir tilgjengelig i hver oppdatering. Kundene kan bruke funksjonsbehandling til å aktivere funksjonene. Kundene bør planlegge å validere disse nye funksjonene ved hjelp av prosessene de allerede har på plass og bruker til å validere andre oppdateringer i miljøet.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Hva vil skje med egendefinerte integrasjoner med eksterne systemer?

Kundene må migrere integreringen i Finance and Operations-miljøet. Siden dette miljøets endepunkt er forskjellig, kan det hende at kundene må oppdatere eller endre integreringene slik at de peker til det nye miljøet. Denne oppgaven vil primært være en manuell prosess, og endringene som kreves, vil avhenge av integreringens arkitektur. Kundene bør samarbeide med Microsoft-partneren sin for å finne beste metode for å flytte integrasjoner.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Hva skjer med Microsoft Power Platform-utvidelser (Dataverse) hvis kunder slår sammen et Dynamics 365 Human Resources miljø med et eksisterende Finance and Operations-miljø?

Hvis kundene bestemmer seg for å slå sammen et Dynamics 365 Human Resources-miljø og et eksisterende Finance and Operations-miljø til én enkelt Dataverse-forekomst etter migreringen, må Dataverse-miljøene kombineres som en del av sammenslåingsprosessen. Denne oppgaven krever at alle apper som er opprettet med Power Apps, og alle andre tilpasninger, blir distribuert på nytt i det nye miljøet.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Hva vil skje med dokumenter under migrering?

Når kunder migrerer Dynamics 365 Human Resources-miljøet til Finance and Operations-infrastrukturen, forblir dokumentene i den eksisterende dokumentlagringen, og de vil automatisk bli tilordnet det nye miljøet i Finance and Operations-infrastrukturen.

I en fremtidig versjon vil det bli angitt nye dataenheter. Etter at endringen er gjort, vil kunder som velger å slå sammen Dynamics 365 Human Resources-miljøet med et eksisterende Finance and Operations-miljø, kunne eksportere dokumenter og flytte dem til det eksisterende miljøet.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Etter migreringen, hva skjer med de satsvise jobbene som ble konfigurert i Dynamics 365 Human Resources?

Satsvise jobber må konfigureres på nytt i Finance and Operations-miljøet. Kundene må evaluere hver satsvise jobb og sammenligne den med den gjeldende listen over satsvise jobber i Finance and Operations-miljøet. Kundene bør også analysere den helhetlige satsvise planen når de slår sammen de to settene med satsvise jobber, for å finne ut om det skal gjøres endringer i den satsvise planen, prioriteten eller de satsvise gruppene.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Hvordan påvirker migreringen LCS-prosjektet for Dynamics 365 Human Resources?

Kundene må opprette et nytt Microsoft Dynamics LCS-prosjekt (Lifecycle Service), og de må velge økonomi- og driftsapper som produkt og **Implementering** som prosjekttype. I tillegg er et nytt felt for underprosjekttypen tilgjengelig når det opprettes et LCS-prosjekt. Kundene må velge alternativet for Dynamics 365 Human Resources-migrering for å migrere et eksisterende LCS-prosjekt i Human Resources til Finance and Operations-infrastrukturen.

Funksjonene i LCS-prosjekter i Finance and Operations er forskjellige fra funksjonene i LCS-prosjekter i Human Resources.

For at nye kunder skal bli aktive, må de følgende oppgavene utføres:

- Fullfør prosjektpålasting.
- Fullfør metodikken.
- Fyll ut en abonnementsberegner.
- Fullfør klargjøringsprosessen for å bli aktivert.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Hvordan migreres forretningsprosessmodellereren?

Kundene må eksportere forretningsprosessmodellerbiblioteket fra LCS-prosjektet i Human Resources og importere det til LCS-prosjektet Finance and Operations. I tillegg må kundene oppdatere hjelpeinnstillingene i appen slik at de peker til det nye LCS-prosjektet.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Hvordan vil tjenesteoppdateringsprosessen bli påvirket av migreringen?

Etter migreringen vil kundene ha mye mer fleksibilitet når det gjelder administrasjon av livssyklus for apper (ALM) og tjenesteoppdateringer. Tjenesteoppdateringer brukes ikke lenger automatisk i Human Resources-miljøer. I stedet vil tjenesten følge prosessene og funksjonaliteten for oppdatering av én versjonstjeneste, og konfigurasjonsalternativer for oppdateringer via LCS blir aktivert.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Vil kunder ha rett på FastTrack-hjelp i forbindelse med sammenslåingen av infrastrukturen?

Microsoft definerer fremdeles hvilke verktøy og ressurser som vil være tilgjengelige fra FastTrack for å hjelpe til med sammenslåingen.

## <a name="licensing-impact"></a>Lisensieringseffekt

Hvis du vil ha mer informasjon om hvordan lisensiering påvirkes, kan du se [Sammenslåing av Dynamics 365 Human Resources-infrastrukturen](hr-infrastructure-merge.md#licensing).
