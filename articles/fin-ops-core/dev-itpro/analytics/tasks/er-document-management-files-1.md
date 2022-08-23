---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 1 - Klargjøre datamodell)
description: Dette artikkelen beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 1)
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
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog
ms.openlocfilehash: f407555eca4c4bd08d09047e9d8f8512cb99d254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291032"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER Bruke dokumentbehandlingsfiler i formatutdata (del 1 - Klargjøre datamodell)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få tilgang til listen over konfigurasjoner som leveres av Microsoft
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.

    Forsikre deg om at leverandøren Litware, Inc er tilgjengelig og merket som aktiv.  

2. Velg Litware, Inc. som leverandør.
3. Klikk på Repositorier.

    Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.  

4. Klikk på Legg til for å åpne nedtrekksdialogen.
5. Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.
6. Klikk på Opprett repositorium.
7. Klikk på OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Få konfigurasjonene for kundefakturamodell fra Microsoft
1. Klikk på Vis filtre.
2. Bruk følgende filtre: Skriv inn en filterverdi for "Operasjonsressurser" i Navn-feltet ved hjelp av filteroperatoren "begynner med". Skriv inn en filterverdi for "" i Beskrivelse-feltet ved hjelp av operatoren "begynner med".
3. Klikk på Vis filtre.
4. Klikk på Åpne.
5. Velg Kundefakturamodell i treet.

    Velg modellkonfigurasjonen Kundefakturamodell for å importere den.  

6. Klikk på Importer.

    Klikk på Importer for versjon 1 av den valgte konfigurasjonen.  

7. Klikk på Ja.
8. Lukk siden.
9. Lukk siden.
10. Klikk på Rapporteringskonfigurasjoner.
11. Velg Kundefakturamodell i treet.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Opprett den avledede modellen for å støtte tilgang til dokumentbehandlingsfilene
Du vil opprette vår egen konfigurasjon for kundefakturamodellen og avlede den fra konfigurasjonen som leveres av Microsoft. Du vil bruke denne konfigurasjonen til å implementere tilgang til dokumentbehandlingsfilene, og gjøre dem tilgjengelige for elektroniske dokumenter som du vil opprette basert på denne modellen.  
1. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I Ny-feltet angir du Avled fra navnet: Kundefakturamodell, Microsoft.
3. I Navn-feltet skriver du inn Kundefakturamodell (egendefinert).
4. Klikk på Opprett konfigurasjon.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
