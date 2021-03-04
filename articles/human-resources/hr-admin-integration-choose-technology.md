---
title: Velge en dataintegreringsteknologi
description: Denne artikkelen inneholder informasjon om integrering med data som administreres av Human Resources. Den beskriver forskjellige typer integreringsteknologi som hjelper deg med å finne ut hvilke typer som passer best til dine behov.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
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
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528347"
---
# <a name="choose-a-data-integration-technology"></a>Velge en dataintegreringsteknologi

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen inneholder informasjon om integrering med data som administreres av Dynamics 365 Human Resources. Den beskriver forskjellige typer integreringsteknologi som hjelper deg med å finne ut hvilke typer som passer best til dine behov.

## <a name="data-integration-background"></a>Bakgrunn for dataintegrering

Forretningsdata er et viktig aktivum som gjør firmaet ditt unikt. Bedriftens data er svært verdifulle. Du kan bruke forholdene mellom data som samles inn i hele virksomheten, til å forbedre forretningsprosesser og forretningsintelligens på tvers av organisasjonen. Vi arbeider med å gi enkel, sikker og stabil tilgang til forretningsdataene dine, uansett hvilket system de kommer fra.

Det har historiske sett vært vanskelig å integrere data mellom flere systemer.
Microsoft utfører tiltak for å gjøre dataintegrering enklere, og et stort trinn i det aktuelle målet realiseres via [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Human Resources sørger for at Common Data Service blir det foretrukne offentlige grensesnittet for Human Resources-data. Over tid forventer vi at alle de viktigste dataene som administreres av personalavdelingen, vil bli vist i Common Data Service. Vi anbefaler Common Data Service som den foretrukne teknologien for de fleste typer integrering.

Vi er klar over at Common Data Service kanskje ikke inneholder alle dataene programmet trenger enda. Vi er også klar over at tidslinjen for prosjektet ditt kan kreve en annen teknologi. Husk å gi oss beskjed hvis Common Data Service ikke tilfredsstiller dine integreringsbehov.

## <a name="integration-technologies"></a>Integreringsteknologier

Følgende deler beskriver de ulike dataintegreringsteknologiene som er tilgjengelige for bruk med Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service-enheter

Common Data Service er det foretrukne offentlige datagrensesnittet for Human Resources. Det er basert på Dynamics 365 XRM-plattformen, som brukes av [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-løsninger.

Common Data Service fungerer som en plattform og et API for dataenheter. Når du distribuerer Human Resources, kobles det til en Common Data Service-forekomst. Enhetene for Human Resources-data distribueres til denne Common Data Service-forekomsten. Enhetene og dataene er tilgjengelige for alle apper som kan koble til Common Data Service-forekomsten. Human Resources synkroniserer data til og fra Common Data Service-enhetene.

Når dataenhetene som kreves av appene som integreres, er i Common Data Service kan du bruke [Common Data Service og API-ene som det støtter](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer), full ut. Blant de støttede API-ene er [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), som sørger for en OData-implementering for å få tilgang til Common Data Service-data.

Common Data Service-enheter og tilknyttede API-er er det beste alternativet for å få tilgang til data om Human Resources fra webprogrammer, webtjenester/API-er og fra et hvilket som helst annet program som kobler til OData-feeder.

> [!NOTE]
> Med avgjørelsen om å gjøre Common Data Service til det foretrukne datagrensesnittet for Human Resources som er forholdsvis nylig, kan det hende at personaldataenhetene du trenger for integreringen, ikke er tilgjengelige i Common Data Service ennå.
</br>
> Hvis du vil ha en liste over Human Resources-enheter som er tilgjengelige i Common Data Service, kan du se [Human Resources og Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Hvis Human Resources-enhetene som kreves for integreringen, ikke er tilgjengelige ennå, må du vente til dataenhetene blir tilgjengelige, eller du må bruke en av de andre integreringsteknologiene som er beskrevet nedenfor.
> </br>
> Som standard er Common Data Service-integrering deaktivert i nye miljøer som ikke inneholder demodataene. Den slått på i nye miljøer som inneholder demonstrasjonsdata, og miljøene begynner å synkronisere data når de er klargjort. Når miljøet er klart til å synkronisere data, kan du aktivere integreringen.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-enheter

Human Resources, bygd primært på samme plattform som Finance and Operations-apper, fungerer som et [Data Management Framework (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). DMF er også kjent som DIXF (rammeverk for dataimport-/eksport). Human Resources inneholder et sett med dataenheter som du kan bruke til å importere og eksportere Human Resources-data. Common Data Service-enhetene er det foretrukne grensesnittet for dataintegrering for Human Resources, men DMF-enhetene vil likevel være nyttige i enkelte tilfeller, for eksempel:

- Common Data Service-enheter er ikke tilgjengelige ennå.

- Integreringen krever høy ytelse på grunn av masseimport- og eksport.

DMF-enhetene gir nå den mest komplette datadekningen for personaldata.

DMF er ikke egnet for sanntidsintegrasjoner, for eksempel når du trenger umiddelbar tilbakemelding fra brukerne i et brukergrensesnitt. Pakkeoperasjoner er planlagt med satsvise jobber, og har ofte minimum 1-2 minutts ventetid før den satsvise tjenesten plukker opp jobben som skal kjøres, i tillegg til tiden for å fullføre import-/eksportoperasjonen.

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

DMF har i tillegg en kraftig funksjon (kjent som [Ta med din egen database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database), eller BYOD), som gjør det mulig for Human Resources å eksportere data til din egen Microsoft Azure SQL-database. Denne funksjonen gir stor fleksibilitet. Når dataene finnes i din egen SQL-database, kan du bruke alle programmer eller mellomvare som kan koble til et SQL-datalager.

BYOD er hovedsakelig en skrivebeskyttet løsning. Selv om du kan manipulere og lagre de dataene du ønsker i Azure SQL-databasen (for eksempel for datamashup), vil ikke data som er lagret i Azure SQL-databasen, bli synkronisert til Human Resources.

BYOD er egnet for rapportering av løsninger, dataintegreringer, datamashup, som datakilde for en [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) pipeline.

> [!NOTE]
> BYOD er ikke tilgjengelig for Attract og Onboard.

### <a name="odata-enabled-entities"></a>OData-aktiverte enheter

De fleste DMF-enheter aktiveres også for tilgang via tjenesten for personaldata (OData). Dokumentasjonen som er angitt for [Finance and Operations OData-tjenesten](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata), gjelder for Human Resources, bortsett fra oppretting av dine egne OData-eksponerte enheter.

Selv om Common Data Service og OData-implementeringen som leveres av Common Data Service (via [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), foretrekkes over tjenesten Human Resourcesdata, har Human Resourcesdata i øyeblikket mer fullstendig enhetsdekning for personaldataene.

### <a name="excel-add-in"></a>Excel-tillegg

[Excel-tillegget](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) gjør bruk av OData-aktiverte enheter i bakgrunnen. Det er en praktisk måte for sluttbrukere å hente og endre personal informasjon via det velkjente Excel-grensesnittet.

Excel-tillegget er egnet for ad hoc-dataimporter/-eksporter av forretningsdomeneeksperter. For en regelmessig dataintegrering som krever programmatisk automatisering, vil en annen integreringsteknologi være mer hensiktsmessig.

### <a name="data-integrator"></a>Dataintegrator

Du kan bruke [tjenesten Dataintegrator](https://docs.microsoft.com/powerapps/administrator/data-integrator) til å integrere data til og fra Common Data Service. Med Dataintegrator kan du definere integreringsprosjekter, ofte basert på forhåndsdefinerte maler som programutviklere har skreddersydd for bestemte integreringer. Du kan planlegge integreringsprosjektene til å kjøres automatisk i en regelmessig plan, eller du kan kjøre dem manuelt.

Dataintegrator-prosjekter er passende for satsvise integreringer i Common Data Service. De er et godt valg for integreringer mellom Dynamics 365-serien med apper. Microsoft tilbyr for eksempel en Dataintegrator-mal for å integrere data fra Human Resources i Dynamics 365 Finance. Du kan lære mer om malen i [Integrasjon fra Dynamics 365 Human Resources til Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Dataintegrator støtter [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) via den [avanserte spørringsfunksjonen](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query gir kraftig, fleksibel datafiltrering og -transformasjon, inkludert det rike M-formelspråket. Power Query vil sannsynligvis være kjent hvis du har utviklet Power BI-rapporter.

## <a name="deciding-on-an-integration-technology"></a>Bestemme seg for en integreringsteknologi

Med så mange forskjellige integreringsteknologier tilgjengelige, kan det være overveldende å avgjøre hvilken integrasjonstilnærming som skal brukes. Etter hvert som datadekningen i Common Data Service modnes, vil beslutningen bli enklere, med Common Data Service som det foretrukne datagrensesnittet i de fleste tilfeller. Men til da kan det hende at du synes at Common Data Service ikke tilfredsstiller dine behov. Tabellen nedenfor oppsummerer noen av de viktigste egenskapene til alternativene for integreringsteknologi.

| Teknologi/verktøy/API    | Gjentakende integreringer                   | Synkron/asynkron                    | Programmatisk tilgang gjennom en API        | Riktige datavolumer                                   | Datadekning                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-enheter           | Ja, med dataintegrator eller mellomvare | Synkront/asynkront, parti (via dataintegrator) | Ja, via Dynamics 365 Web API (OData) | Varierer med brukstilfelle (støtter sideveksling for interaktiv bruk) | Forbedre<sup>2</sup>                       |
| DMF-enheter           | Ja, planlagt via mellomvare        | Asynkront, parti                                | Ja, via REST-API for DMF-pakke         | Høy (flere hundre tusen poster)                    | Høy                                |
| REST-API for DMF-pakke   | Ja, planlagt via mellomvare        | Asynkront, parti                                | Ja                                       | Høy (flere hundre tusen poster)                    | API støtter alle DMF-enheter       |
| BYOD                   | Ja, planlagt av administrator i Human Resources        | Asynkront, parti                                | Nei<sup>3</sup>                                    | Høy (flere hundre tusen poster)                    | Støtter alle DMF-enheter           |
| OData-aktiverte enheter | Ja, med mellomvare                    | Synkroniser                                        | Ja, via datatjenesten for Human Resources (OData)  | Varierer med brukstilfelle (støtter sideveksling for interaktiv bruk) | Høy                                |
| Excel-tillegg           | Nei                                       | Synkroniser                                        | Nei                                        | Middels (flere titusener med poster)                      | Støtter alle OData-aktiverte enheter |
| Dataintegrator        | Ja, planlagt i dataintegrator        | Asynkront, parti                                | Nei                                        | Varierer med brukstilfelle                                       | Støtter alle Common Data Service-enheter           |

<sup>2</sup>Microsoft investerer svært mye i å øke datadekning for Common Data Service-enheter. Vi anbefaler at du bruker Common Data Service når dekning er tilgjengelig. For øyeblikket er Common Data Service-datadekningen liten sammenlignet med DMF- og OData-aktiverte enheter.

<sup>3</sup>SQL-database kan åpnes programmatisk.


[!INCLUDE[footer-include](../includes/footer-banner.md)]