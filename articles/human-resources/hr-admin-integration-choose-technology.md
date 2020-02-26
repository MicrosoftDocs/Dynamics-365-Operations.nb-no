---
title: Velg en dataintegreringsteknologi
description: Denne artikkelen inneholder veiledning om forskjellige alternativer for integrering med data som administreres av personalavdelingen, og som beskriver egenskapene til forskjellige integreringsteknologier, slik at integratorer kan ta veloverveide avgjørelser om hvilke teknologier som passer best deres behov.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029894"
---
# <a name="choose-a-data-integration-technology"></a>Velg en dataintegreringsteknologi

Dynamics 365 Human Resources administrerer forretningsdata som er nyttig i en rekke forretningsprosesser. Denne artikkelen inneholder veiledning om forskjellige alternativer for integrering med data som administreres av personalavdelingen, og som beskriver egenskapene til forskjellige integreringsteknologier, slik at integratorer kan ta veloverveide avgjørelser om hvilke teknologier som passer best deres behov.

## <a name="data-integration-vision"></a>Dataintegreringsvisjon

Microsoft ser forretningsdata som et viktig aktivum som gjør firmaet ditt unikt. Bedriftens data er svært verdifulle. Data som samles inn og vedlikeholdes av én del av forretningsvirksomheten, er relatert til data som samles inn av en annen del av virksomheten, og disse relasjonene kan brukes til å forbedre forretningsprosesser og forretningsintelligens på tvers av organisasjonen. Det å gi enkel, sikker og stabil tilgang til forretningsdataene, uansett hvilket system som "eier" dataene, er en nøkkelforutsetning for visjonen vi har om dataintegrering med personalavdelingen.

