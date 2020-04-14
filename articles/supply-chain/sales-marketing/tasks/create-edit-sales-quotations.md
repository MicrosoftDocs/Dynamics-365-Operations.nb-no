---
title: Opprette og redigere salgstilbud
description: Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f313aafb79faaf1344b7e70759405b3bab2d7e45
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148727"
---
# <a name="create-and-edit-sales-quotations"></a>Opprette og redigere salgstilbud

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud. Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.


## <a name="create-a-sales-quotation"></a>Opprett et salgstilbud
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgstilbud > Alle tilbud**.
2. Klikk på **Ny**.
3. Velg **Kundeemnetype** i feltet Kontotype.
4. Angi eller velg en verdi i feltet **Kundeemne**.
5. Utvid delen **Generelt**. Fordi du valgte å opprette et tilbud fra området Salg og markedsføring settes typen automatisk til Salgstilbud. Hvis du vil opprette et tilbud for et prosjekt, må du åpne det fra modulen **Prosjektstyring og regnskap**.
6. Klikk **OK**. Feltene og handlinger i tilbudslinjene er veldig lik de i salgsordrelinjene.   Som salgsordrer kan du kan opprette tilbud for en bestemt vare, eller når varenummeret er ukjent eller ikke finnes på tidspunktet for oppretting av tilbud, kan tilbud opprettes for en salgskategori.     
7. Angi eller velg en verdi i feltet **Vare**.
8. Skriv inn en verdi i **Område**-feltet.
9. Angi et tall i **Antall**-feltet. Hvis det finnes gyldige forretningsavtaler for varen som er valgt på linjen, kopieres den aktuelle prisen og rabattene automatisk til tilbudslinjen. Kontroller at Enhetspris-feltet inneholder en verdi, og du kan også angi rabattverdier hvis du vil. 
10. Klikk **Lagre**.
11. Klikk på **Salgstilbud** i **handlingsruten**.
12. Klikk på **Totaler**.
13. Klikk **OK**.
14. Velg salgstilbudlinjen.
15. Klikk på **Tilbud** i **handlingsruten**.
16. Klikk på **Prissimulering**.
    - På siden **Kjør prissimulering** kan du eksperimentere med å justere forventet omsetning eller lønnsomhet for tilbudet basert på ønsket enhetspris, rabattbeløp, rabattprosent, totalbeløp, margin eller dekningsgrad. Når du er fornøyd med måltallene, du bruker forslaget på tilbudslinjen, og de prisrelaterte feltene oppdateres tilsvarende.  
    - Du kan opprette så mange prissimuleringer som du ønsker. Når du klikker på **Ny**, kopieres prisbetingelsene fra gjeldende tilbudslinje til siden. Du kan deretter endre verdiene i de prisrelaterte feltene til målene. En endring i ett av feltene vil utløse omberegning i alle de andre feltene. For at systemet skal beregne salgsmargin og dekningsgrad, må produktets enhetskostnad være kjent. Bruk kategorien Simulerte priser for en detaljert visning av de opprinnelige prisene, foreslåtte endringer og deres virkning på tilbudstotalene. Som regel når en simulering som angir et nytt beløp brukes for tilbudslinjen, beregner systemet på nytt og angir en ny verdi i feltet Enhetspris. Hvis simuleringen er basert på en ny margin eller et nytt dekningsbidrag, oppdateres bare feltet Nettobeløp og enhetsprisen er tom. I begge tilfeller slettes eventuelle rabatter som var på tilbudslinjen før simuleringen.
17. Klikk på **Tilbud** i **handlingsruten**.
18. Klikk på **Send tilbud**.
19. Velg Ja i feltet **Skriv ut tilbud**.
20. Klikk **OK**. Rapporten kan ta litt tid å generere. Ikke lukk siden før dette gjøres.

## <a name="update-a-sales-quotation"></a>Oppdater et salgstilbud
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgstilbud > Alle tilbud**.
2. Klikk på **Følg opp** i **handlingsruten**.
3. Klikk på **Konverter til kunde**.
4. Skriv inn en verdi i **Kundekonto**-feltet.
5. Klikk på **Kontroller**. Kontroller at det vises en melding om at kontonummeret som du skrev inn, er ledig for bruk.  
6. Klikk **OK**. Systemet har nå opprettet en ny kundekonto for kundeemnet på tilbudet.  
7. Lukk siden.
8. Klikk på **Følg opp** i **handlingsruten**.
9. Klikk **Bekreft**.
10. Angi eller velg en verdi i **Årsak**-feltet.
11. Klikk **OK**.
12. Klikk på **Generelt** i **handlingsruten**.
13. Klikk på **Salgsordrer**.
14. Lukk siden.

