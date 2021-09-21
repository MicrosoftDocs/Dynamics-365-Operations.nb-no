---
title: Kjøpe og selge permisjon
description: Dette emnet beskriver hvordan du sender forespørsler om å kjøpe og selge permisjon i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 716afdc4e52c3e4a0432b987cb82077012d4d0c2
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431516"
---
# <a name="buy-and-sell-leave"></a>Kjøpe og selge permisjon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Dynamics 365 Human Resources kan du sende forespørsler om å kjøpe og selge permisjon basert på retningslinjene for kjøp og salg som er satt opp av firmaet.  

## <a name="request-to-buy-leave"></a>Forespørsel om å kjøpe permisjon

1. I arbeidsområdet **Ansattselvbetjening** velger du **Forespørsel om å kjøpe permisjon** på flisen **Avspaseringssaldoer**. 

2. Legg til en **Permisjonstype**, og angi et **Antall** som indikerer hvor mye permisjon du vil kjøpe. 

3. Velg **Send inn** når du er klar til å sende inn forespørselen. 

Saldoene blir enten automatisk oppdaterte eller går gjennom en godkjenningsprosess før oppdatering. Dette avhenger av hvordan kjøpspolicyen er konfigurert.

## <a name="request-to-sell-leave"></a>Forespørsel om å selge permisjon

1. I arbeidsområdet **Ansattselvbetjening** velger du **Forespørsel om å selge permisjon** på flisen **Avspaseringssaldoer**. 

2. Legg til en **Permisjonstype**, og angi et **Antall** som indikerer hvor mye permisjon du vil selge. 

3. Velg **Send inn** når du er klar til å sende inn forespørselen.

Saldoene blir enten automatisk oppdaterte eller går gjennom en godkjenningsprosess før oppdatering. Dette avhenger av hvordan kjøpspolicyen er konfigurert.


## <a name="troubleshooting"></a>Feilsøking 

Hvis arbeidsflyten for kjøp eller salg av permisjonsforespørsel mislykkes, kan brukere med rettigheten **EssLeaveBuySellRequestApprover** se gjennom meldingsloggen for alle forespørsler om kjøp og salg av permisjon. Hvis du vil gjøre dette, kan du gå til **Permisjon og fravær > Koblinger > Forepørsel om kjøp og salg av permisjon > Meldingslogg** (øverst til venstre). **Meldingsloggen** viser brukere hvordan transaksjonene ble behandlet og den tilknyttede arbeidsflytloggen.


## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)</br>
[Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
