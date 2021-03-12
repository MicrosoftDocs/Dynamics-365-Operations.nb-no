---
title: Salgspriser for abonnement
description: Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet Salgspris (abonnement).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974229"
---
# <a name="subscription-sales-prices"></a>Salgspriser for abonnement   

[!include [banner](../includes/banner.md)]


Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet **Salgspris (abonnement)**.

I skjemaet **Salgspris (abonnement)** kan du opprette salgspriser for et bestemt abonnement, eller du kan opprette salgspriser som er mer generelle. Før en salgspris kan brukes på et abonnement, må periodekoden og valutaen for abonnementet være identisk med periodekoden og valutaen for salgsprisen.

Hvis periodekoden og valutaen er identiske for abonnementet og salgsprisen, velges salgspriser for abonnement på grunnlag av prioritetene som er angitt i følgende tabell. En to celle i tabellen angir et tomt felt, og en X angir en verdi som er lik verdien i abonnementet der transaksjonen genereres fra.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prioritet </p></th>
<th><p><strong>Kategori</strong></p></th>
<th><p><strong>Prosjekt-ID</strong></p></th>
<th><p><strong>Abonnement</strong></p></th>
<th><p><strong>Salgsvaluta</strong></p></th>
<th><p><strong>Periodekode</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


Når det opprettes en abonnementsavgift, velges salgsprisen med det største detaljnivået, som angitt i tabellen ovenfor, som salgsprisen for abonnement.

## <a name="update-and-index-subscription-sales-prices"></a>Oppdatere og indeksere salgspriser for abonnement

Du kan oppdatere salgsprisen for abonnement ved å oppdatere basisprisen eller indeksen. Du kan oppdatere med en prosentverdi eller til en ny verdi.

## <a name="subscription-fee-sales-prices"></a>Salgspriser for abonnementsavgift

Når du oppretter en abonnementsavgift, er salgsprisen basert på salgsprisoppsettet for abonnementet. Du kan enten bruke basisprisen fra abonnementets prisoppsett eller opprette indekserte salgspriser.

## <a name="example"></a>Eksempel

Du vil definere salgspriser for abonnement på EUR 500 for det nye prosjektet 9030. I skjemaet **Salgspris (abonnement)** oppretter du en salgsprislinje for abonnement som vist i følgende tabell.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Gyldig fra</p></th>
<th><p>Kategori</p></th>
<th><p>Project</p></th>
<th><p>Abonnement</p></th>
<th><p>Periodekode</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Måned</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Legg merke til at feltene **Kategori** og **Abonnement** er tomme.

Deretter oppretter du følgende abonnementer:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Serviceabonnement</p></th>
<th><p>Project</p></th>
<th><p>Abonnementsgruppe</p></th>
<th><p>Kategori</p></th>
<th><p>Valuta</p></th>
<th><p>Periodekode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>EUR</p></td>
<td><p>Månedlig</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>Månedlig</p></td>
</tr>
</tbody>
</table>


Nå oppretter du abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1:

1.  Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.

2.  I skjemaet **Abonnementsgrupper** klikker du **Funksjon** \> **Opprett abonnementsavgift**.

3.  Angi aktuell informasjon i skjemaet **Opprett abonnementsavgift**. Hvis du vil ha mer informasjon, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).

Abonnementsavgifter med en salgspris på EUR 500 opprettes for begge abonnementer, som vist i følgende tabell.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prosjektdato</p></th>
<th><p>Serviceabonnement</p></th>
<th><p>Project</p></th>
<th><p>Kategori</p></th>
<th><p>Startdato</p></th>
<th><p>Sluttdato</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Senere bestemmer du deg for at du vil angi salgspriser for kategorien SubCat1 for prosjekt 9030. Derfor oppretter du en ny salgsprislinje som har en salgspris på EUR 550 for kombinasjonen av prosjekt 9030 og gebyrkategorien SubCat1. Det finnes nå to salgsprislinjer for abonnement for prosjekt 9030, som vist i følgende tabell:

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Gyldig fra</p></th>
<th><p>Kategori</p></th>
<th><p>Project</p></th>
<th><p>Abonnement</p></th>
<th><p>Periodekode</p></th>
<th><p>Valuta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Måned</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Måned</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


Du gjentar fremgangsmåten som er beskrevet ovenfor for å opprette abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1. Tabellen nedenfor viser transaksjonene som opprettes for hvert abonnement som er knyttet til abonnementsgruppen.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prosjektdato</p></th>
<th><p>Abonnement</p></th>
<th><p>Project</p></th>
<th><p>Kategori</p></th>
<th><p>Startdato</p></th>
<th><p>Sluttdato</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.07.2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28.07.2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


I den første transaksjonen for abonnement 00020\_135 er salgsprisen på EUR 550 avledet fra salgsprisen for abonnement som er definert for kombinasjonen av det bestemte prosjektet og kategorien. I den andre transaksjonen for abonnement 00021\_135 brukes salgsprisen på EUR 500 som salgsprisen for prosjektabonnement, fordi det ikke er definert en pris for kombinasjonen av prosjekt 9030 og kategori SubCat2.

## <a name="see-also"></a>Se også

[Oppdatere og indeksere salgspriser for abonnement](update-and-index-subscription-sales-prices.md)

  


