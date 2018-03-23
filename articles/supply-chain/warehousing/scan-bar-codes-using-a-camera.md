---
title: "Skanne strekkoder ved hjelp av et kamera i Dynamics 365 for Finance and Operations – Warehousing"
description: "Dette emnet forklarer hvordan du konfigurerer Dynamics 365 for Finance and Operations – Warehousing for å skanne strekkoder med et kamera på en mobil enhet."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: nb-no
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Skanne strekkoder ved hjelp av et kamera i Dynamics 365 for Finance and Operations – Warehousing

[!include[banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer Dynamics 365 for Finance and Operations – Warehousing for å skanne strekkoder med et kamera på en mobil enhet. 

## <a name="prerequisites"></a>Nødvendig programvare
Hvis du vil bruke denne funksjonen, må du ha versjon 1.2.0.0 av Warehousing installert, og enheten må ha et kamera. Når du åpner appen når du har oppdatert, blir du bedt om å tillate at Dynamics 365 for Finance and Operations – Warehousing-programmet kan bruke kameraet. Hvis enheten ikke har kamera, vises ingen ledetekst, og du kan ikke bruke kamera som skanner. 

## <a name="setup"></a>Definere
Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i Warehousing-programmet. Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**. 

For å kontrollere om inndatafeltet kan skannes, går du til siden **Navn på lagerappfelt** i Dynamics 365 for Finance and Operations og setter **Foretrukket inndatamodus** til **Skanning**. Når dette alternativet er valgt, kan kameraet brukes til å skanne i programmet Warehousing. Hvis du vil ha informasjon om hvordan du konfigurerer appfeltnavn i Warehousing, kan du se [Konfigurere appfeltnavn i Warehousing-appen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Støttede strekkodeformater
De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder. 

## <a name="navigation"></a>Navigering
Kamerasiden startes på hver side der inndatafeltet har den foretrukne inndatamodusen satt til Skanning. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:
- Klikk tilbakeknappen for å gå tilbake til oppgave- og detaljsiden. 
- Klikk blyanten på oppgave- og detaljsiden for å gå til siden der du kan skrive inn manuelt.
- Klikk kameraet på oppgave- og detaljsiden for å gå tilbake til kamerasiden. 

| Oppgave- og detaljsiden | Kamerasiden | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

På kamerasiden, når du klikker Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode. Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen. Du kan deretter prøve å skanne en strekkode på nytt.

Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat. Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn. Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt. Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.


