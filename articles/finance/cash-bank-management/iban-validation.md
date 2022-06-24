---
title: Administrere validering av internasjonale bankkontnumre (IBAN)
description: Denne artikkelen forklarer hvordan du administrerer validering av internasjonale bankkontnumre (IBAN).
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880906"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering av internasjonale bankkontnumre (IBAN)

[!include [banner](../includes/banner.md)]

Validering av et internasjonalt bankkontonummer (IBAN) øker valideringsmengden som utføres når du legger til et IBAN-nummer for en bankkonto.

Informasjon om strukturen til IBAN-nummeret lagres i Microsoft Dynamics 365 Finance og lastes inn automatisk når du bruker IBAN på bankkontoer. Det inneholder lengden på IBAN-nummeret, startposisjonene for bankkontonummeret og registreringsnummeret samt lengden på bankkontonummeret og registreringsnummeret.

## <a name="set-up-iban-structures"></a>Definere IBAN-strukturer

1. Gå til **Kontant- og bankbehandling \> Oppsett \> IBAN-strukturer**.
2. Legg merke til at IBAN-strukturene for hvert land eller område er opprettet automatisk.
3. Velg **Rediger**-knappen hvis strukturen må oppdateres for et bestemt land eller område.
4. Strukturdefinsjonene blir en del av hver nye versjon. Du kan bruke menyen **Tilbakestill strukturer** til å laste inn de nyeste definisjonene etter hver oppdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen i en bankkonto

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Opprett en bankkonto.
3. Angi et IBAN-nummer på hurtigfanen **Tilleggsinformasjon**.

    Hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert for hvert land eller område, får du en advarsel. Du kan ikke fortsette hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert i IBAN-strukturen.

    Valideringen kontrollerer også at bankkontonummeret samsvarer med delen av IBAN-nummeret som representerer bankkontonummeret. Hvis bankkontonummeret ikke samsvarer, får du en advarsel. Denne meldingen er bare en advarsel. Du kan fortsette selv om bankkontonummeret ikke samsvarer.

    Valideringen kontrollerer også at bankregistreringsnummeret samsvarer med delen av IBAN-nummeret som representerer bankregistreringsnummeret. Registreringsnummeret inneholder et banknummer og ofte en ekstra bankavdeling. Hvis bankregistreringsnummeret ikke samsvarer, får du en advarsel. Denne meldingen er bare en advarsel. Du kan fortsette selv om bankregistreringsnummeret ikke samsvarer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
