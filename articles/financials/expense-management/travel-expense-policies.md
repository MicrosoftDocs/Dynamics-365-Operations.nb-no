---
title: Definer utgiftspolicyer
description: "Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a>Utgiftspolicyer

[!INCLUDE [banner](../includes/banner.md)]

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
 
  Du kan også sette opp en datoperioden for når utgiftpolicyen er effektiv. For eksempel, flybilletter for fly mellom Danmark      
  og New York City kan være kostbare i høysesongen. Du kan definere en utgiftsregel for flyvninger som begrenses av      
  en grense for kostnaden på flybilletter til New York City på DKK 5000, og du kan spesifisere at regelen er gyldig mellom 15. mars og      
  15. september.

