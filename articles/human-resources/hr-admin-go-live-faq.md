---
title: Vanlige spørsmål om aktivering
description: Dette emnet viser vanlige spørsmål om hvordan du kan arbeide med et Dynamics 365 Human Resources-implementeringsprosjekt.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4a06da220fd90de91fb9091c41f35a1fb95442c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804023"
---
# <a name="go-live-faq"></a>Vanlige spørsmål om aktivering 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet viser vanlige spørsmål om hvordan du kan arbeide med et Dynamics 365 Human Resources-implementeringsprosjekt. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Når kan jeg konfigurere og be om produksjonsmiljøet? 

Vanligvis distribueres et produksjonsmiljø etter å ha oppfylt følgende kriterier:

- Alle tilpassinger er kodefullført.
- Testing av brukergodkjenning (UAT) er fullført.
- Kunden har godkjent løsningen.
- Det er ingen problemer med blokkering for aktivering. 

Når kvalifiserte kunder er i dette stadiet, vil Microsoft FastTrack-teamet arbeide med prosjektgruppen for å utføre en aktiveringsvurdering. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Hva er forutsetningene for å distribuere et produksjonsmiljø? 

Hvis du vil ha en liste over forutsetningene, kan du se [Klargjøre for aktivering](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Hva er en aktiveringsvurdering?  

Aktiveringsvurderingen er en del av [Microsoft FastTrack-programmet](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). I løpet av denne gjennomgangen vurderer en løsningsarkitekt om implementeringsprosjektet er klart for en vellykket overgang og aktivering. Denne gjennomgangen er obligatorisk for hvert implementeringsprosjekt før du kan be om å aktivere et produksjonsmiljø. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Våre sandkassemiljøer er distribuert i datasenteret USA, sentralt. Vi vil at våre produksjonsmiljøer skal distribueres i datasenteret USA, vest. Kan jeg velge USA, vest som datasenter i produksjonskonfigurasjonen? 

LCS hindrer deg ikke i å velge et annet datasenter når du distribuerer et Human Resources-miljø, men vi anbefaler sterkt at du ikke velger et annet datasenter.  

Hvis du vil at produksjonsmiljøet skal være i datasenteret USA, vest, bør du først distribuere dine sandkassemiljøer til datasenteret USA, vest, teste dem og deretter godkjenne. 

Hvis du vil ha informasjon om hvordan du velger riktig datasenter, se [Nettverkskrav](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Hvilket tilgangsnivå har jeg til Azure-ressursene for Human Resources-miljøene?  

Tilgang til Human Resources-miljøene er begrenset. Du får ikke tilgang til den virtuelle maskinen (VM) eller Microsoft Internet Information Services (IIS). Du får heller ikke tilgang til databasen gjennom Microsoft SQL Server Management Studio. 

Selv om du ikke kan få tilgang til Azure-ressursene eller Dynamics 365 Human Resources-miljøet direkte, kan du bruke flere funksjoner for å få tilgang til dataene:

- Du kan distribuere en Azure SQL-database i din egen Azure-leier og bruke funksjonen Vise din egen database (BYOD) til å synkronisere data. Hvis du vil ha mer informasjon, kan du se [Vise din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Du kan bruke Dataverse-integrering til å synkronisere utvalgte enheter i Dataverse-databasen. Hvis du vil ha mer informasjon, kan du se [Dataverse-tabeller](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Hvor ofte sikkerhetskopieres produksjonsdatabasen? 

Databaser beskyttes av automatisk sikkerhetskopiering med følgende frekvenser:

| Type sikkerhetskopiering | Frekvens |
| --- | --- |
| Full sikkerhetskopi av database | Ukentlig |
| Differensiell sikkerhetskopi av database | Hver 12-24. time |
| Sikkerhetskopi av transaksjonslogg | Hver 5 til 10 minutter |

Microsoft beholder tilstrekkelige sikkerhetskopier for å tillate tidspunktbasert gjenoppretting (PITR) i løpet av de siste 14 dagene. 

Hvis du vil ha mer informasjon, se [Lær om automatisk sikkerhetskopiering av SQL-databasen](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Kan jeg be om en kopi av sikkerhetskopien av produksjonsdatabasen? 

Nr. Du kan imidlertid sende en tjenesteforespørsel om databaseoppdatering for å kopiere produksjonsmiljøet til sandkassemiljøet. Du kan distribuere en Azure SQL-database i din egen Azure-leier og bruke BYOD-funksjonen til å synkronisere data fra produksjonsmiljøet. Hvis du vil ha mer informasjon, kan du se [Vise din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Hvordan flytter jeg sandkassemiljøet til produksjon for aktivering? 

Fordi en kopieringsfunksjon ikke er tilgjengelig for å flytte ditt miljø fra et sandkasse- til et produksjonsmiljø, må du bruke datapakker til å flytte data til produksjonsmiljøet.  

Det anbefales at du vedlikeholder en klar liste over enheter som er konfigurert i sandkassen gjennom hele prosjektet. Deretter tester du prosessen med overgang og migrering av datapakker som er nødvendig for aktivering. Du må manuelt flytte datapakker til produksjonsmiljøet når du er klar for aktivering. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Hva bør jeg gjøre hvis produksjonsmiljøet er nede? 

Hvis du vil rapportere en produksjonsnedetid, følger du prosessen som er beskrevet i [Rapportere en produksjonsnedetid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Se også

 [Klargjøre for aktivering](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]