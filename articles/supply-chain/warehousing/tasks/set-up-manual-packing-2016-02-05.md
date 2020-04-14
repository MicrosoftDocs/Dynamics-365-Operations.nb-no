---
title: Definere manuell pakking (februar 2016 og mai 2016)
description: Pakkeprosessen lar deg validere og pakke produkter i containere.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec4d86673555f594bb2f81010235fd7eb6e83f27
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148291"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a>Definere manuell pakking (februar 2016 og mai 2016)

[!include [banner](../../includes/banner.md)]

Pakkeprosessen lar deg validere og pakke produkter i containere. I denne prosessen plukker lagermedarbeidere varer fra lagerlokasjoner og flytter dem på en pakkestasjon der de kontrollerer vareantall og typer og tilordner dem til riktige containere. Når en container er fullstendig pakket, kan de lukke den og flytte den til utleveringsportene, og produktene er klare til forsendelse. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Denne fremgangsmåten gjelder bare for februar 2016- og mai 2016-versjonen av Dynamics 365 for Operations.


## <a name="set-up-location-profiles"></a>Konfigurer lokasjonsprofiler
1. Gå til Lagerstyring > Oppsett > Lager > Lokasjonsprofiler.
2. Klikk Ny.
    * Lokasjonsprofilen brukes for emballasjestasjoner og inneholder informasjon og regler for en lokasjon.  
3. Skriv inn en verdi i feltet Profil-ID for lokasjon.
4. Skriv inn en verdi i Navn-feltet.
5. Angi eller velg en verdi i feltet Lokasjonsformat.
6. Angi eller velg en verdi i feltet Lokasjonstype.
7. Velg Ja i feltet Tillat kombinerte varer.
8. Velg Ja i feltet Tillat kombinerte lagerstatuser.
9. Velg Ja i feltet Overstyr regler for partidager.
10. Lukk siden.

## <a name="set-up-warehouse-management-parameters"></a>Definere lagerstyringsparametere 
1. Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.
2. Klikk kategorien Pakking.
3. Angi eller velg en verdi i feltet Profil-ID for emballasjelokasjoner.
    * Merk lokasjonsprofilen som du vil bruke til pakking.  
4. Lukk siden.

## <a name="set-up-container-types"></a>Definere containertyper
1. Gå til Lagerstyring > Oppsett > Containere > Containertyper.
2. Klikk Ny.
    * Du kan definere containertypene som skal brukes. Du kan angi de fysiske målene til containeren, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og vekt.  Attributtene er egendefinerte felt som lar deg legge til ekstra dimensjoner for containertypen.     
3. Skriv inn en verdi i feltet Containertype.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi et tall i feltet Taravekt.
6. Angi et tall i feltet Maksimumsvekt.
7. Angi et tall i feltet Volum.
8. Angi et tall i feltet Lengde.
9. Angi et tall i feltet Bredde.
10. Angi et tall i feltet Høyde.
11. Klikk Lagre.
12. Lukk siden.

## <a name="set-up-packing-profiles"></a>Definere pakkeprofiler
1. Gå til Lagerstyring > Oppsett > Pakking > Pakkeprofiler.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Pakkeprofil-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi eller velg en verdi i feltet Containerlukkingsprofil.
    * En ID for containerlukkingsprofil er valgfri, og er standard containerlukkingsprofil for denne emballasjeprofilen.  
6. Velg et alternativ i feltet Modus for container-ID.
    * Dette alternativet avgjør om en container-ID genereres automatisk når det opprettes en container eller hvis en container-ID opprettes manuelt.  
7. Angi eller velg en verdi i feltet Containertype.
    * Containertypen brukes som standard når det opprettes en ny container.  
8. Merk av for Opprett container automatisk ved containerlukking.
9. Klikk Lagre.
10. Lukk siden.

## <a name="set-up-container-closing-profiles"></a>Definere containerlukkingsprofiler
1. Gå til Lagerstyring > Oppsett > Containere > Containerlukkingsprofiler.
    * Containerlukkingsprofil definerer hva som skjer når en container lukkes. Du kan definere flere containerlukkingsprofiler.       
2. Klikk Ny.
3. Angi en verdi i feltet Containerlukkingsprofil-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg et alternativ i feltet Manifest den.
    * Angi om manifestering skal skje når du containere lukkes eller ved bekreftelse av forsendelsen. Legg merke til at manifestering krever transportstyring. Manifestering må implementeres i transportmotorer for at det skal fungere.  
6. Angi eller velg en verdi i feltet Lager.
7. Angi eller velg en verdi i feltet Standardlokasjon for endelig forsendelse.
    * Dette blir lokasjonen der produkter flyttes til når containere lukkes. Denne lokasjonen må ha en lokasjonsprofil som er definert for lagerparametere.  
8. Angi eller velg en verdi i feltet Vektenhet.
9. Klikk Lagre.

