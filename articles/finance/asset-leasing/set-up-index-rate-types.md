---
title: Definere indeksrenter
description: Dette emnet forklarer hvordan du konfigurerer indeksrenter. Indeksrenter kreves hvis organisasjonen knytter leierbetalingsbeløp med et sett med indeksrenter.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40f230a9d69a142b18eb27a2d5e420dbadc600d2
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880966"
---
# <a name="set-up-index-rates"></a>Definere indeksrenter

[!include [banner](../includes/banner.md)]

Hvis leiebetalinger er avhengige av en indeks, kan indeksrentetypene legges til og vedlikeholdes i systemet. Når du skal revaluere leiebetalinger fra siden **Indeksrentetype**, bruker revalueringsprosessen for indeksrente den nyligste indeksrenten fra datoen for revalueringen.

Følg denne fremgangsmåten for å legge til indeksrentetyper og indeksrenter.

1. Gå til **Aktivaleie \> Oppsett \> Indeksrentetype**.
2. Velg **Ny**.
3. I de aktuelle feltene angir du rentetypen og navnet på indeksrenten.
4. Hvis du vil legge til en ny verdi for en indeksrenteverdi, velger du indeksrentetypen, og deretter velger du **Legg til**.
5. Velg den gjeldende startdatoen for renten, og velg renteverdien.

Du må velge enten **verdidifferanse for indeksrente** eller **indeksrenteverdi** som indeksrentemetode.

- Velg metoden for **verdidifferanse for indeksrente** for å beregne en ny leiebetaling basert på forskjellen mellom indeksrenten på startdatoen og den seneste indeksrenten. Indeksrenten er definert i feltet for **indeksrente (%)**.
- Velg metoden for **indeksrenteverdi** for å beregne leiebetalingen ved å bruke prosenten som er angitt i feltet for **indeksrente (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
