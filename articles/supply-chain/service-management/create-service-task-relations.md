---
title: Opprette serviceoppgaverelasjoner
description: Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9a7808357916ed80ddfa46e1e4f362e0dde1671
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819070"
---
# <a name="create-service-task-relations"></a>Opprette serviceoppgaverelasjoner    

[!include [banner](../includes/banner.md)]

Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren. Denne informasjonen er tilgjengelig for teknikere og kunder.

## <a name="create-a-relation-with-a-service-agreement"></a>Opprette en relasjon med en serviceavtale

1.  Gå til **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.

2.  Velg en eksisterende serviceavtale, eller opprett en ny serviceavtale.

3.  Velg knappen **Serviceoppgaver** i handlingsruten.

4.  I skjemaet **Serviceoppgaver** velger du **Ny** for å opprette en ny linje, og velg deretter en serviceoppgave fra listen **Serviceoppgave** for å knytte serviceoppgaven til serviceavtalen.

5.  Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i fanen **Beskrivelse**.

6.  Lukk skjemaet for å lagre posten.

Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceavtalen. Du kan nå angi disse serviceoppgavene for alle tilknyttede avtalelinjer.

En serviceoppgaverelasjon som er opprettet i en serviceavtale, er tilgjengelig fra alle serviceordrer som er knyttet til serviceavtalen.

## <a name="create-a-relation-with-a-service-order"></a>Opprette en relasjon med en serviceordre

1.  Gå til **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Velg en eksisterende serviceordre, eller opprett en ny serviceordre.

3.  Velg knappen **Serviceoppgaver** i handlingsruten.

4.  I skjemaet **Serviceoppgaver** velger du **Ny** for å opprette en ny linje, og velg deretter en serviceoppgave fra listen **Serviceoppgave** for å knytte serviceoppgavene til servicordren.

5.  Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i fanen **Beskrivelse**.

6.  Lukk skjemaet for å lagre posten.

Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceordren. Deretter kan du velge serviceoppgaven du har opprettet relasjonen til, når du oppretter nye serviceordrelinjer.

Serviceoppgaverelasjoner som er opprettet i en serviceordre, er tilgjengelige i den aktuelle serviceordren.

## <a name="see-also"></a>Se også

[Oversikt over serviceoppgaver](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]