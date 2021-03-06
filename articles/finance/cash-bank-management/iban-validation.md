---
title: Administrere validering av internasjonale bankkontnumre (IBAN)
description: Dette emnet forklarer hvordan du administrerer validering av internasjonale bankkontnumre (IBAN).
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e44b855165752baeb42d3c9952c35982ef24b0f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815866"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering av internasjonale bankkontnumre (IBAN)

[!include [banner](../includes/banner.md)]

Validering av et internasjonalt bankkontonummer (IBAN) øker valideringsmengden som utføres når du legger til et IBAN-nummer for en bankkonto.

Informasjon om strukturen til IBAN er lagret i Microsoft Dynamics 365 Finance. Denne informasjonen lastes automatisk første gang du bruker IBAN-nummeret på bankkontoer. Det inneholder lengden på IBAN-nummeret, startposisjonene for bankkontonummeret og registreringsnummeret samt lengden på bankkontonummeret og registreringsnummeret.

## <a name="set-up-iban-structures"></a>Definere IBAN-strukturer

1. Gå til **Kontant- og bankbehandling \> Oppsett \> IBAN-strukturer**.
2. Legg merke til at IBAN-strukturene for hvert land eller område er opprettet automatisk.
3. Hvis du vil tilpasse strukturene for et bestemt land eller område, kan du redigere dem.
4. Strukturdefinsjonene blir en del av hver nye versjon. Du kan bruke menyen **Tilbakestill strukturer** til å laste inn de nyeste definisjonene etter hver oppdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen i en bankkonto

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Opprett en bankkonto.
3. Angi et IBAN-nummer på hurtigfanen **Tilleggsinformasjon**.

    Hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert for hvert land eller område, får du en advarsel. Du kan ikke fortsette hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert i IBAN-strukturen.

    Valideringen kontrollerer også at bankkontonummeret samsvarer med delen av IBAN-nummeret som representerer bankkontonummeret. Hvis bankkontonummeret ikke samsvarer, får du en advarsel. Denne meldingen er bare en advarsel. Du kan fortsette selv om bankkontonummeret ikke samsvarer.

    Valideringen kontrollerer også at bankregistreringsnummeret samsvarer med delen av IBAN-nummeret som representerer bankregistreringsnummeret. Registreringsnummeret inneholder et banknummer og ofte en ekstra bankavdeling. Hvis bankregistreringsnummeret ikke samsvarer, får du en advarsel. Denne meldingen er bare en advarsel. Du kan fortsette selv om bankregistreringsnummeret ikke samsvarer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]