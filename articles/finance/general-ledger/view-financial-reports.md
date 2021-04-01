---
title: Vise finansrapporter
description: Dette emnet beskriver hvordan du kan vise og utforske finansrapporter i Microsoft Dynamics 365 Finance. Den inneholder informasjon om de forskjellige alternativene du kan bruke på finansrapporter for å endre utseendet og dataene de inneholder.
author: kweekley
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54d407eb33060c61a5899ba5cc021c8c1c6c77c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240622"
---
# <a name="view-financial-reports"></a>Vise finansrapporter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan vise og utforske finansrapporter. Den inneholder informasjon om de forskjellige alternativene du kan bruke på finansrapporter for å endre utseendet og dataene de inneholder.

<a name="financial-reporting-overview"></a>Oversikt over finansrapportering
----------------------------

## <a name="open-a-financial-report"></a>Åpne en finansrapport
Hvis du vil åpne en rapport, velger du rapportnavnet. Første gang en rapport åpnes, genereres den automatisk for forrige måned. Hvis du for eksempel åpner en rapport for første gang i august 2015, genereres rapporten for 31. juli 2015. Når en rapport åpnes, kan du begynne å utforske den ved å gå nedover i bestemte deler av data og endre rapportalternativer.

## <a name="drill-down-on-a-financial-report"></a>Vise detaljer for en finansrapport
Finansrapporter kan inneholde flere ulike detaljnivåer. Finansnivået er det første nivået som vises når du åpner en finansrapport. Velg dataene du vil vise detaljer for, for å gå til kontonivået. Hvis du for eksempel vil vise kontodetaljer for salg, kan du velge salgsdataene du vil utforske. Fra kontonivået kan du drille ned for å vise transaksjonene som utgjør kontosaldoen. Du kan vise transaksjoner på to måter: rapporttransaksjoner og bilagstransaksjoner.

-   **Rapporttransaksjoner** – Transaksjoner vises i en formatert visning som er inkludert i finansrapporten. Hvis du vil vise transaksjoner i den formaterte visningen, velger du dataene du vil vise detaljer for, og deretter klikker du **Drill ned til transaksjonsnivå i rapporten**.
-   **Bilagstransaksjoner** – En bilagstransaksjonsforespørsel åpnes, der du kan vise transaksjoner. Hvis du vil vise transaksjoner i bilagstransaksjonsforespørselen, velger du dataene du vil vise detaljer for, og deretter klikker du **Åpne kontotransaksjoner**.

Hvis dataene er budsjettdata, kan du velge å åpne budsjettkontooppføringer. Hvis du vil lukke noen av nivåene i rapporten og gå tilbake til der du startet, kan du enten trykke Esc-tasten eller klikke **lukkeknappen** (**X**) øverst til høyre.

## <a name="change-report-options"></a>Endre rapportalternativer
Du kan bruke attributt- og dimensjonsfiltre eller endre budsjettscenariet i rapporten **Faktisk kontra budsjett**. I handlingsruten klikker du **Rapportalternativer** og følger deretter ett eller flere av disse trinnene:

-   Hvis du vil bruke attributtfiltre på en rapport, velger du **Legg til et attributtfilter**. Velg attributtet, skriv inn attributtverdien, og klikk deretter **OK**. Hvis du for eksempel velger attributtet **Kontokategori**, angir du **SALG** som attributtverdi. Hvis du vil fjerne et attributtfilter, klikker du **Fjern**.
-   Hvis du vil bruke dimensjonsfiltre på en rapport, velger du **Legg til et dimensjonsfilter**. Velg dimensjon, og skriv deretter inn dimensjons-ID eller velg dimensjon i listen. Hvis du vil fjerne et dimensjonsfilter, klikker du **Fjern**.
-   Hvis du vil endre scenariet i rapporten **Faktisk kontra budsjett**, velger du et nytt scenario og klikker deretter **OK**. Hvis det valgte scenarioet er for et annet regnskapsår, blir ingen resultater returnert. Hvis for eksempel en rapport blir generert for FY2015 og gjeldende scenario er for FY2015, og det nye scenarioet som er valgt, er for FY2016, returneres ingen resultater. Hvis et nytt scenario for et annet regnskapsår kreves, genereres en ny versjon av rapporten for regnskapsåret som er knyttet til scenarioet.

