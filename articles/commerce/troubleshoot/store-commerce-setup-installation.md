---
title: Feilsøk problemer med oppsett og installasjon i Store Commerce
description: Denne artikkelen beskriver hvordan du feilsøker problemer med oppsett og installasjon i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 92d4a9d78485b681b4e802f695d54f44ecd7c5de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870472"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Feilsøk problemer med oppsett og installasjon i Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du feilsøker problemer med oppsett og installasjon i Microsoft Dynamics 365 Commerce Store Commerce-appen.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Jeg kan ikke aktivere appen, og jeg får en feilmelding om tilkobling

Når du har angitt den gyldige URL-adressen for salgssted i skyen (CPOS), kan du få en feilmelding som ligner på følgende eksempel:

> Det har oppstått en tilkoblingsfeil, og enheten kan ikke koble til CPOS. Det kan være noen problemer med den innskrevne URL-adressen for CPOS.

I dette tilfellet kan du se etter skrivefeil i URL-adressen, eller finne ut om CPOS ikke kan nås fordi den er offline.

I tillegg må du kontrollere at CSU-versjonen (Cloud Scale Unit) er 10.0.25 (9.35.\*.\*) eller senere. CPOS-versjon 10.0.25 eller senere er nødvendig for å bruke Store Commerce-appen.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Jeg kan ikke installere appen fordi Moderne POS allerede er installert

Under installasjonen kan du få en feilmelding som ligner på følgende eksempel:

> En versjon (9.\*.\*.\*) av dette produktet (Moderne POS) er installert tidligere via det eldre installeringsprogrammet.

Du kan løse feilen ved å avinstallere MPOS-appen (Moderne salgssted) for alle brukerne på maskinen, og deretter prøve på nytt. Du kan bekrefte om MPOS er fjernet for alle brukerne ved å kjøre følgende PowerShell-kommando.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Jeg kan ikke aktivere appen på grunn av en ugyldig URL-adresse eller en feiltilstand

Hvis URL-adressen for CPOS du har angitt, ikke er gyldig og du vil endre den, eller hvis Store Commerce-appen er i en feiltilstand under aktiveringen, kan du starte prosessen på nytt ved å tilbakestille appen. Store Commerce-appen lagrer bare en gyldig URL-adresse for CPOS.

Følg denne fremgangsmåten for å tilbakestille Store Commerce-appen.

1. På **Start**-menyen i Windows velger du og holder (eller høyreklikker på) appen, og deretter velger du **Mer \> Appinnstillinger**.
2. Bla nedover på siden med appinnstillinger til du finner **Tilbakestill**-knappen.
3. Velg **Tilbakestill**. Når du blir bedt om det, bekrefter du at du vil tilbakestille appen.
