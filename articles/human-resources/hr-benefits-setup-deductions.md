---
title: Konfigurere fradrag
description: Bruk fradrag i Microsoft Dynamics 365 Human Resources for å fastslå hvor mye hvis det er, hvis noe, å trekke fra en ansatts lønn for hver fordel.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf7ddbfb8717c0311fab7388f346f03618a7b43d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065849"
---
# <a name="configure-deductions"></a>Konfigurere fradrag


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bruk fradrag i Microsoft Dynamics 365 Human Resources for å fastslå hvor mye hvis det er, hvis noe, å trekke fra en ansatts lønn for hver fordel. Fradrag gjelder for dato, slik at du kan holde en historisk oversikt over fradragsinformasjon. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Fradrag**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Fradrag** | En unik ID som brukes til å identifisere fordelsfradraget. |
   | **Beskrivelse** | En beskrivelse for fradraget. |
   | **Effektiv** | Startdatoen. Standardverdien er gjeldende systemdato. |
   | **Utløp** | Sluttdatoen. Standardverdien er 12/31/2154, som i praksis betyr aldri. |
   | **Overskrift** | Overskriftskoden fra lønnssystemet som dette fradraget vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn. Dette brukes når du bruker en tredjeparts lønnsleverandør. |
   | **Referanse for lønnstrekk for ansatt** | Fradragskoden fra lønnssystemet som dette fradraget bruker for ansattdelen av fradraget ved behandling av fordelene til lønn. |
   | **Beløpsoverskrift** | Overskriftskoden fra lønnssystemet som dette fradragsbeløpet vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn. Dette brukes normalt når du bruker en tredjeparts lønnsleverandør. |
   | **Kan slette** | Angir om en eksportert verdi fra Dynamics 365 for Finance and Operations kan føre til at verdien slettes i lønningssystemet. |
   | **Parede kolonner** | Angir om overskrift og fradragsbeløp skal eksporteres i parede sammenliggende kolonner til et lønningssystemet. |
   | **Ikrafttredelsesdato for endring** | Datoen når endringen av fordelsfradraget settes i kraft. På denne datoen endres fordelsfradraget og alle fordelsplanene som er knyttet til dette fradraget, blir oppdatert, så lenge du kjører behandling av **oppdatering av fradragsendring**. |
   | **Fradragsendring fullført** | Avmerkingsboksen for **Fradragsendring fullført** blir valgt automatisk når fordelsfradragsendringene er fullført av fradrag av oppdaterings endrings behandling. |
   
4. Hvis du vil spore og vedlikeholde endringer i fordelssatsoppsettet, velger du **Handlinger** og deretter **Vedlikehold versjoner**.

5. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
