---
title: ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat som teller og summerer basert på data fra tekstutdataene som allerede er generert. (Del 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749051"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få tilgang til listen over konfigurasjoner som leveres av Microsoft
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Forsikre deg om at leverandøren Litware, Inc er tilgjengelig og merket som aktiv.  
2. Velg Litware, Inc. som leverandør.
3. Klikk på Repositorier.
    * Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.  
4. Klikk på Legg til for å åpne nedtrekksdialogen.
5. Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.
6. Klikk på Opprett repositorium.
7. Klikk på OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Få Intrastat-konfigurasjoner som leveres av Microsoft
1. Klikk på Åpne.
2. Velg Intrastat-modell\Intrastat (DE) i treet.
3. Klikk på Importer.
    * Klikk på Importer for versjon 1.1 av den valgte konfigurasjonen.  
4. Klikk på Ja.
5. Lukk siden.
6. Lukk siden.
7. Klikk på Rapporteringskonfigurasjoner.
8. Utvid Intrastat-modell i treet.
9. Velg Intrastat-modell\Intrastat (DE) i treet.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]