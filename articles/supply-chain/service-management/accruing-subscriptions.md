---
title: Avsetning av abonnementer
description: Med serviceabonnementer kan du manuelt avsette omsetning i periodene etter datoen da du fakturerte en gebyrtransaksjon.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0d6c25cc8a19f5ebea3477cd2c957876752fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966086"
---
# <a name="accruing-subscriptions"></a>Avsetning av abonnementer 

[!include [banner](../includes/banner.md)]


Med serviceabonnementer kan du manuelt avsette omsetning i periodene etter datoen da du fakturerte en gebyrtransaksjon.

Det opprettes avsetningsperioder for fakturaperioden du har definert for abonnementsgebyret, og avsetningsperiodene er basert på periodekoden for abonnementet.

Du kan avsette og tilbakeføre påløpt omsetning.

## <a name="reverse-accruals-of-credit-amounts"></a>Tilbakefør avsetninger av kreditbeløp

Hvis du krediterer fakturerte abonnementsbeløp, kan du bruke to metoder for å tilbakeføre de påløpte beløpene:

  - Du kan tilbakeføre hvert påløpte inntektstransaksjon enkeltvis før du oppretter et kreditnotaforslag for transaksjonen. Dette er den manuelle metoden. (manuell)

  - Du kan få de påløpte beløpene tilbakeført på datoen når kreditnotaen posteres eller på den opprinnelige posteringsdatoen for avsetningen.

Hvis du vil ha mer informasjon, kan du se [Abonnementsparametere (skjema)](https://technet.microsoft.com/library/aa619615.aspx).

## <a name="setup-requirements"></a>Installasjonskrav

Hvis du vil avsette omsetning, må du sørge for at følgende datakravene oppfylles:

## <a name="account-setup"></a>Kontooppsett

Kontoene **VIA – abonnement** og **Påløpt inntekt – abonnement** må være konfigurert i **Prosjekt**-modulen.

Når du posterer påløpt omsetning, debiteres kontoen **VIA – abonnement** med det påløpte beløpet, og kontoen **Påløpt inntekt – abonnement** krediteres med det påløpte beløpet.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Definere kontoer for avsetning av abonnementsomsetning

1.  Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Postering** \> **Finansposteringsoppsett**.

2.  Klikk på fanen **Inntektskontoer**, og velg **VIA – abonnement** eller **Påløpt inntekt – abonnement** for å konfigurere kontoene.

## <a name="subscription-group-setup"></a>Oppsett for abonnementsgruppe

For å kunne avsette inntekt for abonnementer må det være merket av for **Avsett inntekt**. Dette finnes i skjemaet **Abonnementsgrupper** for gruppen som er knyttet til abonnementet. Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Aktivere omsetningsavsetning på en abonnementsgruppe

1.  Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.

## <a name="periods"></a>Perioder

Du må definere en periodekode for fakturering. Med mindre du vil avsette omsetning i de samme tidsintervallene du bruker for fakturering, må du også definere en avsetningsperiode.

I følgende tabell får du en oversikt over hvilke avsetningsperioder du kan definere for hver faktureringsperiode:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Faktureringstermin</p></th>
<th><p>Avsetningsperiode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>År</strong></p></td>
<td><ul>
<li><p><strong>År</strong></p></li>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Kvartal</strong></p></td>
<td><ul>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Måned</strong></p></td>
<td><ul>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Uke</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Dag</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Definering av faktureringsperioden er en obligatorisk del av det totale oppsettet for abonnementsgrupper. Du kan bestemme om du vil også definere en avsetningsperiode for abonnementsgruppen. Hvis du definerer en avsetningsperiode for abonnementsgruppen, foreslås denne perioden i **Periodekode**-feltet. Dette feltet finnes i skjemaet **Avsett abonnementsomsetning** når du avsetter abonnementsomsetning. Avsetningsperioden er imidlertid valgfri informasjon om abonnementsgruppen.


> [!NOTE]
> <P>Bruk følgende bane til å åpne skjemaet <STRONG>Avsett abonnementsomsetning</STRONG>. Klikk på <STRONG>Servicestyring</STRONG> &gt; <STRONG>Periodisk</STRONG> &gt; <STRONG>Serviceabonnementer</STRONG> &gt; <STRONG>Avsett abonnementsomsetning</STRONG>.</P>


## <a name="transactions"></a>Transaksjoner

Du kan styre antallet finanstransaksjoner som opprettes når du posterer påløpt inntekt. For abonnementer kan du definere om finanstransaksjoner skal opprettes som en total eller per linje.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Angi nivået av posteringsdetaljer som skal vises for avsatte transaksjoner

1.  Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.

2.  På fanen **Økonomisk** i **Faktura**-feltet velger du **Total** eller **Linje**.


## <a name="see-also"></a>Se også

[Avsett abonnementsomsetning](accrue-subscription-revenue.md)

  


