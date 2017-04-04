---
title: Definere strekkodemasker
description: Dette emnet beskriver hvordan du definerer strekkoden masketegn, strekkodemasker, og hvordan du kan tilordne strekkode maskerer til strekkoder.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Definere strekkodemasker

Dette emnet beskriver hvordan du definerer strekkoden masketegn, strekkodemasker, og hvordan du kan tilordne strekkode maskerer til strekkoder.

<a name="set-up-bar-code-mask-characters"></a>Definere tegn for strekkodemaske
-------------------------------

Strekkodemasker brukes til å opprette strekkoder og raskt identifisere strekkoder som er skannet inn i punkt for salg (POS). Masker består av tegn som fungerer som plassholdere som angir formatet for strekkoder som blir opprettet. Hvis du vil konfigurere en strekkodemaske, må du definere tegn for strekkodemaske. Gå til **Retail og commerce**&gt;**Inventory management**&gt;**strekkoder og etiketter**&gt;**maskere tegn**. Klikk **ny** til å opprette tegn for strekkodemaske. Masketegn kan opprettes for å angi følgende strekkodedata.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Plassholder for produkt-IDen.                                                                                     |
| **Any number**       | Brukes til å angi et tall som vil være vanskelig kodet i strekkoder.                                                  |
| **Check digit**      | Angir at formatet for strekkode i en strekkodemaske bruker et kontrollsiffer for å bekrefte gyldigheten av en strekkode. |
| **Size digit**       | Angir størrelsen i en strekkode som er opprettet for et produktvariant som inkluderer størrelse.                                 |
| **Color digit**      | Angir farge i en strekkode som er opprettet for et produktvariant som inkluderer.                               |
| **Style digit**      | Angir stilen i en strekkode som er opprettet for et produktvariant som inneholder en stil.                             |
| **EAN license code** | Plassholder for EAN-lisens som er utstedt for EAN lisenskoder.                                                       |
| **Pris**            | Angir pris pris innebygde strekkoder.                                                                   |
| **Quantity**         | Angir antallet i antall/tilfeldig vekt innebygd strekkoder.                                                |
| **Employee**         | Angir segmentet for strekkode for ansatt-IDen som brukes for strekkode POS-pålogging.                                  |
| **Customer**         | Viser kunde-ID-segment.                                                                                  |
| **Dataregistrering**       | *Ikke implementert ennå.*                                                                                          |
| **Discount code**    | Angir rabattkode for en strekkode som brukes til å legge til en rabatt til et punkt av salgstransaksjon             |
| **Gavekort**        | Angir en gavekortnummer når utsteder eller betale med gavekort.                                               |
| **Loyalty card**     | Legger til en fordelskunde i transaksjonen, og kan brukes ved betaling av lojalitet.                             |

## <a name="define-bar-code-masks"></a>Definere strekkodemasker
Når tegn for strekkodemaske er angitt for de nødvendige strekkodemasker, gå til **Retail og commerce**&gt;**Lagerstyring**&gt;**strekkoder og etiketter**&gt;**strekkodeoppsettet maske**. Du kan definere strekkodemasker som bruker tidligere angitte tegnene på denne siden. Disse strekkode masker som skal brukes ved generering av strekkoder, og vil også bidra til å identifisere strekkoder som er skannet på Salgsstedet.

1.  Klikk **ny** til å opprette en ny strekkodemaske.
2.  Angi verdier i de **maske-ID** og **beskrivelse** felt, og velg deretter en maske for strekkodetype den **Type** feltet.
3.  I den **Generelt** velger en verdi i den **standard strekkode** -feltet, og angi deretter strekkode-prefiks, om nødvendig.
4.  I den **segment for strekkodemaske** -delen, legge til strekkode-segmentene som skal brukes i strekkoden skal opprettes.

Som et eksempel for å opprette en strekkodemaske med maske-ID for produktet, gjør du følgende:

1.  Opprette en ny strekkodemaske, og velg 'Produkt'.
2.  Velg strekkodetypen som standard, for eksempel 'kode 39".
3.  Angi prefikset som skal brukes til å identifisere strekkoden. For eksempel "22".
4.  Legge til et segment i masken. 'Produkt' maske segmentet blir valgt.
5.  Angi en lengde for produkt-segmentet, for eksempel 10. Lengden må samsvare med lengden på en produkt-ID som vanligvis brukes i butikken. Masken vises som en forhåndsvisning i den **Generelt** -delen **maske**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Tilordne strekkodemasker til strekkoder
Strekkodemasker må være tilordnet strekkoder før de kan brukes. Fortsetter med det forrige eksemplet, til masken strekkoden tilordnes en strekkode, kan du gjøre følgende:

1.  Gå til **organisasjonsadministrasjon**&gt;**Setup**&gt;**strekkoder**. Klikk **ny** til å opprette en ny strekkode.
2.  Angi verdier i de **strekkode****setup** og ** installasjonsprogrammet ** felt.
3.  I den **Generelt** -delen i den **strekkodetype** velger "Kode 39". I den **maske****ID** velger 'Produkt' masken som er opprettet tidligere.
4.  Under **størrelse**, skriver du inn '12'.
5.  Click **Save**.

Strekkodemasken kan nå brukes til å opprette strekkoder for produkter. Trinnene ovenfor er eksempler på hvordan du oppretter strekkodemasker for produkter, men de også illustrerer hvordan du oppretter strekkodemasker for noen av de andre støttede strekkode. Strekkodemasker, typer og lengder skal justeres for bruk i ditt spesifikke miljø.


