--- 
title: Definere rettighetsregler og policyer for fordel
description: Denne registreringen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere rettighetsregler og policyer for fordel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne registreringen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.  

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


