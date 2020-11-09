---
title: Aldersfordelt saldoliste for kunder
description: Rapport for aldersfordeling for kunde for kunder viser saldoene som forfaller fra kunder, sortert etter dato intervall eller periode for aldersfordelings.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: e43aef72b7d65db1dcb014dfada5233ac051ba7c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2020
ms.locfileid: "4013059"
---
# <a name="customer-aging-report"></a>Aldersfordelt saldoliste for kunder 

**Rapport for aldersfordeling for kunde** viser saldoene som forfaller fra kunder, sortert etter dato intervall eller periode for aldersfordelings.

Når du genererer denne rapporten, vises standardparametrene nedenfor. Du kan bruke disse parametrene til å filtrere dataene som skal vises i rapporten. Hvis du vil ha mer informasjon, kan du se [Definere innkreving](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Felt</p></th>
<th><p>beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Faktureringsklassifisering</strong></p></td>
<td><p>Velg én eller flere faktureringsklassifiseringer som skal tas med i rapporten.</p>
<div class="alert">

**Obs!** Denne kontrollen er bare tilgjengelig hvis konfigurasjonsnøkkelen for <STRONG>offentlig sektor</STRONG> er valgt.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Inkluder transaksjoner uten faktureringsklassifisering</strong></p></td>
<td><p>Hvis det er merket av for dette, vises alle transaksjoner som ikke er tilordnet en faktureringsklassifisering, i rapporten.</p>
<div class="alert">

**Obs!** Denne kontrollen er bare tilgjengelig hvis konfigurasjonsnøkkelen for <STRONG>offentlig sektor</STRONG> er valgt.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Aldersfordeling per</strong></p></td>
<td><p>Angi datoen som brukes i gjeldende aldersfordelingen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Saldo per</strong></p></td>
<td><p>Skriv inn en dato du vil vise kundesaldo for. Dette kalles også en frist for transaksjoner.</p></td>
</tr>
<tr class="even">
<td><p><strong>Startdato</strong></p></td>
<td><p>Angi datoen som er i første periodeintervall eller aldersfordelingsperiode som skal tas med i rapporten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Vilkår</strong></p></td>
<td><p>Velg datotypen som rapporten skal baseres på.</p>
<ul>
<li><p><strong>Transaksjonsdato</strong> – Posteringsdatoen for de valgte transaksjonene. Dette kan for eksempel være en fakturadato som er grunnlaget for beregningen av forfallsdatoen.</p></li>
<li><p><strong>Forfallsdato</strong> – Forfallsdatoen til transaksjonene basert på betalingsbetingelsene.</p></li>
<li><p><strong>Dokumentdato</strong> – En brukerdefinert dokumentdato som er grunnlaget for beregning av forfallsdatoen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Definisjon av aldersfordelingsperiode</strong></p></td>
<td><p>Velg en definisjon av aldersfordelingsperiode. <strong>Intervall</strong>-feltet brukes ikke hvis du velger en definisjon av aldersfordelingsperiode.</p>
<p>Definisjoner for aldersfordelingsperiode som har mer enn seks aldersfordelingsperioder, kan ikke brukes på den utskrevne rapporten.</p>
<div class="alert">

**Obs!** Du kan definere aldersfordelingsperioder på siden <STRONG>Definisjoner av aldersfordelingsperiode</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Skriv ut beskrivelse for aldersfordelingsperiode</strong></p></td>
<td><p>Velg <strong>Ja</strong> for å inkludere beskrivelser av aldersfordelingsperiode øverst på hver kolonne for aldersfordelingsperiode i rapporten. Velg <strong>Nei</strong> for å skrive ut rapporten uten kolonneoverskrifter.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intervall</strong></p></td>
<td><p>Definer perioden som skal brukes, ved å angi nummeret på dagen eller månedsenheter i hver periode. Hvis du for eksempel vil vise aldersfordelingsinformasjon etter uke, angir du 7 i dette feltet og velger <strong>Dag</strong> i <strong>Dag/mnd</strong>-feltet.</p>
<div class="alert">

**Obs!** Informasjonen du har angitt i dette feltet, brukes bare hvis du ikke har valgt en definisjon av aldersfordelingsperiode. Hvis ikke defineres utskriftsretningen på definisjon av aldersfordelingsperiode.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Dag/mnd</strong></p></td>
<td><p>Velg enheten, enten <strong>Dag</strong> eller <strong>Måned</strong>, som brukes til å definere perioden i <strong>Intervall</strong>-feltet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Utskriftsretning</strong></p></td>
<td><p>Velg om du skal beregne saldoer og skrive ut rapport for aldersfordeling for tidligere eller fremtidige perioder. Datoene evalueres i forhold til datoen som er valgt i <strong>Saldo per</strong>-feltet. Velg <strong>Bakover</strong> for å vise informasjon for tidligere perioder. Velg <strong>Forover</strong> for å vise informasjon for fremtidige perioder.</p>
<div class="alert">
  
<STRONG>Obs!</STRONG> Informasjonen du har angitt i dette feltet, brukes bare hvis du ikke har valgt en definisjon av aldersfordelingsperiode.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Detaljer</strong></p></td>
<td><p>Velg å vise en liste over transaksjoner som er inkludert i saldoene som vises i rapporten.</p></td>
</tr>
<tr class="even">
<td><p><strong>Inkluder beløp i transaksjonsvaluta</strong></p></td>
<td><p>Velg for å ta med beløp i transaksjonsvalutaen i tillegg til beløp i regnskapsvalutaen. Hvis det ikke er merket av i denne boksen, vises beløpene i rapporten bare i regnskapsvalutaen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negativ saldo</strong></p></td>
<td><p>Velg dette for å ta med kundekontoer med negative saldoer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ekskluder null saldo-kontoer</strong></p></td>
<td><p>Velg dette for å utelate kundekontoer med null i saldo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Betalingsposisjonering</strong></p></td>
<td><p>Velg for å vise betalinger som ikke er utlignet. Disse vises i den første kolonnen i rapporten.</p></td>
</tr>
</tbody>
</table>

