---
title: Arbeidsflyt for kunde
description: Denne artikkelen gir informasjon om kundearbeidsflyten. Du endrer bestemte felter for en kunde og deretter sende endringene til godkjenning ved hjelp av arbeidsflyten før de legges til for kunden.
author: abruer
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 883e77b5480a52201673e58a641c7180009a129c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864432"
---
# <a name="customer-workflow"></a>Arbeidsflyt for kunde

[!include [banner](../includes/banner.md)]

Arbeidsflyten for kunde har blitt lagt til i versjon 8.0.4. Du kan endre bestemte felt for en kunde og deretter sende endringene til godkjenning ved hjelp av arbeidsflyten før de legges til for kunden.

## <a name="set-up-the-customer-workflow"></a>Definere arbeidsflyten for kunde

Før du kan bruke funksjonen for arbeidsflyt for kunde, må du aktivere den.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
2. I fanen **Generelt** i hurtigfanen **Kundegodkjenning** setter du verdien for alternativet **Aktiver kundegodkjenninger** til **Ja** for å aktivere funksjonen.
3. I feltet **Virkemåte for dataenhet** velger du virkemåten som dataenhetene skal bruke når data importeres:

    - **Tillat endringer uten godkjenning** – en enhet kan oppdatere kundeposten uten å behandle den med arbeidsflyten.
    - **Forkast endringer** – kan ikke gjøre endringer i kundeposten. Importen vil mislykkes for feltene som er aktivert for arbeidsflyten.
    - **Opprette forslag til endring** – alle felt blir endret, bortsett fra feltene som er aktivert for arbeidsflyten. De nye verdiene for disse feltene legges til kunden som foreslåtte endringer, og arbeidsflyten vil starte automatisk.

4. I listen over kundefelt merker du deretter av for **Aktiver** for hvert felt som må godkjennes før endringene kan utføres.
5. Gå til **Kunder \> Oppsett \> Arbeidsflyter for Kunde**.
6. Velg **Ny**.
7. Velg **Arbeidsflyten til foreslåtte kundeendringer**. 
8. Definere arbeidsflyten slik at den samsvarer med godkjenningsprosessen. Elementet **Arbeidsflytgodkjenning for foreslåtte kundeendringer** for godkjenning av arbeidsflyt vil gjelde for endringene for kunden.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Endre kundeinformasjon og sende inn endringene til arbeidsflyten

Når du endrer et felt som er aktivert for arbeidsflyten, vises siden **Foreslått endringer**. Denne siden viser den opprinnelige verdien i feltet og den nye verdien du angav. Feltet du endret, tilbakestilles til opprinnelig verdi. En statusmelding på siden informerer deg om at endringene ikke har blitt sendt.

Hver gang du endrer et felt som er aktivert for arbeidsflyten, legges feltet til i listen over foreslåtte endringer. Hvis du vil forkaste den foreslåtte verdien for et felt, bruker du **Forkast**-knappen ved siden av feltet i listen. Hvis du vil forkaste alle endringer, kan du bruke knappen **Forkast alle endringer** nederst på siden. Velg **OK** for å lukke siden.

Når du har minst én foreslått endring, vises det to ytterligere menyer i handlingsruten: **Foreslåtte endringer** og **Arbeidsflyt**.

1. Velg **Foreslåtte endringer** for å åpne siden **Foreslåtte endringer** og se gjennom endringene.
2. Velg **Arbeidsflyt \>Send** for å sende endringene til arbeidsflyten.

    Statusen på siden endres til **Endringer som venter på godkjenning**.

Arbeidsflyten følger standard arbeidsflytprosessen i appen. Godkjenneren er rettet mot siden **Kunde**, der endringene kan gjennomgås på siden **Foreslåtte endringer** og deretter velge **Arbeidsflyt \> Godkjenn** for å godkjenne arbeidsflyten. Når alle godkjenninger er fullført, oppdateres feltene med verdier som du har foreslått.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
