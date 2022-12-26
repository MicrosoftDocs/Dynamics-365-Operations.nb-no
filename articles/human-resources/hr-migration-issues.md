---
title: Kjente problemer med sammenslåing av Dynamics 365 Human Resources-infrastruktur
description: Denne artikkelen viser problemer som kan oppstå under sammenslåing av Microsoft Dynamics 365 Human Resources-infrastruktur.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3fe21df8be010ace3070ad08ed95f3d3efc7b01d
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838562"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Kjente problemer med sammenslåing av Dynamics 365 Human Resources-infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Delte Dataverse-miljøer

Rammeverket for dobbel skriving støtter ikke kobling av to økonomi- og driftsappmiljøer til samme Dataverse-miljø. Hvis du har et Dataverse-miljø som deles med begge følgende elementer, må du enten duplisere Dataverse-miljøet eller dele det:

- En økonomi- og driftsapp
- Et gjeldende Human Resources-miljø

## <a name="environment-type-requirements"></a>Miljøtypekrav

Følgende miljøtyper er nødvendige før du kan foreta overføringen:

- Hvis du ikke har noen frittstående sandkassemiljøer, må du opprette et for å validere overføringen.
- Hvis du har flere frittstående produksjonsmiljøer, kan du overføre det ene av dem. Kontakt Microsoft Kundestøtte for å merke de andre miljøene som sandkasser.

## <a name="teams-integration"></a>Teams-integrering

Den eksisterende Human Resources-appen i Teams flyttes for øyeblikket til en Microsoft Power Platform-løsning. For mer informasjon, se [Human Resources-app i Teams](hr-admin-teams-leave-app.md).

## <a name="dual-write-integration"></a>Integrering med dobbel skriving

Dobbel skriving er en bruksklar infrastruktur som gir samhandling med minimal forsinkelse mellom kundeengasjementsapper og økonomi- og driftsapper. Hvis organisasjonen bruker skrivetilgang for integreringer, kan det påvirkes av noen av problemene som ble funnet. Hvis du vil ha mer informasjon om Dataverse-tabeller og -problemer, kan du se [Dataverse-tabeller](hr-developer-entities.md).

