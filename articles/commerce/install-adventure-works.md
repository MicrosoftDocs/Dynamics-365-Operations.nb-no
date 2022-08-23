---
title: Installere Adventure Works-temaet
description: Denne artikkelen beskriver hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274293"
---
# <a name="install-the-adventure-works-theme"></a>Installere Adventure Works-temaet

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works-temaet og modulene er tilgjengelige fra Dynamics 365 Commerce 10.0.20-versjonen. De er tilgjengelige fra Microsoft AppSource.

## <a name="prerequisites"></a>Forutsetninger

Før du installerer Adventure Works-temaet, må du ha et Dynamics 365 Commerce-miljø (Commerce versjon 10.0.20 eller senere) som inkluderer Retail Cloud Scale Unit (RCSU), Commerce Online Software Development Kit (SDK), og Commerce-modulbiblioteket. Hvis du vil ha informasjon om hvordan du installerer Commerce SDK og modulbiblioteket, kan du se [Definere et utviklingsmiljø](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Installasjonstrinn

### <a name="install-the-adventure-works-theme-in-your-application"></a>Installere Adventure Works-temaet i programmet

Adventure Works-temapakken er tilgjengelig i **dynamics365-commerce**-feed, som **@msdyn365-commerce-theme/adventureworks-theme-kit**. Men selv om Adventure Works-temapakken er en del av denne oppdateringen, er den under et annet navneområde. Derfor må du følge disse trinnene for å legge til registeroppføringer for navneområdet.

1. Oppdater **.npmrc**-filen slik at den inneholder følgende registeroppføring (hvis oppføringen ikke allerede er inkludert):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Oppdater **.yarnrc**-filen slik at den inneholder følgende registeroppføring (hvis oppføringen ikke allerede er inkludert):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Hvis du vil installere pakken i ditt lokale miljø, kjører du `yarn add THEME_PACKAGE@VERSION`-kommandoen fra ledeteksten, der **THEME_PACKAGE** er temapakken (@msdyn365-commerce-theme/adventureworks-theme-kit) og **VERSJON** er versjonsnummeret til modulbiblioteket som brukes. Det er viktig at versjonene av temapakken og modulbiblioteket samsvarer. Hvis du vil finne det riktige versjonsnummeret for modulbiblioteket som skal brukes, åpner du filen package.json og finner verdien **starter-pack** under **avhengigheter**-delen. I følgende eksempel bruker filen package.json versjon 9.32 av modulbiblioteket som tilordnes til Dynamics 365 Commerce 10.0.22-versjonen.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Følgende eksempel viser hvordan du kjører kommandoen `yarn add` for å legge til versjon 9.32 av Adventure Works-temaet. Kommandoen oppdaterer automatisk filen package.json slik at den inkluderer avhengigheten.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Hvis du vil ha mer informasjon om oppdatering av modulbibliotekversjonen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md). 

> [!IMPORTANT]
> - Temaversjonen bør samsvare med modulbibliotekversjonen for å sikre at alle funksjoner fungerer som forventet. 
> - Minimumsversjonen for Commerce-modulbiblioteket og SDK må være 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Legge til skriftfilene for Adventure Works-temaet

Når Adventure Works-temaet er installert i appen, må du legge til skriftfilene som er nødvendige for det. Du kan fullføre dette trinnet ved å kopiere alle skriftfilene fra **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** til felleskatalogbanen for partnerprogrammet **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Konfigurere ressursene for Adventure Works-temaet

Det neste trinnet er å oppdatere den nødvendige standardressursen for temaet. Du kan fullføre dette trinnet ved å kopiere innholdet fra global.json-filen under **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** til partnerprogramfilen global.json under **\src\resources\modules**. Hvis målkatalogen **\src\resources** ikke finnes, kan den kopieres i sin helhet fra kildekatalogen **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** til målkatalogen **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Hent oppdateringer og validerer temaet

Hvis du vil ha informasjon om hvordan du henter de siste SDK-, modulbibliotek- og andre avhengighetsoppdateringer, kan du se delen "Hent oppdateringer" i [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#pull-updates).

Når de siste avhengighetene er hentet, kan du kjøre **yarn start**-kommandoen for å starte nodeserveren i utviklingsmiljøet, og teste det nye Adventure Works-temaet. Bla gjennom programmet lokalt ved å bruke spørringsstrengparameteren `?theme=adventureworks` (for eksempel `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Tilleggsressurser

[Adventure Works-tema](adventure-works-theme.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
