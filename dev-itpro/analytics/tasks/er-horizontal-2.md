--- 
title: "Kjøre et format som bruker områder som kan utvides vannrett for å legge til kolonner i Excel-rapporter dynamisk for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4b859151edd28e39c1f97b2f600da6e304b1d065
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Kjøre et format som bruker områder som kan utvides vannrett for å legge til kolonner i Excel-rapporter dynamisk for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke vannrett utvidbare områder for legge til kolonner i Excel-rapporter dynamisk (del 1: Utforme format)".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="find-created-format"></a>Søke etter opprettet format
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Eksempelmodell for finansdimensjoner i treet.
3. Velg Eksempelmodell for finansdimensjoner\Eksempelrapport med vannrett utvidbare områder i treet.

## <a name="execute-format-to-create-excel-output"></a>Kjøre format for å opprette Excel-utdata
1. Klikk Kjør.
2. I Dimensjonsnavn-feltet skriver du inn BusinessUnit;CostCenter;Department.
    * Angi eller velg en verdi i feltet Dimensjonsnavn.  Hvis du vil velge alle dimensjoner for gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Utvid delen Poster som skal inkluderes.
4. Klikk Filter.
5. Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.
6. Skriv inn 00057..00058 i Kriterier-feltet.
    * 00057..00058  
7. Klikk OK.
8. Klikk OK.
    * Se gjennom de genererte utdataene. Legg merke til at den nylig opprettede Excel-filen inneholder samme antall kolonner som ble valgt for finansdimensjoner. Rapporthodet i disse kolonnene representerer finansdimensjonenes navn. Linjene til transaksjonene i disse kolonnene representerer finansdimensjoner. Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten av Dynamics 365 for Finance and Operations, Enterprise Edition.  


