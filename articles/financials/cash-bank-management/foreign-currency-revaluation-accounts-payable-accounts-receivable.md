---
title: "Revaluering av utenlandsk valuta for leverandører og kunder"
description: "Endringer i valutakursene kan føre til at den teoretiske verdien (bokført verdi) av åpne kundetransaksjoner i utenlandsk valuta varierer over tid. Denne artikkelen inneholder informasjon om prosessen for revaluering av utenlandsk valuta som du kjører for å oppdatere verdien av åpne transaksjoner i leverandører og kunder."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 259b487b0f11b19af9609d63f12114dcaa61be52
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Revaluering av utenlandsk valuta for leverandører og kunder

[!include [banner](../includes/banner.md)]

Endringer i valutakursene kan føre til at den teoretiske verdien (bokført verdi) av åpne kundetransaksjoner i utenlandsk valuta varierer over tid. Denne artikkelen inneholder informasjon om prosessen for revaluering av utenlandsk valuta som du kjører for å oppdatere verdien av åpne transaksjoner i leverandører og kunder. 

Den teoretiske verdien, eller bokførte verdien, av åpne transaksjoner i utenlandsk valuta varierer over tid på grunn av endringer i valutakursene. Hvis du vil oppdatere verdien av åpne transaksjoner i leverandører og kunder, kan du kjøre prosessen for revaluering av utenlandsk valuta. Revaluering av utenlandsk valuta kan kjøres for både for leverandører og kunder. Prosessen bruker en ny valutakurs til å revaluere de åpne beløpene, eller ikke utlignede beløp, på en bestemt dato. Forskjellen mellom de opprinnelige posterte beløpene og de revaluerte beløpene fører til urealisert fortjeneste eller tap for hver åpen transaksjon. Underfinans for Leverandør og Kunder oppdateres deretter for å gjenspeile urealisert fortjeneste eller tap, og en regnskapspost posteres til økonomimodulen.

## <a name="simulate-a-foreign-currency-revaluation"></a>Simulere en revaluering av utenlandsk valuta
Før du revaluerer beløp i utenlandsk valuta på åpne transaksjoner, kan du kjøre en simuleringsrapport for revaluering av utenlandsk valuta for samme dato og metode. For å kjøre simuleringsrapporten velger du siden **Revaluering av utenlandsk valuta** og klikker **Simulering**-knappen. Rapporten inneholder en forhåndsvisning av beløpet urealisert fortjeneste eller tap, basert på parameterne som er definert for simuleringen.

## <a name="process-a-foreign-currency-revaluation"></a>Behandle en revaluering av utenlandsk valuta
Bruk siden **Revaluering av utenlandsk valuta** under **Periodiske oppgaver** til å revaluere åpne transaksjoner. Du kan kjøre prosessen i sanntid eller planlegge å kjøre den ved hjelp av en satsvis jobb. Når du definerer innstillingene for revalueringsprosessen, må du bekrefte om du vil skrive ut en rapport med resultatene. Revalueringsrapporten kan ikke skrives ut på nytt når prosessen er fullført. Hvis du genererer rapporten for revaluering av utenlandsk valuta, vises ulike saldoer på kunde-/leverandørnivået og valutanivået:

-   Saldoene for kunder eller leverandører som har transaksjoner i utenlandsk valuta som er revaluert. Følgende saldoer vises:
    -   Den totale opprinnelige saldoen i utenlandsk valuta.
    -   Det totale fremmedvalutabeløpet i regnskapsvalutaen, i henhold til den tidligere revalueringen.
    -   Det totale fremmedvalutabeløpet i regnskapsvalutaen, i henhold til den gjeldende revalueringen.
    -   Differansen mellom den tidligere og gjeldende revalueringen. Denne forskjellen er tillegget for urealisert fortjeneste eller tap.
-   Totalen for urealisert fortjeneste eller tap for hver valuta.

