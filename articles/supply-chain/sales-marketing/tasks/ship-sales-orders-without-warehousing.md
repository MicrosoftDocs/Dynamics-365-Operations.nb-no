--- 
title: Sende salgsordrer uten lagerstyring
description: "Denne veiledningen beskriver hvordan du oppdaterer en salgsordre når produkter sendes til kunden."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f1b9dd4b99bcbcc6cfbc5cfd8e3271fa80c628c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Sende salgsordrer uten lagerstyring

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen beskriver hvordan du oppdaterer en salgsordre når produkter sendes til kunden. Veiledningen er tilgjengelig for fullføringsflyten som ikke er definert for lagerstyring (verken grunnleggende eller avansert lagerstyring), og krever derfor ikke at produktplukking registreres før forsendelse. Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF. I begge tilfeller før du starter oppgaven, oppretter du en salgsordre for en lagerført vare med et antall som er større enn 1. For å unngå en posteringsfeil må du kontrollere at produktets lagerbeholdning i området og lageret som du har valgt, dekker ordreantallet.


## <a name="post-packing-slip-for-an-order"></a>Postere følgeseddel for en ordre
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Finn og velg ordren du har opprettet for denne oppgaven, i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Plukk og pakk i handlingsruten.
5. Klikk Poster følgeseddel.
6. Vis eller skjul delen Parametere.
7. Velg Alle i feltet Antall.
    * Andre alternativer omfatter Lever nå og Plukket. Hvis ordrelinjen skal leveres delvis og Lever nå-feltet på ordrelinjen som inneholder et antall, velger du Lever nå. Hvis organisasjonens fullføringsflyt inkluderer plukking som en egen prosess som administreres av og er registrert i en plukkliste, velger du Plukket.  
    * Kontroller at alternativet Postering er satt til Ja.  
8. Velg Ja for alternativet Skriv ut følgeseddel.
    * Kategorien Oversikt viser en liste med følgesedler som skal genereres i denne posteringen. Hvis du leverer en enkelt ordre, vil det vanligvis være én følgeseddel. Men hvis den ordrelinjer skal sendes fra forskjellige områder, vil postering automatisk deles inn i det aktuelle antallet dokumenter. Dette er en obligatorisk betingelse som ikke kan endres. På samme måte bokføringen også deles i flere dokumenter hvis ordrens linjer skal leveres til forskjellige leveringsadresser, og policyen for levering settes opp slik at det kreves en deling.  
9. Merk raden for ordrelinjen som skal leveres, i kategorien Linjer.
10. Angi et tall som er lavere enn det opprinnelige antallet i feltet Oppdater.
11. Klikk OK.
12. Klikk Ja.
13. Lukk siden.
14. Klikk Alternativer i handlingsruten.
15. Klikk Bytt visning.
16. Klikk Hodevisning.
    * Hvis alle linjene i ordren er levert, endres ordrestatusen fra Åpen til Levert.  
    * I dette eksemplet er ordrelinjen levert delvis. Dette er grunnen til at ordrestatusen er Åpen.     
    * Dokumentstatus-feltet er satt til Følgeseddel, fordi minst én av bestillingslinjene er levert.  
17. Klikk Generelt i handlingsruten.
18. Velg Linjeantall.
19. Lukk siden.
20. Klikk Plukk og pakk i handlingsruten.
21. Klikk Følgeseddel.
    * Siden Følgeseddeljournal inneholder alle følgeseddeldokumentene som ble generert for ordren. Du kan se nærmere på detaljene for hvert dokument og skrive dem ut, hvis du ønsker.  


