---
title: Konserninternt Regnskapsoppsett
description: "Dette emnet forklarer hvordan du konfigurerer konserninternt regnskap, slik at du kan bruke konserninterne kladder for finans tildelinger og finansjournaler, for eksempel daglige journaler, leverandøren fakturaen Kjøpskladder og utbetalingskladder."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Konserninternt Regnskapsoppsett

Dette emnet forklarer hvordan du konfigurerer konserninternt regnskap, slik at du kan bruke konserninterne kladder for finans tildelinger og finansjournaler, for eksempel daglige journaler, leverandøren fakturaen Kjøpskladder og utbetalingskladder.

Konserninterne kladder kan opprettes i ulike scenarier, for eksempel for daglige journaler, leverandørfakturajournaler, finans tildelinger og sentralisert betaling. Hvis du vil aktivere disse scenariene, må du definere konserninternt regnskap.

## <a name="define-main-accounts"></a>Definere hovedkontoer
Først må du opprette de konserninterne hovedkontoene som skal brukes til regnskapsoppføringer for betaling til og betaling fra. Det er lurt å bruke unike hovedkontoer for hvert firma for å forenkle avstemmingen og elimineringen av konserninterne regnskapsoppføringer. Hvis du bruker en handelspartner eller importfilfeltet dimensjon til å identifisere parten som konserninterne, kan du definere denne dimensjonen som en fast dimensjon på hovedkontoen som er definert i det konserninterne regnskapet. Når du setter opp hovedkontoene, bør du angi den **Main kontotypen** feltet til **balansen** på den **Main kontoer** siden.

## <a name="define-journal-names"></a>Definere journalnavn
Deretter må du definere et journalnavn. Angi de **journaltypen** feltet til **daglig** på den **journalnavn** siden. Det er lurt å bruke et spesifikt journalnavn for konserninternt regnskap.

## <a name="define-intercompany-accounting-setup"></a>Definere konserninternt Regnskapsoppsett
Den **i det konserninterne regnskapet** siden brukes til å opprette par med juridiske enheter kan transact med hverandre. Konserninternt regnskap installasjonsprogrammet deles slik at oppsettet er synlig fra alle juridiske enheter. Når du oppretter en ny juridisk enhet-par, sikrer du at du er klar over hvilke juridisk enhet er definert som det opprinnelige selskapet kontra målfirmaet. Når du angir konserninterne transaksjoner, bestemmer transaksjonen hvilke juridisk enhet starter eller opprinnelige for transaksjonen. Konserninternt regnskap for eksempel er satt opp for USMF (opprinnelig) og USSI (målet). Hvis en bruker er aktiv i USSI, og angir en konsernintern transaksjon som inkluderer USMF, bokfører transaksjonen ikke fordi konserninternt regnskap defineres bare for USMF som avsenderen. Hvis et selskap kan denne formen er hentet en transaksjon, må du opprette noen andre juridisk enhet for gjensidig oppsettet. 

Velg den **debiterer (skal betales fra)** og **kreditkonto (som)** for både det opprinnelige varelageret og destinasjonsvarelageret juridisk enhet. Definere hvilke **journalnavnet** vil bli brukt når transaksjonen blir opprettet i målfirmaet. Journal for det opprinnelige selskapet er allerede kjent fordi den er valgt av brukeren når du oppretter en konsernintern transaksjon. 

Til slutt velger du hvilke juridisk enhet vil motta regnskap som støtter beløp, for eksempel kontantrabatt eller realisert agio/disagio for sentralisert betaling. 

Et gjensidig forhold kan enkelt defineres på den **konserninternt regnskap** side ved hjelp av den **opprette gjensidig forhold** -knappen etter at de første par juridisk enhet er opprettet. Når det opprettes en motsvarende paret, kopieres informasjonen for målfirmaet til det opprinnelige selskapet og vice versa. Journal som er definert for målfirmaet forblir. De fleste organisasjoner bruker samme navnekonvensjonen for journalnavn, slik at journalnavnet er den samme. Hvis journalnavnet er forskjellig, vises en advarsel på feltet for å informere om at kladden ikke finnes, og du kan velge en annen kladd.


