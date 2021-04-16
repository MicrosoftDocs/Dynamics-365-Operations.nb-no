---
title: Konfigurere alternativer for personlige kontaktrettigheter
description: Konfigurer rettighetsalternativer for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790890"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurere alternativer for personlige kontaktrettigheter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikkelen får du vite hvordan du konfigurerer typer personlige kontakter som skal brukes i fordeler i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige. 

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