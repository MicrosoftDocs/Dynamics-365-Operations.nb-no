---
title: Fordelsplan for lønnsarbeider
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Fordelsplan for lønnsarbeider i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068440"
---
# <a name="payroll-worker-benefit-plan"></a>Fordelsplan for lønnsarbeider


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver enheten Fordelsplan for lønnsarbeider for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>beskrivelse

Denne enheten gir informasjon om fordelsplanen for en angitt arbeider.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Det unike personalnummeret til den ansatte. |
| **ID for juridisk enhet**</br>mshr_legalentityID</br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Periode-ID**</br>mshr_periodid</br>*Streng* | Skrivebeskyttet | Identifikatoren for perioden. |
| **Plan-ID**</br>mshr_planid</br>*Streng* | Skrivebeskyttet | ID-en til planen. |
| **Dekningsalternativ**</br>mshr_coverageoptionid</br>*Streng* | Skrivebeskyttet | Identifikasjon av dekningsalternativet. |
| **Startdato for fradrag**</br>mshr_deductionstartdatetime</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Startdato for fradrag. |
| **Fradragssluttdato**</br>mshr_deductionenddatetime</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Fradragssluttdato. |
| **Status**</br>mshr_status</br>*[Alternativsett for planstatus for fordelsansatt](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Skrivebeskyttet | Status for fordelsplanen. |
| **Gyldig fra**</br>mshr_validfrom</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Klokkeslettet denne posten er gyldig fra. |
| **Gyldig til**</br>mshr_validto</br>*Motregning av dato/klokkeslett* |  Skrivebeskyttet | Klokkeslettet denne posten er gyldig til. |
| **Plantype-ID**</br>mshr_plantypeid</br>*Streng* | Skrivebeskyttet | ID-en til plantypen. |
| **Kode for plantype**</br>mshr_plantypecode</br>*[alternativsett for fordelsplantypedekning](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Skrivebeskyttet | Spesifikasjonen til plantypen. |
| **Antall lønnsperioder**</br>mshr_payperiod</br>*Heltall* | Skrivebeskyttet | Antall lønnsperioder som representerer hvor ofte fordelsleverandøren eller de ansatte skal betales. Dette beløpet blir brukt til å beregne den ansattes årlige fordelslønnsbeløp. |
| **Ansattbeløp**</br>mshr_amountemployee</br>*Desimal* | Skrivebeskyttet | Ansattes beløp eller prosent. |
| **Arbeidsgiverbeløp**</br>mshr_amountemployer</br>*Desimal* | Skrivebeskyttet | Arbeidsgivers beløp eller prosent. |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Systemgenerert | Primærfelt. |
| **Verdi for arbeider-ID** </br>_mshr_fk_worker_id_value</br>*GUID* | Sekundærnøkkel: mshr_hcmworkerbaseentityid i mshr_hcmworkerbaseentity-enhet. | Systemgenerert unik identifikator for arbeider. |
| **Periode-ID-verdi**</br> _mshr_fk_period_id_value</br>*GUID* | Sekundærnøkkel: mshr_benefitperiodentityid for mshr_benefitperiodentity-enhet. | Systemgenerert unik identifikator for perioden. |
| **Plan-ID-verdi**</br> _mshr_fk_plan_id_value</br>*GUID* | Sekundærnøkkel: mshr_benefitplanentityid for mshr_benefitplanentity-enhet. | Systemgenerert unik identifikator for planen. |
| **Verdi for plantype-ID**</br> _mshr_fk_plantype_id_value</br>*GUID* | Sekundærnøkkel: mshr_benefitplantypeentityid for mshr_benefitplantypeentity-enhet. | Systemgenerert unik identifikator for planen. |
| **Verdi for dekningsalternativ-ID**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Sekundærnøkkel: mshr_benefitcoverageoptionentityid for mshr_benefitcoverageoptionentity-enhet. | Systemgenerert unik identifikator for planen. |
| **Verdi for planenhets-ID for lønnsarbeiderfordel**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Skrivebeskyttet </br> Systemgenerert | Systemgenerert unik identifikator for posten. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Eksempelspørring for fordelsplan for lønnsarbeider

**Forespørsel**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
