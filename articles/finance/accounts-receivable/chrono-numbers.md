---
title: Nummerere dokumenter og bilag kronologisk
description: Denne artikkelen beskriver hvordan du definerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.custom: 401195
ms.search.form: NumberSequenceGroup
ms.openlocfilehash: 1a1b8887eff625d9e4095380fbb7c8963682ef3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272436"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Nummerere dokumenter og bilag kronologisk

[!include [banner](../includes/banner.md)]


I noen land er det et juridisk krav om å nummerere dokumenter og tilknyttede bilag i kronologisk rekkefølge. Kronologien må støttes av perioder. Alle numrene som tilhører tidligere perioder, må være mindre enn numrene som tilhører senere perioder. For å oppfylle dette kravet er kronologisk nummereringsfunksjonalitet implementert. Denne artikkelen beskriver hvordan du konfigurerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.

## <a name="prerequisites"></a>Forutsetninger

I Funksjonsbehandling-arbeidsområdet slår du på funksjonen **Kronologisk nummerering**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Konfigurere kronologisk nummerering

Kronologisk nummerering påvirker følgende dokumenter.

**Kunde**
- Kundefaktura
- Kundefakturabilag
- Salgskreditnota
- Bilag for salgskreditnota
- Fritekstfaktura
- Fritekstfakturabilag
- Fritekstkreditnota
- Kreditnotabilag i fritekst
- Følgeseddel
- Følgeseddelbilag
- Korrigeringsbilag for følgeseddel
- Rentenotabilag
- Purringsbilag

**Leverandører**
- Fakturabilag
- Kreditnotabilag
- Mottaksseddelbilag

**Prosjektstyring**
- Faktura
- Fakturabilag
- Kreditnota
- Kreditnotabilag 

### <a name="define-number-sequences"></a>Definere nummerserier

Hvis du vil definere nummerserier, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Nummerserier**. Du kan definere så mange nummerserier som du trenger for å dekke de berørte periodene for nødvendige dokumenter. 

Angi et selskap for hver nummerserie. Segmentene i nummerseriene må defineres slik at de gir kronologisk rekkefølge for perioder. Segmentnavnene kan for eksempel inneholde et spesielt prefiks som identifiserer en bestemt periode.

![Oppsett av nummerserier.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Konfigurere nummerseriegrupper

Hvis du vil konfigurere nummerseriegrupper, kan du gå til **Kunde** > **Oppsett** > **Kundeparametere**. I kategorien **Nummerserier** definerer du så mange nummerseriegrupper som nødvendig for å dekke de berørte periodene. 

For hver gruppe i **Referanse**-delen velger du en av dokumentreferansene som støttes, og i **Nummerseriekode**-feltet kan du se en nummerserie som ble opprettet tidligere for den tilknyttede perioden.

![Oppsett av nummerseriegruppe.](media/chrono-num-sequence-group.jpg)

På samme måte konfigurerer du nummerseriegrupper i modulene **Leverandør** og **Prosjektstyring og regnskap**.

### <a name="configure-number-sequence-groups-chronology"></a>Konfigurere kronologi for nummerseriegrupper

Hvis du vil konfigurere kronologi for nummerseriegrupper, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Kronologiske nummerseriegrupper**. Definere anvendelsesvilkår for nummerseriegrupper.

![Oppsett av kronologiske numre.](media/chrono-num-sequence-group-period.jpg)

| Felt            | beskrivelse                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Effektiv  | Startdato for anvendelse av nummerseriegruppe. |
| Utløp      | Sluttdato for anvendelse av nummerseriegruppe. Hvis ingen sluttdato brukes, velger du **Aldri**. |
| Nummerseriegruppe | Nummerseriegruppe som skal brukes til å generere dokumentnumre i løpet av perioden. |
| Opprinnelig nummerseriegruppe | Denne nummerseriegruppekoden brukes for tilleggsfiltrering for tilfellene der dokumenter allerede har en bestemt *permanent* nummerseriegruppe tilordnet. En tom verdi regnes som en spesifikk verdi. Hvis du må ignorere en foreløpig tilordnet gruppe, bruker du **Standard**-alternativet for dette oppsettet. |
| Standard | Hvis den er aktivert, ignorerer systemet den midlertidig tilordnede dokumentnummerseriegruppen og bruker bare periodens start- og sluttdatoer til gjeldende analyse. Hvis den er slått av, bruker systemet hele kombinasjonen **Gyldig** + **Utløp** + **Opprinnelig nummerseriegruppe** for valg. |

## <a name="document-posting"></a>Dokumentpostering
Når du posterer et dokument, tilordnes den riktige nummerseriegruppen til dokumentet, basert på dokumentets posteringsdato og brukes deretter til å generere et dokumentnummer basert på den oppdagete nummerserien. Systemet gir en melding om tilordning av nummerseriegruppe.

![Dokumentnr.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> I noen land er det allerede implementert en bestemt logikk for dokumentnummerering. I dette tilfellet vil landspesifikk logikk overstyre funksjonen **Kronologisk nummerering**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
