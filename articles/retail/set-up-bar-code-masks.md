---
title: Definere strekkodemasker
description: Dette emnet beskriver hvordan du definerer tegn for strekkodemaske, strekkodemasker og hvordan du kan tilordne strekkodemasker til strekkoder.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e61524feab1b06f4a863a140b883bf8fe49af1e2
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bar-code-masks"></a>Definere strekkodemasker

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer tegn for strekkodemaske, strekkodemasker og hvordan du kan tilordne strekkodemasker til strekkoder.

<a name="set-up-bar-code-mask-characters"></a>Definere tegn for strekkodemaske
-------------------------------

Strekkodemasker brukes til å opprette strekkoder og raskt identifisere strekkoder som skannes inn på salgsstedet (POS). Masker består av tegn som fungerer som plassholdere som angir formatet for strekkodene som blir opprettet. Hvis du vil konfigurere en strekkodemaske, må du definere tegn for strekkodemasken. Gå til **Detaljhandel** &gt; **Lagerstyring** &gt; **Strekkoder og etiketter** &gt; **Masketegn**. Klikk på **Ny** for å opprette tegn for strekkodemaske. Masketegn kan opprettes for å angi strekkodedataene nedenfor.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Felt**            | **Beskrivelse**                                                                                                 |
| **Produkt**          | Plassholder for produkt-ID.                                                                                     |
| **Tall**       | Brukes til å angi et tall som vil være hardkodet i strekkoder.                                                  |
| **Kontrollsiffer**      | Angir at strekkodeformatet i en strekkodemaske bruker et kontrollsiffer for å bekrefte gyldigheten av en strekkode. |
| **Størrelsessiffer**       | Angir størrelsen i en strekkode som er opprettet for et produktvariant som inkluderer størrelse.                                 |
| **Fargesiffer**      | Angir fargen i en strekkode som er opprettet for et produktvariant som inkluderer farge.                               |
| **Stilsiffer**      | Angir stilen i en strekkode som er opprettet for et produktvariant som inkluderer en stil.                             |
| **EAN-lisenskode** | Plassholder for EAN-lisens som er utstedt for EAN lisenskoder.                                                       |
| **Pris**            | Angir pris for strekkoder med innebygd pris.                                                                   |
| **Antall**         | Angir antallet i strekkoder med innebygd antall / tilfeldig vekt.                                                |
| **Ansatt**         | Angir strekkodesegmentet for ansatt-ID-nummeret som brukes for strekkodepålogging på salgsstedet.                                  |
| **Kunde**         | Viser kunde-ID-segment.                                                                                  |
| **Dataoppføring**       | *Ikke implementert ennå.*                                                                                          |
| **Rabattkode**    | *Avskrevet* per vår 2017-versjonen av 365 Dynamics for Retail. Tidligere: Angir rabattkoden for en strekkode som brukes til å legge til en rabatt i en transaksjon på salgsstedet.                                                                   |
| **Kupongkode**      | Angir kupongkoden for en strekkode som brukes til å legge til en rabatt i en detaljhandelsordre. Dette erstattet rabattkoden.     |
| **Gavekort**        | Angir et gavekortnummer ved utstedelse av eller betaling med gavekort.                                               |
| **Fordelskort**     | Legger til en fordelskunde i transaksjonen, og kan brukes ved betaling av fordel.                             |

## <a name="define-bar-code-masks"></a>Definere strekkodemasker
Når tegn for strekkodemaske er angitt for de nødvendige strekkodemaskene, går du til **Detaljhandel** &gt; **Lagerstyring** &gt; **Strekkoder og etiketter** &gt; **Oppsett for strekkodemaske**. På denne siden kan du definere strekkodemasker som bruker de tidligere angitte tegnene. Disse strekkodemaskene brukes ved generering av strekkoder, og vil også bidra til å identifisere strekkoder som skannes på salgsstedet.

1.  Klikk på **Ny** for å opprette en ny strekkodemaske.
2.  Angi verdier i feltene **Maske-ID** og **Beskrivelse**, og velg deretter en type for strekkodemaske i **Type**-feltet.
3.  I **Generelt**-delen velger du en verdi i feltet **Strekkodestandard**, og deretter angi du strekkodeprefikset etter behov.
4.  I delen **Segment for strekkodemaske** legger du til strekkodesegmentene som skal brukes i strekkoden som skal opprettes.

Eksempel: Hvis du vil opprette en strekkodemaske med maske-ID Produkt, gjør du følgende:

1.  Opprett en ny strekkodemaske, og velg typen Produkt.
2.  Velg en strekkodestandard, for eksempel Code 39.
3.  Angi prefikset som skal brukes til å identifisere strekkoden på en enkel måte. For eksempel 22.
4.  Legg til et maskesegment. Produkt-maskesegmentet blir valgt.
5.  Angi en lengde for produktsegmentet, for eksempel 10. Lengden må samsvare med lengden på en produkt-ID som vanligvis brukes i butikken. Masken vises som en forhåndsvisning i **Generelt**-delen under **Maske**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Tilordne strekkodemasker til strekkoder
Strekkodemasker må tilordnes til strekkoder før de kan brukes. Vi fortsetter med det forrige eksemplet, og gjør følgende for å tilordne strekkodemasken til en strekkode:

1.  Gå til **Organisasjonsstyring** &gt; **Oppsett** &gt; **Strekkoder**. Klikk på **Ny** for å opprette en ny strekkode.
2.  Angi verdier i feltet **Strekkodeoppsett** og **Oppsett**.
3.  I **Generelt**-delen i feltet **Strekkodetype** velger du Code 39. I **Maske-****ID**-feltet velger du Produkt-masken du opprettet tidligere.
4.  Under **Størrelse** skriver du inn 12.
5.  Klikk **Lagre**.

Strekkodemasken kan nå brukes til å opprette strekkoder for produkter. Fremgangsmåten ovenfor et eksempel på hvordan du oppretter strekkodemasker for produkter, men illustrerer også hvordan du oppretter strekkodemasker for alle strekkodetyper som støttes. Strekkodemasker-, typer og -lengder må justeres for bruk i ditt spesifikke miljø.