En post opprettholdes hver gang du kjører en revaluering av utenlandsk valuta. Fra oppføringen på siden **Revaluering av utenlandsk valuta** velger du **Transaksjoner** for å vise detaljert liste over transaksjoner som ble opprettet på grunn av revalueringen. Hver bilagstransaksjonen representerer den åpne transaksjonen som ble revaluert. Hvis en åpen transaksjon ble revaluert mer enn én gang, vises to oppføringer som bruker det samme bilaget. Én post vil være for tilbakeføringen av forrige urealisert fortjeneste eller tap, og den andre oppføringen er for ny urealisert fortjeneste eller tap. For å kjøre revalueringsprosessen klikk knappen **Revaluering av utenlandsk valuta**. Definer passende innstillinger for følgende parametere:

-   **Metode** – Metoden som brukes i den valgte jobben for revaluering av utenlandsk valuta:
    -   **Standard** – Jobber for revaluering av utenlandsk valuta blir postert uavhengig av om resultatet er fortjeneste eller tap.
    -   **Minimum** – Jobbene for revaluering av utenlandsk valuta er postert bare hvis resultatet er tap.
    -   **Fakturadato** – Jobbene for revaluering av utenlandsk valuta bruker transaksjonenes opprinnelige valutakurs for transaksjonene, som revalueres til den opprinnelige verdien i regnskapsvalutaen. Resultatet av en tidligere revaluering av utenlandsk valuta er avbrutt.
-   **Vurdert dato** – Datoen som alle transaksjoner som har åpne (ikke utlignede) mengder på denne datoen, finnes på. Beløp i utenlandsk valuta revalueres ved hjelp av valutakursene som er angitt på **Valutakurser**-siden for den vurderte datoen. Når beløp i utenlandsk valuta revalueres på en vurdert dato, blir denne datoen den siste datoen for revaluering av utenlandsk valuta for transaksjonene som justeres. Hvis du kjører en revaluering av utenlandsk valuta for en vurdert dato som er før den siste datoen for revaluering av utenlandsk valuta for transaksjoner som allerede er justert, justeres ikke transaksjoner som er åpne på den tidligere vurderte datoen, men som har en nyere siste dato for revaluering av utenlandsk valuta, av den periodiske jobben.
-   **Kursdato** – Datoen som avgjør valutakursen som skal brukes i revalueringen av utenlandsk valuta.
-   **Bruk posteringsprofil fra** – Posteringsprofilen som brukes til å angi standard hovedkonto for Kunder eller Leverandører for regnskapsoppføringene for transaksjoner for revaluering av utenlandsk valuta:
    -   **Postering** – Posteringsprofilen til kundetransaksjonen brukes.
    -   **Velg** – Angi posteringsprofilen i **Posteringsprofil**-feltet.
-   **Posteringsprofil** – Hvis du velger **Velg** i **Bruk posteringsprofil fra**-feltet, bestemmes posteringsprofilen for transaksjonene for revaluering av utenlandsk valuta av posteringsprofilen i dette feltet.
-   **Finansdimensjoner** – Finansdimensjonene som posteres på regnskapsoppføringene for transaksjonene for revaluering av utenlandsk valuta:
    -   **Ingen** – Ingen finansdimensjoner posteres. Hvis du har en nødvendig finansdimensjon i kontostrukturen, kjøres revalueringsprosessen fremdeles og oppretter regnskapsoppføringer som ikke har noen finansdimensjoner. Du vil få en advarselsmelding først, slik at du kan avbryte revalueringen.
    -   **Tabell** – Finansdimensjonene for kunde- eller leverandørkontoen posteres i transaksjonene for revaluering av utenlandsk valuta.
    -   **Postering** – Finansdimensjonene for transaksjonen som revalueres, posteres i transaksjonene for revaluering av utenlandsk valuta. Som standard brukes finansdimensjonene fra den opprinnelige transaksjonens kunde-/leverandørfinanskonto for revalueringstransaksjonens kunde-/leverandørhovedkonto, og finansdimensjonene fra den opprinnelige transaksjonens finanskonto for utgift/aktiva/omsetning brukes for revalueringstransaksjonens hovedkonto for urealisert tap/vinning.





