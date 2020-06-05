---
title: Definer utgiftspolicyer
description: Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389721"
---
# <a name="define-expense-policies"></a>Definer utgiftspolicyer

[!include [banner](../includes/banner.md)]

Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger.         
Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte.         

For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250.       
Hvis en ansatt sender en reiseregning eller en reiserekvisisjon der romprisen per dag er høyere enn dette beløpet, vasler systemet        
den ansatte om at policybeløpet for utgifter er overskredet. Du kan konfigurere meldingen som den ansatte får når du        
definer policyreglene.      
        
Du kan definere tre typer policyer.         
        
- Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere        
  for senere rapportering.        

- Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen.       
 
 - Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning.        

## <a name="policy-tips"></a>Policytips
Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for reiseregninger. 
* Policyer har ikrafttredelsesdato og vil ikke tre i kraft hvis policyen opprettes med en dato etter datoen da utgiften fant sted. Hvis du for eksempel oppretter en ny policy i dag for å bruke en maksimal måltidsutgift på NOK 500, blir eksisterende utgifter registrert fra i går ikke kontrollert mot denne policyen.
* Når du oppretter en policy for en utgiftskategori som kan være spesifisert, må du vurdere å legge til en betingelse for utgiftslinjetype. Noen policyer, for eksempel å kreve en kvittering, vil kanskje ikke gi mening for spesifiserte linjer, og bør bare brukes på hodelinjen eller en ikke-spesifisert linje. 
* Policyer for reiseregning evalueres mot kildeenheten som standard. I konserninterne scenarioer kan du angi at policyen i stedet skal evalueres mot målenheten (enheten som låner). Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen Evaluer utgiftspolicy mot juridisk enhet som låner i arbeidsområdet **Funksjonsbehandling**.

## <a name="when-to-evaluate-policies"></a>Når skal policyer evalueres

I reiseregningsparametere finnes det et alternativ for å evaluere policyer for utgiftsadministrasjon når en linje lagres eller når en reiseregning sendes. Hvis du velger å evaluere når en linje lagres, sikrer du at brukerne har tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig. Ellers kan du utsette policyevalueringen og spare tid hvis du lar valideringen skje på slutten, under sending til arbeidsflyt.
