---
title: Oversikt over innkjøpsrekvisisjoner
description: Dette emnet beskriver arbeidsflyten for innkjøpsrekvisisjoner og de ulike statusene som en innkjøpsrekvisisjon kan ha.
author: Henrikan
ms.date: 11/02/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2174"
- intro-internal
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acd0deebe79e29bd1beb32ea21cd179f5bf12c43
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982908"
---
# <a name="purchase-requisition-overview"></a>Oversikt over innkjøpsrekvisisjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver arbeidsflyten for innkjøpsrekvisisjoner og de ulike statusene som en innkjøpsrekvisisjon kan ha.

Avhengig av oppsettet for organisasjonen kan du opprette innkjøpsrekvisisjoner for produkter som organisasjonen din bruker. En innkjøpsrekvisisjon er et internt dokument som gir innkjøpsavdelingen autorisasjon til å kjøpe inn varer eller tjenester.  

Når en innkjøpsrekvisisjon er godkjent, kan den brukes til å generere en bestilling. Bestillinger er de eksterne dokumentene som innkjøpsavdelingen sender til leverandører.

## <a name="creating-purchase-requisitions"></a>Opprette innkjøpsrekvisisjoner
Du kan opprette en innkjøpsrekvisisjon på siden **Mine innkjøpsrekvisisjoner** og velge varene og tjenestene du trenger. Du kan velge varer fra en innkjøpskatalog som organisasjonen har opprettet, eller du kan be om varer som ikke finnes i katalogen, ved å velge en innkjøpskategori og angi produktdetaljene.  

Før du kan sende en innkjøpsrekvisisjon til gjennomgang må en arbeidsflyter være konfigurert. Du bruker en arbeidsflyt til å flytte en innkjøpsrekvisisjon gjennom vurderingsprosessen, fra den innledende statusen **Utkast** til den endelige statusen **Godkjent**.

### <a name="purchase-requisition-statuses"></a>Innkjøpsrekvisisjonsstatuser

Når du oppretter en innkjøpsrekvisisjon, blir en status tilordnet. En status tilordnes også til hver linje du legger til i en innkjøpsrekvisisjon. Når du har sendt en innkjøpsrekvisisjon til en arbeidsflyt for gjennomgang, oppdateres statusen for innkjøpsrekvisisjonen og statusen for hver linje når linjene går gjennom arbeidsflytprosessen.  

Du kan konfigurere arbeidsflytprosessen for innkjøpsrekvisisjon for å sende en innkjøpsrekvisisjon gjennom vurderingsprosessen som ett dokument. Alternativt kan linjene i en innkjøpsrekvisisjon sendes enkeltvis til de aktuelle kontrollørene. Hvis innkjøpsrekvisisjonslinjene gjennomgås hver for seg, kan statusen for hver innkjøpsrekvisisjonslinje oppdateres når linjen går gjennom kontrollprosessen. Når alle linjer har fullført kontrollprosessen og ingen vurderingstrinn gjenstår for innkjøpsrekvisisjonen, oppdateres statusen for hele innkjøpsrekvisisjonen.

### <a name="purchase-requisition-workflow"></a>Arbeidsflyt for innkjøpsrekvisisjon

Diagrammet nedenfor viser statusene som er tilordnet til en innkjøpsrekvisisjon og en innkjøpsrekvisisjonslinje når de flyttes i arbeidsflytprosessen.  

