---
title: Definere en produktkonfigurasjonsmodell
description: Denne artikkelen beskriver fremgangsmåten for å sette opp og opprette en produktkonfigurasjonsmodell.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a0adc1f553c8f92c62310c28478407fb53ee98915999f10c0fa4f42e00995f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714914"
---
# <a name="set-up-a-product-configuration-model"></a>Definere en produktkonfigurasjonsmodell

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten for å sette opp og opprette en produktkonfigurasjonsmodell.

| Oppgave                                                        | beskrivelse                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opprette en produktstandard.                                    | Opprett en produktstandard fra **Produktstandard**-listen. Frigi produktstandarden for alle relevante selskaper. For en produktstandard som brukes som en versjon for en produktkonfigurasjonsmodell eller som en underkomponent, må **Restriksjonsbasert konfigurasjon** velges som konfigurasjonsteknologi og konfigurasjonsdimensjonen må bare velges for produktdimensjonsgruppen. |
| Opprette komponenter.                                          | Opprett komponenter på **Komponenter**-siden. Komponentene er byggesteinene i en produktkonfigurasjonsmodell og kan brukes på nytt i flere produktkonfigurasjonsmodeller.                                                                                                                                                                                                                      |
| Opprette attributtyper.                                     | Opprett attributtyper på **Attributtyper**-siden. Attributtyper spesifiserer hvilke datatyper for alle attributter som brukes i produktkonfigurasjonsmodeller. Attributtypene **Boolsk**, **Tekst** med en fast liste og **Heltall** med et område angir settet med verdier som er tilgjengelige når du konfigurerer en produktvariant basert på en produktkonfigurasjonsmodell.       |
| Opprette en produktkonfigurasjonsmodell.                       | Opprett en produktkonfigurasjonsmodell på siden **Ny produktkonfigurasjonsmodell**.                                                                                                                                                                                                                                                                                                              |
| Legge til attributter i en produktkonfigurasjonsmodell.            | Opprett et attributt i hurtigfanen **Attributter** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Attributter beskriver funksjonene til produktkonfigurasjonsmodellen.                                                                                                                                                                                                       |
| Legge til restriksjoner i en produktkonfigurasjonsmodell.           | Opprett begrensninger i hurtigfanen **Begrensninger** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Begrensninger er restriksjoner som en produktkonfigurasjon må oppfylle. Begrensninger er uttrykksbegrensninger eller tabellbegrensninger.                                                                                                                                 |
| Legge til underkomponenter for produktkonfigurasjonsmodell.         | Opprett underkomponenter i hurtigfanen **Underkomponenter** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Underkomponenter er knyttet til komponenter og er koblet til varer som representerer underkomponenten.                                                                                                                                                                       |
| Legge til brukerkrav for produktkonfigurasjonsmodell.     | Brukerkrav ligner på underkomponenter, men de refererer ikke til en vare. Du kan se på brukerkrav som en fantomstykkliste. Alle stykklistelinjer eller ruteoperasjoner som plasseres direkte under brukerkravet, blir slått sammen med den overordnede komponenten.                                                                                                                       |
| Legge stykklistelinjer til en produktkonfigurasjonsmodell.             | Opprett stykklistelinjer i hurtigfanen **Stykklistelinjer** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Stykklistelinjene representerer en del som er nødvendig for å opprette en variant av produktet.                                                                                                                                                                                                 |
| Legge til ruteoperasjoner i en produktkonfigurasjonsmodell.      | Opprett ruteoperasjoner i hurtigfanen **Ruteoperasjoner** på siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell**. Ruteoperasjoner representerer et trinn i en trinnrekkefølge som utføres for å lage en variant av produktet.                                                                                                                                                    |
| Opprette en aktiv versjon for en produktkonfigurasjonsmodell. | Opprett en aktiv versjon av produktkonfigurasjonsmodellen på **Versjoner**-siden. En versjon er forholdet mellom en produktkonfigurasjonsmodell og en produktstandard. En produktkonfigurasjonsmodell som har en aktiv versjon kan konfigureres fra en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.                                                               |
| Teste en produktkonfigurasjonsmodell.                         | Test produktkonfigurasjonsmodellen fra siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell** eller **Produktkonfigurasjonsmodeller**. Testing av produktkonfigurasjonsmodellene simulerer produktmodellkonfigurasjonsprosessen som skjer under ordrebehandlingen.                                                                                                |
| Opprette malen produktkonfigurasjonsmodellen.                | Opprett en mal for produktkonfigurasjonsmodellen på siden **Konfigurasjonsmaler**. En konfigurasjonsmal inneholder verdier for attributter i produktkonfigurasjonsmodellen. Velg attributtverdiene på **Konfigurer linje**-siden. Du kan velge å laste inn en mal for produktmodellkonfigurasjon under produktmodellkonfigurasjonen.                                                   |
| Konfigurere en vare.                                          | Produktkonfigurasjonsmodeller kan konfigureres fra en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre.                                                                                                                                                                                                                                                                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]