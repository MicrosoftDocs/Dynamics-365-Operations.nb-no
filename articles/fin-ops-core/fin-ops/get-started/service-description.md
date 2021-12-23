---
title: Tjenestebeskrivelse for Finance and Operations apper
description: Dette emnet inneholder tjenestebeskrivelsen for Finance and Operations apper.
author: tomhig
ms.date: 12/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: f7ce73018fda79156cc7ef3d4e1faa3fedf966f8
ms.sourcegitcommit: b101c21f972fdad2667431f712222e040cd69d43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/07/2021
ms.locfileid: "7898395"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Tjenestebeskrivelse for Finance and Operations apper

[!include[banner](../includes/banner.md)]

Finance and Operations-apper er ERP-programvare (Enterprise Resource Planning) programvare som en tjeneste (SaaS)-tilbud som er bygd på og for [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Finance and Operations-tjenesten tilbyr organisasjoner ERP-funksjonalitet som støtter dere unike krav, og hjelper dem med å tilpasse seg endrede forretningsmiljøer uten å kreve at de administrerer infrastruktur. Finance and Operations-appene kan omfatte ett eller flere av følgende løsningsområder:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Sammen med [forretningsintelligens](/power-bi/fundamentals/power-bi-service-overview), [infrastruktur](https://azure.microsoft.com/global-infrastructure/), [databehandling](/azure/service-fabric/service-fabric-overview) og [databasetjenester](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/), gjør disse appene det mulig for organisasjoner å kjøre bransjespesifikke prosesser og driftsforretningsprosesser. Kunder som støttes av implementeringspartneren, fastslår konfigurasjonen til forretningsprogramlogikken som passer best til de unike forretningsprosessene. Funksjonalitet og forretningsprosesser kan forsterkes og utvides gjennom én eller en kombinasjon av følgende løsninger:

- Innebygd [tilpasningserfaring](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)-verktøy
- [Visual Studio](https://visualstudio.microsoft.com)-basert [Finance and Operations programvareutviklingssett (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) og [Azure DevOps automatisering av bygging](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Uavhengige programvareleverandørløsninger (ISV) fra [AppSource](https://appsource.microsoft.com/partners)

Kundene velger løsningen sin, basert på kravene. Sammen med implementeringspartneren kan de definere, utvikle og teste løsningen ved hjelp av verktøyene og anbefalte fremgangsmåter som tilbys i [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Det finnes fire vanlige scenarier:

- Standard Finance and Operations apper "ut av boksen"-konfigurasjon (ingen utvidelser)
- Finance and Operations-apper som inneholder én eller flere ISV-løsninger
- Finance and Operations-apper som inkluderer én eller flere kundespesifikke utvidelser
- Konfigurasjon av Finance and Operations-apper som inneholder en kombinasjon av kundespesifikke utvidelser og én eller flere ISV-løsninger

Organisasjoner kan samsvare med forretningsøkningen ved å legge til brukere og forretningsprosesser via en enkel, oversiktlig abonnementsmodell. Hvis du vil ha mer informasjon, kan du se [lisensieringsveiledningen for Dynamics 365](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Driftsmodell

Driftsmodellen for Finance and Operations apper definerer bestemte roller og ansvarsområder for kunden, implementeringspartneren og Microsoft gjennom hele tjenestens levetid. Hvis du vil ha mer informasjon, kan du se [Skyoperasjoner og -betjening](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Kundeaktiviteter

Kunder samarbeider med partneren sin og [Microsoft FastTrack](/dynamics365/fasttrack/) etter [Dynamics 365 Implementation Guide](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), rammeverket [Success by Design](/dynamics365/fasttrack/success-by-design-overview), og verktøyene og malene for beste fremgangsmåte som tilbys i [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) for å implementere løsningen. Vanlige aktiviteter inkluderer:

- Brukeridentitet og sikkerhetsadministrasjon
- Definere, utvikle og operere forretningsprosesser
- Definere, utvikle, teste og bruke utvidelser
- Overvåke og administrere distribusjoner som ikke kommer fra produksjon
- Administrere programoppdateringer og validere utvidelser
- Administrere ISV-løsninger og trepartsintegrering

### <a name="microsoft-responsibilities"></a>Microsofts ansvarsområder

Microsoft administrerer Finance and Operations tjenesten ved å distribuere, aktivt overvåke og vedlikeholde kundesandkasser og produksjonsmiljøer i Microsoft SaaS-abonnementet. Denne administrasjonen omfatter tildeling av den nødvendige systeminfrastrukturen for å kjøre tjenesten og kommunisere proaktivt med kunder om tjenestens tilstand. Ansvarsområdene omfatter:

**Infrastrukturadministrasjon**
- Sikkerhet og isolasjon
- Operativsystemer og virtualisering
- Servere, lagring og nettverk
- Datasentereffekt, nettverk, kjøling

**Administrasjon av programplattformer**
- 24/7-applikasjonsovervåking og -meldinger
- Diagnoser, plattformoppdateringer, oppdateringer, serviceoppdateringer
- Søknadsruting, belastningsfordeling, områdereplikering
- Miljøklargjøring og -styring
- Databaseadministrasjon, høy tilgjengelighet (HA)/disaster recovery (DR), skala, operasjoner
- Beregn distribusjon, oppskalering, nedskalering

## <a name="system-configuration"></a>Systemkonfigurasjon

Finance and Operations-apper skaleres i henhold til transaksjonsvolumet og brukerbelastningen. Hver kundeimplementering gir en unik løsning som består av følgende elementer:

- **Datasammensetning** – Et unikt sett med parametere som kontrollerer virkemåten, oppsettet til organisasjonen, strukturen til hoveddataene (for eksempel finans- og lagerdimensjoner) og detaljverdien for transaksjonssporing.
- **Utvidelse og konfigurasjon** – Utvidelsesmekanismer som bruker kodetillegg, ISV-løsninger og unike konfigurasjoner som omfatter arbeidsflyter, integreringer og rapportkonfigurasjoner.
- **Bruksmønstre** – En unik kombinasjon av online- og satsvis bruk, sammen med mulighet til å integrere med upassende og nedstrømssystemer for samlet dataflyt og muligheten til å differensiere basert på informasjonsvisninger som kunder bruker i sine forretningsprosesser.

Microsoft konfigurerer kundeproduksjonsmiljøer med størrelse for å håndtere transaksjonsvolumene og brukersamtidigheten. Microsoft er ansvarlig for følgende oppgaver:

- Tildeling av ressursene i produksjonsmiljøer på riktig måte, basert på kundens profileringsinformasjon i [LCS-abonnementsberegneren](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Overvåke og diagnostisere servicetilgjengeligheten i produksjonsmiljøer kontinuerlig
- Analysere og feilsøke systemytelsesproblemer med Finance and Operations apper

For å sikre at en implementering er konfigurert for høy ytelse, må kunder fullføre disse oppgavene:

- Gi nøyaktig bruksinformasjon om Finance and Operations implementeringen i [LCS-abonnementsberegneren](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Bygge og teste utvidelser for ytelse og skala.
- Teste datakonfigurasjoner riktig for ytelse.
- Sikre skalerbarhet ved å utføre [ytelsestesting](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) før aktivering.

## <a name="onboarding-and-implementation"></a>Pålasting og implementering

Tabellen nedenfor viser vanlige pålasting- og implementeringshendelser.

| Forespørsel | Forventet Microsoft-handling | Forventet handling for kunde/implementeringspartner |
|---|---|---|
| Første tilbudsinnkjøp | Et LCS-prosjekt opprettes etter kjøp av tilbudet, basert på en hendelse som utløses av kunden. | Gå gjennom den [kommersielle prosessen](before-you-buy.md) for Microsoft Foretaksavtale (EA) eller leverandør av skyløsninger (CSP). Partneren oppretter en leietaker for kunden, hvis det er aktuelt. |
| Tilleggsinnkjøp | Gi kunden tilgang til tillegget som velges under implementering. | Gjelder ikke |
| Implementeringsplanlegging og -analyse | Bruk relevante verktøy i LCS, for eksempel [Forretningsprosessmodelerer (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) og [interoperabilitet med Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Fullfør prosjektplanlegging, konfigurer Azure DevOps fullfør systempålasting og definer administrasjonskontoer. |

Hvis du vil ha mer informasjon, kan du se [Pålasting av et implementeringsprosjekt](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalisering

Finance and Operations-apper leveres fra flere steder i Azure-områder over hele verden. Finance and Operations-apper gir funksjonalitet som støtter forskjellige land/regioner og morsmål. Hvis du vil ha mer informasjon, kan du se [Lokalisering og forskriftsmessige funksjoner](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Lands-/områdespesifikke hensyn

- Kunder i regulerte industri- eller forretningsorganisasjoner som gjør forretninger med enheter i Frankrike, som krever lokal datalagring, bør se gjennom [Finance and Operations i Frankrike](../../dev-itpro/deployment/france-local-deployment.md).
- Kunder som har operasjoner i Kina, bør gjennomgå [Finance and Operations styrt av 21Vianet i Kina](../../dev-itpro/deployment/china-local-deployment.md).
- Kunder som har operasjoner i Russland, bør gjennomgå den [russiske loven om lokalisering av personlige data](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>EUs personvernforordning (GDPR)

For Finance and Operations apper fungerer Microsoft som en behandler. Som databehandler tilbyr Finance and Operations prosesser og funksjoner som kan gjøre det en mulig for kunder å oppfylle GDPR-forpliktelser som datakontroller. Hvis du vil ha mer informasjon, kan du se [Oversikt over GDPR](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Miljø- og dataadministrasjon

Denne delen beskriver noen vanlige miljø- og datastyringshendelser som forekommer i tjenesten.

### <a name="environment-and-data-management-events-for-production-instances"></a>Hendelser for miljø og datastyring for produksjonsforekomster

LCS tilbyr [selvbetjeningsverktøy](../../dev-itpro/deployment/infrastructure-stack.md) og [operasjoner for databasebevegelse](../../dev-itpro/database/dbmovement-operations.md) som brukes til å utføre miljø- og dataadministrasjonsoppgaver. Her er noen eksempler:

**Hendelse:** [Anmode om en produksjonsforekomst](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Fullfør [kontrollisten for aktivering](../imp-lifecycle/prepare-go-live.md), og send den til [Microsoft FastTrack](/dynamics365/fasttrack/)-teamet.
- Fullfør [LCS-abonnementsberegningen](../../dev-itpro/lifecycle-services/subscription-estimator.md) før du ber om en produksjonsforekomst.
- Fullfør alle implementeringsoppgavene som er angitt i [LCS-metoden](../../dev-itpro/lifecycle-services/create-methodology.md).

**Hendelse:** [Kopiere en sandkassedatabase til en produksjonsforekomst](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Utført for en testovergang eller faktisk overgang.

**Hendelse:** [Vedlikeholdsmodus](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Aktiver vedlikeholdsmodus i LCS.
2. Fullfør vedlikeholdet etter behov.
3. Deaktiver vedlikeholdsmodus i LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Hendelser for miljø og datastyring for ikke-produksjonsforekomster

LCS tilbyr [selvklargjøringsverktøy](../../dev-itpro/deployment/infrastructure-stack.md) og [operasjoner for databasebevegelse](../../dev-itpro/database/dbmovement-operations.md) som brukes til å utføre miljø- og dataadministrasjonsoppgaver. Her er noen eksempler:

**Hendelse:** [Distribuere en ny sandkasseforekomst](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Kontroller at alle nødvendige forekomster er [planlagt](../imp-lifecycle/environment-planning.md), og at de aktuelle tilleggstilbudene er kjøpt inn.
- Kjør distribusjonsprosessen i LCS.
- Fullfør alle implementeringsoppgavene som er angitt i LCS-sjekklistene.
    
>[!NOTE]
>Et utviklingssandkassemiljø er en virtuell maskin (VM) som [distribueres til kundens Azure-abonnement](../../dev-itpro/dev-tools/access-instances.md) og administreres av kunden.

**Hendelse:** [Kopiere en gyllen konfigurasjonsdatabase de sandkasse til produksjon](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Utført for en testovergang eller faktisk overgang.

**Hendelse:** [Gjenopprette en produksjonspunktsikkerhetskopi til en ikke-produksjonsforekomst](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Kjør alternativet [Oppdater database](../../dev-itpro/database/database-refresh.md) i LCS.
- Etter kopiering: Slett eller tildekk sensitive data via skript, juster miljøspesifikke programkonfigurasjoner (for eksempel integreringssluttpunkt) og aktiver eller legg til brukere. Legg merke til at disse endringene gjøres ved å bruke en [datapakke](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Hendelse:** [Tidsgjenoppretting av ikke-produksjonsforekomstdatabase](../../dev-itpro/database/database-point-in-time-restore.md)

- Godta at prosessen ikke kan angres.
- Kjør tidsgjenopprettingsoperasjonen i LCS.

**Hendelse:** Kopiere en sandkassedatabase for lag 2 til en utviklingssandkasse for [feilsøking](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Kjør databaseeksportoperasjonen i LCS i Lager 2-sandkassemiljø.
- Importer og oppdater databasen i utviklingsmiljøet.

## <a name="data-backup-and-retention"></a>Sikkerhetskopiering og oppbevaring av data

Databaser for Finance and Operations miljøer i SaaS-abonnementet er beskyttet av automatiske sikkerhetskopier. I produksjonsmiljøer beholdes automatiske sikkerhetskopier i 28 dager, med mindre Microsoft gjør en tilbakerulling. For sandkassemiljøer (lag 2+) beholdes de i sju dager. En tilbakerulling av produksjonsmiljøet kan gjøres hvis det oppstår en feil under en planlagt vedlikeholdsoppdatering.

Hvis du vil ha mer informasjon om automatiske sikkerhetskopier, kan du se [Automatisk sikkerhetskopiering - Azure SQL Database og SQL administrert forekomst](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Serviceaktivitetsansvar

Tabellen nedenfor beskriver vanlige scenarier og aktiviteter for tjenesten. Den viser også om Microsoft, kunden eller både Microsoft og kunden er ansvarlig for aktivitetene.

| Aktivitet | Microsofts ansvarsområder | Kundens ansvarsområder |
|---|---|---|
| **Klargjøre første leietakere** | | |
| Skaler prosjektert belastning i LCS ved hjelp av verktøyet for abonnementsberegner, og be om at bestemte miljøer klargjøres. | | X |
| Klargjør alle produksjonsforekomster og ikke-produksjonsforekomster. | X | |
| Valider de distribuerte produksjonsforekomstene og ikke-produksjonsforekomstene. | | X |
| **Serviceoppdateringer** | |
| Bruk serviceoppdateringer for utpekte ikke-produksjons- og produksjonsforekomster. | X | |
| Bruk serviceoppdateringer fra LCS manuelt i sandkasseforekomster. Definer, utvikle, test oppdateringen og gi pakke med kodeoppdatering tilbake til LCS. | | X |
| Be om og planlegg at det brukes utvidelsesoppdateringer for produksjonsforekomsten. | | X |
| Opprett en kode og en datasikkerhetskopi for produksjonsforekomsten før det blir brukt oppdateringer. | X | |
| Hvis det oppstår feil, tilbakeruller du produksjonsforekomsten til koden og datasikkerhetskopien. | X | |
| **Dataadministrasjon (sikkerhetskopier, gjenopprett og oppdater)** | | |
| Sikkerhetskopier databasen. | X | |
| Fastslå høy tilgjengelighet og en nødgjenopprettingsplan. | X | |
| Overvåk ytelsen til produksjonsforekomstdatabasen. | X | |
| Juster ytelsen til produksjonsforekomstdatabasen. | X | |
| Utfør databasepunktoppdatering av produksjonsforekomst til en forekomst som ikke gjelder produksjon. | | X |
| **Oppdatere infrastrukturen** | | |
| Planlegge regelmessige infrastrukturoppdateringer. | X | |
| **Skalere opp og ned (brukere, lagring og forekomster)** | | |
| Kjøpe ekstra brukere og ikke-produksjon-tillegg. | | X |
| Oppdater bruksendringer i verktøyet for LCS-abonnementsberegner. | | X |
| Rapporter eventuelle vesentlige ytelsesproblemer som påvirker bruken av tjenesten. | | X |
| Behandle ressursene som kreves for den aktuelle tjenesten, proaktivt. | X | |
| Undersøk og feilsøk hendelser. | X | |
| **Sikkerhet (brukertilgang)** | | |
| Gi brukeren tilgang til tjenesten. | | X |
| Gi LCS-prosjekttilgang til administrasjon og drift av forekomster som ble distribuert gjennom LCS. | | X |
| **Overvåke produksjonsforekomster** | | |
| Overvåk produksjonsforekomster 24/7. | X | |
| Varsle kunden om hendelser som omfatter produksjonsforekomsten, proaktivt. | X | |
| **Administrere og overvåke forekomster som ikke er til produksjon** | | |
| Administrer forekomster som ikke er til produksjon, ved hjelp av LCS. | | X |
| Overvåk ikke-produksjonsforekomster. | | X |

## <a name="service-update-strategy"></a>Strategi for tjenesteoppdatering

I henhold til [policyen for programvarelivssyklus](../../dev-itpro/migration-upgrade/versions-update-policy.md) følger Finance and Operations apper Microsofts [policy for moderne livssyklus](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), som dekker produkter som vedlikeholdes og støttes kontinuerlig. 

Microsoft utgir åtte tjenesteoppdateringer for Finance and Operations apper hvert år i de følgende månedene:

- Januar
- Februar
- April
- Mai
- Juli
- August
- Oktober
- November

>[!NOTE]
>April og oktober er lanseringsbølger for viktige funskjoner. Kunder kan stanse en individuell serviceoppdatering midlertidig i opptil tre fortløpende oppdateringssykluser.

Hvis du vil ha mer informasjon, kan du se følgende emner:

- [Oversikt over oppdatering av én versjonstjeneste](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Konfigurere serviceoppdateringer via LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Stanse serviceoppdateringer midlertidig via LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Bli varslet om serviceoppdateringer via LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regresjonstestingsverktøy for å validere serviceoppdateringer](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365-veikart og lanseringsbølger](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Sikkerhet og administrativ tilgang

Administrativ tilgang til et Finance and Operations produksjonsmiljø kontrolleres og logges strengt. Kundedata håndteres i henhold til [vilkårene for Microsofts onlinetjenester](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Kundeadministrativ tilgang

Kundens leieadministrator kan få tilgang til produksjonsforekomster eller ikke-produksjonsforekomster, som beskrevet i følgende tabell:

| Miljøtype | Formål | Nivå av kundetilgang |
|---|---|---|
| **Ikke-produksjon**<br>Lag 1-sandkasse | Et ikke-produksjonsmiljø som kunder distribuerer til utviklings-, demonstrasjons- eller opplæringsformål. | En lag 1-sandkasse (også omtalt som et skybasert miljø) er en kundestyrt VM som distribueres til kundens Azure-abonnement fra LCS. Fordi det er et VM i kundens Azure-abonnement, har kunden full administrativ tilgang til miljøet via Eksternt skrivebord. |
| **Ikke-produksjon**<br>Sandkasse for lag 2 (eller høyere) | Et ikke-produksjonsmiljø som kunder distribuerer for brukeraksepttesting, integreringstesting, opplæring, klargjøring eller andre scenarier før produksjon. | Lag 2 og høyere sandkasser distribueres til Finance and Operations-SaaS-abonnementet. Tilgang til Azure SQL-databaser som er knyttet til ikke-produksjonsmiljøet, gis tilgang via [just-in-time-tilgang](../../dev-itpro/database/database-just-in-time-jit-access.md). Tilgang til Eksternt skrivebord er ikke tilgjengelig. |
| **Produksjon** | Et produksjonsmiljø distribueres når prosjektet er [klart til første aktivering](/imp-lifecycle/environment-planning.md#production-system-readiness). | Produksjonsmiljøer distribueres til SaaS-abonnementet. All tilgang går gjennom webleseren, servicesluttpunktene eller LCS. |

### <a name="microsoft-administrative-access"></a>Microsoft administrativ tilgang

Tabellen nedenfor viser de ulike tilgangsnivåene for ulike Microsoft-administratorer:

| Administrator | Kundedata |
|---|---|
| Operasjonssvarteam<br>(Begrenset til bare nøkkelpersonell) | Tilgang gis via en støtteforespørsel. Tilgangen kontrolleres og begrenses til varigheten til støtteaktiviteten. |
| Microsofts kundestøttetjenester (CSS) | Ingen direkte tilgang. Kunden kan bruke skjermdeling til å arbeide med kundestøttepersonalet for å feilsøke problemer. |
| Utvikling | Ingen direkte tilgang. Operasjonssvargruppen kan bruke skjermdeling til å arbeide med ingeniørvirksomhet for å feilsøke problemer. |
| Andre i Microsoft | Ingen tilgang. |

## <a name="monitoring"></a>Overvåking

Microsoft har investert i en omfattende verktøysett for å overvåke og diagnosere produksjonsforekomster for kunder. Microsoft overvåker kundenes produksjonsmiljøer 24 timer i dagen, 7 dager i uken. Hvis du vil ha mer informasjon, kan du se [Produksjonsstøtte og overvåking](../imp-lifecycle/production-support-monitoring.md).

| Microsofts ansvarsområder | Kundeansvar |
|---|---|
| <ul><li>Overvåk tilgjengeligheten av tjenesten.</li><li>Overvåk og varsle kontinuerlig gjennom tilstandsmåledata og watchdogs for kritiske komponenter som Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce og Management Reporter.</li><li>Overvåk for ytelsesreduksjon som forårsakes av infrastrukturtjenester (for eksempel Azure Active Directory \[Azure AD\] og Azure SQL).</li><li>Hvis Microsoft finner ut at én enkelt prosess eller satsvis jobb forårsaker avvik, avsluttes denne prosessen eller jobben etter kommunikasjon med kunden.</li></ul> | <ul><li>Overvåk endringer i programkonfigurasjoner og -tillegg som kan forårsake funksjons- og ytelsesproblemer.</li><li>Programfeil må diagnostiseres ved hjelp av overvåkingsverktøyene. Bruk disse verktøyene til å diagnostisere brukerrapporterte ytelsesavvik.</li><li>Informer Microsoft om det er forventet belastning på systemet ut over forventet største bruk.</li><li>Hvis tjenesten som gjelder, ikke er tilgjengelig i produksjonsforekomsten, kan kunden bruke LCS til å rapportere et [produksjonsbrudd](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Ved å sende støtteforespørsler online, via LCS, gjør kundene at Microsoft kan levere rask og grundig teknisk kompetanse på den mest effektive måten. Selv om telefonalternativet er tilgjengelig, bør det bare brukes hvis online-alternativet ikke er tilgjengelig. Hvis du vil ha mer informasjon, kan du se [Alternativer for telefonstøtte](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Hendelsesbehandling

Microsoft svarer på og retter opp hendelser basert på alvorlighetsnivåer. Microsofts alvorlighetsnivåer for hendelser kan endres under innledende vurdering av hendelsen, og etter hvert som mer informasjon om innvirkningen og omfanget blir tilgjengelig. Hvis hendelsen reduseres, forblir hendelsens viktighet uendret.

Hvis du vil ha mer informasjon om alvorlighetsnivåer, kan du se [denne alvorlighetstabellen](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Forretningskontinuitet gjennom høy tilgjengelighet og nødgjenoppretting 

Microsoft gir forretningskontinuitet og nødgjenoppretting for produksjonsforekomster av Finance and Operations apper ved avbrudd på hele Azure-området. Hvis du vil ha mer informasjon, kan du se [Forretningskontinuitet og nødgjenoppretting](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Høy tilgjengelighet** – HA-funksjonalitet gir måter å forhindre nedetid som forårsakes av feil på en enkelt node i et Azure-datasenter. Skyarkitekturen til hver tjeneste bruker Azure-tilgjengelighetssett for beregningslaget for å forhindre feilhendelser på enkeltpunkt. HA for databaser leveres gjennom [Azure SQL HA-funksjoner](/azure/azure-sql/database/high-availability-sla).
- **Nødgjenoppretting** – [Azure nødgjenopprettingfunksjoner](/azure/best-practices-availability-paired-regions) beskytter hver tjeneste mot avbrudd som påvirker et helt Azure-datasenter bredt. Her er noen av disse funksjonene:

    - Azure SQL aktiv geo-replikering for hoveddatabasen (forretningsdatabase).
    - Geo-overflødige kopier av Azure Blob Storage (som inneholder dokumentvedlegg) i andre Azure-områder.
    - Sekundært område for Azure SQL- og Azure Blob Storage-replikeringer.

De primære datalagrene støttes for replikering. Derfor bruker komponenter for hver tjeneste, for eksempel Management Reporter og enhetsbutikk, transformerte data fra hoveddatabasen. Disse dataene må genereres etter at gjenopprettingsområdet er konfigurert og tjenesten er startet. Kundekodeartefakter og gjenopprettede datalagre brukes til å distribuere området på nytt. Med denne nye distribusjonen kan tilstandsreplikering av databehandlingsnodene, sammen med andre nettverk og andre komponenter, bruke de gjenopprettede datalagrene til å opprette det sekundære området. Hvis nødgjenoppretting brukes til å gjenopprette kundens produksjonsforekomst, vil Microsoft og kunden oppfylle ansvarsområdene for [hendelsesbehandling](service-description.md#incident-management).

Microsofts planer og prosedyrer for nødgjenoppretting undersøkes regelmessig gjennom SOC-kontroller. Disse samsvarsrevisjonene bekrefter den tekniske prosessen og fremgangsmåten i Microsofts DR, inkludert Dynamics 365 Finance and Operations apper. Overvåkingsrapporter for[SOC-samsvar](/compliance/regulatory/offering-soc-2) og alle andre rapporter om overholdelse er tilgjengelige på [Microsoft Trust Center Compliance Offerings](/compliance/regulatory/offering-home).

| Microsofts ansvarsområder | Kundeansvar |
|---|---|
| Microsoft klargjør et sekundært miljø i det Azure-parede datasenteret når den primære produksjonsforekomsten distribueres. Hvis du vil ha mer informasjon, kan du se [Forretningskontinuitet og nødgjenoppretting (BCDR): Azure-parede områder](/azure/best-practices-availability-paired-regions). | None |
| Microsoft aktiverer geo-redundans for Azure SQL og Azure Blob Storage når den primære produksjonsforekomsten distribueres. | None |
| Microsoft aktiverer automatisk sikkerhetskopiering på Azure SQL-databaser. | None |
| <p>Når strømbrudd oppstår, avgjør Microsoft om det må utføres en failover for kunden, og om det vil bli tap av data. Kunder kan oppleve tap av data på opptil 15 minutter, avhengig av arten og tidsberegningen for avbruddet. | Hvis det oppstår tap av data, kan det hende at kunden må gi skriftlig godkjenning for å utløse failoveren. |
| Når en failover forekommer, fungerer den gjeldende tjenesten i begrenset modus. Oppdatering av vedlikehold kan ikke utløses i failover-modus. | Kunden kan ikke be om pakkedistribusjoner eller andre regelmessige vedlikeholdsforespørsler i failover-modus. |
| Når datasenteret blir operativt, gjør Microsoft en failback tilbake til produksjonsforekomsten i det primære Azure-området. Normale operasjoner gjenopptas. | Det kan hende at kunden må godkjenne failback til produksjonsforekomst i det primære Azure-området. |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operations-støttetilbud

Teknisk kundestøtte er tilgjengelig i markeder der Finance and Operations tjenester tilbys. [Støtteopplevelser](../../dev-itpro/lifecycle-services/lcs-support.md) leveres i LCS eller Finance and Operations apper. Her er noen eksempler:

- [Problemsøk](../../dev-itpro/lifecycle-services/issue-search-lcs.md) i LCS
- [Integrert teknisk støtte](../../dev-itpro/lifecycle-services/support-experience.md) i Finance and Operations apper
- [Skybasert støtte](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) i LCS

Microsoft tilbyr Finance and Operations kundene tre støtteplaner: Premier, Professional Direct og støtten som er inkludert i abonnementet. Støttenivået varierer per plan. Følgende tabell viser en sammenligning av de tre planene.

| Støttefunksjon | Premier | Professional Direct | Abonnement |
|---|---|---|---|
| Ubegrenset pause-/fast hendelsesinnsending | Ja | Ja | Ja |
| 24/7-tilgang via LCS | Ja | Ja | Ja |
| Svartid for hendelser | Mindre enn én time | Mindre enn én time | Neste arbeidsdag |
| Rådgivningstid | Puljer anskaffes per avtale. | Nei | Nei |
| Dedikert kundestøttekontoansvarlig | Ja | Nei | Nei |
| Dedikert støttetekniker | Engasjert under en egen avtale | Nei | Nei |

Hvis du vil ha mer informasjon, kan du se [Oversikt over kundestøtte](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Prosess for å engasjere støtte

Hvis det oppstår hendelser som involverer Finance and Operations apper, sender kundene støtteforespørsler til Microsoft via LCS. CSS håndterer hendelsene, basert på kundens støtteplan og alvorligheten for hendelsen, slik det er angitt av CSS.

### <a name="service-level-agreement"></a>Servicenivåavtale

Microsoft har forpliktet seg til en tilgjengelighetsrate på 99,9 prosent per måned for tjenesten. Hvis Microsoft ikke oppnår og vedlikeholder servicenivået for den gjeldende tjenesten som er beskrevet i servicenivåavtalen, kan kunden kvalifisere for kreditt mot en del av den månedlige serviceavgiften for denne tjenesten. Hvis du vil ha mer informasjon om hvordan du starter en servicekreditt, kan du se delen "Krav" i [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Viktige ressurser

- **[Klareringssenter](https://www.microsoft.com/trust-center)** – Få informasjon om hvor Finance and Operations dataene er lagret, i tillegg til tilleggsinformasjon om personvern, samsvar og sikkerhetsprosedyrer.
- **[Lisensieringsbetingelser og dokumentasjon](https://www.microsoftvolumelicensing.com/)** – Få raskt tilgang til lisensvilkår og -betingelser og tilleggsinformasjon som er relevant for bruken av produkter og tjenester som er lisensiert via Microsofts volumlisensprogrammer.
- **[Lisensvilkår](https://www.microsoft.com/licensing/product-licensing/)**– Ressursene på denne siden definerer vilkårene for programvaren og onlinetjeneste-produktene du kjøper gjennom Microsofts kommersielle lisensprogrammer.
- **[Livssykluspolicy for Microsoft](/lifecycle/)** – Denne siden inneholder konsekvente og forutsigbare retningslinjer for tilgjengelighet av støtte gjennom hele levetiden til et produkt.
- **[Lisensieringsveiledning](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Bruk denne veiledningen til å finne ut mer om hvordan du lisensierer Dynamics 365.
- **[Kundestøtte](https://dynamics.microsoft.com/support/)** – Få bransjeledende støtte for Dynamics 365-appene.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – Administrer livssyklusen til programmet, og gå mot forutsigbare, gjentakbare implementeringer av høy kvalitet.

## <a name="definitions"></a>Definisjoner

### <a name="azure-region"></a>[Azure-område](/azure/availability-zones/az-overview#regions)

Geografisk område der ett eller flere Azure-datasentre finnes. Eksempler inkluderer USA og Europa.

### <a name="business-process-modeler-bpm"></a>[Forretningsprosessmodelerer (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Et verktøy i LCS som hjelper deg med å fullføre en tilpasningsgapanalyse for en gitt implementering ved å bruke forretningsprosessdefinisjoner fra American Productivity & Quality Center (APQC) som støttes i Finance and Operations apper.

### <a name="cloud-solution-provider"></a>Leverandør av skyløsning

En partner som er en del av Microsoft-leverandør av skyløsninger (CSP-program), og som gir kunder merverdibaserte skytjenester, støtte, én faktura og kundeadministrasjon i skala.

### <a name="customer"></a>Kunde

En forretningsenhet som forbruker Finance and Operations apper og representeres av en leietaker i Office 365.

### <a name="development-environment"></a>Utviklingsmiljø

Et ikke-produksjons sandkassemiljø som brukes til å utvikle utvidelser. Kunder distribuerer dette miljøet til sitt eget Azure-abonnement fra LCS. Dette miljøet kan også brukes til demonstrasjon, opplæring eller andre testoppgaver. Det er også kjent som en [Lag 1-sandkasse](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Nedetid

Perioder når brukere ikke kan logge seg på eller få tilgang til sin aktive leietaker på grunn av en feil på den ikke-utløpte plattformen eller tjenesteinfrastrukturen, som Microsoft fastslår fra automatisert tilstandsovervåking og systemlogger. Nedetid omfatter ikke planlagt nedetid, utilgjengelighet for tilleggsfunksjoner for service, manglende tilgang til tjenesten på grunn av endringer i tjenesten eller perioder der skalaenhetskapasiteten er overskredet.

### <a name="implementation-partner"></a>Implementeringspartner

Partneren som kunden velger for å tilpasse, konfigurere, implementere og administrere Finance and Operations løsningene.

### <a name="incident"></a>Tilfelle

Et problem som kunder oppdager mens de bruker Finance and Operations tjenesten, og som de sender sender en billett for via LCS.

### <a name="microsoft-customer-support-services-css"></a>Microsofts kundestøttetjenester (CSS)

Det globale Microsoft-støtteteamet som er dedikert til å tilby kvalitetsservice for Finance and Operations apper.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Den administrative portalen for livssyklusadministrasjon av Finance and Operations apper fra prøveversjon til implementering, til etterproduksjonsadministrasjon og -støtte. Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Ikke-produksjonsforekomst

Alle av de følgende forekomstene av en tjeneste som kunden bruker til å validere utvidelser og utføre andre utviklingsoppgaver:

- **Sandkasselag 1** – Utviklerforekomst (kundebasert)
- **Sandkasselag 2** – Standard testforekomst for godkjenning
- **Sandkasselag 3–5** – Tilleggssandkasser

Hvis du vil ha mer informasjon om lag 2 til og med 5, kan du se [Velge riktig lag 2 eller høyere miljø](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Produksjonsforekomst

Et Finance and Operations-miljø som kunden bruker til å administrere de daglige transaksjonene og forretningsprosessene "live".

### <a name="sandbox-environment"></a>Sandkassemiljø

Et ikke-produksjonsmiljø som kunden bruker til demonstrasjon, opplæring, brukergodkjenningstesting, validering av utvidelser og andre testoppgaver.

### <a name="service"></a>Service

Noen av kjernetjenestene som er inkludert i Finance and Operations apper.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Servicenivåavtale (SLA) for Microsofts onlinetjenester

Serviceavtalen gjelder for Microsofts onlinetjenester. Hvis du vil ha mer informasjon, se [Serviceavtaler](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Serviceoppdatering

Microsofts Finance and Operations tjenestemiljøer på konsekvent basis gjennom serviceoppdateringer. Kundene definerer sin egen serviceoppdateringskalender basert på deres forretningsbehov. Hvis du vil ha mer informasjon, kan du se [Oppdatering av én versjonstjeneste](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="user"></a>Bruker

Én enkelt person som bruker Finance and Operations miljøer, og som er knyttet til kundens leietaker.
