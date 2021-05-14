---
title: Arbeidsflyter for rabattbehandlingsavtale
description: Dette emnet beskriver hvordan du konfigurerer en arbeidsflyt for rabattbehandlingsavtale for å godkjenne og aktivere avtaler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 16f1c56ecd69f4dc7bfd80e74d3f35147cc173d6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919825"
---
# <a name="rebate-management-deal-workflows"></a>Arbeidsflyter for rabattbehandlingsavtale

[!include [banner](../includes/banner.md)]

Når du skal godkjenne rabattavtaler, bruker Rabattbehandling den samme arbeidsflytplattformen som andre Finance and Operations-apper. To jobbprosesser er tilknyttet hver arbeidsflyt:

- Ett av elementene i arbeidsflyten aktiverer avtalen, slik at bruker- eller arbeidsflytprosessen kan godkjenne transaksjonene.
- Ett av elementene i arbeidsflyten godkjenner avtalen.

Før du kan bruke en rabattavtale, må den være aktiv i **Rabattbehandling**-modulen. Hvis du vil aktivere en avtale, må du først opprette og konfigurere en *arbeidsflyt for rabattbehandlingsavtale*.

Når en arbeidsflyt er aktivert for Rabattbehandling, kan brukere ikke godkjenne avtaler manuelt. Arbeidsflyten må alltid brukes.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Opprett og administrer arbeidsflyter for rabattbehandlingsavtale

For å arbeide med arbeidsflyter for rabattbehandlingsavtale må du gå til **Rabattbehandling \> Oppsett \> Arbeidsflyter for rabattbehandling**. Der kan du vise, opprette og oppdatere arbeidsflyter etter behov. Bare én arbeidsflyt av denne typen kan være aktiv om gangen. Hvis du vil ha mer informasjon om arbeidsflyter, hvordan du arbeider med siden **Arbeidsflyter for rabattbehandling** og hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterte emnene.

## <a name="use-a-workflow-to-activate-a-deal"></a>Bruk en arbeidsflyt til å aktivere en avtale

Hvis du vil aktivere en avtale via en arbeidsflyt, åpner du avtalen (for eksempel på siden **Alle rabattbehandlingsavtaler**). Velg deretter **Arbeidsflyt \> Send inn** i handlingsruten. Etter at den nye avtalen er behandlet og godkjent via arbeidsflyten, vil den være aktiv og klar til bruk.

Når en avtale er aktivert, kan du ikke endre oppsettet. Hvis du må endre en aktiv avtale, må du deaktivere den og deretter opprette en ny avtale. Hvis den nye avtalen kommer til å ligne på den gamle avtalen, kan du opprette den ved å kopiere den gamle avtalen.
