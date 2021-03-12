---
title: Sende salgsordrer uten lagerstyring
description: Dette emnet forklarer hvordan du oppdaterer en salgsordre når produkter sendes til kunden.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45884bd5ff70b31c62a7e0affafb6c5ddb457be3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974866"
---
# <a name="ship-sales-orders-without-warehousing"></a>Sende salgsordrer uten lagerstyring

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppdaterer en salgsordre når produkter sendes til kunden. Veiledningen er tilgjengelig for fullføringsflyten som ikke er definert for lagerstyring (verken grunnleggende eller avansert lagerstyring), og krever derfor ikke at produktplukking registreres før forsendelse. Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF. I begge tilfeller før du starter oppgaven, oppretter du en salgsordre for en lagerført vare med et antall som er større enn 1. For å unngå en posteringsfeil må du kontrollere at produktets lagerbeholdning i området og lageret som du har valgt, dekker ordreantallet.

## <a name="post-packing-slip-for-an-order"></a>Postere følgeseddel for en ordre
1. I navigasjonsruten går du til **Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
2. Finn og velg ordren du har opprettet for denne oppgaven, i listen.
3. Klikk på **Plukk og pakk** i handlingsruten.
4. Velg **Poster følgeseddel**.
5. Vis eller skjul delen **Parametere**.
6. Velg **Alle** i **Antall**-feltet.
    - Andre alternativer omfatter **Lever nå** og **Plukket**. Hvis ordrelinjen skal leveres delvis og **Lever nå**-feltet på ordrelinjen som inneholder et antall, velger du **Lever nå**. Hvis organisasjonens fullføringsflyt inkluderer plukking som en egen prosess som administreres av og er registrert i en plukkliste, velger du **Plukket**.  
    - Kontroller at alternativet **Postering** er satt til **Ja**.  
7. Velg **Ja** for alternativet **Skriv ut følgeseddel**. fanen **Oversikt** viser en liste med følgesedler som skal genereres i denne posteringen. Hvis du leverer en enkelt ordre, vil det vanligvis være én følgeseddel. Men hvis den ordrelinjer skal sendes fra forskjellige områder, vil postering automatisk deles inn i det aktuelle antallet dokumenter. Dette er en obligatorisk betingelse som ikke kan endres. På samme måte bokføringen også deles i flere dokumenter hvis ordrens linjer skal leveres til forskjellige leveringsadresser, og policyen for levering settes opp slik at det kreves en deling.  
8. Merk raden for ordrelinjen som skal leveres, i fanen **Linjer**.
9. Angi et tall som er lavere enn det opprinnelige antallet i feltet **Oppdater**.
10. Velg **OK**.
11. Velg **Ja**.
12. Lukk siden.
13. Velg **Alternativer** i handlingsruten.
14. Velg **Endre visning**.
15. Velg **Topptekstvisning**.
    - Hvis alle linjene i ordren er levert, endres ordrestatusen fra Åpen til Levert.  
    - I dette eksemplet er ordrelinjen levert delvis. Dette er grunnen til at ordrestatusen er Åpen.     
    - **Dokumentstatus**-feltet er satt til Følgeseddel, fordi minst én av bestillingslinjene er levert.  
16. Klikk på **Generelt** i handlingsruten.
17. Velg **Linjeantall**.
18. Lukk siden.
19. Klikk på **Plukk og pakk** i handlingsruten.
20. Velg **Følgeseddel**. Siden **Følgeseddeljournal** inneholder alle følgeseddeldokumentene som ble generert for ordren. Du kan se nærmere på detaljene for hvert dokument og skrive dem ut, hvis du ønsker.  

