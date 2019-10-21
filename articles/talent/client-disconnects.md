---
title: Frakoblinger for Talent-klient
description: Dette emnet forklarer hva du gjør hvis kunden kobles fra hans eller hennes miljø og ikke vet hvorfor.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008181"
---
# <a name="talent-client-disconnects"></a>Frakoblinger for Talent-klient

[!include [banner](includes/banner.md)]

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

Microsoft Dynamics 365 Talent kobler fra brukere når to forskjellige økter er åpne samtidig for samme bruker og samme weblesertype. (For eksempel viser bruker A både miljø 1 og miljø 2 i Chrome.) Det spiller ingen rolle om brukerne åpner ulike leservinduer eller forskjellige faner. Hvis den samme brukerlegitimasjonen brukes til å logge på både miljø 1 og miljø 2 samtidig og i den samme weblesertypen, kobler Talent fra én av øktene.

**Løsning**

Kontroller at bare ett miljø er åpent om gangen for en bestemt webleser. Brukere kan åpne flere økter i samme miljø (det vil si flere faner i samme webleser).

Brukere som vil hoppe mellom to miljøer samtidig, bør åpne hvert miljø i en annen webleser. (For eksempel kan bruker A vise miljø 1 i Chrome og miljø 2 i Microsoft Edge.)