Når du klikker **OK**, brukes alle alternativene du har valgt, på rapporten. Hvis du bestemmer deg for at du ikke vil bruke de valgte alternativene, velger du **Avbryt**.

## <a name="update-a-financial-report"></a>Oppdatere en finansrapport
Du kan oppdatere en finansrapport slik at den viser de nyeste dataene for perioden og året som rapporten ble generert for. Hvis du for eksempel oppdaterer en finansrapport som ble generert for oktober 2015, gjenspeiler rapporten alle nye transaksjoner som er postert for oktober 2015. Klikk **Oppdater** i handlingsruten for å oppdatere en finansrapport.. En oppdatert rapport er bare tilgjengelig for personen som oppdaterte den. Rapporten må publiseres før andre kan se de samme dataene.

## <a name="publish-a-financial-report"></a>Publisere en finansrapport
Når du har oppdatert en finansrapport, kan du publisere den. Andre personer i organisasjonen kan deretter vise den. Klikk **Publiser** i handlingsruten for å publisere en rapport.

## <a name="display-a-financial-report-in-a-different-currency"></a>Vise en finansrapport i en annen valuta
En finansrapport kan når som helst vises i en hvilken som helst valuta. Hvis du vil vise en rapport i en annen valuta, klikker du **Valuta** i handlingsruten og velger deretter en valuta. Rapporten omregnes til denne valutaen, og resultatene vises. Valutakoder eller -symboler som er inkludert som en del av rapportutformingen, oppdateres for å gjenspeile den nye valutaen. Valutaene som vises i listen, er rapporteringsvalutaene som er konfigurert i Finance.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Vise en sammendragsvisning av finansrapporten
En finansrapport kan inneholde detaljlinjer og sammendragslinjer. Detaljlinjer er linjer som inneholder hovedkontoer eller dimensjoner. Sammendragslinjer er beskrivelses-, total- og beregningslinjer. Klikk **Vis**, og klikk deretter **Bare sammendragslinjer** for å vise bare sammendragslinjer i en rapport. Rapporten er skjult og viser bare sammendragslinjer. Klikk **Vis**, og klikk deretter **Bare sammendragslinjer** på nytt for å vise detaljlinjene sammen med sammendragslinjene.

## <a name="print-a-financial-report"></a>Skrive ut en finansrapport
Utskriving av en finansrapport oppretter en PDF-fil som deretter kan skrives ut manuelt. For å opprette en utskrivbar finansrapport, klikker du **Skriv ut** i handlingsruten og følger deretter ett eller flere av disse trinnene for å angi alternativene for utskrift:

-   Hvis du vil ta med ulike detaljnivåer i den utskrevne rapporten, setter du glidebryteren til **Ja** eller **Nei**. Hvis en rapport bruker et rapporteringstre, kan du velge å ta med alle rapportenheter eller bare gjeldende rapportenhet.
-   Hvis du vil angi sidestørrelsen, velger du en sidestørrelse i listen.
-   Hvis du vil angi sideoppsettet, velger du et oppsett i listen. Hvis du vil at rapportinnholdet skal passe til bredden du har valgt, setter du glidebryteren til **Ja**.
-   Hvis du vil angi sidemargene, skriver du inn størrelsen på toppmargen, bunnmargen og venstre og høyre marg i tommer.

Når du har fullført angivelse av utskriftsalternativene, klikker du **Skriv ut** for å fortsette å bli spurt om du vil laste ned filen eller lagre filen til OneDrive eller SharePoint. Hvis du bestemmer deg for at du ikke vil fortsette, velger du **Avbryt** i stedet. Når du fortsetter, vil rapporten begynne å gjengi på serveren, og du blir bedt om å laste ned rapporten i PDF-format. Du kan nå vise rapporten i PDF-visningsprogrammet, og her kan du velge hvilken skriver du vil sende rapporten til, og foreta ytterligere justeringer for utskriftsalternativer.

## <a name="export-a-financial-report"></a>Eksportere en finansrapport
Klikk **Eksport** i handlingsruten for å eksportere en finansrapport. Rapporten eksporteres til Microsoft Excel, og nettleseren ber deg om å åpne eller lagre den eksporterte filen. Eksportinnstillingene som er definert i rapportutformingen, brukes på den eksporterte rapporten.    

<a name="additional-resources"></a>Tilleggsressurser
--------

[Finansrapportering](../../dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]