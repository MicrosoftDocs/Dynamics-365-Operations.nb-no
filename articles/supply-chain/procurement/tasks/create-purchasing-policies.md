---
title: Opprette innkjøpspolicyer
description: Dette emnet viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp.
author: RichardLuan
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8d29f4bd5840ff70fd918a05d68aa043216e27f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211916"
---
# <a name="create-purchasing-policies"></a>Opprette innkjøpspolicyer

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp. Før du kan opprette innkjøpspolicyer, må du definere parametere for innkjøpspolicy. Det er mulig å opprette, endre og avslutte en innkjøpspolicy, men du kan ikke slette en innkjøpspolicy. Denne fremgangsmåten utføres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-policy-parameters"></a>Angi policyparametere
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer**.
2. Velg **Parametere** i handlingsruten.
- Regler for policyprioritet gjelder for forskjellige nivåer i organisasjonen. Organisasjonsenheter som vises avhengig av din organisasjonshierarkiet og på hvilke nivåer i hierarkiet de er tilordnet formålet Internkontroll av innkjøp. Organisasjonen har for eksempel kanskje juridiske enheter, kostsentre, områder og avdelinger, men det kan hende at noen av disse har hierarkiformålet Internkontroll av innkjøp. Organiseringen av typen Firma er tilgjengelig som standard.  
3. Velg fanen **Parametere for policyregeltype**.
4. I treet går du til **Velg Innkjøpspolicy > Kontrollregel for innkjøpsrekvisisjon**.
- Du definerer prioritetsrekkefølgen for policyløsning på policynivået. For enkelte policytyper kan du imidlertid overstyre prioritetsrekkefølgen for individuelle policyregeltyper. La oss si at du vil definere prioritetsrekkefølgen for innkjøpspolicyer slik: kostsenter, avdeling, firma. For katalogpolicyregelen vil du imidlertid at prioritetsrekkefølgen skal være: avdeling, kostsenter, firma. Du kan endre prioritetsrekkefølgen for katalogpolicyregelen. Når en arbeider oppretter en rekvisisjon, vil katalogen som vises, bestemmes av policyene som er knyttet til arbeiderens avdeling, deres kostsenter og deretter firmaet.  
- Hvis det ikke er oppført mer enn ett organisasjonsnivå, kan du bruke pil opp eller pil ned for å angi prioritetsrekkefølgen for Kontrollregel for innkjøpsrekvisisjon.  
5. Lukk siden.

## <a name="create-a-new-policy"></a>Opprett en ny policy
1. Velg **Ny**.
2. Skriv inn en verdi i **Navn**-feltet.
3. Skriv inn en verdi i **Beskrivelse**-feltet.
- Én enkelt innkjøpspolicy kan bare gjelde for ett organisasjonshierarki. Du kan for eksempel ha ett hierarki som kalles Geografisk og ett som kalles Avdeling, og ha en forskjellig innkjøpspolicy for hver av dem.  
- Velg en organisasjon som policyen skal gjelde for.  
4. Velg pilen for å legge til den valgte organisasjonen.
- Du kan gjenta denne prosessen for å legge til flere organisasjoner.  

## <a name="add-a-policy-rule"></a>Legge til en policyregel
1. Velg **Regel for rekvisisjonsformål** i listen **Type policyregel**.
- Du oppretter en regel som setter standardformål for rekvisisjonen til Forbruk, men tillater at Etterfylling-typen velges i stedet.  
2. Velg **Opprett policyregel**.
3. Velg **Ja** i feltet **Tillat manuell overstyring**.
4. Velg **Lukk**.
- Nå kan du definere andre policyregler for innkjøpspolicyen. Legg merke til at en policyregeltype ikke kan ha overlappende regler som er aktive samtidig i én enkelt innkjøpspolicy.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]