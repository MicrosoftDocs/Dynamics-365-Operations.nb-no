---
title: Klientfrakoblinger
description: Denne artikkelen forklarer hva du gjør hvis kunden kobles fra miljøet og ikke vet hvorfor.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40605fd14384dbeed933057621d0160b698c938a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869872"
---
# <a name="client-disconnects"></a>Klientfrakoblinger


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Miljødetaljer** 

Dette problemet kan oppstå i alle miljøer.
 
**Symptom** 

Kunden kobles fra miljøet og vet ikke hvorfor. Kunden mottar én av følgende feilmeldinger:

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
