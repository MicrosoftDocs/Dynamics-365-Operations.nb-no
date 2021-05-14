---
title: Kontrollere varekvaliteten
description: Dette emnet beskriver hvordan du behandler kvalitetsordre.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956140"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrollere varekvaliteten

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du behandler kvalitetsordre. Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.

Hvis standard demodata er installert, kan du bruke dem til å fullføre prosedyrene i dette emnet. For å bruke demodata velger du den juridiske enheten *USMF* før du begynner. Deretter må du bekrefte bestillingen *000016* og postere et produktmottak. En kvalitetsordre genereres automatisk.

## <a name="step-1-select-a-quality-order"></a>Trinn 1: Velge en kvalitetsordre

For å velge en kvalitetsordre følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg kvalitetsordren som ble generert før du startet denne prosedyren.

## <a name="step-2-record-test-results"></a>Trinn 2: Registere testresultater

Følg disse trinnene for å registrere testresultater.

1. Velg **Resultater**.
1. Velg **Rediger**.
1. Angi et tall i **Resultatantall**-feltet.
1. Velg ønsket oppføring i feltet **Resultat**. I dette eksemplet er resultatet basert på et forhåndsdefinert resultat. Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.
1. Velg **Lagre**.
1. Lukk siden.

## <a name="step-3-validate-the-quality-order"></a>Trinn 3: Valider kvalitetsordren

For å validere kvalitetsordren følger du disse trinnene.

1. Velg **Valider**.
1. Velg brukeren som gjennomfører inspeksjonen, i feltet **Godkjent av**.
1. Velg **Velg**.
1. Velg **OK**.
1. Lukk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
