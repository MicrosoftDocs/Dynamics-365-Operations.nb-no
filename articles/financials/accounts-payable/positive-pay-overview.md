---
title: Oversikt over positiv betaling
description: Denne artikkelen inneholder informasjon om positiv betaling, som brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a7af2fc0e2c9915c4267f60e27dbddac320af6a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315182"
---
# <a name="positive-pay-overview"></a>Oversikt over positiv betaling

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om positiv betaling, som brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank. 

Positiv betaling brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank. Positive betalingsfiler kan hjelpe banker med å forhindre sjekksvindel. Du definerer positiv betaling for å generere en elektronisk liste over sjekker hver gang det skrives ut sjekker. Når en sjekk mottas av banken, sammenligner banken sjekken med listen over sjekker som du sendte tidligere. Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken. Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.

Positiv betaling er også kjent som SafePay. 

Positive betalingsfiler kan inneholde sensitiv informasjon om betalingsmottakere og sjekkbeløp. Derfor må du sørge for at du bruker riktige sikkerhetstiltak fra tidspunktet som filene er generert, til de er mottatt av banken. Positive betalingsfiler blir lastet ned i henhold til nedlastingsinstruksjonene for nettleseren. 

Positive betalingsfiler opprettes ved hjelp av dataenheter. Før du genererer en positiv betalingsfil, må du definere transformasjonsformatene for XML som oversetter dataene til et format som banken kan bruke. 

For hver bankkonto du vil generere informasjon om positiv betaling for, må du tilordne det positive betalingsformatetl. Når du har generert betalinger, kan du generere en positiv betalingsfil for én juridisk enhet og én bankkonto. Du kan også generere positive betalingsfiler for flere juridiske enheter og bankkontoer samtidig. 

Når kontrollene som er oppført i en positiv lønnsfilen er betalt, får du et bekreftelsesnummer fra banken. Du kan deretter bekrefte den positive lønnsfilen i Microsoft Dynamics 365 for Finance and Operations. 

Hvis du må endre en positiv betalingsfil, kan du tilbakekalle den. For hver kontroll i den positive betalingsfilen tilbakestilles deretter feltet som angir om kontrollen er inkludert i en positiv betalingsfil.

Hvis du vil ha mer informasjon, kan du se [Definere og generere positive betalingsfiler](set-up-generate-positive-pay-files.md).



