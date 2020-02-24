---
title: Klientfrakoblinger
description: Denne artikkelen forklarer hva du gjør hvis kunden kobles fra hans eller hennes miljø og ikke vet hvorfor.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010042"
---
# <a name="client-disconnects"></a>Klientfrakoblinger

**Miljødetaljer** 

Dette problemet kan oppstå i alle miljøer.
 
**Symptom** 

Kunden kobles fra hans eller hennes miljø og vet ikke hvorfor. Kunden mottar én av følgende feilmeldinger:

- Forbindelsen er brutt. Klikk Lukk for å fortsette å arbeide.
- Det virker som du har mistet nettverkstilkoblingen. Klikk Prøv på nytt for å prøve på nytt.

**Rødt flagg**

Dette skjer ofte når brukere er i fasen for implementeringen, sammenligner informasjon på tvers av produksjon og testmiljøer og glemmer at de flytter mellom økter. Hvis brukere er på dette tidspunktet, vil de mest sannsynlig oppleve dette problemet.

**Avgang** 

**Weblesertyper:** Google Chrome, Internet Explorer og Microsoft Edge

Microsoft Dynamics 365 Human Resources kobler fra brukere når to forskjellige økter er åpne samtidig for samme bruker og samme weblesertype. (For eksempel viser bruker A både miljø 1 og miljø 2 i Chrome.) Det spiller ingen rolle om brukerne åpner ulike leservinduer eller forskjellige faner. Hvis den samme brukerlegitimasjonen brukes til å logge på både miljø 1 og miljø 2 samtidig og i den samme weblesertypen, kobler Human Resources fra én av øktene.

**Løsning**

Kontroller at bare ett miljø er åpent om gangen for en bestemt webleser. Brukere kan åpne flere økter i samme miljø (det vil si flere faner i samme webleser).

Brukere som vil hoppe mellom to miljøer samtidig, bør åpne hvert miljø i en annen webleser. (For eksempel kan bruker A vise miljø 1 i Chrome og miljø 2 i Microsoft Edge.)
