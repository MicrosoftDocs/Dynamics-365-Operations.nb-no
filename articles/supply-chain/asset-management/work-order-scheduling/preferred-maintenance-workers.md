---
title: Definer foretrukne vedlikeholdspersoner
description: Dette emnet forklarer hvordan du definerer foretrukne vedlikeholdspersoner i Aktivastyring.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511d875baed029df9083da36baf6c48ca4b7abf866ae569038b554bf594473c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734433"
---
# <a name="set-up-preferred-maintenance-workers"></a>Definer foretrukne vedlikeholdspersoner

[!include [banner](../../includes/banner.md)]

 

Under planlegging av arbeidsordrer kan du angi hvilke vedlikeholdspersoner eller hvilken arbeidsgruppe som foretrekkes til å fullføre arbeidsordren. Bruk av denne funksjonaliteten er valgfri, men den kan hjelpe deg med å velge vedlikeholdspersonen som er mest kvalifisert for å fullføre en jobb, basert på arbeiderkompetanse. Bare vedlikeholdspersoner som er tilgjengelige på planleggingstidspunktet, vil bli planlagt. Hvis et oppsett av foretrukken vedlikeholdsperson samsvarer med en arbeidsordre under planlegging, men vedlikeholdspersonen er tilordnet andre jobber, blir arbeidsordren planlagt til en annen, tilgjengelig vedlikeholdsperson.

Før du kan definere foretrukne vedlikeholdspersoner, må du først definere vedlikeholdspersonene og arbeidsgruppene. Se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md) hvis du vil ha en beskrivelse av hvordan du definerer vedlikeholdspersoner og arbeidsgrupper.

## <a name="set-up-preferred-workers"></a>Definere foretrukne arbeidere

En foretrukket vedlikeholdsperson eller arbeidsgruppe kan knyttes til én eller flere av følgende:

- handel  
- variant av vedlikeholdsjobbtype  
- type vedlikeholdsjobb  
- kategori for type vedlikeholdsjobb  
- eiendeler  
- aktivumtype  

Jo flere valg du gjør for den samme posten, jo mer spesifikt blir oppsettet.

1. Klikk på **Aktivastyring** > **Oppsett** > **Arbeidere** > **Foretrukne vedlikeholdspersoner**.

2. Klikk på **Ny** for å opprette en ny post.

3. Start ved å opprette en "standard" vedlikeholdsperson eller arbeidsgruppe. Dette betyr at du bare gjør et valg i feltet **Foretrukket vedlikeholdspersongruppe** eller feltet **Foretrukket vedlikeholdsperson**. I skjermdumpen nedenfor ser du et eksempel i den første posten der "Forespørsler" er valgt som **Foretrukket vedlikeholdspersongruppe**.

    [!NOTE] Standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren.

4. Gjenta trinn 2 for å opprette en ny post. Gjør de nødvendige valgene, avhengig av detaljnivået for den foretrukne arbeideren eller arbeidsgruppen. 

    *Eksempel:* I skjermdumpen nedenfor i den sjette posten er vedlikeholdspersonen Shawn Richardson valgt som foretrukket arbeider. Han velges automatisk under planlegging av en arbeidsordre som inneholder aktivumet "CH-BP1-03-02" og vedlikeholdsjobbtypen "Fasilitetsvurdering" hvis han er tilgjengelig på det planlagte tidspunktet.

    [!NOTE] Når en foretrukket vedlikeholdsperson velges under planlegging av arbeidsordre, går vanligvis Aktivastyring gjennom alle **Foretrukne vedlikeholdspersoner**-postene for å se etter et mulig treff, og kontrollerer alltid den mest spesifikke kombinasjonen først. Hvis det ikke blir funnet noe treff, brukes standardposten med et valg i enten feltet **Foretrukket vedlikeholdsarbeidsgruppe** eller feltet **Foretrukket vedlikeholdsperson**.

![Figur 1.](media/02-work-order-scheduling.png)

Du kan også definere *ansvarlige* vedlikeholdspersoner som kan velges når en vedlikeholdsforespørsel eller arbeidsordre opprettes. I **Alle arbeidsordrer** og **Alle vedlikeholdsforespørsler** kan du redigere valget hvis det er nødvendig. Se [Ansvarlige vedlikeholdspersoner](../setup-for-maintenance-requests/responsible-workers.md) for å få mer informasjon.

Under planleggingen av arbeidsordrer beregnes ulike poeng for å bestemme hvilke arbeidere som skal fullføre jobbene for en arbeidsordre (disse resultatene defineres i **Aktivabehandlingsparametere** > **Planlegging av arbeidsordre**-koblingen). Hvis to eller flere foretrukne vedlikeholdspersoner eller ansvarlige vedlikeholdspersoner får samme resultat under planleggingen av arbeidsordre, blir én arbeider tilfeldig valgt. Ellers er det alltid arbeideren med den høyeste poengsummen som tilordnes for å fullføre en arbeidsordre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]