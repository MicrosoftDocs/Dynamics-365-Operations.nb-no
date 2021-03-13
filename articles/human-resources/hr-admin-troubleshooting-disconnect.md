---
title: Klientfrakoblinger
description: Denne artikkelen forklarer hva du gjør hvis kunden kobles fra hans eller hennes miljø og ikke vet hvorfor.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
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
ms.openlocfilehash: d02916283bbd4cee6502942020df1b275a0242b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113735"
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
