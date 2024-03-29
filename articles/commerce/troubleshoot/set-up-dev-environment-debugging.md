---
title: Konfigurere et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin for Retail Server på Lag 1
description: Denne artikkelen forklarer hvordan du konfigurerer et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin (VM) for Retail Server på Lag 1.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 64e03c742f7095e2e485f32ad534f2a755ddd062
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277886"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Konfigurere et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin for Retail Server på Lag 1

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin (VM) for Retail Server på Lag 1.

## <a name="description"></a>beskrivelse

Microsoft Dynamics 365 Commerce Lag 1-miljøer distribueres vanligvis for Commerce Runtime (CRT) og utvikling av POS-utvidelse (point of sale). De er frittstående miljøer. På grunn av SaaS (software as a service) i arkitekturen, omfatter de ikke e-handelkomponenter.

I noen scenarioer vil du kanskje teste kall til utvidelser i et Lag 1-miljø, slik at du kan feilsøke utvidelser fra e-commerce-komponenter. For generelle instruksjoner kan du se [Feilsøke mot et Commerce-utviklingsmiljø på lag 1](../e-commerce-extensibility/debug-tier-1.md).

Når du feilsøker mot et Lag 1-miljø, ettersom området nå kaller en annen Retail Server, kan kall på tvers av servere forårsake ulike feil som er knyttet til innholdssikkerhetspolicyen.

Illustrasjonen nedenfor viser et eksempel på en feil som kan oppstå når en variant er valgt på en produktdetaljerside.

![Feil når en variant er valgt på en produktdetaljerside.](media/unhandled-rejection-error.jpg)

Illustrasjonen nedenfor viser et eksempel på en lignende feil i webleserens feilsøkingsverktøy (F12 Developer Tools). Feilmeldingen nevner et brudd på direktivet for innholdssikkerhetspolicy.

![Feil under feilsøkingsverktøy.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Løsning

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Deaktivere innholdssikkerhetspolicy for området i Commerce-områdebyggeren

1. Velg området du arbeider på.
1. Velg **Innstillinger** og deretter **Utvidelser**.
1. Velg **Deaktiver innholdssikkerhetspolicy** i fanen **Innholdssikkerhetspolicy**.
1. Velg **Lagre og publiser**.

> [!NOTE]
> B2C-pålogging (Business-to-consumer) vil ikke fungere i et lokalt utviklingsmiljø. Du kan imidlertid bruke gjesteutsjekkinger eller lage sidesimuleringer for å etterligne en brukers pålogging etter behov.

## <a name="additional-resources"></a>Tilleggsressurser

[Komme i gang med omfattende elektronisk utvikling av e-handel](../e-commerce-extensibility/sdk-getting-started.md)

[Behandle innholdssikkerhetspolicy (CSP) på e-handelsområde](../manage-csp.md)
