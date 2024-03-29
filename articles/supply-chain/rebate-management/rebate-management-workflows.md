---
title: Arbeidsflyter for rabattbehandlingsavtale
description: Denne artikkelen beskriver hvordan du konfigurerer en arbeidsflyt for rabattbehandlingsavtale for å godkjenne og aktivere avtaler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4f0590c4c906e746b54ac30fd6531b8c1cd67915
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067340"
---
# <a name="rebate-management-deal-workflows"></a>Arbeidsflyter for rabattbehandlingsavtale

[!include [banner](../includes/banner.md)]

Når du skal godkjenne rabattavtaler, bruker Rabattbehandling samme arbeidsflytplattformen som andre økonomi- og driftsapper. To jobbprosesser er tilknyttet hver arbeidsflyt:

- Ett av elementene i arbeidsflyten godkjenner avtalen.
- Ett av elementene i arbeidsflyten aktiverer avtalen, slik at bruker- eller arbeidsflytprosessen kan godkjenne transaksjonene.

Før du kan bruke en rabattavtale, må den være aktiv i **Rabattbehandling**-modulen. Hvis du vil aktivere en avtale, må du først opprette og konfigurere en *arbeidsflyt for rabattbehandlingsavtale*.

Brukere kan ikke godkjenne avtaler manuelt. Arbeidsflyten må alltid brukes.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Opprett og administrer arbeidsflyter for rabattbehandlingsavtale

For å arbeide med arbeidsflyter for rabattbehandlingsavtale må du gå til **Rabattbehandling \> Oppsett \> Arbeidsflyter for rabattbehandling**. Der kan du vise, opprette og oppdatere arbeidsflyter etter behov. Bare én arbeidsflyt av denne typen kan være aktiv om gangen. Hvis du vil ha mer informasjon om arbeidsflyter, hvordan du arbeider med siden **Arbeidsflyter for rabattbehandling** og hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterte artiklene.

## <a name="use-a-workflow-to-activate-a-deal"></a>Bruk en arbeidsflyt til å aktivere en avtale

Hvis du vil aktivere en avtale via en arbeidsflyt, åpner du avtalen (for eksempel på siden **Alle rabattbehandlingsavtaler**). Velg deretter **Arbeidsflyt \> Send inn** i handlingsruten. Etter at den nye avtalen er behandlet og godkjent via arbeidsflyten, vil den være aktiv og klar til bruk.

Når en avtale er aktivert, kan du ikke endre mesteparten av oppsettet. Hvis du må endre en aktiv avtale, må du først deaktivere den og deretter opprette en ny avtale. Hvis den nye avtalen kommer til å ligne på den gamle avtalen, kan du opprette den ved å kopiere den gamle avtalen.

Du kan endre følgende innstillinger for en avtale etter at den er aktivert:

- Avstem etter
- Akkumulert garanti
- Posteringsprofil
- Posteringsprofil for garanti
- Dokumentmerknader
- Valuta.
- Fra dato
- Til dags dato

I tillegg kan rabattlinjer fjernes.

