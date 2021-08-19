---
title: Konfigurere utligning
description: Hvordan og når transaksjonene utlignes kan det være komplekse temaer, slik at det er svært viktig at du forstår og definerer parameterne for å dekke dine forretningsbehov. Dette emnet beskriver parameterne som brukes for utligning for både leverandører og kunder.
author: kweekley
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 323a1e6d426208a880a72dd89f7be04bacbf13a8e6c5d8ab7599217cfc18f2c0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720580"
---
# <a name="configure-settlement"></a>Konfigurere utligning

[!include [banner](../includes/banner.md)]

Hvordan og når transaksjonene utlignes kan det være komplekse temaer, slik at det er svært viktig at du forstår og definerer parameterne for å dekke dine forretningsbehov. Dette emnet beskriver parameterne som brukes for utligning for både leverandører og kunder. 

Følgende parametere påvirker hvordan utligninger behandles i Microsoft Dynamics 365 Finance. Utligning er å utligne en faktura mot en betaling eller en kreditnota. Disse parameterne er i **Utligning**-området på sidene **Kundeparametere** og **Leverandørparametere**.

- **Automatisk utligning** – Sett dette alternativet til **Ja** hvis en transaksjon skal utlignes automatisk mot andre åpne transaksjoner når den posteres. Hvis dette alternativet er satt til **Nei**, kan brukere utligne transaksjoner manuelt når de registrerer betalinger, eller senere, ved å bruke siden **Utlign transaksjoner**.
- **Håndtering av kontantrabatt** – Angi hvordan en [kontantrabatt håndteres når en faktura er overbetalt](cash-discount-handling-overpayments.md). Når det gjelder en overbetaling, kan kontantrabatten reduseres, behandles som en differanse eller forbli på kontoen for kunden eller leverandøren.
  -   **Løs** – Kontantrabattbeløpet blir redusert med overbetalingsbeløpet. Dette gjelder alltid, uansett om overbetalingsbeløpet er mindre eller større enn beløpet som er angitt i feltet **Maksimal over- eller underbetaling**.
  -   **Spesifikk** – Overbetalingsbeløpet blir enten postert til en finanskonto for kontantrabattdifferanse eller forblir en saldo på kundens eller leverandørens konto. Den spesifikke virkemåten avhenger av om overbetalingsbeløpet er mellom 0,00 og beløpet som er angitt i feltet **Maksimal over- eller underbetaling**, eller om overbetalingsbeløpet er større enn beløpet for **Maksimal over- eller underbetaling**.
- **Maksimal øredifferanse** – Angi den maksimale øredifferansen som er tillatt for de utlignede transaksjonene. Hvis differansen er lik eller mindre enn øredifferansen som er angitt i dette feltet, posteres differansen til finanskontoen for øredifferanse som er angitt på siden **Kontoer for automatiske transaksjoner**.
- **Maksimal over- eller underbetaling** – Angi beløpet som er godkjent for over- og underbetaling. Hvis du vil beregne mva på overbetalinger eller underbetalinger, kan du klikke **Merverdiavgift** på **Økonomiparametere**-siden og deretter merke av for **Merverdiavgift på over- eller underbetaling**.
  -   Hvis overbetalingen eller underbetalingen gir en differanse som er mindre enn differansen som er definert i feltet **Maksimal øredifferanse**, posteres øredifferansebeløpet til øredifferansekontoen.
  -   Hvis overbetalingen eller underbetalingen gir en differanse som er større enn differansen som er definert i feltet **Maksimal øredifferanse**, posteres differansebeløpet på differansekontoen som er valgt for posteringstypen **Kundekontantrabatt** eller **Leverandørkontantrabatt** på siden **Kontoer for automatiske transaksjoner**.
- **Beregn kontantrabatter for delvise betalinger** – Sett dette alternativet til **Ja** for å aktivere automatisk beregning av kontantrabatter for delbetalinger.
  -   Effekten av dette alternativet er avhengig av verdien i feltet **Bruk kontantrabatt** på siden **Utlign transaksjoner**. Hvis dette alternativet er satt til **Ja**, brukes rabatten når feltet **Bruk kontantrabatt** er satt til **Normal**. Når feltet **Bruk kontantrabatt** er satt til **Alltid**, brukes alltid kontantrabatten, uavhengig av innstillingen for dette feltet. Når feltet **Bruk kontantrabatt** er satt til **Aldri**, brukes aldri kontantrabatten, uavhengig av innstillingen for dette feltet.
  -   Hvis dette alternativet er satt til **Ja** og en bruker endrer verdien i feltet **Beløp som skal utlignes** på **Utlign transaksjoner**-siden, beregnes rabatten automatisk og vises som standardoppføringen i feltet **Kontantrabattbeløp som skal brukes**.
  -   Hvis dette alternativet er satt til **Nei** og en bruker endrer verdien i feltet **Beløp som skal utlignes** på **Utlign transaksjoner**-siden, er standardoppføringen i feltet **Kontantrabattbeløp som skal brukes** lik **0** (null).
