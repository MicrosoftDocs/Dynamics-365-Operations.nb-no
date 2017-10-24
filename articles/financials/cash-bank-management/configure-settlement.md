---
title: Konfigurere utligning
description: "Hvordan og når transaksjonene utlignes kan det være komplekse temaer, slik at det er svært viktig at du forstår og definerer parameterne for å dekke dine forretningsbehov. Denne artikkelen beskriver parameterne som brukes for utligning for både leverandører og kunder."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ade348540a6d3e9210321d3661e97ac716efaf58
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="configure-settlement"></a>Konfigurere utligning

[!include[banner](../includes/banner.md)]


Hvordan og når transaksjonene utlignes kan det være komplekse temaer, slik at det er svært viktig at du forstår og definerer parameterne for å dekke dine forretningsbehov. Denne artikkelen beskriver parameterne som brukes for utligning for både leverandører og kunder. 

Følgende parametere påvirker hvordan utligninger behandles i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Utligning er å utligne en faktura mot en betaling eller en kreditnota. Disse parameterne er i **Utligning**-området på sidene **Kundeparametere** og **Leverandørparametere**.

-   **Automatisk utligning** – Sett dette alternativet til **Ja** hvis en transaksjon skal utlignes automatisk mot andre åpne transaksjoner når den posteres. Hvis dette alternativet er satt til **Nei**, kan brukere utligne transaksjoner manuelt når de registrerer betalinger, eller senere, ved å bruke siden **Utlign transaksjoner**.
-   **Håndtering av kontantrabatt** – Angi hvordan en [kontantrabatt håndteres når en faktura er overbetalt](cash-discount-handling-overpayments.md). Når det gjelder en overbetaling, kan kontantrabatten reduseres, behandles som en differanse eller forbli på kontoen for kunden eller leverandøren.
    -   **Løs** – Kontantrabattbeløpet blir redusert med overbetalingsbeløpet. Dette gjelder alltid, uansett om overbetalingsbeløpet er mindre eller større enn beløpet som er angitt i feltet **Maksimal over- eller underbetaling**.
    -   **Spesifikk** – Overbetalingsbeløpet blir enten postert til en finanskonto for kontantrabattdifferanse eller forblir en saldo på kundens eller leverandørens konto. Den spesifikke virkemåten avhenger av om overbetalingsbeløpet er mellom 0,00 og beløpet som er angitt i feltet **Maksimal over- eller underbetaling**, eller om overbetalingsbeløpet er større enn beløpet for **Maksimal over- eller underbetaling**.
-   **Maksimal øredifferanse** – Angi den maksimale øredifferansen som er tillatt for de utlignede transaksjonene. Hvis differansen er lik eller mindre enn øredifferansen som er angitt i dette feltet, posteres differansen til finanskontoen for øredifferanse som er angitt på siden **Kontoer for automatiske transaksjoner**.
-   **Maksimal over- eller underbetaling** – Angi beløpet som er godkjent for over- og underbetaling. Hvis du vil beregne mva på overbetalinger eller underbetalinger, kan du klikke **Merverdiavgift** på **Økonomiparametere**-siden og deretter merke av for **Merverdiavgift på over- eller underbetaling**.
    -   Hvis overbetalingen eller underbetalingen gir en differanse som er mindre enn differansen som er definert i feltet **Maksimal øredifferanse**, posteres øredifferansebeløpet til øredifferansekontoen.
    -   Hvis overbetalingen eller underbetalingen gir en differanse som er større enn differansen som er definert i feltet **Maksimal øredifferanse**, posteres differansebeløpet på differansekontoen som er valgt for posteringstypen **Kundekontantrabatt** eller **Leverandørkontantrabatt** på siden **Kontoer for automatiske transaksjoner**.
