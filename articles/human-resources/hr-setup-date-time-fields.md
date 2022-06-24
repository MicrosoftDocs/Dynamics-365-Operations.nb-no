---
title: Forstå felt for dato og klokkeslett
description: Denne artikkelen forklarer hva du kan forvente når du bruker dato- og klokkeslettfelt i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e314efa5ac08288bc7d00c197be59ba9decac203
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856316"
---
# <a name="understand-date-and-time-fields"></a>Forstå felt for dato og klokkeslett

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Dato og klokkeslett**-felt er et grunnleggende begrep i Microsoft Dynamics 365 Human Resources. Det er viktig at du forstår hvordan du arbeider med **Dato og klokkeslett**-data på sider, i Dataverse og i eksterne kilder.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Forstå forskjellen mellom datatypene Dato- og Dato og klokkeslett-felt

**Dato og klokkeslett**-felt inneholder tidssoneinformasjon, mens **Dato**-felt ikke gjør det. **Dato**-felt viser den samme informasjonen på et hvilket som helst sted. Når du angir en dato i et **Dato**-felt, skrives den samme datoen til databasen.

Når data vises i et **Dato og klokkeslett**-felt, justeres datoen og klokkeslettet basert på brukerens tidssone som er valgt på **Brukeralternativer**-siden (**Felles \> Oppsett \> Brukeralternativer**). Dato- og klokkeslettinformasjonen du angir i feltet, er kanskje ikke lik informasjonen som er skrevet til databasen.

[![Brukeralternativer-siden.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Forstå Dato og klokkeslett-felt på sider 

**Dato og klokkeslett**-data som vises på skjermen, er ikke de samme som dataene som er lagret i databasen hvis brukerens tidssone ikke er satt til UTC (Coordinated Universal Time). Data i **Dato og klokkeslett**-felt lagres alltid som UTC.

[![UTC for Arbeider-siden.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Forstå Dato og klokkeslett-felt i databasen 

Når en **Dato og klokkeslett**-verdi skrives til databasen, lagres dataene som UTC. Dermed kan brukerne se alle **Dato og klokkeslett**-data i forhold til tidssonen som er definert i deres brukeralternativer.
 
I eksemplet ovenfor er starttidspunktet et tidspunkt, ikke en bestemt dato. Ved å endre tidssonen til den påloggede brukeren fra GMT + 12:00 til GMT UTC, vil den samme posten vise 04/30/2019 12:00:00 i stedet for 05/01/2019 12:00:00.

I eksemplet nedenfor blir ansettelsen til ansatt 000724 aktiv på samme tid uavhengig av tidssonen. Den ansatte vil være aktiv 04/30/2019 i GMT-tidssonen, som er det samme som 05/01/2019 i GMT+12:00-tidssonen. Begge refererer til samme tidspunkt og ikke en bestemt dato. 

[![GMT for Arbeider-siden.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Dato og klokkeslett-data i Data Management Framework, Excel, Dataverse og Power BI 

Data Management Framework (DMF), Excel-tillegget, Dataverse og Power BI-rapportering er alle utformet for å samhandle med data direkte på databasenivået. Siden det ikke finnes noen klient til å justere **Dato og klokkeslett**-data til tidssonen for brukeren, er alle **Dato og klokkeslett**-verdier i UTC, noe som kan føre til noen feilaktige antakelser når du registrerer eller viser data.
 
Når **Dato og klokkeslett**-data sendes via DMF, Excel eller Dataverse, antar databasen at de er i UTC. Hvis brukere som viser dataene, ikke har brukertidssonen angitt til UTC, vil imidlertid ikke den innsendte **Dato og klokkeslett**-verdien vises som forventet, og brukerne kan bli forvirret. 
 
Det samme kan skje motsatt når data eksporteres. **Dato og klokkeslett**-dataene i den eksporterte DMF-enheten kan være forskjellige fra det som vises i Dynamics-klienten. 
 
Når du bruker eksterne kilder som DMF til å vise eller redigere data, må du huske på at **Dato og klokkeslett**-verdiene anses som standard å være i UTC, uavhengig av tidssonen til brukerens datamaskin eller deres gjeldende innstillinger for brukertidssone. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Eksempler på samme post som vises i forskjellige produktområder 

**Human Resources med brukertidssone satt til UTC**

[![Arbeider-side satt til UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources med brukertidssone satt til GMT + 12:00** 

[![Arbeider-side satt til GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-oppsamling**

[![DMF-oppsamling.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-eksport**

[![DMF-eksport.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel via Dataverse**

[![Excel via Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Se også

[Dato og klokkeslett-data](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Brukerforetrukkede tidssoner](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
