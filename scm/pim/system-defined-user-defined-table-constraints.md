---
title: Systemdefinerte og brukerdefinerte tabellbegrensninger
description: 'Denne artikkelen forklarer de to typene tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell: brukerdefinert og systemdefinert. Tabellbegrensninger representerer matriser for tillatte attributtkombinasjoner, der hver enkelt rad definerer et sett med mulige attributtverdier.'
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 0393c52c9128eb975c26b67323046a289872c4b0
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="system-defined-and-user-defined-table-constraints"></a>Systemdefinerte og brukerdefinerte tabellbegrensninger

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer de to typene tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell: brukerdefinert og systemdefinert. Tabellbegrensninger representerer matriser for tillatte attributtkombinasjoner, der hver enkelt rad definerer et sett med mulige attributtverdier.

Tabellbegrensninger representerer matriser av kombinasjoner av attributter som er tillatt for komponenter i en produktkonfigurasjonsmodell. Hver rad i tabellen definerer et sett med mulige attributtverdier. Du kan angi to typer begrensninger i en produktkonfigurasjonsmodell:

-   **Uttrykksrestriksjon** – Opprett et uttrykk som definerer relasjoner mellom attributter for å garantere at bare kompatible verdier kan velges under produktkonfigurasjon.
-   **Tabellbegrensning** – Opprett en tabell som definerer alle kombinasjonene som er tillatt for et angitt sett med attributter. Det finnes to typer tabellbegrensninger: brukerdefinerte tabellbegrensninger og systemdefinerte tabellbegrensninger.

Denne artikkelen beskriver brukerdefinerte og systemdefinerte tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell.

## <a name="user-defined-table-constraints"></a>Brukerdefinerte tabellbegrensninger
En brukerdefinert tabellbegrensning er en matrisetype som brukes til å beskrive kombinasjonene av attributtverdier som er angitt av attributtyper. Hvis du produserer høyttalere, kan du for eksempel inkludere søyler for kabinettypen og frontgrillen i den brukerdefinerte tabellbegrensningen. Attributtypen for kabinettype har fire verdier, og attributtypen for frontgrill har tre verdier. Hvis begrensninger ikke er brukt, er det derfor 4 x 3 = 12 mulige kombinasjoner. I dette eksemplet er imidlertid bare seks kombinasjoner tillatt, som vist i følgende tabell. Denne informasjonen vises i kategorien **Tillatte kombinasjoner** på siden **Rediger tabellbegrensning**.

| Kabinettyper | Frontgrill |
|----------------|-------------|
| Svart          | Svart       |
| Svart          | Metall       |
| Eik            | Svart       |
| Rosewood       | Hvit       |
| Hvit          | Svart       |
| Hvit          | Hvit       |

Brukerdefinerte tabellbegrensninger defineres av statiske tabellinndata som fungerer på samme måte som en uttrykksrestriksjon. Når du bruker en brukerdefinert tabellbegrensning, er fordelen at tabeller ofte er enklere å opprette, forstå og vedlikeholde enn lange uttrykksrestriksjoner.

## <a name="system-defined-table-constraints"></a>Systemdefinerte tabellbegrensninger
En systemdefinert tabellbegrensning oppretter en dynamisk tilordning mellom en attributtype og et felt i en tabell. Når en systemdefinert tabellbegrensning er inkludert i en produktkonfigurasjonsmodell, garanterer tilordningen at dataene i tabellen vises i stedet for verdiene for attributtypen. Resultatet er en dynamisk betingelse, fordi tabellinnholdet kan endres (for eksempel av andre moduler).  

Når du oppretter en systemdefinert tabellbegrensning, velger du en tabell, definerer eventuelt spørringen som skal brukes, og knytter deretter attributtyper til feltene i den valgte tabellen. Felttypene må samsvare med typene attributtyper.  

Før en tabellbegrensning kan tre i kraft i en produktkonfigurasjonsmodell, må tabellbegrensningen inkluderes i en betingelse på en av komponentene for modellen. Fremgangsmåten er å opprette en ny begrensning, velge tabellbegrensningstypen og deretter velge definisjonen av tabellbegrensning som skal brukes. Til slutt må alle felt i tabellbegrensningen tilordnes til attributter i produktkonfigurasjonsmodellen.

<a name="see-also"></a>Se også
--------

[Nøkkelbegreper i produktkonfigurasjonsmodeller](product-configuration-models.md)