[![Statuser for innkjøpsrekvisisjonshode og -linjer.](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Relasjoner mellom status for innkjøpsrekvisisjonshode og linjer

Den overordnede statusen for en innkjøpsrekvisisjon bestemmes av statusen for innkjøpsrekvisisjonslinjene. Derfor må må vurderingsprosessen fullføres for alle innkjøpsrekvisisjonslinjene før vurderingsprosessen for innkjøpsrekvisisjonen i sin helhet kan fullføres. Tabellen nedenfor beskriver statusene som tilordnes til et innkjøpsrekvisisjonshode og innkjøpsrekvisisjonslinjer når innkjøpsrekvisisjonen flyttes i arbeidsflytprosessen.

<table>
<thead>
<tr class="header">
<th>Status for innkjøpsrekvisisjon</th>
<th>Status til innkjøpsrekvisisjonslinje</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utkast</td>
<td>Utkast</td>
<td>Innkjøpsrekvisisjonen og innkjøpsrekvisisjonslinjen er opprettet, men de er ikke sendt til gjennomgang. Innkjøpsrekvisisjonener og alle innkjøpsrekvisisjonslinjer som har statusen <strong>Utkast</strong> kan endres. En innkjøpsrekvisisjon eller innkjøpsrekvisisjonslinjen har også statusen <strong>Utkast</strong> hvis den har blitt tilbakekalt, men ikke sendt på nytt til gjennomgang. <strong>Obs! </strong> Du kan sende eller hente frem en innkjøpsrekvisisjon på dokumentnivå. Du kan imidlertid ikke sende eller tilbakekalle en enkelt innkjøpsrekvisisjonslinje.</td>
</tr>
<tr class="even">
<td>Til vurdering</td>
<td><ul>
<li>Til vurdering</li>
<li>Avslått</li>
</ul></td>
<td>Hvis arbeidsflyten er konfigurert til å rute innkjøpsrekvisisjonslinjene til individuelle kontrollører, kan hver linje ha statusen <strong>Til vurdering</strong> eller <strong>Avvist</strong>. Statusen for innkjøpsrekvisisjonen oppdateres når kontrollprosessen er fullført for alle innkjøpsrekvisisjonslinjer og ingen vurderingstrinn gjenstår for innkjøpsrekvisisjonen.
<ul>
<li><strong>Til vurdering</strong> – Innkjøpsrekvisisjonslinjene er sendt til gjennomgang. Når arbeidsflytprosessen er fullført for en innkjøpsrekvisisjonslinje, forblir statusen for denne linjen <strong>Til vurdering</strong> til alle gjenværende innkjøpsrekvisisjonslinjer er gjennomgått.</li>
<li><strong>Avvist</strong> – En innkjøpsrekvisisjonslinje er avvist. Innkjøpsrekvisisjonslinjer som er avvist kan endres og sendes på nytt.</li>
</ul>
Hvis du sende en innkjøpsrekvisisjonslinje som er avvist, på nytt, starter kontrollprosessen på nytt for alle linjene i innkjøpsrekvisisjonen som fortsatt er til vurdering. </br><strong>Obs!</strong> Du kan tilbakekalle en innkjøpsrekvisisjon som allerede er sendt. Når du tilbakekaller en innkjøpsrekvisisjon, blir også alle andre innkjøpsrekvisisjonslinjer tilbakekalt. Innkjøpsrekvisisjonslinjer som har blitt tilbakekalt, kan slettes.</td>
</tr>
<tr class="odd">
<td>Avslått</td>
<td>Avslått</td>
<td>Innkjøpsrekvisisjonen og alle innkjøpsrekvisisjonslinjene er avvist. Innkjøpsrekvisisjonener og alle innkjøpsrekvisisjonslinjer sin er avvist, kan sendes på nytt.</td>
</tr>
<tr class="even">
<td>Godkjent</td>
<td><ul>
<li>Godkjent</li>
<li>Annullert</li>
<li>Lukket</li>
</ul></td>
<td>Alle innkjøpsrekvisisjonslinjer har fullført kontrollprosessen, og ingen vurderingstrinn flere gjenstår for innkjøpsrekvisisjonen.
<ul>
<li><strong>Godkjent</strong> – kontrollprosessen for en innkjøpsrekvisisjonslinje er fullført, og linjen er godkjent.</li>
<li><strong>Avbrutt</strong> – innkjøpsrekvisisjonslinjen ble godkjent, men den ble avbrutt fordi den ikke lenger er nødvendig. Bare innkjøpsrekvisisjonslinjer som har blitt godkjent, kan avbrytes.</li>
<li><strong>Lukket</strong> – innkjøpsrekvisisjonslinjen ble godkjent, og dokumenter er generert, avhengig av rekvisisjonsformålet.
<ul>
<li>Hvis innkjøpsrekvisisjonsformålet er forbruk, er en bestilling generert for innkjøpsrekvisisjonslinjen.</li>
<li>Hvis innkjøpsrekvisisjonsformålet er etterfylling, er ett eller flere fullføringsdokumenter generert.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Annullert</td>
<td>Annullert</td>
<td>Innkjøpsrekvisisjonen og alle innkjøpsrekvisisjonslinjer har blitt avbrutt.</br> <strong>Obs!</strong> Hvis du ikke lenger trenger en vare som er på en innkjøpsrekvisisjonslinje, må du avbryte innkjøpsrekvisisjonslinjen hvis den allerede er godkjent. Bare innkjøpsrekvisisjonslinjer som har blitt godkjent, kan avbrytes. Hvis innkjøpsrekvisisjonslinjer er til vurdering, får innkjøpsrekvisisjonen statusen <strong>Til vurdering</strong>. I så fall kan du tilbakekalle innkjøpsrekvisisjonen og slette den aktuelle innkjøpsrekvisisjonslinjen.</td>
</tr>
<tr class="even">
<td>Lukket</td>
<td><ul>
<li>Lukket</li>
<li>Annullert</li>
</ul></td>
<td>Innkjøpsrekvisisjonen er lukket, og ett eller flere fullføringsdokumenter er generert.
<ul>
<li><strong>Lukket</strong> – innkjøpsrekvisisjonslinjen ble godkjent, og dokumenter er generert, avhengig av rekvisisjonsformålet.
<ul>
<li>Hvis innkjøpsrekvisisjonsformålet er forbruk, er en bestilling generert for innkjøpsrekvisisjonslinjen.</li>
<li>Hvis innkjøpsrekvisisjonsformålet er etterfylling, er ett eller flere fullføringsdokumenter generert.</li>
</ul></li>
<li><strong>Avbrutt</strong> – innkjøpsrekvisisjonslinjen ble godkjent, men den ble avbrutt fordi den ikke lenger er nødvendig. Bare innkjøpsrekvisisjonslinjer som har blitt godkjent, kan avbrytes.</li>
</ul>
<strong>Obs!</strong> Hvis du ikke lenger trenger en vare på en innkjøpsrekvisisjonslinje som er lukket, må du avbryte linjen på fullføringsdokumentet som ble generert for innkjøpsrekvisisjonslinjen.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Fordele kostnader på flere finansielle kontoer
Du kan distribuere kostnadene for et produkt som er inkludert i en innkjøpsrekvisisjon, til flere finanskontoer. Hvis organisasjonen bruker dimensjoner, for eksempel kostsentre og avdelinger, kan du distribuere kostnaden for et produkt til dimensjoner for finansielle kontoer.

## <a name="requisition-purposes"></a>Rekvisisjonsformål
Rekvisisjonsformål gjør prosessen med å oppfylle rekvisisjonsbehov mer fleksibel. Når du oppretter en rekvisisjon, kan du tilordne ett av to formål til den: forbruk eller etterfylling. Avhengig av rekvisisjonsformålet og oppsettet av organisasjonen, kan rekvisisjonsbehovet oppfylles av en bestilling, overføringsordre, produksjonsordre eller kanban.  

I innkjøpspolicyene kan du kontrollere rekvisisjonsformålene som er tilgjengelige når en rekvisisjon opprettes for organisasjonen.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Rekvisisjoner med forbruk som formål

En rekvisisjon som har forbruk som formål, representerer et behov for varer eller tjenester som skal brukes internt av organisasjonen. Behovet som opprettes av denne typen rekvisisjon, oppfylles alltid av en bestilling. Hvis Supply Chain Management er konfigurert slik at bestillinger genereres automatisk, opprettes bestillinger etter at innkjøpsrekvisisjonen er godkjent.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Rekvisisjoner med etterfylling som formål

En rekvisisjon som har etterfylling som formål, representerer behov for å etterfylle beholdningen. Du oppretter for eksempel en rekvisisjon for å etterfylle varer for å selge dem på en bestemt detaljhandelslokasjon på et bestemt tidspunkt. Behovet som opprettes av denne typen rekvisisjon, kan oppfylles av en bestilling, overføringsordre, produksjonsordre eller Kanban.  

Når rekvisisjonsformålet er etterfylling, uttrykkes behovet som et antall i stedet for et pengebeløp. Derfor gjelder ikke disposisjonsregnskap, budsjettkontroll, forretningsregler for fastsettelse av anleggsmidler, prosjektregnskap og eventuelle relatert regler. Bare produkter som er lagerført og frigitt til den angitte juridiske enheten, kan oppfylle rekvisisjonsbehovet for etterfylling. For å definere produktene som er tilgjengelige når rekvisisjonsformålet er etterfylling, bruk siden **Policyregel for tilgang til etterfyllingskategori**.  

Hvis du vil bruke innkjøpsrekvisisjoner som har etterfylling som formål, må du konfigurere hovedplanlegging slik at rekvisisjonsbehov inkluderes. Oppfyllingsmetoden for behovet som opprettes av denne typen rekvisisjon, bestemmes deretter automatisk basert på forsyningspolicyene som er definert for varene i organisasjonen og planlagt ved hjelp av hovedplanlegging.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Innkjøpsrekvisisjoner og forespørsler om tilbud
I noen tilfeller må du starte en prosess for tilbudsforespørsel for å identifisere leverandøren og prisen for produkter som er forespurt i en innkjøpsrekvisisjon. En tilbudsforespørsel kan bli generert når innkjøpsrekvisisjonen er til vurdering. Når du godkjenner et bud, overføres informasjon om leverandør, pris og så videre, til rekvisisjonen.  

Du kan sette en innkjøpsrekvisisjon på vent ved å merke av for **På vent** på siden **Detaljer om innkjøpsrekvisisjon**. Behandling av innkjøpsrekvisisjonen kan fortsette bare etter at du fjerner sperren ved å fjerne merket.  

> [!NOTE]
> I e-procurement kan tilbudsforespørselen for din innkjøpsrekvisisjon kanskje tillate at leverandører kan legge til alternative linjer. I så fall gjenspeiler innkjøpsrekvisisjonen godkjente alternativer.

## <a name="demand-consolidation"></a>Behovskonsolidering
Hvis du konsoliderer innkjøpsrekvisisjonslinjer fra flere innkjøpsrekvisisjoner, kan du forbedre forhandlingsposisjonen overfor leverandører for å oppnå bedre priser, lavere kostnader ved forsendelse og behandling og lavere administrasjonskostnader.  

Innkjøpsrekvisisjonslinjer er bare kvalifisert for behovskonsolidering hvis de følgende setninger er sanne:

-   Innkjøpsrekvisisjonen må godkjennes.
-   Innkjøpsrekvisisjonen oppfyller innkjøpspolicyregelkriteriene for manuell behandling og behovskonsolidering.

Godkjente innkjøpsrekvisisjonslinjer som oppfyller kriteriene for manuell behandling, vises på siden **Frigi godkjente innkjøpsrekvisisjoner**. Hvis en innkjøpsrekvisisjonslinje også oppfyller kriteriene for behovskonsolidering, kan linjen legges til i en konsolideringsmulighet.  

En konsolideringsmulighet er et sett med innkjøpsrekvisisjonslinjer som er gruppert sammen slik at innkjøper kan forhandle den beste avtalen med leverandører. Innkjøpsrekvisisjonslinjer som du velger for en konsolideringsmulighet, vises på siden **Konsolidering av innkjøpsrekvisisjon**. Du kan endre linjene på denne siden, hvis det er nødvendig. Du kan også legge til nye linjer i konsolideringsmuligheten eller fjerne eksisterende linjer.  

Når du har lagt til rekvisisjonslinjene i en konsolideringsmulighet og foretatt endringer som du ønsker, kan du opprette en bestilling for de konsoliderte innkjøpsrekvisisjonslinjene.  

> [!NOTE]
> Endringer du foretar på en innkjøpsrekvisisjonslinje på siden **Konsolidering av innkjøpsrekvisisjon**, gjenspeiles i bestillingen du oppretter. Linjen forblir imidlertid uendret i innkjøpsrekvisisjonen, slik at historikken beholdes.  

Hvis du vil opprette en bestilling for innkjøpsrekvisisjonslinjer som ikke er kvalifisert for behovskonsolidering, eller som ikke er valgt for en konsolideringsmulighet, må du behandle linjene manuelt.

### <a name="consolidating-purchase-requisition-lines"></a>Konsolidere innkjøpsrekvisisjonslinjer

Prosessen for behovskonsolidering starter når en innkjøpsrekvisisjon er godkjent i en arbeidsflyt, og, hvis budsjettkontroll er er konfigurert for organisasjonen, når budsjettreservasjonene og forhåndsdisposisjoner er registrert. Diagrammet nedenfor viser prosessflyten for behovskonsolidering.  

[![Prosessflyt for behovskonsolidering.](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Hvis du vil konsolidere godkjente innkjøpsrekvisisjonslinjer, gjør du følgende:

1.  Se gjennom godkjente rekvisisjonslinjer som har vært sperret for manuell behandling, og som er kvalifisert for behovskonsolidering.
2.  Velg linjene som du vil legge til i en konsolideringsmulighet.
3.  Opprette en ny konsolideringsmulighet, eller legg til rekvisisjonslinjer i en eksisterende konsolideringsmulighet.
4.  Foreta eventuelle ønskede endringer i rekvisisjonslinjene, og fjern innkjøpsrekvisisjonslinjer du ikke lenger vil ha med i konsolideringsmuligheten.
5.  Opprette bestillinger for konsoliderte innkjøpsrekvisisjonslinjer eller for innkjøpsrekvisisjonslinjer i en konsolideringsmulighet.


## <a name="additional-resources"></a>Tilleggsressurser

[Opprette en rekvisisjon for forbruk](tasks/create-requisition-consumption.md)

[Arbeidsflyt for innkjøpsrekvisisjon](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]