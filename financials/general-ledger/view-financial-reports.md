---
title: Vis finansrapporter
description: "Denne artikkelen beskriver hvordan du kan vise og utforske finansrapporter i Microsoft Dynamics AX. Den inneholder informasjon om de forskjellige alternativene du kan bruke på finansrapporter for å endre utseendet og dataene de inneholder."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b02dbc0181c08611674cdf571075c20d78cebdc
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="view-financial-reports"></a>Vis finansrapporter

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan vise og utforske finansrapporter i Microsoft Dynamics AX. Den inneholder informasjon om de forskjellige alternativene du kan bruke på finansrapporter for å endre utseendet og dataene de inneholder.

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
Du kan endre rapportdatoen, bruke attributt- og dimensjonsfiltre eller endre budsjettscenariet i rapporten **Faktisk kontra budsjett**. I handlingsruten klikker du **Rapportalternativer** og følger deretter ett eller flere av disse trinnene:

-   Hvis du vil endre basisperioden og basisåret i en rapport, velger du en basisperiode og et basisår og klikker deretter **OK**.
-   Hvis du vil bruke attributtfiltre på en rapport, velger du **Legg til et attributtfilter**. Velg attributtet, skriv inn attributtverdien, og klikk deretter **OK**. Hvis du for eksempel velger attributtet **Kontokategori**, angir du **SALG** som attributtverdi. Hvis du vil fjerne et attributtfilter, klikker du **Fjern**.
-   Hvis du vil bruke dimensjonsfiltre på en rapport, velger du **Legg til et dimensjonsfilter**. Velg dimensjon, og skriv deretter inn dimensjons-ID eller velg dimensjon i listen. Hvis du vil fjerne et dimensjonsfilter, klikker du **Fjern**.
-   Hvis du vil endre scenariet i rapporten **Faktisk kontra budsjett**, velger du et nytt scenario og klikker deretter **OK**. Hvis det valgte scenariet er for et annet år, må du passe på å oppdatere basisåret. Hvis det gjeldende scenariet for eksempel er for FY2015 og du velger et nytt scenario som er for FY2016, må du endre basisåret til **2016**.

Når du klikker **OK**, brukes alle alternativene du har valgt, på rapporten. Hvis du bestemmer deg for at du ikke vil bruke de valgte alternativene, velger du **Avbryt**.

## <a name="update-a-financial-report"></a>Oppdatere en finansrapport
Du kan oppdatere en finansrapport slik at den viser de nyeste dataene for perioden og året som rapporten ble generert for. Hvis du for eksempel oppdaterer en finansrapport som ble generert for oktober 2015, gjenspeiler rapporten alle nye transaksjoner som er postert for oktober 2015. Klikk **Oppdater** i handlingsruten for å oppdatere en finansrapport.. En oppdatert rapport er bare tilgjengelig for personen som oppdaterte den. Rapporten må publiseres før andre kan se de samme dataene.

## <a name="publish-a-financial-report"></a>Publisere en finansrapport
Når du har oppdatert en finansrapport, kan du publisere den. Andre personer i organisasjonen kan deretter vise den. Klikk **Publiser** i handlingsruten for å publisere en rapport.

## <a name="display-a-financial-report-in-a-different-currency"></a>Vise en finansrapport i en annen valuta
En finansrapport kan når som helst vises i en hvilken som helst valuta. Hvis du vil vise en rapport i en annen valuta, klikker du **Valuta** i handlingsruten og velger deretter en valuta. Rapporten omregnes til denne valutaen, og resultatene vises. Valutakoder eller -symboler som er inkludert som en del av rapportutformingen, oppdateres for å gjenspeile den nye valutaen. Valutaene som vises i listen, er rapporteringsvalutaene som er konfigurert i Microsoft Dynamics AX.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Vise en sammendragsvisning av finansrapporten
En finansrapport kan inneholde detaljlinjer og sammendragslinjer. Detaljlinjer er linjer som inneholder hovedkontoer eller dimensjoner. Sammendragslinjer er beskrivelses-, total- og beregningslinjer. Klikk **Vis**, og klikk deretter **Bare sammendragslinjer** for å vise bare sammendragslinjer i en rapport. Rapporten er skjult og viser bare sammendragslinjer. Klikk **Vis**, og klikk deretter **Bare sammendragslinjer** på nytt for å vise detaljlinjene sammen med sammendragslinjene.

## <a name="open-a-financial-report-from-a-previous-month"></a>Åpne en finansrapport fra en tidligere måned
Du kan vise rapporter for gjeldende måned eller tidligere måneder uten å generere rapporten på nytt. Hvis du vil åpne rapporten for en tidligere måned, klikker du på **Vis** og deretter på **Tidligere rapporter**. Det vises en liste over tidligere måneder som rapporten er generert for. Utvid måneden du vil vise rapporten for, velg datoen, og klikk deretter **OK**. Rapporten for den tidligere måneden vises. Hvis du vil gå tilbake til rapporten for gjeldende måned, klikker du **Avbryt**.

## <a name="print-a-financial-report"></a>Skrive ut en finansrapport
Hvis du vil skrive ut en finansrapport, klikker du **Skriv ut** i handlingsruten og følger deretter ett eller flere av disse trinnene for å angi alternativene for utskrift:

-   Hvis du vil ta med ulike detaljnivåer i den utskrevne rapporten, setter du glidebryteren til **Ja** eller **Nei**. Hvis en rapport bruker et rapporteringstre, kan du velge å ta med alle rapportenheter eller bare gjeldende rapportenhet.
-   Hvis du vil angi sidestørrelsen, velger du en sidestørrelse i listen.
-   Hvis du vil angi sideoppsettet, velger du et oppsett i listen. Hvis du vil at rapportinnholdet skal passe til bredden du har valgt, setter du glidebryteren til **Ja**.
-   Hvis du vil angi sidemargene, skriver du inn størrelsen på toppmargen, bunnmargen og venstre og høyre marg i tommer.

Når du har angitt alternativene for utskrift, klikker du **Skriv ut** for å skrive ut rapporten. Hvis du bestemmer deg for at du ikke vil skrive ut rapporten, velger du **Avbryt** i stedet. Det vises en forhåndsvisning av den utskrevne rapporten. Du kan velge hvilken skriver du vil sende rapporten til, og du kan også justere alternativene for utskrift.

## <a name="export-a-financial-report"></a>Eksportere en finansrapport
Klikk **Eksport** i handlingsruten for å eksportere en finansrapport. Rapporten eksporteres til Microsoft Excel, og nettleseren ber deg om å åpne eller lagre den eksporterte filen. Eksportinnstillingene som er definert i rapportutformingen, brukes på den eksporterte rapporten.    

<a name="see-also"></a>Se også
--------

[Finansrapportering for Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/analytics/financial-reporting-intro)




