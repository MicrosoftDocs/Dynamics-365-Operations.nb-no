---
title: ER Importere en konfigurasjon fra Lifecycle Services
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan importere en ny versjon av etnformatkonfigurasjon for elektronisk rapportering (ER) fra Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142392"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER Importere en konfigurasjon fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan importere en ny versjon av etnformatkonfigurasjon for elektronisk rapportering (ER) fra Microsoft Lifecycle Services (LCS).

I dette eksemplet skal du velge ønsket versjon av ER-konfigurasjonen og importere den for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom firmaer. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Laste opp en ER-konfigurasjon til Lifecycle Services". Tilgang til LCS kreves også for fullføring av denne fremgangsmåten.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Konfigurasjoner.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Slette en delt versjon av datamodellkonfigurasjon
1. Velg Eksempelmodellkonfigurasjon i treet.
    * Den første versjonen av en konfigurasjon for eksempeldatamodell er opprettet og publisert på LCS under prosedyren "Laste opp en ER-konfigurasjon til Lifecycle Services". I denne fremgangsmåten sletter du denne versjonen av ER-konfigurasjonen. Denne versjonen av en konfigurasjon for eksempel data vil senere bli importert fra LCS.  
2. Finn og velg ønsket post i listen.
    * Velg versjonen av denne konfigurasjonen som har statusen Delt. Denne statusen angir at konfigurasjonen er publisert til LCS.  
3. Klikk Endre status.
4. Klikk Avslutt.
    * Endre statusen for den valgte versjonen fra Delt til Utgått for å gjøre den tilgjengelig for sletting.  
5. Klikk OK.
6. Finn og velg ønsket post i listen.
    * Velg versjonen av denne konfigurasjonen som har statusen Utgått.  
7. Klikk Slett.
8. Klikk Ja.
    * Legg merke til at bare utkastversjon 2 av den valgte datamodellkonfigurasjonen er tilgjengelig.  
9. Lukk siden.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Importere en delt versjon av datamodellkonfigurasjon fra LCS
1. Merk den valgte raden i listen.
    * Åpne listen over repositorier for Litware, Inc.- -konfigurasjonsleverandøren.  
2. Klikk Repositorier.
3. Klikk Åpne.
    * Velg LCS-repositorium, og åpne det.  
4. Merk den valgte raden i listen.
    * Velg den første versjonen av eksempelmodellkonfigurasjonen i versjonslisten.  
5. Klikk Importer.
6. Klikk Ja.
    * Bekreft importen av den valgte versjonen fra LCS.  
    * Legg merke til at Informasjonsmeldingen (over skjemaet) bekrefter fullføring av importen av den valgte versjonen.  
7. Lukk siden.
8. Lukk siden.
9. Klikk Konfigurasjoner.
10. Velg Eksempelmodellkonfigurasjon i treet.
11. Finn og velg ønsket post i listen.
    * Velg versjonen av denne konfigurasjonen som har statusen Delt.  
    * Legg merke til at den delte versjon 1 av den valgte datamodellkonfigurasjonen nå også er tilgjengelig.  

