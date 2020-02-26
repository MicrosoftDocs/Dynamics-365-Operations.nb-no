---
title: Definere organisasjonshierarkier
description: Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002341"
---
# <a name="set-up-organization-hierarchies"></a>Definere organisasjonshierarkier


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Før du oppretter kanaler, må du definere organisasjonshierarkiene dine.

Du kan bruke organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver. Du kan for eksempel definere ett hierarki for avgiftsrapportering, juridisk eller lovpålagt rapportering. Du kan deretter definere et annet hierarki for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til intern rapportering.

Før du oppretter et organisasjonshierarki, må du opprette organisasjoner. Hvis du vil ha mer informasjon, kan du se [Opprette juridiske enheter](channels-legal-entities.md) eller [Opprette driftsenheter](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Hvis du vil ha mer informasjon, kan du se følgende emner.
- [Oversikt over organisasjoner og organisasjonshierarkier](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [Planlegge organisasjonshierarkiet](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [Opprette et organisasjonshierarki](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Opprette et organisasjonshierarki

Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.
1. I handlingsruten velger du **Ny**.
1. Angi en verdi i feltet **Navn**.
1. I **Formål**-delen velger du **Tilordne formål**.
1. Finn og velg ønsket post i listen. Velg et formål som skal tilordnes til organisasjonshierarkiet.
1. I delen **Tilordnede hierarkier** velger du **Legg til**.
1. Merk den valgte raden i listen. Finn hierarkiet du nettopp opprettet.
1. Velg **OK**.

Det følgende bildet viser et eksempel på et organisasjonshierarki som er opprettet for et fiktivt "Adventure Works"-sett med butikker.

![Eksempel på organisasjonshierarki](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Legge til organisasjoner i et hierarki

Hvis du vil legge til organisasjoner i et hierarki, følger du disse trinnene.

1. Finn og velg ønsket post i listen. Velg hierarkiet.
1. Velg **Vis** i handlingsruten.
1. Legg til organisasjoner etter behov.
1. Hvis du vil legge til en organisasjon, velger du **Rediger** og deretter **Sett inn**. Når du er ferdig med endringene, kan du lagre en kladd og publisere endringene.

Det følgende bildet viser en juridisk enhet som er lagt til i hierarkiroten med fire kostsentre som er lagt til for kanalene "Kjøpesenter", "Utsalgssted", "Nett" og "Telefonsenter". Det kan også legges til diverse typer detaljhandel-, telefonsenter- og Internett-kanaler.

![Eksempel på hierarkiutformer](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlegge organisasjonshierarkiet](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Opprett juridiske enheter](channels-legal-entities.md)

[Opprette driftsenheter](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)
