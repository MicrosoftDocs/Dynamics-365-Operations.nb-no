---
title: Dynamics 365 Human Resources-kundeoverføring til økonomi- og driftsinfrastrukturen
description: Denne artikkelen beskriver kundeoverføring av Microsoft Dynamics 365 Human Resources til økonomi- og driftsinfrastrukturen.
author: twheeloc
ms.date: 12/06/2022
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
ms.openlocfilehash: ab9680c2d1caa08c15aed325f4153aac6eae63c3
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831727"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources-kundeoverføring

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kundeoverføring er en «løft-og-flytt-overføring» (flytting) av en kundedatabase til økonomi- og driftsinfrastrukturen. Du bruker et automatisert overføringsverktøy til dette. Resultatet er et nytt økonomi- og driftsmiljø som bruker kundens Human Resources-database.

## <a name="prerequisites"></a>Forutsetninger

### <a name="user-access-and-permissions"></a>Brukertilgang og -tillatelser

- Brukeren av Microsoft Dynamics Lifecycle Services må ha rollen **Organisasjonsadministrator**.
- Brukeren må kunne [opprette Azure DevOps-prosjekter](/azure/devops/organizations/projects/create-project) eller bruke et eksisterende Azure DevOps-prosjekt.
- Brukeren må ha tilgang til å [opprette et personlig sikkerhetstoken for tilgang for Azure DevOps](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) eller ha et token som er tilgjengelig for bruk.

### <a name="dataverse-environment-backup-sandbox"></a>Sikkerhetskopi av Dataverse-miljø (sandkasse)

 - Valgfritt, men anbefalt: Oppdater det eksisterende Human Resources-sandkassemiljøet ved å bruke en kopi av Human Resources-produksjonsmiljøet.
 - Opprett et nytt Dataverse-miljø ved å bruke administrasjonssenteret for Power Platform.
 - Kopier det eksisterende Dataverse-miljøet, som er koblet til den frittstående Human Resources-appen, til miljøet du opprettet i det forrige trinnet.

