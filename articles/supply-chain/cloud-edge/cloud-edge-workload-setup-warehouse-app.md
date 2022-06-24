---
title: Konfigurer Warehouse Management-mobilappen for sky- og kantskalaenheter
description: Denne artikkelen beskriver hvordan du konfigurerer Warehouse Management-mobilapper for lagre som betjenes av en sky- eller kantskalaenhet.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865245"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurer Warehouse Management-mobilappen for sky- og kantskalaenheter

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Warehouse Management-mobilapper, slik at de kan brukes som lagre som betjenes av en sky- eller kantskalaenhet.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner å konfigurere mobilenhetene for å koble til en sky- eller kantskalaenhet, må du bekrefte at de kan koble seg til bedriftssenteret. For instruksjoner kan du se [Installere og koble til Warehouse Management-mobilappen](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Tilleggsoppsett når du kjører Warehouse Management-mobilappen mot en skalaenhet

Som en del av [distribusjonsprosessen for arbeidsmengder i lagerskalaenheter](cloud-edge-landing-page.md#scale-unit-manager-portal) blir de fleste av dataene som kreves for å koble til enheter som bruker Warehouse Management-mobilapper, synkronisert automatisk fra bedriftssenteret til skalaenheten. Du må imidlertid angi dataene på siden **Azure Active Directory-apper** (**Systemadministrasjon \> Oppsett \> Azure Active Directory-apper**) i skalaenhetsimplementeringen. I tillegg må du kanskje oppdatere standard **Bedrift**-verdi for bruker-ID-en din eller opprette en ny bruker. Brukere som er knyttet til en bedrift som ikke eksisterer i en skalaenhetsdistribusjon, kan ikke logge seg på når Warehouse Management-mobilappen er koblet til denne skalaenheten.

> [!NOTE]
> Fordi dataene på siden **Azure Active Directory-apper** ikke er synkronisert, må du manuelt vedlikeholde disse dataene hvis du vil flytte lagerarbeidsmengdene til en annen skalaenhet.

Husk at som en del av tilkoblingsoppsettet for hver Warehouse Management-mobilapp må den angitte URL-adressen til Azure Active Directory-ressursen være for skalaenheten i stedet for bedriftssenteret.
