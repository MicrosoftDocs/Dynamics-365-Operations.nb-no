---
title: Konfigurere finansposteringsgrupper for merverdiavgift
description: Merverdiavgiften beregnes og posteres til hovedkontoer som er angitt i finansposteringsgrupper.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30870ea17ea73e48467698166ba14a9184f5a3b1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144818"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Konfigurere finansposteringsgrupper for merverdiavgift

[!include [banner](../../includes/banner.md)]

Merverdiavgiften beregnes og posteres til hovedkontoer som er angitt i finansposteringsgrupper. Finansposteringsgrupper er tilknyttet hver mva-kode. Du kan angi individuelle finansposteringsgrupper for hver mva-kode, bruke én finansposteringsgruppe for alle mva-koder eller tilordne flere finansposteringsgrupper til mva-kodene. Denne registreringen bruker demonstrasjonsfirmaet DEMF. 

1. Gå til **Navigasjonsrute > Moduler > Avgift > Oppsett > Merverdiavgift > Finansposteringsgrupper**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Finansposteringsgruppe**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg hovedkontoen for utgående merverdiavgift som betales til skattemyndighetene, i feltet **Konto, utgående mva**. Merverdiavgift innkreves på vegne av skattemyndighetene når du selger avgiftspliktige varer og tjenester.  
6. Velg hovedkontoen for inngående merverdiavgift som mottas fra skattemyndighetene, i feltet **Innkommende merverdiavgift**. Leverandører samler inn avgifter på vegne av skattemyndighetene når du kjøper avgiftspliktige varer og tjenester. Dette feltet er ikke tilgjengelig hvis alternativet Bruk avgiftsregler for merverdiavgift er valgt på siden **Økonomiparametere**. I stedet blir mva som betales til leverandører, debitert til den samme kontoen som kjøpet.   
7. I feltet **Use tax-utgift** velger du hovedkontoen for postering av fradragsberettiget mva som ikke er gjort krav på eller rapportert til skattemyndighetene av leverandørene som en del av EU snudd avregning for GST/HST. Alternativet **Use tax** må velges for **mva-koden** i **mva-gruppen** som skal brukes i transaksjonen. Dette feltet er ikke tilgjengelig hvis alternativet **Bruk avgiftsregler for merverdiavgift** er valgt på siden **Økonomiparametere**.   
8. Velg hovedkontoen for postering av inngående use tax som betales til skattemyndighetene, i feltet **Forfalt use tax**. Alternativet **Use tax** må velges i **mva-koden** i **mva-gruppen** for å kontere **Use tax**. Hvis alternativet **Bruk avgiftsregler for merverdiavgift** er valgt i **Økonomiparametere**, posteres forskyvningen til utgiftskonto for transaksjonen.   
9. I **Utligningskonto**-feltet velger du hovedkontoen der nettosaldoen for finanskontoene angav i feltene **Forfalt use tax** og **Innkommende merverdiavgift**, blir postert. Saldoen opprettes når du utligner merverdiavgiften og posteringsjobben er kjørt.  Hvis skattemyndighetene for utligningsperioden er knyttet til en leverandørkonto, posteres saldoen i stedet til leverandørkontoen.
10. Velg hovedkontoen for å postere kontorabatt for mva-koder knyttet til denne finansposteringsgruppen, i feltet **Leverandørkontantrabatt**. Dette er valgfritt, og hvis ingen kontoer angis, brukes hovedkontoen i **kontantrabattkoder**. Det kan være nyttig å bruke ulike kontoer per **finansposteringsgruppe** hvis du bruker alternativet Tilbakefør merverdiavgift på kontantrabatt på mva-grupper.  
11. Velg hovedkontoen for å postere kontorabatt for **mva-koder** knyttet til denne **finansposteringsgruppen**, i feltet **Kundekontantrabatt**. Dette er valgfritt, og hvis ingen kontoer angis, brukes hovedkontoen i **kontantrabattkoder**. Det kan være nyttig å bruke ulike kontoer per **finansposteringsgruppe** hvis du bruker alternativet Tilbakefør merverdiavgift på kontantrabatt på **mva-grupper**.  
12. Klikk **Lagre**.