> [!NOTE]
> Når du legger til en database, sørger du for at alternativet **Aktiver Dynamics 365-apper** er satt til **Ja**. Hvis du vil ha detaljert informasjon , kan du se [Klargjør et Power Platform-miljø](hr-cust-migration.md#prepare-a-power-platform-environment).

### <a name="dataverse-capacity"></a>Dataverse-kapasitet

1. Bruk **Sammendrag**-siden i administrasjonssenteret for Power Platform til å kontrollere at [Dataverse-lagring](/power-platform/admin/finance-operations-storage-capacity) har nok ledig kapasitet til miljøkopien.
2. Hvis det ikke er nok ledig kapasitet, kan du bruke [veiledning for å frigjøre lagringsplass](/power-platform/admin/free-storage-space) for å redusere det samlede forbruket. Kunder kan også [legge til ekstra lagringskapasitet](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Kundeoverføring

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Opprett et Lifecycle Services-prosjekt for Human Resources-overføring

Det første trinnet er å opprette et nytt prosjekt for implementering av økonomi og drift i Lifecycle Services. Kunden får et eksisterende Human Resources Lifecycle Services-prosjekt. De eksisterende Human Resources-miljøene overføres til det nye prosjektet for implementering av økonomi og drift.

Hvis du vil opprette et nytt prosjekt, gjør du følgende:

1. Logg deg på Lifecycle Services som global administrator eller den utpekte tjenestekontobrukeren.
2. På startsiden for Lifecycle Services velger du **Opprett/ny (+)**.
3. Velg økonomi- og driftsapper som produktet.
4. I **Prosjektformål**-feltet velger du **Implementering**.
5. Angi et prosjektnavn og en beskrivelse.
6. Velg **Microsoft Dynamics 365 Human Resources-overføring** i feltet **Egendefinert type for prosjekt**.
7. Merk av i avmerkingsboksen for å godta vilkårene og betingelsene.
8. Velg **Opprett**.

Etter at du har opprettet et nytt Lifecycle Services-prosjekt, følger du fremgangsmåten for å konfigurere prosjektet.

1. Velg **Prosjektinnføring** for å fullføre prosjektinnføringen. Hvis du vil ha mer informasjon, kan du se [Prosjektinnføring](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Velg samme område som gjeldende miljøer. Dette valget påvirker ikke overføring.
    - Når det gjelder eldre systemer, velger du **Annet**.

2. Fullfør prosjektinnstillingene. Som en del av dette trinnet bør du konfigurere tilkoblingene til SharePoint Online-bibliotek, Azure DevOps og Azure, hvis de kreves. Hvis du vil ha mer informasjon, kan du se [Brukerveiledning for Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Kunder kan bruke et eksisterende Azure DevOps-prosjekt og det tilknyttede personlige sikkerhetstokenet for tilgang. Hvis et eksisterende prosjekt brukes, er konfigurasjonene som er knyttet til prosjektet, tilgjengelige automatisk, og de kan gjennomgås for nøyaktighet.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Overfør et Human Resources-sandkassemiljø

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Forberedelse til å overføre sandkassemiljøet

Etter at et nytt Lifecycle Services-prosjekt er opprettet, og prosjektinnføringen er fullført, er du klar til å overføre det første miljøet. Før du starter denne prosessen, anbefaler vi at du oppdaterer sandkassemiljøene du ønsker å overføre fra produksjonsmiljøet i den frittstående infrastrukturen.

#### <a name="prepare-a-power-platform-environment"></a>Klargjør et Power Platform-miljø

> [!NOTE]
> Dette trinnet gjelder bare for overføring av sandkassemiljøet. Når du overfører produksjonsmiljøet, overføres det eksisterende miljøet i administrasjonssenteret for Power Platform som er knyttet til produksjonsmiljøet. Når du legger til en database, sørger du for at knappen **Aktiver Dynamics 365-apper** er satt til **Ja**. 

- [Opprett et miljø med en database](/power-platform/admin/create-environment#create-an-environment-with-a-database) i administrasjonssenteret for Power Platform som skal brukes til overføring av sandkasse, eller velg et eksisterende miljø.
- [Kopier et miljø](/power-platform/admin/copy-environment) for å oppdatere Power Platform-miljøet som brukes til tilordning.

#### <a name="migrate-the-sandbox-environment"></a>Overfør sandkassemiljøet

1. Logg deg på Lifecycle Services som global administrator eller den utpekte tjenestekontobrukeren.

    > [!NOTE]
    > Vi anbefaler at du bruker en navngitt brukerkonto. Den påloggede brukeren må ha sikkerhetsrollen **Prosjekteier** eller **Miljøadministrator** i det frittstående Human Resources Lifecycle Services-prosjektet.

2. Åpne det nyopprettede Human Resources-overføringsprosjektet.
3. Gå gjennom og fullfør de aktuelle fasene i overføringsmetoden og prosjektinnføringen.
4. Velg **Overfør HR** i ruten **Standard: Standard aksepttest** på instrumentbordet for prosjekt.
5. Velg det aktuelle Lifecycle Services-prosjektet og det opprinnelige Human Resources-miljøet (fra det frittstående Human Resources-kildeprogrammet) i ruten **Velg miljøet som skal overføres**.
6. Aktiver **Tildel til nytt Power Platform-miljø**, og velg det aktuelle Power Platform-miljøet. Velg deretter **Neste**.
7. Fullfør veiviseren **Distribusjonsinnstillinger (økonomi og drift – sandkasse)** for å bekrefte detaljer og kundens godkjenning, og velg deretter **Distribuer**.

Miljøtilstanden viser fremdriften. Tilstanden endres fra **Laster inn** til **Distribuerer** til **Distribuert**.

> [!NOTE]
> Produksjonsruten blir ikke tilgjengelig før sjekklisten for klargjøring for prosjektaktivering er fullført. Hvis du vil ha mer informasjon, kan du se [Klargjør for aktivering](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Vurderinger og forutsetninger

Det finnes et Human Resources-sandkassmiljø i et Lifecycle Services-prosjekt på leieren som har følgende egenskaper:

- Human Resources-sandkassemiljøet er ikke koblet til et eksisterende sammenslått miljø. Bare én overføring kan utføres om gangen kan for et gitt Human Resources-miljø.
- Antallet sandkassemiljøer som er tillatt om gangen, er basert på Human Resources-lisensiering. Hvis det er kjøpt tilstrekkelig lisensiering for leietakeren, vises flere sandkassemiljøer i **Miljøer**-ruten for prosjektet.
- Overføringer må utføres i miljøer av samme type. Det er med andre ord bare overføringer fra sandkasse til sandkasse eller fra produksjon til produksjon som kan utføres.

    > [!NOTE]
    > Det tas bare hensyn til Human Resources-miljøtyper når statusen for produksjon eller sandkasse fastsettes. Hvis miljøene kategoriseres feil (det vil si at et produksjonsmiljø merkes som et sandkassemiljø, eller et sandkassemiljø merkes som et produksjonsmiljø), kontakter du kundestøtte.

- Hvis overføringen ikke er vellykket, vises det en feilmelding og en **Slett**-knapp. Bruk denne knappen til å slette den mislykkede overføringen. Du kan deretter overføre miljøet på nytt.

#### <a name="validate-the-sandbox-migration"></a>Valider overføringen av sandkassen

Når overføringen av sandkassen er fullført, oppretter du en detaljert testplan for å verifisere og godkjenne alle forretningsprosesser.

Før du begynner å teste, må du validere følgende detaljer:

- Bekreft at det overførte miljøet er tilgjengelig på nettadressen som genereres.
- Bekreft at brukere har tilgang til den overførte sandkassen.
- Bekreft at Dataverse-miljøet som er knyttet til det overførte sandkassemiljøet, er tilgjengelig.
- Ta stikkprøver på ulike data for å bekrefte at de mest oppdaterte dataene er tilgjengelige.
- Fullfør de viktige forretningsprosessene for validering.
- Bekreft at sikkerhetspolicyene gjelder.
- Bekreft at satsvise jobber utløses som forventet.

Du får ikke tilgang til den overførte sandkassen via eksternt skrivebord. Du kan bruke selvbetjeningsfunksjoner og -verktøy til å utføre følgende handlinger for sandkassemiljøene på lag 2 og høyere:

- Gå til [Azure SQL-databasen](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Åpne [loggfiler](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Bruk [perfmon-verktøy](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- [Aktiver/deaktiver vedlikeholdsmodus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Start [tjenester](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services) på nytt.
- Konfigurer [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om distribusjon av selvbetjening](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Overfør et Human Resources-produksjonsmiljø

Etter at du er ferdig å overføre og validere et sandkassemiljø, følger du denne fremgangsmåten for å overføre produksjonsmiljøet.

#### <a name="prerequisites"></a>Forutsetninger

- Abonnementsberegneren må fullføres.
- [Klargjøringsvurderingen](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) for aktivering må fullføres.
- Brukeren som starter produksjonsoverføringen i Lifecycle Services, må ha rollen Systemadministrator i Power Platform. 

#### <a name="migrate-the-production-environment"></a>Overfør produksjonsmiljøet

1. Logg deg på Lifecycle Services som global administrator eller den utpekte tjenestekontobrukeren.

    > [!NOTE]
    > Vi anbefaler at du bruker en navngitt brukerkonto. Den påloggede brukeren må ha sikkerhetsrollen **Prosjekteier** eller **Miljøadministrator** i Lifecycle Services-prosjektet.

2. Åpne det nye Human Resources-overføringsprosjektet.
3. Gå gjennom og fullfør de aktuelle fasene i overføringsmetoden og prosjektinnføringen.
4. Velg **Overfør HR** i **Produksjon**-ruten på instrumentbordet for prosjekt.
5. Velg det aktuelle Lifecycle Services-prosjektet og det opprinnelige Human Resources-miljøet (fra det frittstående Human Resources-kildeprogrammet) i ruten **Velg miljøet som skal overføres**. Velg deretter **Neste**.
6. Fullfør veiviseren **Distribusjonsinnstillinger (økonomi og drift – sandkasse)** for å bekrefte detaljer og kundens godkjenning, og velg deretter **Distribuer**.

Miljøtilstanden viser distribusjonsfremdriften. Tilstanden endres fra **Laster inn** til **Distribuerer** til **Distribuert**.

#### <a name="post-migration-considerations"></a>Hensyn etter overføringen

- Bruk de nyeste [kvalitetsoppdateringene](/fin-ops-core/fin-ops/get-started/quality-updates) på miljøene.
- Hvis du bruker [virtuelle tabeller](hr-admin-integration-common-data-service-virtual-entities.md), kan du konfigurere endepunktene på nytt.
- Konfigurer integrering av dobbel skriving på nytt. Evaluer hvilke enheter som må aktiveres.
- Vurder å bruke virtuelle tabeller til å erstatte dobbel skriving for integrering.

#### <a name="dual-write-integration"></a>Integrering med dobbel skriving

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Konfigurer integrering av dobbel skriving for Microsoft Power Platform

1. Gå til administrasjonssenteret for Power Platform, og velg **Miljøer** i venstre navigasjon.
2. Velg det tidligere kopierte/oppdaterte miljøet, og bekreft at tilstanden er **Klar**.
3. Gå til Lifecycle Services, og bekreft at statusen for overføringsprosjektet er **Distribuert**.
4. Velg **Detaljerte opplysninger** under det overførte miljøet for å gå gjennom ytterligere detaljer og [konfigurere et program for dobbel skriving](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Merk av i avmerkingsboksen i ruten **Konfigurasjon av program for dobbel skriving** for å godta at data tilordnes og synkroniseres mellom databaser, og velg deretter **Konfigurer**.
6. Når en meldingsboks varsler deg om vellykket konfigurasjon av dobbel skriving, velger du **OK**.
7. Du kan overvåke fremdriften til konfigurasjonen i detaljene.
8. Når konfigurasjonen er fullført, velger du **Koble til Power Platform-miljø** for å synkronisere tilgjengelige dataenheter.
9. Når statusen viser at miljøene er koblet sammen, går du til administrasjonssenteret for Power Platform for å gå gjennom og velge de aktuelle dataenhetene.
10. I venstre rute velger du **Dynamics 365-apper \> Ressurser**.
11. Bekreft at statusen for Human Resources-appen for dobbel skriving er **Aktivert**.
12. Velg Human Resources-appen for dobbel skriving, og velg deretter **Installer**.
13. Velg det aktuelle miljøet som pakken skal installeres i, i ruten **Installer Dynamics 365 Human Resources-appen for dobbel skriving**.
14. Merk av i avmerkingsboksen for å godta vilkårene for bruk, og velg deretter **Installer**.
15. I Dynamics 365-appmiljøet er statusen **Installerer** mens installasjonen pågår. Den blir oppdatert til **Installert** når installasjonen er fullført.

##### <a name="review-and-apply-a-dual-write-solution"></a>Gå gjennom og bruk en løsning for dobbel skriving

1. I det nye økonomi- og driftsmiljøet kan du gå til **Databehandling \> Dobbel skriving**.
2. Velg **Bruk løsning**.
3. I ruten velger du **Dynamics-installerte løsninger**, **Enhetstilordninger for programkjerne for dobbel skriving** og **Dynamics 365 Human Resources-tilordninger**. Velg deretter **Bruk**. En melding bekrefter at løsningen brukes. Etter at løsningen har blitt brukt, vises alle de tilgjengelige tabelltilordningene.
4. Gå gjennom de tilgjengelige tabelltilordningene for å velge og kjøre integreringen ved hjelp av dobbel skriving.
5. Når du kjører integrering av dobbel skriving for første gang for tabelltilordninger, merker du av for **Første synkronisering**. Hvis det finnes en eksisterende integrering fra Human Resources-kildemiljøet, trenger du ikke merke av for **Første synkronisering** når du kjører integreringen for tabelltilordninger.

#### <a name="recommended-practices"></a>Anbefalte fremgangsmåter

Denne delen beskriver anbefalinger for overgang fra den frittstående infrastrukturen til økonomi- og driftsinfrastrukturen.

- Vi anbefaler på det sterkeste at du arbeider med Microsoft Dynamics-partneren din for å få hjelp med overføringen av Human Resources-miljøet.
- Planlegg tilstrekkelig tid til å foreta en full testing av brukergodkjenning i det overførte sandkassemiljøet.
- Planlegg og dokumenter de detaljerte trinnene for å overføre integreringer til det overførte miljøet.
- Opprett en detaljert sjekkliste for å skissere overgangsprosessen for overføringen.
- Planlegg en passende mengde nedetid for virksomheten mens du foretar overføringen.
- Vi anbefaler på det sterkeste at FastTrack-kvalifiserte kunder arbeider med FastTrack-løsningsarkitekten for å få hjelp med å føre tilsyn med overføringen.
- Vi anbefaler på det sterkeste at du oppdaterer sandkassemiljøet i den frittstående infrastrukturen før du foretar den første overføringen. Denne oppdateringen bør omfatte Dataverse-miljøet som er koblet til sandkassemiljøet du planlegger å overføre til.
- Vi anbefaler på det sterkeste at du bruker en tjenestekonto når du distribuerer, overfører og oppretter Lifecycle Services-prosjektet.
- Planlegg å oppgradere sandkassemiljøet for testing av brukergodkjenning i den nyeste allment tilgjengelige versjonen. Hvis du vil ha mer informasjon, kan du se [hensyn](hr-infrastructure-merge.md#considerations).
