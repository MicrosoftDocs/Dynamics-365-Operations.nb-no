---
title: Opprette en nettbasert funksjonalitetsprofil
description: Denne artikkelen beskriver hvordan du oppretter en Internett-funksjonalitetsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276808"
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
