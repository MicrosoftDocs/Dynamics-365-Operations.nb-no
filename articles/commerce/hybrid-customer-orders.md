---
title: Hybridkundeordrer
description: En hybridkundeordre er en enkelt ordre som inneholder produkter som kan utføres fra butikken av kunden, i tillegg til produkter som skal hentes eller sendes senere.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4cb448670af9a6ddce8008be008cf3b0ff76bbce65053bf4618ea6668c4568d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739535"
---
# <a name="hybrid-customer-orders"></a>Hybridkundeordrer

[!include [banner](includes/banner.md)]

En hybridkundeordre er en enkelt ordre som inneholder produkter som kan utføres fra butikken av kunden, i tillegg til produkter som skal hentes eller sendes senere.

I Commerce kan du velge å utføre alle produkter eller utføre valgte produkter for en kundeordre. Produktlinjer som er merket som utfør, faktureres automatisk etter at ordren er opprettet. Dette gjelder også for en ordre som skal hentes etter at ordren er opprettet. Beløpet å betale på hybridordrer bestemmes ved å legge innbetalingsprosenten på produktlinjene for plukking og sending til hele beløpet for utføringslinjene. For hybridordrer veksler systemet mellom kundeordremodus og hentesalgmodus som følger:

- Hvis alle produkter i handlekurven er satt til **Utfør levering**, vil ordren bli behandlet som en hentesalgstransaksjon.
- Hvis noen av eller alle linjene i handlekurven er satt til enten **Plukk** eller **send levering**, vil ordren bli behandlet som en kundeordretransaksjon.

Hvis en handlevognlinje er valgt og **Velg valgt**, **Valgt for forsendelse** eller **Utfør valgte** er valgt, angis bare den bestemte handlekurvlinjen med denne leveringsmetoden. I så fall fortsetter nedstrømsflyten av operasjonen som vanlig. Hvis **Velg valgt**, **Valgt for forsendelse**, eller **Utfør valgte** velges uten at en handlevognlinje blir valgt, åpnes imidlertid en ny side som viser alle handlekurvlinjene. På dette skjermbildet kan du velge flere linjer samtidig for å angi leveringsmåte. Når du bruker denne metoden for å velge linjer, vil tidligere leveringsmåter som er knyttet til linjen, bli overstyrt.

## <a name="additional-resources"></a>Tilleggsressurser

[Kundeordrer i Modern POS (MPOS)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]