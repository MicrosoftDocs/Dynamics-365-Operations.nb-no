---
title: Opprette arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434448"
---
# <a name="creating-work-orders"></a>Opprette arbeidsordrer

[!include [banner](../../includes/banner.md)]

 

Når du har planlagt forebyggende vedlikeholdsjobber, er neste trinn å opprette arbeidsordrer for jobbene. Dette gjøres i en av vedlikeholdsplanene. De planlagte jobbene i en vedlikeholdsplan kan ha forskjellige referansetyper:

| Referansetype | Beskrivelse                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Vedlikeholdsplaner     | Forebyggende vedlikeholdsjobber basert på vedlikeholdsplantypene "tid" eller "teller".                       |
| Vedlikeholdsrunder    | Forebyggende vedlikeholdsjobber som inneholder flere anleggsmidler som krever en lignende type vedlikehold.           |
| Forespørsel om vedlikehold   | Manuelt opprettet forespørsel om vedlikehold eller reparasjon av et anleggsmiddel, som kan konverteres til en arbeidsordre. |


1. Klikk **Aktivastyring** > **Felles** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer**.

2. Velg de planlagte vedlikeholdsjobbene du vil opprette en arbeidsordre for, og klikk på **Arbeidsordre**. Det totale antallet prognosetimer for de valgte linjene vises i feltet **Vedlikeholdsprognosetimer** i dialogboksen **Opprett arbeidsordrer**.

3. I **Parametere**-delen velger du hvor mange arbeidsordrer som skal opprettes. Du kan opprette én arbeidsordre per vedlikeholdsplanlinje, eller en rekke arbeidsordrer, basert på valgene i delen **Én arbeidsordre per**.

4. Velg en **Arbeidsordretype** som skal brukes på alle arbeidsordrene du oppretter. Illustrasjonen nedenfor viser et eksempel på dialogboksen **Opprett arbeidsordrer**.

![Figur 1](media/18-preventive-maintenance.png)

5. Klikk **OK**. Én eller flere arbeidsordrer opprettes.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]