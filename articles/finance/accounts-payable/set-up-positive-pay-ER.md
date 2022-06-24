---
title: Definer og generer positive betalingsfiler ved hjelp av elektronisk rapportering
description: Denne artikkelen forklarer hvordan du konfigurerer positiv betaling ved hjelp av elektronisk rapportering.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878225"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Definer positive betalingsfiler ved hjelp av elektronisk rapportering

Denne artikkelen forklarer hvordan du konfigurerer positiv betaling og genererer positive betalingsfiler ved hjelp av Elektronisk rapportering.

> [!NOTE] 
> Før du bruker funksjonen **Generer positiv bankbetalingsfil**, må du oppdatere enhetslisten først.
> Gå til **Databehandling > Import / Ekport > Rammeverkparametere** 
> **Enhetsinnstillinger**-hurtigkategorien, velg **Oppdater enhetsliste**.


Definer positiv betaling for å generere en elektronisk liste over sjekker som leveres til banken. Når sjekken presenteres til banken, sammenligner banken deretter sjekken med listen over sjekker. Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken. Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.

## <a name="security-for-positive-pay-files"></a>Sikkerhetsnøkkel for positive lønnsfiler
Positive betalingsfiler kan inneholde sensitiv informasjon om betalingsmottakere og sjekkbeløp. Derfor må du sørge for at du bruker riktige sikkerhetstiltak fra tidspunktet som filene er generert, til de er mottatt av banken. Positive lønnsfiler blir lastet ned til plasseringen som er angitt i webleseren. Siden positive lønnsfiler kan inneholde sensitiv informasjon, er det viktig at bare autoriserte brukere har tilgang til å generere og vise denne informasjonen i Microsoft Dynamics 365 Finance. Bruk tabellen nedenfor til å hjelpe deg med å bestemme rettighetene som kreves.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Oppgave</th>
<th>Rettighet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generer positiv lønn filer fra listesiden <strong>Bankkontoer</strong> eller siden <strong>Bankkontoer</strong>.</td>
<td><ul>
<li><strong>Vedlikehold informasjon om positiv bankbetaling</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Generere positive betalingsfiler for flere juridiske enheter og bankkontoer fra siden <strong>Generer en positiv betalingsfil</strong>.</td>
<td><ul>
<li><strong>Vedlikehold informasjon om positiv bankbetaling</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vis positive betalingsfiler på siden <strong>Sammendrag av positiv betalingsfil</strong>.</td>
<td><strong>Vis informasjon om positiv bankbetaling for flere juridiske enheter</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bereft en positiv bankbetalingsfil på siden <strong>Sammendrag av positiv betalingsfil</strong>.</td>
<td><strong>Bekreft positiv betalingsfil</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Tilbakekall en positiv bankbetalingsfil på siden <strong>Sammendrag av positiv betalingsfil</strong>.</td>
<td><strong>Tilbakekall positiv betalingsfil</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Sett opp konfigurasjonen av elektronisk rapportering

1. Gå til **Arbeidsområder \> Elektronisk rapportering**.
2. Velg **Repositorier** på flisen for **Microsoft**-konfigurasjonsleverandøren.
3. Velg **Global**, og velg deretter **Åpne**.
4. Hvis det må opprettes en tilkobling til repositoriet, velger du den blå koblingen i dialogboksen.
5. I konfigurasjonslisten finner du og velger **Positiv betalingsmodell \> Positivt betalingsformat**.
6. På hurtigfanen **Versjoner** velger du den nyeste versjonen, og deretter velger du **Importer**.

## <a name="set-up-a-positive-pay-format"></a>Definer et positivt betalingsformat

1. Gå til **Kontant- og bankbehandling \> Oppsett \> Positive betalingsformater**.
2. Velg **Ny**.
3. Angi feltene **Betalingsformat** og **Beskrivelse**.
4. Merk av for **Generelt elektronisk eksportformat**.
5. Sett feltet **Eksportformatkonfigurasjon** til **Positivt betalingsformat**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Tilordne et positivt betalingsformat til en bankkonto
For hver bankkonto du vil generere informasjon om positiv betaling for, må du tilordne det positive betalingsformatet som ble angitt i forrige del. På Bankkontoer-siden velger du det positive lønnsformatet som samsvarer med bankkontoen. I feltet **Startdato for positiv betaling** angir du den første datoen for generering av positive betalingsfiler. 

>[!Important]
> Angi en dato i feltet **Startdato for positiv betaling**. Hvis den står tom, vil den første positive betalingsfilen som genereres, inkludere alle kontrollene som har blitt opprettet for denne bankkontoen.

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne bankkontoen.
3. På hurtigfanen **Generelt** angir du feltet **Positivt betalingsformat** til formatet som ble opprettet tidligere.
4. Sett feltet **Startdato for positiv betaling** til gjeldende dato.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Tilordne en nummerserie for positive betalingsfiler.
Hver positiv lønnsfil må ha et unikt nummer. I kategorien **Nummerserier** på siden **Parametere for kontant- og bankbehandling** oppretter du en nummerserie for positive betalingsfiler.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generere en positiv betalingsfil for én bankkonto
Du kan generere en positiv betalingsfil for én juridisk enhet og én bankkonto. For informasjon om hvordan du genererer positive betalingsfiler for flere juridiske enheter og bankkontoer samtidig, kan du se neste del. Hvis du vil generere en positiv betalingsfilen for en juridisk enhet og én bankkonto, kan du åpne dialogboksen **Generer en positiv betalingsfil** fra **Bankkontoer**-siden. I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen. Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne en bankkonto som positiv betaling er satt opp for.
3. Velg **Behandle betalinger \> Positiv betaling \> Positiv betalingsfil**.
4. Angi **Frist**-feltet. Sjekker som ble generert før denne datoen, vil bli inkludert.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generere en positiv betalingsfil for flere bankkontoer
Hvis du vil generere en positiv betalingsfiler for flere bankkontoer, bruker du den periodiske oppgaven **Positiv betalingsfil**. Velg det positive betalingsformatet for filen, og angi om du vil generere filen for alle juridiske enheter eller for en valgt juridisk enhet. Du kan også generere den positive betalingsfilen for alle bankkontoer som bruker det angitte positive betalingsformatet eller for en valgt bankkonto. I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen. Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Vise resultatene av genereringen av den positive betalingsfilen
Når den positive betalingsfilen er opprettet, kan du vise resultatene på siden **Sammendrag av positiv betalingsfil** side. Hvis du vil vise detaljer om de individuelle kontrollene, går du til siden **Detaljer for positiv betalingsfil**.

## <a name="confirm-a-positive-pay-file"></a>Bekreft en positiv betalingsfil
Når kontrollene som er oppført i en positiv lønnsfilen er betalt, får du et bekreftelsesnummer fra banken. Du kan deretter bekrefte den positive betalingsfilen. På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Angi bekreftelse**. Når du bekrefter en positiv betalingsfil, registreres bekreftelsesnummeret du mottok fra banken.

## <a name="recall-a-positive-pay-file"></a>Tilbakekalle en positiv betalingsfil
Hvis du må endre en positiv betalingsfil, kan du tilbakekalle den. På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Tilbakekall**. For hver kontroll i den positive betalingsfilen tilbakestilles feltet som angir om kontrollen er inkludert i en positiv betalingsfil. Du kan deretter opprette en ny positiv betalingsfil med kontrollen som ble tilbakekalt.


Den resulterende XML-filen lastes ned.
