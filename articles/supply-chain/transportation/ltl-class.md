---
title: Mindre enn vognlastklasser
description: Dette emnet beskriver hva mindre enn vognlastklasser (LTL) er, og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a6e05ea7534ee081778a899d5956e6ca7cd104cb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678073"
---
# <a name="less-than-truckload-ltl-classes"></a>Mindre enn vognlastklasser

[!include [banner](../includes/banner.md)]

En mindre enn vognlast-klasse (LTL) er en fraktforsendelsesklasse som brukes til å klassifisere varer som kan sendes. Hver type produkt eller vare har vanligvis en NMFC-kode (National Motor Freight Classification) som tilsvarer et bestemt fraktklassenummer for LTL-forsendelser. LTL-fraktklasser representerer varekategorier, mens NMFC-koder er relatert til bestemte varer i hver av de 18 fraktklassene.

Denne funksjonen lar deg bruke systemet til å utføre følgende oppgaver:

- Definer LTL-fraktklassene som brukes i firmaet.
- Tilordne hver LTL-klasse til en NMFC-kode på **NMFC-koder**-siden. Hvis du vil ha mer informasjon, kan du se [NMFC-koder (National Motor Freight)](nmfc-codes.md).
- Tilordne en NMFC-kode (og dermed den tilknyttet LTL-koden) til hvert produkt på **Produkt**-siden.
- En nøyaktig evaluering av LTL-klassen for hvert produkt som en NMFC-kode er tilordnet.
- Fastgjør emballasjekrav for hver LTL-klasse ved å kontrollere de internasjonale LTL-standardene. På denne måten sikrer du at produktene er godt beskyttet og trygt sendt.
- Få nøyaktige forsendelsesestimater, basert på LTL-fraktklassen for hvert produkt.

Dette emnet beskriver hvordan du oppretter LTL-klassene i Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Opprette en LTL-klasse

Hvis du vil opprette en LTL-klasse, følger du disse trinnene.

1. Følg ett av disse trinnene:

    - Gå til **Lagerstyring \> Oppsett \> Lager \> LTL-klasser**.
    - Gå til **Transportstyring \> Oppsett \> Transportstandarder \> LTL-klasser**.

2. I handlingsruten velger du **Ny** for å opprette en LTL-klasse. Deretter angir du følgende felt:

    - **LTL-klasse** – Angi firmaets interne LTL-klasse-ID for varetypen. De fleste firmaer bruker den internasjonale standarden. I så fall vil verdien i dette feltet samsvare med verdien i **Klasse**-feltet. Hvis firmaet imidlertid bruker sin egen standard, angir du en kode som oppfyller denne standarden.
    - **Navn** – Angi et beskrivende navn som vil hjelpe deg og andre brukere med å velge riktig LTL-klasse for hver NMFC-kode.
    - **Klasse** – Angi den internasjonale standard LTL-klasse-IDen for varetypen. Koden du angir her, må oppfylle den offisielle standarden.

## <a name="example-set-up-ltl-classes"></a>Eksempel: Konfigurere LTL-klasser

Følgende eksempel viser hvordan du konfigurerer to ulike LTL-klasser som du kan bruke med forskjellige typer produkter.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> LTL-klasser**.
1. Velg **Ny** i handlingsruten.
1. På den nye linjen angir du følgende verdier:

    - **LTL-klasse:** *92.5*
    - **Navn:** *Datamaskiner, skjermer, kjøleskap*
    - **Klasse:** *92.5*

1. Velg **Lagre** i handlingsruten.
1. Velg **Ny** i handlingsruten.
1. På den nye linjen angir du følgende verdier:

    - **LTL-klasse:** *125*
    - **Navn:** *Små hvitevarer*
    - **Klasse:** *125*

1. Velg **Lagre** i handlingsruten.

## <a name="additional-resources"></a>Tilleggsressurser

- [NMFC-koder (National Motor Freight Classification)](nmfc-codes.md)
- [Opprette et fraktbrev](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
