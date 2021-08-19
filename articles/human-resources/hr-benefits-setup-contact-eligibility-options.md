---
title: Konfigurere alternativer for personlige kontaktrettigheter
description: Konfigurer rettighetsalternativer for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50f290bbf53c70a7b33d061aaa80a9a1b3583d2c0fc2bb15f31f877b611187cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735381"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurere alternativer for personlige kontaktrettigheter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emnet får du vite hvordan du konfigurerer typer personlige kontakter som skal brukes i fordeler i Microsoft Dynamics 365 Human Resources. Personlige kontakter er personene som vil bli dekket under planene dine (avhengige) eller som har nytte av planene (mottakere). Avhengige er vanligvis ektefeller eller barn. Mottakere kan være ektefeller, barn, klareringer eller foreldre.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Alternativer for rettighet for personlig kontakt**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Rettighetsalternativ** | Et unikt navn på et rettighetsalternativ eller en kode som identifiserer rettighetsalternativet. |
   | **Beskrivelse** | En kort beskrivelse av rettighetsalternativet. |
   | **Rettighetskode for kontakt** | Systemkoden som best beskriver det personlige rettighetsalternativet. Du kan velge blant: <ul><li>Relasjon</li><li>Student</li><li>Overårig avhengig</li><li>Overårig avhengig som er ufør</li></ul> |
   | **Status** | Statusen for rettighetsalternativet. Hvis statusen for et rettighetsalternativ er satt til Inaktiv, kan du ikke velge dette rettighetsalternativet for personlige kontakter. |
   | **Relasjon** | Angir relasjonen mellom den personlige kontakten og den ansatte. Dette feltet er bare aktivt hvis kontaktrettighetskoden er satt til Relasjon. |
   | **Alder** | Maksimal alder på en personlig kontakt for fordelsplanen. Dette feltet er bare aktivt hvis du velger en relasjon. Denne alderen sammenlignes med den beregnede alderen på den personlige kontakten. Beregnet alder er: (dekningsdato – fødselsdato for personlig kontakt / 365). Dette tallet er alltid et heltall. |

4. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
