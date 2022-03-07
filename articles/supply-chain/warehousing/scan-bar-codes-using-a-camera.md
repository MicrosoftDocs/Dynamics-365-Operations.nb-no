---
title: Skanne strekkoder ved hjelp av et kamera i lagerappen
description: Dette emnet forklarer hvordan du konfigurerer lagerappen for å skanne strekkoder med et kamera på en mobil enhet.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434201"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Skanne strekkoder ved hjelp av et kamera i lagerappen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer lagerappen for å skanne strekkoder med et kamera på en mobil enhet. 

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil bruke denne funksjonen, må du ha versjon 1.2.0.0 av lagerappen installert, og enheten må ha et kamera. Når du åpner appen når du har oppdatert, blir du bedt om å tillate at appen kan bruke kameraet. Hvis enheten ikke har kamera, vises ingen ledetekst, og du kan ikke bruke kamera som skanner. 

## <a name="setup"></a>Installasjon
Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i lagerappen. Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**. 

For å kontrollere om inndatafeltet kan skannes går du til siden **Navn på lagerappfelt** og setter **Foretrukket inndatamodus** til **Skanning**. Når dette alternativet er valgt, kan kameraet brukes til å skanne i lagerappen. Hvis du vil ha informasjon om hvordan du konfigurerer appfeltnavn i Warehousing, kan du se [Konfigurere appfeltnavn i lagerappen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Støttede strekkodeformater
De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder. 

## <a name="navigation"></a>Navigering
Kamerasiden startes på hver side der inndatafeltet har den foretrukne inndatamodusen satt til Skanning. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:
- Klikk tilbakeknappen for å gå tilbake til oppgave- og detaljsiden. 
- Klikk blyanten på oppgave- og detaljsiden for å gå til siden der du kan skrive inn manuelt.
- Klikk kameraet på oppgave- og detaljsiden for å gå tilbake til kamerasiden. 

| Oppgave- og detaljsiden | Kamerasiden | 
| :---------------------: | :--------------------: |
| ![Detaljside med oppgaveeksempel på kameraskanning](./media/camera-scanning-example-task-detail-page50.png)          | ![Mindre kameraside med eksempel på kameraskanning](./media/camera-scanning-example-camera-page50.png)          |

På kamerasiden, når du klikker Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode. Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen. Du kan deretter prøve å skanne en strekkode på nytt.

Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat. Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn. Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt. Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.

