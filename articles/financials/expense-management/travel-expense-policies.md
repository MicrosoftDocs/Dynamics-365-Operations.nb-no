---
title: Definer utgiftspolicyer
description: "Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

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
