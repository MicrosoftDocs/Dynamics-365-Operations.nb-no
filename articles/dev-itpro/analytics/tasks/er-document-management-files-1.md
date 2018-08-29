--- 
title: "Klargjøre datamodeller for å bruke dokumentbehandlingsfiler i ER-utdata"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a>Klargjøre datamodeller for å bruke dokumentbehandlingsfiler i ER-utdata

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få tilgang til listen over konfigurasjoner som leveres av Microsoft
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Forsikre deg om at leverandøren Litware, Inc er tilgjengelig og merket som aktiv.  
2. Velg Litware, Inc. som leverandør.
3. Klikk Repositorier.
    * Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.  
4. Klikk Legg til for å åpne nedtrekksdialogen.
5. Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.
6. Klikk Opprett repositorium.
7. Klikk OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Få konfigurasjonene for kundefakturamodell fra Microsoft
1. Klikk Vis filtre.
2. Bruk følgende filtre: Skriv inn en filterverdi for "Operasjonsressurser" i Navn-feltet ved hjelp av filteroperatoren "begynner med". Skriv inn en filterverdi for "" i Beskrivelse-feltet ved hjelp av operatoren "begynner med".
3. Klikk Vis filtre.
4. Klikk Åpne.
5. Velg Kundefakturamodell i treet.
    * Velg modellkonfigurasjonen Kundefakturamodell for å importere den.  
6. Klikk Importer.
    * Klikk Importer for versjon 1 av den valgte konfigurasjonen.  
7. Klikk Ja.
8. Lukk siden.
9. Lukk siden.
10. Klikk Rapporteringskonfigurasjoner.
11. Velg Kundefakturamodell i treet.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Opprett den avledede modellen for å støtte tilgang til dokumentbehandlingsfilene
    * Du vil opprette vår egen konfigurasjon for kundefakturamodellen og avlede den fra konfigurasjonen som leveres av Microsoft. Du vil bruke denne konfigurasjonen til å implementere tilgang til dokumentbehandlingsfilene, og gjøre dem tilgjengelige for elektroniske dokumenter som du vil opprette basert på denne modellen.  
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I Ny-feltet angir du Avled fra navnet: Kundefakturamodell, Microsoft.
3. I Navn-feltet skriver du inn Kundefakturamodell (egendefinert).
    * Kundefakturamodell (egendefinert)  
4. Klikk Opprett konfigurasjon.


