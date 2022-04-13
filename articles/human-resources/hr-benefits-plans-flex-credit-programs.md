---
title: Definere fleksible kredittprogrammer
description: Du kan bruke fleksible kredittprogrammer i Microsoft Dynamics 365 Human Resources til å registrere ansatte i fordeler i henhold til et forhåndsdefinert antall fleksible kreditter.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1808d703983fd11e29f83c13f6181fb3068bc49
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533775"
---
# <a name="set-up-flex-credit-programs"></a>Definere fleksible kredittprogrammer


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan bruke fleksible kredittprogrammer i Microsoft Dynamics 365 Human Resources til å registrere ansatte i fordeler i henhold til et forhåndsdefinert antall fleksible kreditter. Ansatte kan velge hvordan de skal fordele den fleksible kreditten. Hvis for eksempel en ansatt er dekket under sin ektefelles forsikringsplan, ønsker de kanskje å bruke kredittene de ellers ville ha brukt på helsedekning, på andre fordeler. 

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fleksible kredittprogrammer**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **ID for fordelskreditt** | Den unike ID-en til det fleksible kredittprogrammet. |
   | **Beskrivelse** | En beskrivelse av det fleksible kredittprogrammet. | 
   | **Fra dato** | Datoen da de fleksible kreditt programmet blir aktivt. |
   | **Til dato** | Sluttdatoen for det fleksible kredittprogrammet. Du kan la standardverdien (12/31/2154) bli værende for å angi at det fleksible kredittprogrammet ikke har en planlagt utløpsdato. |
   | **Kredittverdi totalt** | Antall kreditter som hver ansatt skal ha for deres fordeler. |
   | **Fordelingsregel** | Regelen som skal brukes for å fordele fleksible kreditter når en ansatt blir ansatt i midt i en periode for fleksibel kreditt. </br></br><ul><li>**Ingen** – den ansatte får ingen fleksibel kreditt hvis de blir ansatt etter at perioden for det fleksible kredittprogrammet begynner.</li><li>**Full kreditt** – den ansatte mottar hele beløpet med fleksibel kreditt, uansett når de er ansatt.</li><li>**Fordelt** – den ansatte får en fordelt mengde fleksibel kreditt, basert på startdatoen.</li></ul> |
   | **Fordelingsformel for fleksikreditt** | Regelen som skal brukes for å fordele fleksible kreditter for ansatte som blir ansatt i midt i en fordelsperiode for det fleksible kredittprogrammet. Fordelingen er basert på startdatoen for ansettelsen. Feltet brukes bare hvis du velger **Fordeling** i **Fordelingsregel**-feltet. </br></br><ul><li>**Daglig** – Fordeler antallet fleksible kreditter en ansatt mottar til dagsnivået. Det totale antallet fleksible kreditter deles på antall dager i perioden. Hvis fordelsperioden for eksempel er på 400 dager, vil systemet dele det totale antallet fleksible kreditter med 400 for å beregne antallet fleksible kreditter som de ansatte mottar per dag.</li><li>**Gjeldende måned** – Fordeler antallet fleksible kreditter en ansatt mottar til månedsnivået, avrundet til gjeldende måned. Det totale antallet fleksible kreditter deles på antall måneder i perioden. Hvis fordelsperioden for eksempel er på 15 måneder, vil systemet dele det totale antallet fleksible kreditter med 15 for å beregne antallet fleksible kreditter som de ansatte mottar per måned.</li><li>**Følgende måned** – Fordeler antallet fleksible kreditter en ansatt mottar til månedsnivået, avrundet til neste måned. Det totale antallet fleksible kreditter deles på antall måneder i perioden. Hvis fordelsperioden for eksempel er på 15 måneder, deler systemet det totale antallet fleksible kreditter med 15 for å beregne antallet fleksible kreditter som de ansatte mottar per måned.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
