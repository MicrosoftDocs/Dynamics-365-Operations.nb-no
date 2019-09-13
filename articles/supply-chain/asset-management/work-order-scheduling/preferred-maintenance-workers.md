---
title: Definer foretrukne vedlikeholdspersoner
description: Dette emnet forklarer hvordan du definerer foretrukne vedlikeholdspersoner i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887417"
---
# <a name="preferred-maintenance-workers"></a>Foretrukne vedlikeholdspersoner

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan angi hvilke vedlikeholdspersoner som foretrekkes til å fullføre arbeidsordrer under planlegging av arbeidsordrer. Bruk av denne funksjonaliteten er valgfri, men den kan hjelpe deg med å velge vedlikeholdspersonen som er mest kvalifisert for å fullføre en jobb, basert på arbeiderkompetanse. I planleggingen av arbeidsordrer blir derfor oppsettet i **Foretrukne vedlikeholdspersoner** brukt til å avgjøre om en bestemt vedlikeholdsperson eller arbeidsgruppe skal planlegges for en arbeidsordre. Bare vedlikeholdspersoner som er tilgjengelige på planleggingstidspunktet, vil bli planlagt. Hvis et oppsett av foretrukken vedlikeholdsperson samsvarer med en arbeidsordre under planlegging, men vedlikeholdspersonen er tilordnet andre jobber, blir arbeidsordren planlagt til en annen, tilgjengelig vedlikeholdsperson.

Før du kan definere foretrukne vedlikeholdsarbeidere, må du først definere vedlikeholdsarbeidere og vedlikeholdsarbeidergrupper som skal være tilgjengelige for valg. Se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md) hvis du vil ha en beskrivelse av hvordan du definerer vedlikeholdspersoner og arbeidsgrupper.

## <a name="set-up-preferred-workers"></a>Definere foretrukne arbeidere

En foretrukket vedlikeholdsperson eller arbeidsgruppe kan knyttes til en bestemt

- handel  
- variant av vedlikeholdsjobbtype  
- type vedlikeholdsjobb  
- kategori for type vedlikeholdsjobb  
- eiendeler  
- aktivumtype  

eller en kombinasjon av disse valgene. Jo flere valg du gjør for den samme posten, jo mer spesifikt blir oppsettet.

1. Klikk på **Aktivastyring** > **Oppsett** > **Arbeidere** > **Foretrukne vedlikeholdspersoner**.

2. Klikk **Ny** for å opprette en ny post.

3. Start ved å opprette et standardoppsett for vedlikeholdspersoner eller arbeidsgruppe som ikke har noen valg i feltene som vises i punktlisten ovenfor. Dette betyr at du bare gjør et valg i feltet **Foretrukket vedlikeholdspersongruppe** eller feltet **Foretrukket vedlikeholdsperson**. I figuren nedenfor ser du et eksempel i den første posten der "Forespørsler" er valgt som foretrukket vedlikeholdspersongruppe.

>[!NOTE]
>Standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren under arbeidsordreplanleggingen.

4. Gjenta trinn 2 for å opprette en ny post. Gjør de nødvendige valgene, avhengig av detaljnivået for den foretrukne arbeideren eller arbeidsgruppen. *Eksempel:* I figuren nedenfor i den sjette posten er vedlikeholdsarbeideren Shawn Richardson valgt som foretrukket arbeider. Han velges automatisk under planlegging av en arbeidsordre som inneholder aktivaet "CH-BP1-03-02" og vedlikeholdsjobbtypen "Fasilitetsvurdering" hvis han er tilgjengelig på det planlagte tidspunktet.

>[!NOTE]
>Når en foretrukket vedlikeholdsarbeider velges under planlegging av arbeidsordre, går vanligvis Aktivastyring gjennom alle **Foretrukne vedlikeholdspersoner**-postene for å se etter et mulig treff, og kontrollerer alltid den mest spesifikke kombinasjonen først. Hvis det ikke blir funnet noe treff, brukes standardposten med et valg i enten feltet **Foretrukket vedlikeholdsarbeidsgruppe** eller feltet **Foretrukket vedlikeholdsperson**.


![Figur 1](media/02-work-order-scheduling.png)

Du kan også definere ansvarlige vedlikeholdspersoner som kan velges når en vedlikeholdsforespørsel eller arbeidsordre opprettes. I **Alle arbeidsordrer** og **Alle vedlikeholdsforespørsler** kan du redigere valget hvis det er nødvendig. Se [Ansvarlige vedlikeholdsarbeidere](../setup-for-maintenance-requests/responsible-workers.md) for å få mer informasjon.

Under planleggingen av arbeidsordrer beregnes ulike poeng for å bestemme hvilke arbeidere som skal fullføre jobbene for en arbeidsordre (disse resultatene defineres i **Aktivabehandlingsparametere** > **Planlegging av arbeidsordre**-koblingen). Hvis to eller flere foretrukne vedlikeholdsarbeidere eller ansvarlige vedlikeholdsarbeidere får samme resultat under planleggingen av arbeidsordre, blir én arbeider tilfeldig valgt. Ellers er det alltid arbeideren med den høyeste poengsummen som tilordnes for å fullføre en arbeidsordre.

