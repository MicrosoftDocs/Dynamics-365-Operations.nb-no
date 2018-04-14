---
title: Definere og generere positive betalingsfiler
description: Denne artikkelen forklarer hvordan du konfigurerer positiv betaling og genererer positive betalingsfiler.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 41d7b64f8414385629acef071c47a654d56005bd
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-and-generate-positive-pay-files"></a>Definere og generere positive betalingsfiler

[!INCLUDE [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer positiv betaling og genererer positive betalingsfiler. 

Definer positiv betaling for å generere en elektronisk liste over sjekker som leveres til banken. Når sjekken presenteres til banken, sammenligner banken deretter sjekken med listen over sjekker. Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken. Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.

## <a name="security-for-positive-pay-files"></a>Sikkerhetsnøkkel for positive lønnsfiler
Positive betalingsfiler kan inneholde sensitiv informasjon om betalingsmottakere og sjekkbeløp. Derfor må du sørge for at du bruker riktige sikkerhetstiltak fra tidspunktet som filene er generert, til de er mottatt av banken. Positive lønnsfiler blir lastet ned til plasseringen som er angitt i webleseren. Siden positive lønnsfiler kan inneholde sensitiv informasjon, er det viktig at bare autoriserte brukere har tilgang til å generere og vise denne informasjonen i Microsoft Dynamics 365 for Finance and Operations. Bruk tabellen nedenfor til å hjelpe deg med å bestemme rettighetene som kreves.

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

## <a name="set-up-a-positive-pay-format"></a>Definer et positivt betalingsformat
Positive betalingsfiler opprettes ved hjelp av dataenheter. Før du kan generere en positiv betalingsfil, må du definere et transformasjonsinndataformat som skal brukes til å oversette informasjonen i et format som kan kommunisere med banken. På siden **Positivt betalingsformat** kan du opprette en filformat-ID og en beskrivelse. Transformasjonsinndataformatet må være av XML-typen. Det bestemte formatet avhengiger av transformasjonsfilen du bruker. XSLT-eksempelfilen (Extensible Stylesheet Language Transformations) som er oppgitt, bruker formatet **XML-Element**. Bruk handlingen **Last opp fil som brukes for transformasjon** til å angi plasseringen til transformeringsfilen for formatet som banken krever.

## <a name="example-xslt-file-for-positive-pay-file"></a>Eksempel: XSLT-fil for positiv betalingsfil
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BankPositivePayExportEntity">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Tilordne det positive betalingsformatet til en bankkonto
For hver bankkonto du vil generere informasjon om positiv betaling for, må du tilordne det positive betalingsformatet som ble angitt i forrige del. På **Bankkontoer**-siden velger du det positive lønnsformatet som samsvarer med bankkontoen. I feltet **Startdato for positiv betaling** angir du den første datoen for generering av positive betalingsfiler. Det er viktig at du angir en dato i dette feltet. Ellers vil den første positive betalingsfilen du genererer, inkludere alle kontrollene som noen gang har blitt opprettet for denne bankkontoen.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Tilordne en nummerserie for positive betalingsfiler.
Hver positiv lønnsfil må ha et unikt nummer. Bruk kategorien **Nummerserier** på siden **Parametere for kontant- og bankbehandling** til å opprette en nummerserie for positive betalingsfiler.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generere en positiv betalingsfil for én bankkonto
Du kan generere en positiv betalingsfil for én juridisk enhet og én bankkonto. For informasjon om hvordan du genererer positive betalingsfiler for flere juridiske enheter og bankkontoer samtidig, kan du se neste del. Hvis du vil generere en positiv betalingsfilen for en juridisk enhet og én bankkonto, kan du åpne dialogboksen **Generer en positiv betalingsfil** fra **Bankkontoer**-siden. I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen. Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generere en positiv betalingsfil for flere bankkontoer
Hvis du vil generere en positiv betalingsfiler for flere bankkontoer, bruker du den periodiske oppgaven **Generer en positiv betalingsfil**. Velg det positive betalingsformatet for filen, og angi om du vil generere filen for alle juridiske enheter eller for en valgt juridisk enhet. Du kan også generere den positive betalingsfilen for alle bankkontoer som bruker det angitte positive betalingsformatet eller for en valgt bankkonto. I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen. Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Vise resultatene av genereringen av den positive betalingsfilen
Når den positive betalingsfilen er opprettet, kan du vise resultatene på siden **Sammendrag av positiv betalingsfil** side. Hvis du vil vise detaljer om de individuelle kontrollene, kan du bruke siden **Detaljer for positiv betalingsfil**.

## <a name="confirm-a-positive-pay-file"></a>Bekreft en positiv betalingsfil
Når kontrollene som er oppført i en positiv lønnsfilen er betalt, får du et bekreftelsesnummer fra banken. Du kan deretter bekrefte den positive betalingsfilen. På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Angi bekreftelse**. Når du bekrefter en positiv betalingsfil, registreres bekreftelsesnummeret du mottok fra banken.

## <a name="recall-a-positive-pay-file"></a>Tilbakekalle en positiv betalingsfil
Hvis du må endre en positiv betalingsfil, kan du tilbakekalle den. På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Tilbakekall**. For hver kontroll i den positive betalingsfilen tilbakestilles feltet som angir om kontrollen er inkludert i en positiv betalingsfil. Du kan deretter opprette en ny positiv betalingsfil med kontrollen som ble tilbakekalt.




