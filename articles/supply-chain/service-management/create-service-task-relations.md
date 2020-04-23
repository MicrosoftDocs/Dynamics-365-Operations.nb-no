---
title: Opprette serviceoppgaverelasjoner
description: Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b167714dc81cf0e4ee70d7092f2ec030043abe71
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202612"
---
# <a name="create-service-task-relations"></a>Opprette serviceoppgaverelasjoner    

[!include [banner](../includes/banner.md)]

Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren. Denne informasjonen er tilgjengelig for teknikere og kunder.

## <a name="create-a-relation-with-a-service-agreement"></a>Opprette en relasjon med en serviceavtale

1.  Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.

2.  Velg en eksisterende serviceavtale, eller opprett en ny serviceavtale.

3.  Klikk på **Serviceoppgaver**-knappen i handlingsruten.

4.  I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgaven til serviceavtalen.

5.  Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.

6.  Lukk skjemaet for å lagre posten.

Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceavtalen. Du kan nå angi disse serviceoppgavene for alle tilknyttede avtalelinjer.

En serviceoppgaverelasjon som er opprettet i en serviceavtale, er tilgjengelig fra alle serviceordrer som er knyttet til serviceavtalen.

## <a name="create-a-relation-with-a-service-order"></a>Opprette en relasjon med en serviceordre

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Velg en eksisterende serviceordre, eller opprett en ny serviceordre.

3.  Klikk på **Serviceoppgaver**-knappen i handlingsruten.

4.  I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgavene til serviceordren.

5.  Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.

6.  Lukk skjemaet for å lagre posten.

Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceordren. Deretter kan du velge serviceoppgaven du har opprettet relasjonen til, når du oppretter nye serviceordrelinjer.

Serviceoppgaverelasjoner som er opprettet i en serviceordre, er tilgjengelige i den aktuelle serviceordren.

## <a name="see-also"></a>Se også

[Oversikt over serviceoppgaver](service-tasks.md)


  