- **Beregn kontantrabatter for kreditnotaer** – Sett dette alternativet til **Ja** for å beregne en kontantrabatt for kreditnotaer automatisk. I Kunde er en kreditnotatransaksjon en negativ transaksjon som har en verdi i **Faktura**-feltet på siden **Fritekstfaktura** eller en retur på **Salgsordre**-siden.
  - Effekten av dette alternativet er avhengig av verdien i feltet <strong>Bruk kontantrabatt</strong> på siden <strong>Utlign transaksjoner</strong>. Hvis dette alternativet er satt til <strong>Ja</strong>, brukes rabatten når feltet *<strong><em>Bruk kontantrabatt</em></strong>* er satt til <strong>Normal</strong>. Når feltet *<strong><em>Bruk kontantrabatt</em></strong>* er satt til <strong>Alltid</strong>, brukes alltid kontantrabatten, uavhengig av innstillingen for dette feltet. Når feltet *<strong><em>Bruk kontantrabatt</em></strong>* er satt til <strong>Aldri</strong>, brukes aldri kontantrabatten, uavhengig av innstillingen for dette feltet.
  - Hvis dette alternativet er satt til **Ja** og en kreditnota er merket på **Utlign transaksjoner**-siden, beregnes rabatten automatisk og vises som standardoppføringen i feltet **Kontantrabattbeløp som skal brukes**.
  - Hvis dette alternativet er satt til **Nei** og en kreditnota er merket på **Utlign transaksjoner**-siden, er standardoppføringen i feltet **Kontantrabattbeløp som skal brukes** lik **0** (null).

- **Motkontoer for rabatt (bare AP)** – Definer standard finanskonto for kontantrabatt som skal brukes for regnskapsoppføringen for kontantrabatter.
  -   **Bruk Hovedkonto for leverandørrabatter** – Kontantrabatten posteres på hovedkontoen som er definert på siden **Kontantrabattoppsett**.
  -   **Kontoer på fakturalinjene** – Kontantrabatten posteres på finanskontoer på den opprinnelige fakturaen.
- **Marker linjer i fritekstfakturaer og rentenotaer (bare AR)** – Sett dette alternativet til **Ja** for å aktivere knappen **Marker fakturalinjer** på sidene **Angi kundebetalinger**, **Journalbilag for betaling** og **Utlign transaksjoner**. Brukere kan bruke denne knappen til å merke individuelle linjer for utligning.
- **Prioriter utligning (bare AR)** – Sett dette alternativet til **Ja** for å aktivere knappen **Merk etter prioritet** på sidene **Angi kundebetalinger** og **Utlign transaksjoner**. Brukere kan bruke denne knappen til å tilordne den forhåndsbestemte utligningsrekkefølgen til transaksjoner.  Når utligningsrekkefølgen er brukt på en transaksjon, kan rekkefølgen og betalingsfordelingen endres før postering.
- **Bruk prioritet for automatiske utligninger** – Sett dette alternativet til **Ja** for å bruke den angitte prioritetsrekkefølgen når transaksjonene utlignes automatisk. Dette feltet er tilgjengelig bare hvis **Prioriter utligning** og **Automatisk utligning** er angitt til **Ja**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Faste dimensjoner på leverandører/kunder-hovedkontoer

Når det brukes faste dimensjoner på leverandører/kunder-hovedkontoen, blir flere regnskapsoppføringer og to ekstra leverandørtransaksjoner postert av utligningsprosessen. Utligning sammenligner leverandør/kunde-finanskonto fra fakturaen og betalingen.  Når betaling og utligning er fullført sammen, som er det vanlige scenariet, posteres ikke betalingens regnskapsoppføring til økonomimodulen før utligningsprosessen også er fullført. På grunn av hendelsesrekkefølgen for behandling kan ikke utligningen fastsette den faktiske leverandør/kunde-finanskontoen fra betalingens regnskapspost. Utligningen rekonstruerer hva finanskontoen blir for betalingen. Dette er et problem når en fast dimensjon brukes for leverandør/kunde-hovedkontoen.

For å rekonstruere finanskontoen hentes leverandør/kunde-hovedkontoen fra posteringsprofilen, og finansdimensjonene hentes fra leverandørtransaksjonsposten for betalingen, som definert i betalingsjournalen. Faste dimensjoner legges ikke som standard inn i betalingsjournaler, men brukes i stedet på hovedkontoen som det siste trinnet av posteringsprosessen. Dermed er den faste dimensjonsverdien trolig ikke å finne på leverandørtransaksjonen, med mindre den som standard kom fra en annen kilde, for eksempel leverandøren. Den rekonstruerte kontoen inneholder ikke den faste dimensjonen. Behandling av utligningen bestemmer at en justeringsoppføring må opprettes, fordi fakturaen som er bokført med den faste dimensjonsverdien og den rekonstruerte betalingskontoen ikke ble det.  Siden utligningen fortsetter med postering av justeringsoppføringen, er siste trinn i posteringen at den faste dimensjonen anvendes. Ved å legge til den faste dimensjon i justeringsoppføringen posteres den med en debet og kreditt til samme finanskonto. Utligningen kan ikke rulle tilbake regnskapsposten.

Hvis du vil unngå ekstra regnskapsoppføringer, debet og kreditt til samme finanskonto, må følgende løsninger vurderes, avhengig av dine forretningsbehov. 

-   Organisasjoner bruker ofte faste dimensjoner til å nullfylle en finansdimensjon som ikke er nødvendig. Dette er vanligvis tilfelle for balansekontoer, for eksempel leverandører/kunder. Kontostrukturer kan brukes til å ikke spore finansdimensjoner som vanligvis nullfylles.  Du kan fjerne finansdimensjonen for balansekontoer og dermed eliminere behovet for å bruke faste dimensjoner.
-   Hvis organisasjonen din krever faste dimensjoner på kunder/leverandører-hovedkontoen, må du finne en måte å legge den faste dimensjonen til betalingen som standard, slik at den faste dimensjonsverdien lagres på leverandørtransaksjonen for betalingen. Dette gjør at systemet kan rekonstruere kunde/leverandør-hovedkontoen for å inkludere de faste dimensjonsverdiene. Den faste dimensjonsverdien kan defineres som en standard på enten leverandører eller journalnavnet for betalingsjournalen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]