---
title: "Justere lagernivåer i lageret (grunnleggende lageraktiviteter)"
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: f96db79bcb6ec26daaeb66d29edb18486daafab0
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# Justere lagernivåer i lageret (grunnleggende lageraktiviteter)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret. Du må ha en lagerjournalnavn definert for lagerjusteringer før du starter dette. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Disse oppgavene vil vanligvis utføres av en lageransatt.


## Opprette en beholdningsjusteringsjournal
1. Gå til Lagerstyring > Journaloppføringer > Varer > Beholdningsjustering.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Klikk journalnavnet for beholdningsjustering som du vil bruke, i listen.
    * Noen andre felt fylles ut basert på oppsettet av navnet på lagerjusteringsjournal som du velger.  
5. Klikk OK.

## Opprette journallinjer
1. Klikk Ny.
2. Merk varenummerfeltet i listen.
3. Velg en vare i Varenummer-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, skriver du inn "D0001".
4. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
5. Velg et område i listen.
6. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
7. Velg et lager i listen.
    * Hvis du har valgt en vare med Lokasjon som en obligatorisk dimensjon, må du angi lokasjonen her.  
8. Angi et tall i feltet Antall.
    * Kostprisfeltet angir kostnaden per enhet for lagertilganger. Hvis kostnaden ikke er angitt for varenummeret, eller hvis du vil endre den manuelt, gjør du det her.  

## Validere og postere beholdningsjusteringsjournalen
1. Klikk Valider.
2. Klikk OK.
3. Klikk Poster.
    * Når du posterer denne typen journal, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.  
4. Klikk OK.
5. Lukk skjemaet.
6. Lukk siden.
