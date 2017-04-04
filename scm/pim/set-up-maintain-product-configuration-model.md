---
title: Konfigurere en produktmodell for konfigurasjon
description: "Denne artikkelen beskriver fremgangsmåten for å sette opp og opprette en produktkonfigurasjonsmodell."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e7138dcc15cb8e16ad5cee83b40ba72555d89e6a
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-product-configuration-model"></a>Konfigurere en produktmodell for konfigurasjon

Denne artikkelen beskriver fremgangsmåten for å sette opp og opprette en produktkonfigurasjonsmodell.

| Oppgave                                                        | beskrivelse                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opprette en produktstandard.                                    | Opprett en produktstandard fra **Produktstandard**-listen. Frigi produktstandarden for alle relevante selskaper. For en produktstandard som brukes som en versjon for en produktmodell for konfigurasjon, eller som en underkomponent **restriksjonsbaserte konfigurasjon** må være valgt i konfigurasjonsteknologi og konfigurasjonsdimensjonen må være valgt for produktdimensjonsgruppen. |
| Opprette komponenter.                                          | Opprett komponenter på **Komponenter**-siden. Komponentene er byggesteinene i en produktkonfigurasjonsmodell og kan brukes på nytt i flere produktkonfigurasjonsmodeller.                                                                                                                                                                                                                      |
| Opprette attributtyper.                                     | Opprett attributtyper på **Attributtyper**-siden. Attributtyper spesifiserer hvilke datatyper for alle attributter som brukes i produktkonfigurasjonsmodeller. Attributtypene **Boolsk**, **Tekst** med en fast liste og **Heltall** med et område angir settet med verdier som er tilgjengelige når du konfigurerer en produktvariant basert på en produktkonfigurasjonsmodell.       |
| Opprette en produktkonfigurasjonsmodell.                       | Opprett en produktkonfigurasjonsmodell på siden **Ny produktkonfigurasjonsmodell**.                                                                                                                                                                                                                                                                                                              |
| Legge til attributter i en produktkonfigurasjonsmodell.            | Opprett et attributt i hurtigkategorien **Attributter** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Attributter beskriver funksjonene til produktkonfigurasjonsmodellen.                                                                                                                                                                                                       |
| Legge til restriksjoner i en produktkonfigurasjonsmodell.           | Opprett begrensninger i hurtigkategorien **Begrensninger** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Begrensninger er restriksjoner som en produktkonfigurasjon må oppfylle. Begrensninger er uttrykksbegrensninger eller tabellbegrensninger.                                                                                                                                 |
| Legge til underkomponenter for produktkonfigurasjonsmodell.         | Opprett underkomponenter i hurtigkategorien **Underkomponenter** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Underkomponenter er knyttet til komponenter og er koblet til varer som representerer underkomponenten.                                                                                                                                                                       |
| Legge til brukerkrav for produktkonfigurasjonsmodell.     | Brukerkrav ligner på underkomponenter, men de refererer ikke til en vare. Du kan se på brukerkrav som en fantomstykkliste. Alle stykklistelinjer eller ruteoperasjoner som plasseres direkte under brukerkravet, blir slått sammen med den overordnede komponenten.                                                                                                                       |
| Legge stykklistelinjer til en produktkonfigurasjonsmodell.             | Opprett stykklistelinjer i hurtigkategorien **Stykklistelinjer** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Stykklistelinjene representerer en del som er nødvendig for å opprette en variant av produktet.                                                                                                                                                                                                 |
| Legge til ruteoperasjoner i en produktkonfigurasjonsmodell.      | Opprett ruteoperasjoner i hurtigkategorien **Ruteoperasjoner** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Ruteoperasjoner representerer et trinn i en trinnrekkefølge som utføres for å lage en variant av produktet.                                                                                                                                                    |
| Opprette en aktiv versjon for en produktkonfigurasjonsmodell. | Opprett en aktiv versjon av produktkonfigurasjonsmodellen på **Versjoner**-siden. En versjon er forholdet mellom en produktkonfigurasjonsmodell og en produktstandard. En produktkonfigurasjonsmodell som har en aktiv versjon kan konfigureres fra en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.                                                               |
| Teste en produktkonfigurasjonsmodell.                         | Test produktkonfigurasjonsmodellen fra siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell** eller **Produktkonfigurasjonsmodeller**. Testing av produktkonfigurasjonsmodellene simulerer produktmodellkonfigurasjonsprosessen som skjer under ordrebehandlingen.                                                                                                |
| Opprette malen produktkonfigurasjonsmodellen.                | Opprett en mal for produktkonfigurasjonsmodellen på siden **Konfigurasjonsmaler**. En konfigurasjonsmal inneholder verdier for attributter i produktkonfigurasjonsmodellen. Velg attributtverdiene på **Konfigurer linje**-siden. Du kan velge å laste inn en mal for produktmodellkonfigurasjon under produktmodellkonfigurasjonen.                                                   |
| Konfigurere en vare.                                          | Produktkonfigurasjonsmodeller kan konfigureres fra en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.                                                                                                                                                                                                                                                                           |




