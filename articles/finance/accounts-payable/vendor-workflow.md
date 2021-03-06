---
title: Arbeidsflyt for leverandør
description: Endre informasjon om leverandør og bruke arbeidsflyt til å godkjenne den.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e5aef18a7f541c6a0d4abf9d4461d1dd9cd27880
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810276"
---
# <a name="vendor-workflow"></a>Arbeidsflyt for leverandør

[!include [banner](../includes/banner.md)]

Når det brukes arbeidsflyt for leverandør, sendes endringene som gjøres i bestemte felt i arbeidsflyten for godkjenning før de kan legges til leverandøren.

## <a name="set-up-the-vendor-workflow"></a>Definere arbeidsflyten for leverandør

Før du kan bruke funksjonen for arbeidsflyt, må du aktivere den.

1. Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
2. I kategorien **Generelt** i hurtigfanen **Leverandørgodkjenning** angir du alternativet **Aktiver leverandørgodkjenninger** til **Ja**.
3. I feltet **Virkemåte for dataenhet** velger du virkemåten som skal brukes når data importeres:

    - **Tillat endringer uten godkjenning** – dataenheten kan oppdatere leverandørposten uten å behandle den med arbeidsflyten.
    - **Forkast endringer** – kan ikke gjøre endringer i leverandørposten. Importen vil mislykkes for feltene som er aktivert for arbeidsflyten.
    - **Opprette forslag til endring** – alle felt blir endret, bortsett fra feltene som er aktivert for arbeidsflyten. De nye verdiene for disse feltene legges til leverandøren som foreslåtte endringer, og arbeidsflyten vil starte automatisk.

4. I listen over leverandørfelt merker du av for **Aktiver** for hvert felt som må godkjennes før endringene kan utføres.
5. Gå til **Leverandører \> Oppsett \> Arbeidsflyter for leverandørreskontro**.
6. Velg **Ny**.
7. Velg **Arbeidsflyten til foreslåtte leverandørendringer**. 
8. Definere arbeidsflyten slik at den samsvarer med godkjenningsprosessen. Elementet **Arbeidsflytgodkjenning for foreslåtte leverandørendringer** for godkjenning av arbeidsflyt vil gjelde for endringene for leverandøren.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Endre leverandørinformasjon og sende inn endringene til arbeidsflyten

Når du endrer et felt som er aktivert for arbeidsflyten, vises siden **Foreslått endringer**. Denne siden viser den opprinnelige verdien i feltet og den nye verdien du angav. Feltet du endret, tilbakestilles til opprinnelig verdi. En statusmelding informerer deg også om at endringene ikke har blitt sendt. 

Hver gang du endrer et felt som er aktivert for arbeidsflyten, legges feltet til i listen på siden **Foreslåtte endringer**. Hvis du vil forkaste den foreslåtte verdien for et felt, bruker du **Forkast**-knappen ved siden av feltet i listen. Hvis du vil forkaste alle endringer, kan du bruke knappen **Forkast alle endringer** nederst på siden. Velg **OK** for å lukke siden.

Når du har minst én foreslått endring, vises det to ytterligere kategorier i handlingsruten: **Foreslåtte endringer** og **Arbeidsflyt**.

1. Velg **Foreslåtte endringer** for å åpne siden **Foreslåtte endringer** og se gjennom endringene.
2. Velg **Arbeidsflyt \> Send for å sende endringene til arbeidsflyten**.

    Statusen på siden endres til **Endringer som venter på godkjenning**.

Arbeidsflyten følger standard arbeidsflytprosess. Godkjenneren er rettet mot siden **Leverandør**, der endringene kan gjennomgås på siden **Foreslåtte endringer** og deretter velge **Arbeidsflyt \> Godkjenn** for å godkjenne arbeidsflyten. Når alle godkjenninger er fullført, oppdateres feltene med verdier som du har foreslått.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]