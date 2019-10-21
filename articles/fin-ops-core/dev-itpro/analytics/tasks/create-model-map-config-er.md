---
title: Opprette konfigurasjoner av modelltilordning for elektronisk rapportering (ER)
description: Bruk denne fremgangsmåten for å utforme en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruke innebygde ER-funksjoner for effektive aggregerte beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcfc258e7fe364779fd77cc79413e8d5e871e214
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182698"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Opprette konfigurasjoner av modelltilordning for elektronisk rapportering (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten for å utforme en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruke innebygde ER-funksjoner for effektive aggregerte beregninger. I denne prosedyren skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. 

Denne fremgangsmåten er opprettet for bruk med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.

Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv."

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
2. Klikk Rapporteringskonfigurasjoner.
3. Klikk Vis filtre.
4. Angi filterverdien "Intrastat" i Navn-feltet og bruk filteroperatoren "begynner med".
    * Bruk dette filteret hvis du vil finne konfigurasjon av Intrastat-datamodellen. Denne modellen finnes kanskje allerede i konfigurasjonstreet. Hvis den finnes, kan du hoppe over neste underoppgave.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Få Intrastat-modellkonfigurasjonen som leveres av Microsoft
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
4. Finn og velg ønsket post i listen.
    * Velg flisen Microsoft-leverandør.  
5. Klikk Repositorier.
    * Klikk på Repositorier i Microsoft-leverandørflisen.  
6. Klikk Vis filtre.
7. Angi filterverdien "ressurser" i Typenavn-feltet og bruk filteroperatoren "inneholder". 
8. Klikk Åpne.
9. Velg 'Intrastat-modell' i treet.
10. Klikk Importer.
11. Klikk Ja.
    * Du har importert ER-modellkonfigurasjonen som inneholder datamodellen som du vil bruke til å undersøke hvordan den nye ER-funksjonen kan brukes.  
12. Lukk siden.
13. Lukk siden.
14. Klikk Rapporteringskonfigurasjoner.

## <a name="add-a-new-model-mapping-configuration"></a>Legg til en ny modelltilordningskonfigurasjon
1. Velg 'Intrastat-modell' i treet.
2. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Modelltilordning basert på datamodell Intrastat.
4. Skriv inn Eksempeltilordning for Intrastat i Navn-feltet.
    * Eksempeltilordning for Intrastat  
5. Klikk Opprett konfigurasjon.
