---
title: ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 4)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f14be560ab014224e32169b4ac97682a669249b4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605311"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten). Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering. Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon. 


## <a name="run-report"></a>Kjøre rapport
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Eksempelmodell for finansdimensjoner i treet.
3. Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.
4. Klikk på Kjør.
![Siden ER-konfigurasjoner.](../media/er-financial-dimensions-guides-run1.png)
5. Angi eller velg en verdi i feltet Dimensjonsnavn.
    * Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende informasjon: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Lysbilde av parametere for elektronisk rapport, rullegardinmenyen for dimensjonsnavn.](../media/er-financial-dimensions-guides-run2.png)
6. Utvid delen Poster som skal inkluderes.
7. Klikk på Filter.
8. Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.
9. Skriv inn 00057 i Kriterier-feltet.
10. Klikk på OK.
11. Klikk på OK.
![Lysbilde av parametere for elektronisk rapport, delen Rapporter som skal inkluderes.](../media/er-financial-dimensions-guides-run3.png)
    * Se gjennom de genererte utdataene. For hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet. Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.  
![ER-konfigurasjoner genererte utdata.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
