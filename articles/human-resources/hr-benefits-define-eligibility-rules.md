---
title: Definere rettighetsregler og policyer for fordel
description: Dette emnet forklarer hvordan du oppretter rettighetsregler og policyer for fordeler og deretter tilordne regler til fordeler.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 59a0ee2f8a1411e921da1d348b87038f9aafccd3
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416863"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere rettighetsregler og policyer for fordel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet forklarer hvordan du oppretter rettighetsregler og policyer for fordeler og deretter tilordne regler til fordeler.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Opprette policyregeltype for fordelsrettigheter

1. Gå til **Human resources > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter**.
2. Velg **Ny**.
3. Angi en verdi i feltet **Regelnavn**.
4. Angi en verdi i feltet **Beskrivelse**.
5. I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget.
6. Velg koblingen i den valgte raden i listen.
7. Velg **Lagre**.
8. Lukk siden.

## <a name="benefit-eligibility-policy"></a>Policy for fordelsrettigheter

1. Gå til **Human resources > Fordeler > Rettighet > Policyer for fordelsrettigheter**.
2. Velg en eksisterende fordelspolicy.
3. Velg koblingen i den valgte raden i listen.
4. Aktiver/deaktiver utvidelsen av delen **Policyorganisasjoner**. Du kan legge til eller fjerne alle organisasjoner som du vil ta med i policyen.
5. Vis eller skjul delen **Policyregler**.
6. I listen finner du policyregelen som ble opprettet tidligere.
7. Velg **Opprett policyregel**.
8. I feltet **Gjelder fra** angir du datoen du vil at policyen skal aktiveres.
    * Ved å angi effektive sluttdatoer kan du endre fremtidige policyregler, slik at du ikke må gå tilbake til policyen når du vil at endringene skal tre i kraft.  
9. Om nødvendig legger du til et where-uttrykk i feltet **Legg til betingelse**.
    * Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef. Du kan legge til flere where-uttrykk sammen i en regel.  
10. Velg **OK**.
11. Lukk siden.

## <a name="assign-rule-to-benefit"></a>Tilordne regel til fordel

1. Gå til **Human resources > Fordeler > Fordeler**.
2. Finn og velg ønsket post i listen.
3. Velg koblingen i den valgte raden i listen.
4. Vis eller skjul delen **Rettighetsregler**.
5. Velg **Rediger**.
6. Velg regelen i **Rettighet**-feltet.
7. I feltet **Regeltype** velger du regelen som ble opprettet tidligere.
9. Velg koblingen i den valgte raden i listen.
10. Velg **Lagre**.
11. Lukk skjemaet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
