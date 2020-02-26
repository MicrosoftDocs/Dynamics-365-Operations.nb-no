---
title: Konfigurere alternativer for personlige kontaktrettigheter
description: Konfigurer rettighetsalternativer for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010093"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurere alternativer for personlige kontaktrettigheter

[!include [banner](includes/preview-feature.md)]

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
