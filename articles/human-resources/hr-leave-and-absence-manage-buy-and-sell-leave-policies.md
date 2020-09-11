---
title: Administrere policyer for kjøp og salg av permisjon
description: Du kan gjøre det mulig for ansatte å kjøpe og selge permisjon i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712123"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Administrere policyer for kjøp og salg av permisjon

Du kan la de ansatte kjøpe og selge permisjon ved å opprette en policy for å kjøpe og selge permisjon. Du kan konfigurere disse policyene til å bruke arbeidsflyt for godkjenninger, angi maksimumsbeløp og -satser og angi satser for kjøp og salg. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Gjør det mulig for ansatte å kjøpe og selge permisjon

1. På **Parametere for permisjon og fravær**-siden velger du **Ja** for **Tillat ansatte å kjøpe permisjon** og **Tillat ansatte å selge permisjon**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Opprette en policy for kjøp og salg av permisjon

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen. 

2. Velg **Policy for kjøp og salg av permisjon**.

3. Velg **Ny**.

4. Angi et **Navn** og en **Beskrivelse** for policyen under **Policy for kjøp og salg av permisjon**. 

5. Velg en **Policytype**. 

   De tilgjengelige policytypene er **Antall** og **Timer per uke**. Velg **Antall** for å angi et **Fast antall** for det maksimale antallet de ansatte kan kjøpe og selge. Hvis du velger **Timer per uke**, brukes arbeidstiden som er definert i den ansattes tilordnede arbeidstidskalender, til å bestemme maksimumsantallet for policyen. 

6. Velg en **Startdato** og **Sluttdato** for policyen. Forespørsler om å kjøpe eller selge permisjon kan bare sendes innenfor denne tidsrammen. 

7. Velg en **Arbeidsflyt-ID** for policyen. Alle kjøps- og salgsforespørsler vil bruke denne arbeidsflyten til gjennomgang og godkjenning. 

8. Under **Kjøpspolicy** velger du **Fulltidsekvivalent** (fte) for å fordele maksimumsantallet proporsjonalt på grunnlag av fulltidsekvivalenten som er definert i den ansattes stilling. Hvis policytypen er **Antall**, angir du et **Maksimalt fastsatt antall**. 

9. Velg **Legg til** for å legge til permisjonstyper for ansatte som vil kjøpe permisjon. Du kan legge til flere permisjonstyper i policyen. 

10. Angi **Måneder med jobberfaring** som permisjonstype for å aktivere forskjellige måneder med jobberfaring og fastslå det maksimale antallet en ansatt kan kjøpe. 

11. Angi **Maksimalt antall** for permisjonstypen. 

12. Angi en **Sats** som den ansatte kan kjøpe permisjon til. 

13. Du kan eventuelt angi en **Inntektskode** som kan brukes til å kjøpe permisjon. 

14. Angi eventuelt om du vil bruke FTE til å bestemme det maksimale antallet for permisjonstypen. 

15. Hvis du vil opprette en salgspolicy, følger du trinn 8 til 14 under **Salgspolicy**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Legge til policyen for kjøp og salg av permisjon i en permisjons- og fraværsplan

1. På **Permisjon og fravær**-siden velger du en permisjons- og fraværsplan.

2. Under **Regler** velger du **Policy for kjøp og salg av permisjon**.

## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)</br>
[Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)</br>
[Avsett permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)</br>
[Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

