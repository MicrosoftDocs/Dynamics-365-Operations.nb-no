---
title: Angi hvordan du kvitter deg med returnerte varer
description: Angi hvordan du kvitter deg med returnerte varer.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c827df81621346733953dc77e16e269f8c3767a8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910119"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Angi hvordan du kvitter deg med returnerte varer 

[!include [banner](../includes/banner.md)]


Når du håndterer en returordre, må du angi en returårsakskode for å identifisere produktet som returneres. Du må også angi en disposisjonskode og en disposisjonshandling for å avgjøre hva som skal gjøres med det returnerte produktet.

En disposisjonskode kan brukes når du oppretter returordren, registrerer vareankomst eller følgeseddeloppdaterer en vareankomst og avslutter karanteneordrer.

Du kan angi hvilken som helst disposisjonskode for å støtte forretningsprosessene. Tabellen nedenfor inneholder et sett med vanlige koder som kan tildeles returvaredisposisjon.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Disposisjonstype</p></th>
<th><p>Felleskode</p></th>
<th><p>beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Avhending</p></td>
<td><p>SC</p></td>
<td><p>Kasting/avhending</p></td>
</tr>
<tr class="even">
<td><p>Avhending</p></td>
<td><p>DC</p></td>
<td><p>Gave til veldedig organisasjon</p></td>
</tr>
<tr class="odd">
<td><p>Avhending</p></td>
<td><p>TD</p></td>
<td><p>Avhending av tredjepart</p></td>
</tr>
<tr class="even">
<td><p>Avhending</p></td>
<td><p>SL</p></td>
<td><p>Gjenbruk</p></td>
</tr>
<tr class="odd">
<td><p>Avhending</p></td>
<td><p>TS</p></td>
<td><p>Salg av tredjepart (annenhåndsmarkeder)</p></td>
</tr>
<tr class="even">
<td><p>Reparasjon/modifisering</p></td>
<td><p>RW</p></td>
<td><p>Omarbeiding</p></td>
</tr>
<tr class="odd">
<td><p>Reparasjon/modifisering</p></td>
<td><p>RF</p></td>
<td><p>Refabrikkering/renovering</p></td>
</tr>
<tr class="even">
<td><p>Reparasjon/modifisering</p></td>
<td><p>MD</p></td>
<td><p>Modifisering</p></td>
</tr>
<tr class="odd">
<td><p>Reparasjon/modifisering</p></td>
<td><p>RP</p></td>
<td><p>Reparering</p></td>
</tr>
<tr class="even">
<td><p>Reparasjon/modifisering</p></td>
<td><p>RV</p></td>
<td><p>Retur til leverandør</p></td>
</tr>
<tr class="odd">
<td><p>Annet</p></td>
<td><p>AI</p></td>
<td><p>Bruk varen som den er</p></td>
</tr>
<tr class="even">
<td><p>Annet</p></td>
<td><p>RS</p></td>
<td><p>Videresalg</p></td>
</tr>
<tr class="odd">
<td><p>Annet</p></td>
<td><p>EX</p></td>
<td><p>Veksle</p></td>
</tr>
<tr class="even">
<td><p>Annet</p></td>
<td><p>MS</p></td>
<td><p>Diverse</p></td>
</tr>
</tbody>
</table>


Du må velge en disposisjonshandling for hver ny disposisjonskode du angir. Disposisjonshandlingen avgjør de fysiske og økonomiske implikasjonene for disposisjonskodene. Disposisjonshandlingen avgjør for eksempel den fysiske handlingen for den returnerte varen, den økonomiske effekten av den returnerte varen, og om det må sendes en erstatningsvare til kunden. Du kan konfigurere et ubegrenset antall disposisjonskoder i henhold til dine forretningsbehov, men du kan bare velge blant seks forhåndsdefinerte disposisjonshandlinger. Tabellen nedenfor inneholder disposisjonshandlingene og definisjonene.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Disposisjonshandling</p></th>
<th><p>beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kreditt</strong></p></td>
<td><p>Returner varen til lageret, og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bare kreditering</strong></p></td>
<td><p>Krediter kunder uten å kreve eller forvente at varen returneres.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Svinn</strong></p></td>
<td><p>Kasser varen, og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Erstatt og krediter</strong></p></td>
<td><p>Returner varen til lageret, opprett en erstatningsordre og krediter kunden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Erstatt og kasser</strong></p></td>
<td><p>Kasser varen, opprett en erstatningsordre og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Returner til kunde</strong></p></td>
<td><p>Avvis den returnerte varen, og returner den til kunden.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Velg en disposisjonskode for en karanteneordre

1.  Klikk på **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karanteneordrer**.

2.  Velg en handling fra feltet **Disposisjonskode** i fanen **Oversikt** hvis det gjelder en eksisterende karanteneordre.



## <a name="see-also"></a>Se også

[Karanteneordre (skjema)](/dynamicsax-2012//quarantine-order-form)

[Disposisjonskoder (skjema)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]