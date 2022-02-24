---
title: Definere rettighetsregler og policyer for fordel
description: Denne artikkelen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419886"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere rettighetsregler og policyer for fordel

Denne artikkelen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.  

Demonstrasjonsdatafirmaet USMF brukes til å opprette dette opptaket.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Opprette policyregeltype for fordelsrettigheter
1. Gå til Personale > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Regelnavn.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk rullegardinknappen i Spørringsnavn-feltet for å åpne oppslaget.
6. Klikk koblingen i den valgte raden i listen.
7. Klikk Lagre.
8. Lukk siden.

## <a name="benefit-eligibility-policy"></a>Policy for fordelsrettigheter
1. Gå til Personale > Fordeler > Rettighet > Policyer for fordelsrettigheter.
2. Velg en eksisterende fordelspolicy.
3. Klikk koblingen i den valgte raden i listen.
4. Aktiver/deaktiver utvidelsen av delen Policyorganisasjoner.  Her kan du legge til eller fjerne alle organisasjoner som du vil ta med i policyen.
5. Vis eller skjul delen Policyregler.
6. I listen finner du policyregelen som ble opprettet tidligere.
7. Klikk Opprett policyregel.
8. I feltet Gjelder fra angir du datoen du vil at policyen skal aktiveres.
    * Ved å angi effektive datoer og sluttdatoer kan du endre fremtidige policyregler og fjerne behovet for å gå tilbake til policyen når du vil at endringene skal tre i kraft.  
9. 
    * Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef.  Du kan bruke And eller Or og flere Where-uttrykk sammen i regelen.  
10. Klikk OK.
11. Lukk siden.
12. Lukk siden.

## <a name="assign-rule-to-benefit"></a>Tilordne regel til fordel
1. Gå til Personale > Fordeler > Fordeler.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Vis eller skjul delen Rettighetsregler.
5. Klikk Rediger.
6. Velg Regelbasert fra listen i Rettighet-feltet.
7. Klikk rullegardinknappen i Regeltype-feltet for å åpne oppslaget.
8. I listen finner og velger du regelen som ble opprettet tidligere.
9. Klikk koblingen i den valgte raden i listen.
10. Klikk Lagre.
11. Lukk skjemaet.

