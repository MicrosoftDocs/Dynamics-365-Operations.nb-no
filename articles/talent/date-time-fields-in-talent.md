---
title: Arbeide med dato og klokkeslett i Microsoft Dynamics 365 Talent
description: Forstå hva du kan forvente når du bruker dato- og klokkeslettfelt i Microsoft Dynamics 365 Talent. Få klarhet i hva du kan forvente når du samhandler med dato- og klokkeslettdata i et skjema i Talent, en ekstern kilde eller Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f5bb3432ba3e57a4ef08dfa3c25cb61705efc33
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898764"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a>Arbeide med dato og klokkeslett i Microsoft Dynamics 365 Talent

**Dato og klokkeslett**-felt er et grunnleggende begrep i Dynamics 365 Talent. Det er viktig å forstå hvordan du arbeider med **Dato og klokkeslett**-data i et Dynamics 365-skjema, Common Data Service og eksterne kilder.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Forstå forskjellen mellom datatypene Dato- og Dato og klokkeslett-felt

**Dato og klokkeslett**-felt inneholder tidssoneinformasjon, mens **Dato**-felt ikke gjør det. **Dato**-felt viser den samme informasjonen på et hvilket som helst sted. Når du angir en dato i et **Dato**-felt, skriver Talent den samme datoen til databasen.

Når du viser data i et **Dato og klokkeslett**-felt, justerer Talent datoen og klokkeslettet basert på brukerens tidssone som er angitt i **Brukeralternativer**-skjemaet (**Felles > Oppsett > Brukeralternativer**). Dato- og klokkeslettinformasjonen du angir i feltet, er kanskje ikke lik informasjonen som er skrevet til databasen.

[![Brukeralternativer-skjema](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Forstå Dato og klokkeslett-felt i skjemaer 

Når du angir data i et **Dato og klokkeslett**-felt, er ikke dataene som vises på skjermen, de samme som dataene som er lagret i databasen hvis brukerens tidssone ikke er satt til UTC (Coordinated Universal Time). Data i **Dato og klokkeslett**-felt lagres alltid som UTC.

[![Arbeider-skjema](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Forstå Dato og klokkeslett-felt i databasen 

Når Talent skriver en **Dato og klokkeslett**-verdi til databasen, lagres dataene i UTC. Dermed kan brukerne se alle **Dato og klokkeslett**-data i forhold til tidssonen som er definert i deres brukeralternativer.
 
I eksemplet ovenfor er starttidspunktet et tidspunkt, ikke en bestemt dato. Ved å endre tidssonen til den påloggede brukeren fra GMT + 12:00 til GMT UTC, vil den samme posten som nettopp ble opprettet, vise 04/30/2019 12:00:00 i stedet for 05/01/2019 12:00:00.
  
I eksemplet nedenfor blir ansettelsen til ansatt 000724 aktiv på samme tid uavhengig av tidssonen. Den ansatte vil være aktiv 04/30/2019 i GMT-tidssonen, som er det samme som 05/01/2019 i GMT+12:00-tidssonen. Begge refererer til samme tidspunkt og ikke en bestemt dato. 

[![Arbeider-skjema](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Dato og klokkeslett-data i Data Management Framework, Excel, Common Data Service og Power BI 

Data Management Framework, Excel-tillegget, Common Data Service og Power BI-rapportering er alle utformet for å samhandle med data direkte på databasenivået. Siden det ikke finnes noen klient til å justere **Dato og klokkeslett**-data til tidssonen for brukeren, er alle **Dato og klokkeslett**-verdier i UTC, noe som kan føre til noen feilaktige antakelser når du registrerer eller viser data.  
 
**Dato og klokkeslett**-data som sendes via DMF, Excel eller Common Data Service, antas å være i UTC av databasen. Dette kan føre til litt forvirring når den sendte **Dato og klokkeslett**-verdien ikke vises som forventet fordi brukeren som viser dataene, ikke har sin brukertidssone satt til UTC. 
 
Det samme kan skje motsatt når data eksporteres. **Dato og klokkeslett**-dataene i den eksporterte DMF-enheten kan være forskjellige fra det som vises i Dynamics-klienten. 
 
Når du bruker eksterne kilder som DMF til å vise eller redigere data, er det viktig å huske på at **Dato og klokkeslett**-verdiene anses som standard å være i UTC, uavhengig av tidssonen til brukerens datamaskin eller deres gjeldende innstillinger for brukertidssone. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Eksempler på samme post som vises i forskjellige produktområder 

**Talent med brukertidssone satt til UTC**

[![Arbeider-skjema](./media/worker-form3.png)](./media/worker-form3.png)

**Talent med brukertidssone satt til GMT +12:00** 

[![Arbeider-skjema](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-oppsamling**

[![DMF-oppsamling](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-eksport**

[![DMF-oppsamling](./media/DMFexport.png)](./media/DMFexport.png)

**Excel via Common Data Service**

[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>Se også

[Dato og klokkeslett-data](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Brukerforetrukkede tidssoner](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
