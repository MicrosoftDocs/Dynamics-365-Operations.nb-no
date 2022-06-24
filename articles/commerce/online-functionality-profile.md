---
title: Opprette en nettbasert funksjonalitetsprofil
description: Denne artikkelen beskriver hvordan du oppretter en Internett-funksjonalitetsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 686bc6440c31f3a4d729f2d92e3e57a1cc7b641f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895432"
---
# <a name="create-an-online-functionality-profile"></a>Opprette en nettbasert funksjonalitetsprofil

[!include [banner](includes/banner.md)]

Denne artikkelen viser en oversikt over hvordan du konfigurerer en Internett-funksjonalitetsprofil for Microsoft Dynamics 365 Commerce.

Internett-funksjonalitetsprofilen inneholder ulike innstillinger som brukes for Internett-kanaler. Hver Internett-kanal må angi en Internett-funksjonalitetsprofil.

## <a name="create-an-online-functionality-profile"></a>Opprett en Internett-funksjonalitetsprofil

Prosedyren nedenfor forklarer hvordan du oppretter en Internett-funksjonalitetsprofil fra Commerce Headquarters-appen.

1. I navigasjonsruten går du til **Moduler \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonalitetsprofiler**.
1. I handlingsruten velger du **Ny**.
1. I **Profil**-feltet angir du en ID for profilen.
1. I **Beskrivelse**-feltet skriver du inn en verdi ("Adventure Works-profil" i eksempelbildet nedenfor).
1. I **Funksjoner**-delen endrer du innstillingene for **HANDLEKURV**, **DETALJHANDELSKUNDER** eller **UTSJEKKING** etter behov.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en Internett-funksjonalitetsprofil.
  
![Eksempel på Internett-funksjonalitetsprofil.](media/online-functionality-profile.png)

## <a name="functions"></a>Funksjoner

- **Slå sammen produkter**: Når denne funksjonen er aktivert, kan antallet i handlekurven oppdateres når den samme varen legges til flere ganger.
- **Tillat utsjekking uten betalinger**: Når dette er aktivert, håndterer funksjonen scenarioet når varer som legges til i handlekurven, har en pris på 0,00.
- **Opprett kunde i asynkron modus**: Dette er en eldre innstilling som gjelder for tredjeparts e-handelskanaler, og som ikke gjelder for e-handelsområdet i Dynamics 365.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Definere en Internett-kanal](channel-setup-online.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)

[Definere en telefonsenterkanal](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
