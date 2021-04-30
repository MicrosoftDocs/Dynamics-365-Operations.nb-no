---
title: Lønnsstillingsjobb
description: Dette emnet inneholder informasjon og en eksempelspørring for Lønnsstillingsjobb-enheten i Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72f3109f5bea36a390b04b7165fc3831d777b640
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882048"
---
# <a name="payroll-position-job"></a>Lønnsstillingsjobb

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder informasjon og en eksempelspørring for Lønnsstillingsjobb-relasjonsenheten i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Jobb-ID**<br>mshr_jobid<br>*Streng* | Readp-only<br>Obligatorisk |ID-en for jobben. |
| **Gyldig fra**<br>mshr_validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som posterings- og jobbrelasjonen er gyldig fra. |
| **Gyldig til**<br>mshr_validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som stillings- og jobbrelasjonen er gyldig til.  |
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | ID-en for stillingen. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Obligatorisk<br>Systemgenerert |  |
| **ID-verdi for stillingsjobb**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_PayrollPositionJobEntity av mshr_payrollpositionjobentity |ID-en for jobben som er knyttet til stillingen.|
| **ID-verdi for fast kompensasjonsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_FixedCompPlan_id av mshr_payrollfixedcompensationplanentity  | ID-en for den faste kompensasjonsplanen som er knyttet til stillingen. |
| **ID for Lønnsstillingsjobb-enhet**<br>mshr_payrollpositionjobentityid<br>*Guid* | Obligatorisk<br>Systemgenerert. | En systemgenerert GUID-verdi som entydig identifiserer jobben.  |

