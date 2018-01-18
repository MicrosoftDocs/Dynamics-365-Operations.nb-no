---
title: Definer utgiftspolicyer
description: "Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a>Utgiftspolicyer

[!include[banner](../includes/banner.md)]

Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger. Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte. 

For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250. Hvis en arbeidstaker sender inn en utgiftsrapport for en reiseregning hvor romprisen er større enn dette beløpet, vil systemet varsle arbeidstakeren om at policybeløpet for denne utgiften er overskredet. Du kan konfigurere meldingen arbeidstakeren mottar når du definerer denne policyen. 

Du kan definere tre typer policyer. 

 - Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere  
 for senere rapportering. 
 - Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen. 
 - Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning. 

Du kan også sette opp en datoperioden for når utgiftpolicyen er effektiv. For eksempel kan flyprisene for flyvninger mellom Danmark og New York City være dyre under høysesonger. Du kan definere en utgiftsregel for flyvninger som begrenser kostanden for flyvninger til New York City til en grense på DKK 5000, og du kan spesifisere at denne regelen skal gjelde mellom 15. mars og 15. september. 

