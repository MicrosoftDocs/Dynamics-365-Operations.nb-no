---
title: Installere Adventure Works-temaet
description: Dette emnet beskriver hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad704c6c3b95abcfd52e449a0ffbb4b82b236498ae8d2775c4e65811de3ef503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763842"
---
# <a name="install-the-adventure-works-theme"></a>Installere Adventure Works-temaet

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works-temaet og modulene er tilgjengelige fra Dynamics 365 Commerce 10.0.20-versjonen. De er tilgjengelige fra Microsoft AppSource.

## <a name="prerequisites"></a>Forutsetninger

Før du installerer Adventure Works-temaet, må du ha et Dynamics 365 Commerce-miljø (Commerce versjon 10.0.20 eller senere) som inkluderer Retail Cloud Scale Unit (RCSU), Commerce Online Software Development Kit (SDK), og Commerce-modulbiblioteket. Hvis du vil ha informasjon om hvordan du installerer Commerce SDK og modulbiblioteket, kan du se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Installasjonstrinn

### <a name="install-the-adventure-works-theme-in-your-application"></a>Installere Adventure Works-temaet i programmet

Adventure Works-temapakken er tilgjengelig i **dynamics365-commerce**-feed, som **@msdyn365-commerce-theme/adventureworks-theme-kit**. Men selv om Adventure Works-temapakken er en del av denne oppdateringen, er den under et annet navneområde. Derfor må du følge disse trinnene for å legge til registeroppføringer for navneområdet.

1. Oppdater **.npmrc**-filen slik at den inneholder følgende registeroppføring (hvis oppføringen ikke allerede er inkludert):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Oppdater **.yarnrc**-filen slik at den inneholder følgende registeroppføring (hvis oppføringen ikke allerede er inkludert):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Hvis du vil installere pakken i det lokale miljøet, kjører du følgende kommando fra ledeteksten. Denne kommandoen oppdaterer automatisk filen package.json slik at den inkluderer avhengigheten.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

I **package.json**-filen bør du oppdatere temaversjonen til en bestemt versjon.

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
