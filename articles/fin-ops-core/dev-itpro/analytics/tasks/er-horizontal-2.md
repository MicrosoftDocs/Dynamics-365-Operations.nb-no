---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)
description: Denne artikkelen beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som OPENXML-regnearkfiler (Excel). (Del 2)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, SysQueryForm
ms.openlocfilehash: 08755eafa2a18993ba669f0deccd75477bfae410
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290402"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke vannrett utvidbare områder for legge til kolonner i Excel-rapporter dynamisk (del 1: Utforme format)".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="find-created-format"></a>Søke etter opprettet format
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Eksempelmodell for finansdimensjoner i treet.
3. Velg Eksempelmodell for finansdimensjoner\Eksempelrapport med vannrett utvidbare områder i treet.

## <a name="execute-format-to-create-excel-output"></a>Kjøre format for å opprette Excel-utdata
1. Klikk på Kjør.
2. I Dimensjonsnavn-feltet skriver du inn BusinessUnit;CostCenter;Department.
    * Angi eller velg en verdi i feltet Dimensjonsnavn.  Hvis du vil velge alle dimensjoner for gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Utvid delen Poster som skal inkluderes.
4. Klikk på Filter.
5. Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.
6. Skriv inn 00057..00058 i Kriterier-feltet.
    * 00057..00058  
7. Klikk på OK.
8. Klikk på OK.
    * Se gjennom de genererte utdataene. Legg merke til at den nylig opprettede Excel-filen inneholder samme antall kolonner som ble valgt for finansdimensjoner. Rapporthodet i disse kolonnene representerer finansdimensjonenes navn. Linjene til transaksjonene i disse kolonnene representerer finansdimensjoner. Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
