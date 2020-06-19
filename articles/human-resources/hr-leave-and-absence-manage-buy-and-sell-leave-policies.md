---
title: Administrere policyer for kjøp og salg av permisjon
description: Du kan gjøre det mulig for ansatte å kjøpe og selge permisjon i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429019"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Administrere policyer for kjøp og salg av permisjon

[!include [banner](includes/preview-feature.md)]

Du kan la de ansatte kjøpe permisjon ved å opprette en policy for å kjøpe permisjon.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Gjør det mulig for ansatte å kjøpe og selge permisjon

1. På **Parametere for permisjon og fravær**-siden velger du **Ja** for **Tillat ansatte å kjøpe permisjon**. 

## <a name="create-a-buy-leave-policy"></a>Opprette en policy for kjøp av permisjon

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen. 

2. Velg **Policy for kjøp og salg av permisjon**.

3. Velg **Ny**.

4. Angi et **Navn** og en **Beskrivelse** for policyen under **Policy for kjøp og salg av permisjon**. 

5. Velg en **Policytype**. 

   De tilgjengelige policytypene er **Antall** og **Timer per uke**. Velg **Antall** for å angi et **Fast antall** for det maksimale antallet de ansatte kan kjøpe og selge. Hvis du velger **Timer per uke**, brukes arbeidstiden som er definert i den ansattes tilordnede arbeidstidskalender, til å bestemme maksimumsantallet for policyen. 

6. Velg en **Startdato** og **Sluttdato** for policyen. Forespørsler om å kjøpe eller selge permisjon kan bare sendes innenfor denne tidsrammen. 

7. Under **Kjøpspolicy** velger du **Fulltidsekvivalent** (fte) for å fordele maksimumsantallet proporsjonalt på grunnlag av fulltidsekvivalenten som er definert i den ansattes stilling. Hvis policytypen er **Antall**, angir du et **Maksimalt fastsatt antall**. 

8. Velg **Legg til** for å legge til permisjonstyper for ansatte som vil kjøpe permisjon. Du kan legge til flere permisjonstyper i policyen. 

9. Angi **Måneder med jobberfaring** som permisjonstype for å aktivere forskjellige måneder med jobberfaring og fastslå det maksimale antallet en ansatt kan kjøpe. 

10. Angi **Maksimalt antall** for permisjonstypen. 

11. Angi en **Sats** som den ansatte kan kjøpe permisjon til. 

12. Du kan eventuelt angi en **Inntektskode** som kan brukes til å kjøpe permisjon. 

13. Angi eventuelt om du vil bruke FTE til å bestemme det maksimale antallet for permisjonstypen. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Legge til policyen for kjøp og salg av permisjon i en permisjons- og fraværsplan

1. På **Permisjon og fravær**-siden velger du en permisjons- og fraværsplan.

2. Under **Regler** velger du **Policy for kjøp og salg av permisjon**.

## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)</br>
[Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)</br>
[Avsett permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)</br>
[Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

