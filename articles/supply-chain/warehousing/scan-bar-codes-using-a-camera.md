---
title: Skanne strekkoder ved hjelp av et kamera i mobilappen Warehouse Management
description: Denne artikkelen forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8459ea6912328fa589b92f1731551f56df89c11b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862344"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Skanne strekkoder ved hjelp av et kamera i mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.

## <a name="setup"></a>Installasjon

Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i mobilappen Lagerstyring. Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**.

For å kontrollere om inndatafeltet kan skannes går du til siden **Navn på lagerappfelt** og setter **Foretrukket inndatamodus** til **Skanning**. Når dette alternativet er valgt, kan kameraet brukes til å skanne i mobilappen Lagerstyring. For mer informasjon, se [Konfigur felter for mobilappen Lagerstyring](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Støttede strekkodeformater

De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.

## <a name="navigation"></a>Navigering

Kamerasiden startes på hver side der inndatafeltet har **Foretrukket inndatamodus** satt til *Skanning*. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:

- Klikk på tilbakeknappen for å gå tilbake til siden **Oppgave og detaljer**.
- Klikk på blyanten på siden **Oppgave og detaljer** for å gå til siden der du kan skrive inn manuelt.
- Klikk på kameraet på siden **Oppgave og detaljer** for å gå tilbake til kamerasiden.

På kamerasiden, når du velger Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode. Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen. Du kan deretter prøve å skanne en strekkode på nytt.

Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat. Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn. Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt. Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]