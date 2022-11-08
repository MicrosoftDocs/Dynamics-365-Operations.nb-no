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
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733478"
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

## <a name="licensing"></a>Lisensiering

Det finnes ingen endringer i lisensieringen for Dynamics 365 Human Resources i følgende områder: 

- **Minstekrav til antall lisenser du kan kjøpe**
- **Lisenser til et produksjonsmiljø og et sandkassemiljø** – Hvis du har eksisterende frittstående Human Resources-lisenser som omfatter ett produksjonsmiljø og ett sandkassemiljø, er samme antall lisenser tilgjengelige i økonomi- og driftsinfrastrukturen.
- **Flere sandkasselisenser** – Hvis du har kjøpt flere sandkasselisenser for det frittstående Human Resources-programmet, er det samme antallet lisenser tilgjengelig for sandkassemiljøer i økonomi- og driftsinfrastrukturen. 
