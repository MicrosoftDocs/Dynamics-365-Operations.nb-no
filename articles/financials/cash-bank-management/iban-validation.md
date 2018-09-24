---
title: Administrere validering av internasjonale bankkontnumre (IBAN)
description: Dette emnet forklarer hvordan du administrerer validering av internasjonale bankkontnumre (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: nb-no
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering av internasjonale bankkontnumre (IBAN)

[!include [banner](../includes/banner.md)]

Validering av et internasjonalt bankkontonummer (IBAN) øker valideringsmengden som utføres når du legger til et IBAN-nummer for en bankkonto.

Strukturen til IBAN-nummeret lagres i Microsoft Dynamics 365 for Finance and Operations og lastes automatisk når du først bruke IBAN-nummeret på bankkontoer. Bankkontonummeret er en del av den definerte strukturen for et IBAN-nummer. Basert på denne strukturen, om plasseringen og lengden på kontonummeret i IBAN-nummeret ikke samsvarer med stillingen som er definert i strukturen for hvert land eller område, får du advarsler.

## <a name="set-up-iban-structures"></a>Definere IBAN-strukturer

1. Gå til **Kontant- og bankbehandling \> Oppsett \> IBAN-strukturer**.
2. Legg merke til at IBAN-strukturene for hvert land eller område er opprettet automatisk.
3. Hvis du må tilpasse strukturer for et bestemt land eller område, kan du redigere dem.
4. Strukturdefinsjonene blir en del av hver nye versjon. Du kan bruke menyen **Tilbakestill strukturer** til å laste inn de nyeste definisjonene etter hver oppdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen i en bankkonto

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Opprett en bankkonto.
3. Angi et IBAN-nummer på hurtigfanen **Tilleggsinformasjon**.

    Hvis plasseringen og lengden på kontonummeret i IBAN-nummeret ikke samsvarer med stillingen som er definert i strukturen for hvert land eller område, får du en melding. Du kan ikke fortsette hvis lengden på IBAN-nummeret ikke samsvarer med lengden i IBAN-strukturen.

    Valideringen kontrollerer også at bankkontonummeret samsvarer med delen av IBAN-nummeret som representerer bankkontonummeret. Hvis bankkontonummeret ikke samsvarer, får du en advarsel. Denne meldingen er bare en advarsel. Du kan fortsette selv om bankkontonummeret ikke samsvarer.

