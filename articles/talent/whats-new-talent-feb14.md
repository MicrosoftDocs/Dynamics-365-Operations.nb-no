---
title: Hva er nytt eller endret i Dynamics 365 Talent (14. februar 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462124"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (14. februar 2019)?

Dette emnet beskriver funksjoner som enten er nye eller endret i Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Det er mindre feilrettinger inkludert i denne utgivelsen.

## <a name="changes-in-onboarding"></a>Endringer i jobbintroduksjon
Det er mindre feilrettinger inkludert i denne utgivelsen.
 
## <a name="changes-in-core-hr"></a>Endringer i Core HR 
**Build 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Enheten Fast kompensasjon for ansatt eksporterer ikke alle poster
Med denne endringen vil enheten **Fast kompensasjon for ansatt** nå eksportere alle poster. Enheten kan brukes til å opprette og oppdatere eksisterende poster for fast kompensasjon for ansatte. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Sluttdato for ansettelse overholder ikke innstillinger for foretrukket tidssone for ansatte
Sluttdatoer for ansettelse tar nå hensyn til brukervalgt tidssone når ansettelse i et firma opprettes eller avsluttes.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Adresser i Storbritannia vises som adresser i det østlige Sveits i Analyse
En endring er gjort i denne versjonen for å rette opp feilplasserte adresser i rapporten **Personaladministrasjon** "Antall ansatte etter sted".
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Opphørskode fylles ikke ut på tilordningsposten for arbeiderstilling ved avslutning av stillingen
En endring er gjort for å angi "Avslutningsårsak"-koden som standard ved avslutning av ansattes stillingstilordning.

### <a name="new-entity-created-for-job-compensation-levels"></a>Ny enhet opprettet for jobbkompensasjonsnivåer
En ny enhet for rammeverk for databehandling (DMF) er opprettet. Enheten muliggjør oppretting og oppdatering til kompensasjonsnivåer, markedsverdier og undersøkelsesinformasjon for hver jobb som er definert i systemet.
