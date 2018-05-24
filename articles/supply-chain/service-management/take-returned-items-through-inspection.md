---
title: Ta returnerte varer gjennom inspeksjon
description: Ta returnerte varer gjennom inspeksjon.
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: df209cfdbdef591e9f24161b3651316c43d69ee0
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---


# <a name="take-returned-items-through-inspection"></a>Ta returnerte varer gjennom inspeksjon 

[!include [banner](../includes/banner.md)]


1.  Klikk **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karanteneordrer**.

2.  Finn ordrelinjen som tilsvarer den returnerte varen du undersøker.

    > [!NOTE]
    > <P>En karanteneordre kan bare tilknyttes ett enkelt varenummer. Hvis 10 varer som har forskjellige varenumre returneres i én enkelt forsendelse og sendes i karantene, opprettes det 10 forskjellige karanteneordrer.</P>

3.  Når du er ferdig med å undersøke varen, velger du et alternativ i **Disposisjonskode**-feltet som angir hva som skal gjøres med varen og hvordan de tilknyttede finanstransaksjonene skal håndteres. Du kan for eksempel velge å returnere varen til lager og refundere kunden, kassere varen og sende kunden en ny, eller returnere varen til kunden uten godtgjøring.
    
    > [!NOTE]
    > <P>Hvis det returnerte partiet består av flere varer med samme partinummer, men som krever forskjellige disposisjonskoder, må du dele opp karanteneordren (<STRONG>Funksjoner</STRONG> &gt; <STRONG>Del</STRONG>) for å kunne tildele hvert delparti en egen disposisjonskode.</P>


4.  Når du er ferdig med undersøkelsen, klikker du **Ferdigmeld** for å frigi de returnerte varene og opprette en oppføring i vareankomstjournalen. Personen eller avdelingen som mottar varene behandler deretter journalen, slik at varene kan returneres til lager.
    
    – eller –
    
    Avslutt karanteneordren, og flytt varene tilbake til lager direkte med en av **Lager**-funksjonene.

5.  Lukk skjemaet for å lagre endringene.

## <a name="see-also"></a>Se også

[Angi hvordan du kvitter deg med returnerte varer](specify-how-to-dispose-of-returned-items.md)

  



