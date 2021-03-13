---
title: Forstå dato- og klokkeslettfelt
description: Forstå hva du kan forvente når du bruker dato- og klokkeslettfelt i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d843eb8cefcd0f2f45c8956cd451f88ca6336efb
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130453"
---
# <a name="understand-date-and-time-fields"></a>Forstå felt for dato og klokkeslett

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Dato og klokkeslett**-felt er et grunnleggende begrep i Dynamics 365 Human Resources. Det er viktig å forstå hvordan du arbeider med **Dato og klokkeslett**-data i skjemaer, Dataverse og eksterne kilder.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Forstå forskjellen mellom datatypene Dato- og Dato og klokkeslett-felt

**Dato og klokkeslett**-felt inneholder tidssoneinformasjon, mens **Dato**-felt ikke gjør det. **Dato**-felt viser den samme informasjonen på et hvilket som helst sted. Når du angir en dato i et **Dato**-felt, skriver Human Resources den samme datoen til databasen.

Når du viser data i et **Dato og klokkeslett**-felt, justerer Human Resources datoen og klokkeslettet basert på brukerens tidssone som er angitt i **Brukeralternativer**-skjemaet (**Felles > Oppsett > Brukeralternativer**). Dato- og klokkeslettinformasjonen du angir i feltet, er kanskje ikke lik informasjonen som er skrevet til databasen.

[![Brukeralternativer-skjema](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Forstå Dato og klokkeslett-felt i skjemaer 

**Dato og klokkeslett**-data som vises på skjermen, er ikke de samme som dataene som er lagret i databasen hvis brukerens tidssone ikke er satt til UTC (Coordinated Universal Time). Data i **Dato og klokkeslett**-felt lagres alltid som UTC.

[![Arbeiderskjema UTC](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Forstå Dato og klokkeslett-felt i databasen 

Når Human Resources skriver en **Dato og klokkeslett**-verdi til databasen, lagres dataene i UTC. Dermed kan brukerne se alle **Dato og klokkeslett**-data i forhold til tidssonen som er definert i deres brukeralternativer.
 
I eksemplet ovenfor er starttidspunktet et tidspunkt, ikke en bestemt dato. Ved å endre tidssonen til den påloggede brukeren fra GMT + 12:00 til GMT UTC, vil den samme posten vise 04/30/2019 12:00:00 i stedet for 05/01/2019 12:00:00.
  
I eksemplet nedenfor blir ansettelsen til ansatt 000724 aktiv på samme tid uavhengig av tidssonen. Den ansatte vil være aktiv 04/30/2019 i GMT-tidssonen, som er det samme som 05/01/2019 i GMT+12:00-tidssonen. Begge refererer til samme tidspunkt og ikke en bestemt dato. 

[![Arbeiderskjema GMT](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Dato og klokkeslett-data i Data Management Framework, Excel, Dataverse og Power BI 

Data Management Framework, Excel-tillegget, Dataverse og Power BI-rapportering er alle utformet for å samhandle med data direkte på databasenivået. Siden det ikke finnes noen klient til å justere **Dato og klokkeslett**-data til tidssonen for brukeren, er alle **Dato og klokkeslett**-verdier i UTC, noe som kan føre til noen feilaktige antakelser når du registrerer eller viser data.  
 
**Dato og klokkeslett**-data som sendes via DMF, Excel eller Dataverse, antas å være i UTC av databasen. Dette kan føre til litt forvirring når den sendte **Dato og klokkeslett**-verdien ikke vises som forventet fordi brukeren som viser dataene, ikke har sin brukertidssone satt til UTC. 
 
Det samme kan skje motsatt når data eksporteres. **Dato og klokkeslett**-dataene i den eksporterte DMF-enheten kan være forskjellige fra det som vises i Dynamics-klienten. 
 
Når du bruker eksterne kilder som DMF til å vise eller redigere data, må du huske på at **Dato og klokkeslett**-verdiene anses som standard å være i UTC, uavhengig av tidssonen til brukerens datamaskin eller deres gjeldende innstillinger for brukertidssone. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Eksempler på samme post som vises i forskjellige produktområder 

**Human Resources med brukertidssone satt til UTC**

[![Arbeiderskjema satt til UTC](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources med brukertidssone satt til GMT + 12:00** 

[![Arbeiderskjema satt til GMT](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-oppsamling**

[![DMF-oppsamling](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-eksport**

[![DMF-eksport](./media/DMFexport.png)](./media/DMFexport.png)

**Excel via Dataverse**

[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Se også

[Dato og klokkeslett-data](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Brukerforetrukkede tidssoner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