-   **Beregn kontantrabatter for delvise betalinger** – Sett dette alternativet til **Ja** for å aktivere automatisk beregning av kontantrabatter for delbetalinger.
    -   Effekten av dette alternativet er avhengig av verdien i feltet **Bruk kontantrabatt** på siden **Utlign transaksjoner**. Hvis dette alternativet er satt til **Ja**, brukes rabatten når feltet **Bruk kontantrabatt** er satt til **Normal**. Når feltet **Bruk kontantrabatt** er satt til **Alltid**, brukes alltid kontantrabatten, uavhengig av innstillingen for dette feltet. Når feltet **Bruk kontantrabatt** er satt til **Aldri**, brukes aldri kontantrabatten, uavhengig av innstillingen for dette feltet.
    -   Hvis dette alternativet er satt til **Ja** og en bruker endrer verdien i feltet **Beløp som skal utlignes** på **Utlign transaksjoner**-siden, beregnes rabatten automatisk og vises som standardoppføringen i feltet **Kontantrabattbeløp som skal brukes**.
    -   Hvis dette alternativet er satt til **Nei** og en bruker endrer verdien i feltet **Beløp som skal utlignes** på **Utlign transaksjoner**-siden, er standardoppføringen i feltet **Kontantrabattbeløp som skal brukes** lik **0** (null).
-   **Beregn kontantrabatter for kreditnotaer** – Sett dette alternativet til **Ja** for å beregne en kontantrabatt for kreditnotaer automatisk. I Kunde er en kreditnotatransaksjon en negativ transaksjon som har en verdi i **Faktura**-feltet på siden **Fritekstfaktura** eller en retur på **Salgsordre**-siden.
    -   Effekten av dette alternativet er avhengig av verdien i feltet **Bruk kontantrabatt** på siden **Utlign transaksjoner**. Hvis dette alternativet er satt til **Ja**, brukes rabatten når feltet ****Bruk kontantrabatt**** er satt til **Normal**. Når feltet ****Bruk kontantrabatt**** er satt til **Alltid**, brukes alltid kontantrabatten, uavhengig av innstillingen for dette feltet. Når feltet ****Bruk kontantrabatt**** er satt til **Aldri**, brukes aldri kontantrabatten, uavhengig av innstillingen for dette feltet.
    -   Hvis dette alternativet er satt til **Ja** og en kreditnota er merket på **Utlign transaksjoner**-siden, beregnes rabatten automatisk og vises som standardoppføringen i feltet **Kontantrabattbeløp som skal brukes**.
    -   Hvis dette alternativet er satt til **Nei** og en kreditnota er merket på **Utlign transaksjoner**-siden, er standardoppføringen i feltet **Kontantrabattbeløp som skal brukes** lik **0** (null).
-   **Motkontoer for rabatt (bare AP)** – Definer standard finanskonto for kontantrabatt som skal brukes for regnskapsoppføringen for kontantrabatter.
    -   **Bruk Hovedkonto for leverandørrabatter** – Kontantrabatten posteres på hovedkontoen som er definert på siden **Kontantrabattoppsett**.
    -   **Kontoer på fakturalinjene** – Kontantrabatten posteres på finanskontoer på den opprinnelige fakturaen.
-   **Marker linjer i fritekstfakturaer og rentenotaer (bare AR)** – Sett dette alternativet til **Ja** for å aktivere knappen **Marker fakturalinjer** på sidene **Angi kundebetalinger**, **Journalbilag for betaling** og **Utlign transaksjoner**. Brukere kan bruke denne knappen til å merke individuelle linjer for utligning.
-   **Prioriter utligning (bare AR)** – Sett dette alternativet til **Ja** for å aktivere knappen **Merk etter prioritet** på sidene **Angi kundebetalinger** og **Utlign transaksjoner**. Brukere kan bruke denne knappen til å tilordne den forhåndsbestemte utligningsrekkefølgen til transaksjoner.  Når utligningsrekkefølgen er brukt på en transaksjon, kan rekkefølgen og betalingsfordelingen endres før postering.
-   **Bruk prioritet for automatiske utligninger** – Sett dette alternativet til **Ja** for å bruke den angitte prioritetsrekkefølgen når transaksjonene utlignes automatisk. Dette feltet er tilgjengelig bare hvis **Prioriter utligning** og **Automatisk utligning** er angitt til **Ja**.





