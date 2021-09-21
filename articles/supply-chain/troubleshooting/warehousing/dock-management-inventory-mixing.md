---
title: Blandete lagertyper når du bruker sonebehandlingsprofil
description: Du må først konfigurere et arbeidshodeskift for at sonebehandlingsprofilen skal kunne styre kombinasjonen av lager på en effektiv måte. Denne siden beskriver hvordan du gjør det.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477184"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Lagertyper blandes når du bruker en sonebehandlingsprofil

## <a name="symptoms"></a>Symptomer

Du bruker *policyer for forsendelseskonsolidering*. Du har definert en *sonebehandlingsprofil* for en *lokasjonsprofil*, men når arbeidet opprettes, er lagertypene kombinert ved den endelige lokasjonen.

## <a name="resolution"></a>Løsning

Sonebehandlingsprofiler krever at arbeid deles på forhånd. Med andre ord forventer sonebehandlingsprofilen at et arbeidshode ikke vil ha flere plasseringslokasjoner.

Du må konfigurere et arbeidshodeskift for at sonebehandlingsprofilen skal kunne styre kombinasjonen av lager på en effektiv måte.

I dette eksemplet konfigureres vår sonebehandlingsprofil slik at **Lagertyper som ikke skal kombineres**, settes til *Forsendelses-ID*, og vi konfigurerer et hodeskift for profilen:

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Velg **arbeidsordretypen** du vil redigere (for eksempel *Bestillinger*).
1. Velg arbeidsmalen du vil redigere.
1. I handlingsruten velger du **Rediger spørring**.
1. Åpne fanen **Sortering**, og legg til en rad med følgende innstillinger:
    - **Tabell** - *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell** - *Midlertidige arbeidstransaksjoner*
    - **Felt** - *Forsendelses-ID*
1. Velg **OK**.
1. Du kommer tilbake til siden **Arbeidsmaler**. Velg **Arbeidshodeskift** i handlingsruten.
1. I handlingsruten velger du **Rediger**.
1. Merk av i avmerkingsboksen som er knyttet til **Feltnavn** *Forsendelses-ID*.
1. Velg **Lagre** i handlingsruten.
