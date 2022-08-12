---
title: Vanlige spørsmål om integrasjon med Finance
description: Denne artikkelen beskriver hvilke data som synkroniseres i en integrasjon med Human Resources og Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f57e995dfcc04de8384d15f238c45290b3c3cbd
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067624"
---
# <a name="integration-with-finance-faq"></a>Vanlige spørsmål om integrasjon med Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Denne artikkelen gir svar på vanlige spørsmål som er tilknyttet hvilke data som synkroniseres når Dynamics 365 Human Resources er integrert med Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Kan jeg redigere Dynamics 365 Talent-appbrukeren i Power Apps?

Nei Hvis du redigerer Human Resources-appbrukeren, kan integreringen mellom Human Resources og Dataverse mislykkes. Følgende tabell viser standardinnstillingene for Talent-appbrukeren.

| Fullt navn | App-ID | Objekt-ID for Azure AD | URI for app-ID |
| --- | --- | --- | --- |
| Dynamics365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Standardinnstillinger for Talent-appbruker.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Er alle data synkronisert eller bare noen dataenheter?

Et delsett av dataene synkroniseres. Hvis du vil ha en liste over alle enheter, kan du se [Integrering med Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Hvorfor ser jeg ingen data synkronisert til Dataverse?

Som standard er Dataverse-integreringen deaktivert i nye miljøer som ikke inneholder demodataene. Som standard er den slått på i nye miljøer som inneholder demonstrasjonsdata, og datasynkronisering begynner når miljøet klargjøres. Når miljøet er klart til å synkronisere data, kan du aktivere integreringen. Hvis du vil ha mer informasjon, kan du se [Konfigurere Dataverse-integrasjon](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kan jeg opprette en ny tilordning uten å bruke malene?

Malene er startpunktet. Du kan opprette din egen mal, men en mal er alltid nødvendig når du oppretter et prosjekt for integrasjon. Hvis du vil ha mer informasjon om dataintegrator (DI), maler og prosjekter, kan du se [Integrere data til Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Kan jeg tilordne finansdimensjoner for å overføre mellom Human Resources og Finance?

Finansdimensjoner er ikke i Dataverse og er dermed ikke en del av standardmalen. Denne enheten er planlagt, men ingen tidslinje for frigivelse er for øyeblikket tilgjengelig.

For data som ligger i Finance, men ikke finnes i Human Resources, koble sammen de to systemene ved å bruke **Konfigurer koblinger** i Human Resources.

![Tilordne finansdimensjoner.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Noen ganger når jeg importerer ansatte, blir de inaktive arbeidere i Finance. Hvorfor?

Du kan få denne feilen hvis ansatte ikke har en aktiv ansettelsesdetaljpost i Human Resources. Hvis du vil løse dette problemet, kan du gå til **Personaladministrasjon \> Ansatte \> Ansettelseshistorikk \> Datobehandling**, og kontroller at det finnes en aktiv ansettelsesdetaljpost.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Hvis jeg velger å tilordne bare et delsett av feltene, vil endringer i ikke-tilordnede felt utløse en synkronisering?

Datasynkronisering følger tidsplanen for kjøring. Integreringen henter en post hvis et felt i posten endres, uansett om feltet er en del av integreringstilordning.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hvordan kan jeg sende bare aktive arbeiderendringer og ikke de avsluttede postene?

Ved hjelp av "Avansert spørring" kan du filtrere og endre kildedataene før de sendes til målet.

![Avansert spørring for aktive arbeidere.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Kan jeg angi hvilke felt som skal sendes til Finance for en bestemt enhet?

Feltene kan legges til eller fjernes fra integrasjonsoppgaven. Ikke alle datafelt som finnes i Dataverse-tabellen, fylles ut fra Human Resources.
Tilleggsdata fylles via Power Apps.

![Legge til eller fjerne felt fra en integrasjonsoppgave.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Jeg har satt opp integrasjon som en satsvis jobb, men Human Resources mistet forbindelsen til målsystemet. Hvordan kan jeg sende det samme settet med endringer til målsystemet?

Det kreves ingen spesielle oppsett for unntaksbehandling. Dataintegratoren finner og rapporterer feil som oppstår ved kilden og målet, og tillater nye manuelle forsøk. Den tillater imidlertid ikke manuell datakorrigering. Hvis dataoppdateringer kreves, skal dette skje enten ved kilden eller målet.

## <a name="can-i-set-up-bi-directional-integration"></a>Kan jeg konfigurere toveis integrasjon?

Nei, integrasjon er énveis (fra Human Resources til Finance and Operations). Det finnes imidlertid en standardmal som er tilgjengelig for å sende data fra Human Resources til Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kan jeg tillate sletting av oppføringer som en del av min integrasjon?

Nei, Dataintegrator registrerer ikke slettede poster for dataoverføring. Bare oppretting og oppdatering av data (UPSERT) er for øyeblikket inkludert.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kan jeg utføre kjøringen med feil på nytt? Sendes i så fall en fullstendig fil eller bare endringene?

Den første kjøringen av Dataintegrator er alltid en full kjøring. Senere kjøringer er basert på endringssporing. Når en feilkjøring utføres, trekker den ut postene i omfanget for kjøringen og sender ut de siste endringene fra Dataverse.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Når jeg lagrer prosjektet, får jeg feilen: "Prosjektet har tilordningsfeil." Hva gjør jeg?

Kontroller oppsettet for integrasjonsnøklene, foreta nødvendige endringer i oppsettet, og oppdater enhetene i prosjektet.

Når standardmalen brukes, blir nøklene for integrering automatisk importert. Dette problemet kan oppstå når nye aktiviteter legges til i den eksisterende malen.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Hvis jeg har N antall juridiske enheter der arbeidere har ansettelser, trenger jeg å opprette en tilordning for hver av dem?

Ja, for hver juridiske enhet i Finance må du ha et eget integrasjonsprosjekt i dataintegreringen.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Jeg vil overføre data som ikke er en del av standardmalen fra Microsoft. Kan jeg gjøre dette?

Ja, feltene kan legges til eller fjernes fra den eksisterende malen. Malen kan endres for å ta med flere data fra andre Dataverse-tabeller. Enheten må være i Dataverse for at den skal inkluderes i malen. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Jeg har nettopp opprettet nye Finance- og Human Resources-miljøer, og jeg får feilen "Dataverdien bryter integritetsbegrensninger." Hvorfor?

Årsaker til denne feilen kan omfatte:

- Dataoverføringen resulterte i duplisert postuttrekk ved kilden (Dataverse).

- Dataoverføringen har nullverdier for feltene som kreves i Finance and Operations. Kontroller at dataene er i Dataverse og oppfyller kravene fra Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Hvis det er kjøringsfeil og ansatt-ID-en ikke synkroniseres, hvordan kan jeg finne den historiske jobben som har feil ansattpost?

Dataintegratoren oppretter flere prosjekter i Finance. Relasjonen mellom Dataintegrator-oppgaven og Finance-prosjektet er én til én.

Spor tiden fra Dataintegrator-kjøringshistorikken, og se etter indeksen -1 i Finance. Hvis oppgavenummeret er 9 i Dataintegrator, er indeksen i Finance 8.

1. Lagre oppgaveindeksen fra Dataintegrator (i dette eksemplet er det "9").

    ![Lagre oppgaveindeksen fra Dataintegrator.](media/CaptureTaskIndex.png)

2. Spor kjøretiden for prosjektet.

    ![Spore kjøretiden for prosjektet.](media/CaptureTimeOfExecution.png)

3. Identifiser indeks -1 i Finance. I dette eksemplet samsvarer prosjektet med suffikset "8" og utførelsestiden for indeksen "0"-prosjektet med kjøretiden i trinn 2.

    ![Identifisere indeks.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Etter å ha integrert Human Resources og Finance, ser jeg ikke Human Resources-dataene mine i Finance. Hva gjør jeg?

Integreringen til Finance er en totrinns prosess. Først bekrefter du at Human Resources-dataene er oppdaterte og tilgjengelige i Dataverse. Dette er en nær sanntidssynkronisering og kan kontrolleres i Power Apps ved å se på dataene i datatabeller.

![Data i Dataverse.](media/DataInCDS.png)

Hvis dataene ikke vises som forventet i Dataverse, må du kontrollere at enheten støttes i integreringen. Hvis du vil inkludere flere data i Dataverse, må en endring utføres på Microsoft-siden.

Hvis enheten støttes og dataene er tilgjengelige i Dataverse, må du kontrollere tilordningen er riktig i Dataintegrator. Hvis integratoren ser ok ut, må du bekrefte at databehandlingsjobbene er kjørt. Feil kan oppstå under kjøring av satsvise jobber. Hvis du vil ha mer informasjon om Databehandling, kan du se [Databehandling](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Adressene til mine ansatte er feil når jeg importere dem til Finance. Hva gjør jeg?

Nummerserien for **Plasserings-ID** bruker samme mønster i både Human Resources og Finance. Nummerserien må være unik på begge sider, slik at det ikke finnes noen adressekollisjoner ved integrering av data fra Dataverse til Finance and Operations.

Under implementering av Human Resources må du kontrollere at nummerseriene ikke er de samme i Human Resources og Finance. Valider at alle nummerserier ikke er identiske der data kan vedlikeholdes i begge systemene.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Når jeg oppretter tilkoblingssettet mitt, vises ikke tilkoblingen i rullegardinlisten Tilkobling. Hva gjør jeg?

Kontroller at du velger Dynamics 365 Finance og Dataverse når du oppretter tilkoblinger.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Under synkronisering av distribusjoner får jeg feilen "CompanyInfo_FK finnes ikke" eller "Verdien '12/31/2154 11:59:59 pm' i feltet 'Sluttdato for ansettelse' finnes ikke i den relaterte tabellen 'Ansettelse'". Hva gjør jeg?

Kontroller at du tilordner til de riktige juridiske enhetene. Den juridiske enheten er ikke en del av standardmalen, så det forventes at hver juridiske enhet som finnes i Human Resources og Dataverse, også finnes i Finance. Kontroller også at du velger de riktige juridiske enhetene for det tilknyttede tilkoblingssettet.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Når jeg har definert prosjektet, ser det ut til at felttilordningen for Finance er tomt. Hva gjør jeg?

Oppdater dataenhetene i Finance ved å gå til **Databehandling \> Rammeverkparametere \> Enhetsinnstillinger \> Oppdater enhetsliste**. Dette tar noen minutter å fullføre, og deretter skal du se tilordningene. Dette problemet skjer ved opprettelse av nye prosjekter.

![Mangler felttilordning.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Tilleggsressurser

- Dataintegrator (DI): 

  - [Integrere data til Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [Feiladministrasjon og feilsøking av dataintegrator](/powerapps/administrator/data-integrator-error-management)

  - [Svare på DSR-forespørsler om systemgenererte logger i Power Apps, Microsoft Power Automate og Dataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Databehandling:

  - [Databehandling](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

