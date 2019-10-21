---
title: Bekrefte salgsordrer
description: Denne fremgangsmåten beskriver hvordan du bekrefter salgsordrer.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9274a90ffbf6e5703d3ed97a8b974227b25c2a0
ms.sourcegitcommit: 62d66f98d4bbf916e19184506b90055bb68d219f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/28/2019
ms.locfileid: "1924384"
---
# <a name="confirm-sales-orders"></a>Bekrefte salgsordrer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du bekrefter salgsordrer. Du vil bli vist hvordan du bekrefter en enkelt ordre, og hvordan du bekrefter flere ordrer samtidig. Disse oppgavene vil vanligvis utføres av en salgsordrebehandler. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Før du begynner kontrollerer du at det er flere åpne salgsordrer for den samme kunden. Hvis du bruker USMF, kan du bruke US-027 for kunde.


## <a name="confirm-a-single-sales-order"></a>Bekrefte en enkelt salgsordre
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
2. Finn og velg ordren du vil bekrefte i listen.
3. Klikk koblingen på salgsordrenummeret for å åpne den valgte ordren.
4. I **Handlingsrute** klikker du på **Selg**.
5. Klikk på **Bekreft salgsordre**.
6. Utvid seksjonen **Parametere**. Kontroller at alternativet **Postering** er satt til Ja.  
7. Sett alternativet **Skriv ut bekreftelse** til Ja. Feltet **Kontroller kredittgrense** angir metoden som brukes til å beregne kundens gjenværende kreditt. Den kopieres som standard fra siden Kundeparametere. Hvis du vil hoppe over kredittgrensekontrollen ved bekreftelse av en bestemt salgsordre, setter du **Kontroller kredittgrense** til Ingen. Du bør imidlertid være oppmerksom på at selv om dette feltet er satt til Ingen, vil kredittgrensekontrollen fremdeles utføres hvis alternativet **Obligatorisk kredittgrense** er valgt i hoveddata for kunder. 
8. Klikk **OK**.
9. Klikk **Ja**.
10. Lukk siden.
11. Klikk på **Alternativer** i **handlingsruten**.
12. Klikk på **Bytt visning**.
13. Klikk på **Hodevisning**. Når en ordre er bekreftet, vil **Dokumentstatus** settes til Bekreftelse. 
14. I **Handlingsrute** klikker du på **Selg**.
15. Klikk på **Salgsordrebekreftelse**.
16. Lukk siden.

## <a name="confirm-multiple-sales-orders-at-once"></a>Bekrefte flere salgsordrer samtidig
1. Gå til **Salg og markedsføring > Salgsordrer > Ordrebekreftelse > Bekreft salgsordre**.
2. Klikk **Velg**.
3. I listen i kategorien **Område** finner og velger du posten som refererer til feltet **Kundekonto**.
4. Klikk på rullegardinknappen i **Kriterier**-feltet for å åpne oppslaget.
5. I listen finner og merker du kundekontoen som har flere ordrer som du vil massebekrefte. Hvis du bruker USMF, kan du velge kontoen US-027.  
6. Klikk **OK**.
    - Kategorien **Oversikt** viser en liste over ordrene som samsvarer med spørringskriteriene. Disse vil være inkludert i bekreftelsen.  
    - **Samleoppdatering for**-feltet i **Parametere**-delen angir parameteren som er ordrene som skal summeres etter, i ett bekreftelsesdokument. Som standard kopieres alternativet fra innstillingen **Standardverdier for samleoppdatering** på siden **Kundeparametere**.  
7. I feltet **Samleoppdatering for** velger du Ordre. Minimumsparameterne som kreves for å opprette samleoppdateringer, er **Fakturakonto** og **Valuta**. Dette betyr at samleoppdateringer som har forskjellige fakturakontoer og forskjellige valutaer ikke er tillatt. Tilleggsparametere kan settes opp på siden **Parametere for samleoppdatering**, som er tilgjengelig fra siden **Kundeparametere**. 
8. Klikk på rullegardinknappen i feltet **Salgsordre** for å åpne oppslaget.
9. Velg ordrenummeret som du vil skal være samleordren, i listen.
10. Klikk på **Ordne**.
11. Klikk **OK**.
12. Klikk **OK**.