Det har historiske sett vært vanskelig å integrere data mellom flere systemer.
Microsoft utfører tiltak for å gjøre dataintegrering enklere, og et stort trinn i det aktuelle målet realiseres via [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Hvis vi går videre, sørger personalavdelingen for at Common Data Service blir det foretrukne offentlige grensesnittet for personaldata. Over tid forventer vi at alle de viktigste dataene som administreres av personalavdelingen, vil bli vist i Common Data Service. Vi anbefaler Common Data Service som den foretrukne teknologien for de fleste typer integrering. Vi er klar over at ikke alle data som programmet kan kreve, for øyeblikket finnes i Common Data Service, og at prosjekttidslinjene dine kan kreve en alternativ teknologi. Gi beskjed hvis Common Data Service ikke oppfyller dine integreringsbehov.

## <a name="integration-technologies"></a>Integreringsteknologier

Følgende deler beskriver de ulike dataintegreringsteknologiene som er tilgjengelige for bruk med Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service-enheter

Common Data Service er det foretrukne offentlige datagrensesnittet for Human Resources. Common Data Service bygger på en moden plattform, der Dynamics 365 "XRM"-plattformen er blitt for liten, som [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-løsningene bygger på.

Common Data Service inneholder en plattform for dataenheter og et API for å få tilgang til disse enhetene. Når Human Resources distribueres i organisasjonen, kobles Human Resources til en Common Data Service-forekomst, og enhetene som vedlikeholder personaldata, distribueres til denne Common Data Service-forekomsten, noe som gjør enhetene og dataene tilgjengelige for alle programmer som kan koble til Common Data Service-forekomsten. Avhengig av hvilke Human Resources-apper du bruker, utfører Human Resources dataoperasjoner direkte mot Common Data Service-enhetene (dette er tilfellet for Attract og Onboard) eller synkroniserer data til/fra Common Data Service-enhetene.

Når dataenhetene som viser dataene som integrasjonsappene dine krever, finnes i Common Data Service, kan du dra full nytte av [Common Data Service og API-ene den støtter](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Blant de støttede API-ene er [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), som sørger for en OData-implementering for å få tilgang til Common Data Service-data.

Common Data Service-enhetene og de tilknyttede API-ene er det beste alternativet for å få tilgang til data om Human Resources fra webprogrammer, webtjenester/API-er og fra et hvilket som helst annet program som kobler til OData-feeder.

> [!NOTE]
> Med avgjørelsen om å gjøre Common Data Service til det foretrukne datagrensesnittet for Human Resources som er forholdsvis nylig, kan det hende at personaldataenhetene du trenger for integreringen, ikke er tilgjengelige i Common Data Service<sup>1</sup> ennå. Hvis Human Resourcesnhetene som kreves for integreringen, ikke er tilgjengelige ennå, må du vente til dataenhetene blir tilgjengelige, eller du må bruke en av de andre integreringsteknologiene som er beskrevet nedenfor.
> 
> Som standard er Common Data Service-integrering deaktivert i nye miljøer som ikke inneholder demodataene. Den slått på i nye miljøer som inneholder demonstrasjonsdata, og miljøene begynner å synkronisere data når de er klargjort. Når miljøet er klart til å synkronisere data, kan du aktivere integreringen.

<sup>1</sup>Hvis du vil ha en liste over Human Resourcesnheter som er tilgjengelige i Common Data Service, kan du se [Personale og Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). For Attract og Onboard, er alle enheter tilgjengelige i Common Data Service.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-enheter

Personale, bygd primært på samme plattform som Finance and Operations-programmer, sørger for et [DMF (Data Management Framework)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), noen ganger også kjent som Data Import Export Framework eller DIXF, og et sett med dataenheter som kan brukes til å importere/eksportere data til/fra Human Resources. Common Data Service-enhetene er det foretrukne grensesnittet for dataintegrering for Human Resources, men DMF-enhetene vil likevel være nyttige i enkelte tilfeller, for eksempel:

- Common Data Service-enheter er ikke tilgjengelige ennå.

- Integreringen krever høy ytelse på grunn av masseimport- og eksport.

DMF-enhetene gir nå den mest komplette datadekningen for personaldata.

DMF er ikke aktuelt for integreringer i sanntid (for eksempel når umiddelbar tilbakemelding i et bruker grensesnitt kreves), fordi pakkeoperasjoner er planlagt med satsvise jobber, og det vil ofte ha minst en 1-2 minutters ventetid før den satsvise tjenesten kan plukke opp jobben for utførelse, pluss tiden som kreves for å fullføre import- og eksportoperasjonen.

DMF kan være det beste alternativet når det kreves høy gjennomstrømning (for eksempel en ferdig planlagt import/eksport av mange tusen poster).

> [!NOTE]
> DMF er ikke tilgjengelig for Attract og Onboard.

### <a name="dmf-package-rest-api"></a>REST-API for DMF-pakke

DMF tilbyr en [REST-API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) for manipulering av datapakker. Dette API-et kan brukes til å programmatisk samhandle med DMF, og dermed tillate handlinger som:

- Importere en datapakke.

- Eksportere en datapakke.

- Kontrollere statusen for en import/eksportoperasjon.

REST-API-et for DMF-pakken støttes fullstendig i Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF gir i tillegg en kraftig funksjon (vanligvis kjent som [Ta med din egen database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database), eller BYOD), som gjør det mulig for Human Resources å eksportere data til din egen Microsoft Azure SQL-database. Dette gir stor fleksibilitet, fordi når dataene finnes i din egen SQL-database, kan du bruke alle programmer eller mellomvare som kan koble til et SQL-datalager.

BYOD bør vanligvis regnes som en skrivebeskyttet løsning. Selv om du kan manipulere og lagre de dataene du ønsker i Azure SQL-databasen (for eksempel for datamashup), vil ikke data som er lagret i Azure SQL-databasen, bli synkronisert tilbake til Human Resources.

BYOD er egnet for rapportering av løsninger, dataintegreringer, datamashup, som datakilde for en [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) pipeline.

> [!NOTE]
> BYOD er ikke tilgjengelig for Attract og Onboard.

### <a name="odata-enabled-entities"></a>OData-aktiverte enheter

De fleste DMF-enheter aktiveres også for tilgang via tjenesten for personaldata (OData). Dokumentasjonen som er oppgitt for [Finance and Operations OData-tjenesten](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata), gjelder vanligvis også for Human Resources, selv om dokumentasjonen om hvordan du oppretter dine egne OData-eksponerte enheter ikke gjelder.

Selv om Common Data Service og OData-implementeringen som leveres av Common Data Service (via [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), foretrekkes over tjenesten Human Resourcesdata, har Human Resourcesdata i øyeblikket mer fullstendig enhetsdekning for personaldataene.

### <a name="excel-add-in"></a>Excel-tillegg

[Excel-tillegget](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) gjør bruk av OData-aktiverte enheter i bakgrunnen. Det er en praktisk måte for sluttbrukere å hente og endre personal informasjon via det velkjente Excel-grensesnittet.

Excel-tillegget er egnet for ad hoc-dataimporter/-eksporter av forretningsdomeneeksperter. For en regelmessig dataintegrering som krever programmatisk automatisering, vil en annen integreringsteknologi være mer hensiktsmessig.

### <a name="data-integrator"></a>Dataintegrator

Common Data Service-administratoropplevelsen inneholder en [Data Integrator-tjeneste](https://docs.microsoft.com/powerapps/administrator/data-integrator) som kan brukes til dataintegreringer til/fra Common Data Service. Dataintegrator kan brukes til å definere integreringsprosjekter (ofte basert på forhåndsdefinerte maler som programutviklere har skreddersydd for bestemte integreringer). Integreringsprosjektene kan planlegges til å kjøre automatisk i en regelmessig plan eller kjøres manuelt.

Dataintegrator-prosjekter er egnet for satsvis integrering i Common Data Service og er et flott valg for integreringer mellom Dynamics 365-serien med programmer. Microsoft tilbyr for eksempel en dataintegreringsmal som kan brukes til å integrere data fra Human Resources i Dynamics 365 Finance. Hvis du vil ha mer informasjon, kan du se [Integrasjon fra Dynamics 365 Human Resources til Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Dataintegrator støtter også [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (via den [avanserte spørringsfunksjonen](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power Query gir kraftig, fleksibel datafiltrering og -transformasjon, inkludert det rike M-formelspråket, og vil sannsynligvis være kjent for dem som har erfaring med å utvikle Power BI-rapporter.

## <a name="deciding-on-an-integration-technology"></a>Bestemme seg for en integreringsteknologi

Med så mange forskjellige integreringsteknologier tilgjengelige, kan det være overveldende å avgjøre hvilken integrasjonstilnærming som skal brukes. Over tid, og spesielt etter hvert som datadekningen i Common Data Service modnes, vil beslutningen bli enklere, med Common Data Service som det foretrukne datagrensesnittet i de fleste tilfeller. Men til da kan det hende at du synes at Common Data Service ikke tilfredsstiller dine behov. Tabellen nedenfor hjelper deg med å summere noen av de viktigste egenskapene til de ulike alternativene for integreringsteknologi.

| Teknologi/verktøy/API    | Gjentakende integreringer                   | Synkron/asynkron                    | Programmatisk tilgang gjennom en API        | Riktige datavolumer                                   | Datadekning                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-enheter           | Ja, med dataintegrator eller mellomvare | Synkront/asynkront, parti (via dataintegrator) | Ja, via Dynamics 365 Web API (OData) | Varierer med brukstilfelle (støtter sideveksling for interaktiv bruk) | Forbedre<sup>2</sup>                       |
| DMF-enheter           | Ja, planlagt via mellomvare        | Asynkront, parti                                | Ja, via REST-API for DMF-pakke         | Høy (flere hundre tusen poster)                    | Høy                                |
| REST-API for DMF-pakke   | Ja, planlagt via mellomvare        | Asynkront, parti                                | Ja                                       | Høy (flere hundre tusen poster)                    | API støtter alle DMF-enheter       |
| BYOD                   | Ja, planlagt av administrator i Human Resources        | Asynkront, parti                                | Nei<sup>3</sup>                                    | Høy (flere hundre tusen poster)                    | Støtter alle DMF-enheter           |
| OData-aktiverte enheter | Ja, med mellomvare                    | Synkroniser                                        | Ja, via datatjenesten for Human Resources (OData)  | Varierer med brukstilfelle (støtter sideveksling for interaktiv bruk) | Høy                                |
| Excel-tillegg           | Nei                                       | Synkroniser                                        | Nei                                        | Middels (flere titusener med poster)                      | Støtter alle OData-aktiverte enheter |
| Dataintegrator        | Ja, planlagt i dataintegrator        | Asynkront, parti                                | Nei                                        | Varierer med brukstilfelle                                       | Støtter alle Common Data Service-enheter           |

<sup>2</sup>Microsoft investerer svært mye for å øke datadekningen for Common Data Service-enheter og anbefaler Common Data Service som foretrukket datagrensesnitt når dekning er tilgjengelig. For øyeblikket er Common Data Service-datadekningen liten i forhold til DMF- og OData-aktiverte enheter.

<sup>3</sup>SQL-database kan åpnes programmatisk.

## <a name="summary"></a>Sammendrag

Forretningsdataene dine er et verdifullt aktivum, men verdien kan bli betydelig redusert hvis det er vanskelig å bruke dataene til dine bestemte formål (for eksempel rapportering, datamashup eller egendefinerte bruksområder). Dynamics 365 Human Resources inneholder flere teknologier for å arbeide med data utenfor brukergrensesnittet i Human Resources, som gir integrering av programmer tilgang til dataene. Dette emnet inneholder en beskrivelse av de tilgjengelige integreringsteknologiene og noen av de viktigste egenskapene. Denne informasjonen skal hjelpe deg med å ta bedre avgjørelser om hvilke fremgangsmåter du skal utnytte for integreringsprosjektene.

