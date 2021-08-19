---
title: Skanne strekkoder ved hjelp av et kamera i mobilappen Lagerstyring
description: Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 62280b8401c1f7d5dc859a2130981405e69d03cfb5383123d7069e71e6cb1f47
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711669"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Skanne strekkoder ved hjelp av et kamera i mobilappen Lagerstyring

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.

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