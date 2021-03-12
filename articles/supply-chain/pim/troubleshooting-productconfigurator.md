---
title: Feilsøk produktkonfiguratoren
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktkonfiguratoren.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999612"
---
# <a name="troubleshoot-the-product-configurator"></a>Feilsøk produktkonfiguratoren

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktkonfiguratoren.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Vareteksten overskrives når jeg konfigurerer et produkt på en salgsordrelinje.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet oppstår når du oppretter en salgsordrelinje for en konfigurerbar vare og deretter endrer vareteksten. Når du konfigurerer varen og deretter velger **OK**, overskrives teksten med standardteksten.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er forventet. Tekstfeltet inneholder variantnavnet, som bare fylles ut etter at du har konfigurert linjen. Du må derfor endre teksten etter at du har konfigurert linjen, ikke før.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heltallattributter blir avrundet feil når produktkonfigurasjonsmodeller beregnes.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet kan oppstå når du utfører følgende serie med handlinger:

1. Definer følgende attributter i en produksjonskonfigurasjonsmodell:

    - Inndata (heltall)
    - Prosent (desimal)
    - Resultat (heltall)

2. Opprett en beregning som har følgende uttrykk:

    *Resultat* = *inndata* × *prosent* ÷ 100

I dette tilfellet blir ikke heltallsresultatet alltid avrundet riktig. Inndataene er for eksempel 1 000, og prosenten er 2,40. Derfor forventer du at heltallsresultatet er 24, fordi 2,40 prosent av 1 000 er 24 (eller 24,00 i desimalformat). Resultatet vises i stedet som 23. Når prosenten er 2,39, avrundes imidlertid beregningen til 24 i stedet for 23. Når prosenten er 2,50, avrundes beregningen til 25 som forventet.

### <a name="issue-resolution"></a>Problemløsning

Dette problemet oppstår på grunn av måten som Microsoft Solver Foundation internt representerer tall ved hjelp av brøker. I det foregående eksemplet representeres resultatet av beregningen der prosenten er 2,40 som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Når .NET sender denne verdien som et heltall, returnerer den 23.

Denne virkemåten vil ikke bli endret fordi andre scenarioer er avhengige av den. I det foregående eksemplet kan du løse problemet ved å introdusere et ekstra desimalattributt og en beregning.

Du kan for eksempel definere følgende attributter i en produksjonskonfigurasjonsmodell:

- Inndata (heltall)
- Prosent (desimal)
- ResultDecimal (desimal)
- ResultInteger (heltall)

Du kan deretter legge til følgende beregninger:

- *ResultDecimal* = *inndata* × *prosent* ÷ 100
- *ResultInteger* = *ResultDecimal*
