---
title: Opprette innkjøpspolicyer
description: Denne fremgangsmåten viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "312905"
---
# <a name="create-purchasing-policies"></a>Opprette innkjøpspolicyer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp. Før du kan opprette innkjøpspolicyer, må du definere parametere for innkjøpspolicy. Det er mulig å opprette, endre og avslutte en innkjøpspolicy, men du kan ikke slette en innkjøpspolicy. Denne fremgangsmåten utføres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-policy-parameters"></a>Angi policyparametere
1. Gå til Innkjøpspolicyer.
2. Klikk Parametere.
    * Regler for policyprioritet gjelder for forskjellige nivåer i organisasjonen. Organisasjonsenheter som vises avhengig av din organisasjonshierarkiet og på hvilke nivåer i hierarkiet de er tilordnet formålet Internkontroll av innkjøp. Organisasjonen har for eksempel kanskje juridiske enheter, kostsentre, områder og avdelinger, men det kan hende at noen av disse har hierarkiformålet Internkontroll av innkjøp. Organiseringen av typen Firma er tilgjengelig som standard.  
3. Klikk kategorien Parametere for policyregeltype.
4. Velg Innkjøpspolicy\Kontrollregel for innkjøpsrekvisisjon i treet.
    * Du definerer prioritetsrekkefølgen for policyløsning på policynivået. For enkelte policytyper kan du imidlertid overstyre prioritetsrekkefølgen for individuelle policyregeltyper. La oss si at du vil definere prioritetsrekkefølgen for innkjøpspolicyer slik: kostsenter, avdeling, firma. For katalogpolicyregelen vil du imidlertid at prioritetsrekkefølgen skal være: avdeling, kostsenter, firma. Du kan endre prioritetsrekkefølgen for katalogpolicyregelen. Når en arbeider oppretter en rekvisisjon, vil katalogen som vises, bestemmes av policyene som er knyttet til arbeiderens avdeling, deres kostsenter og deretter firmaet.  
    * Hvis det ikke er oppført mer enn ett organisasjonsnivå, kan du bruke pil opp eller pil ned for å angi prioritetsrekkefølgen for Kontrollregel for innkjøpsrekvisisjon.  
5. Lukk siden.

## <a name="create-a-new-policy"></a>Opprett en ny policy
1. Klikk Ny.
2. Skriv inn en verdi i Navn-feltet.
3. Skriv inn en verdi i feltet Beskrivelse.
    * Én enkelt innkjøpspolicy kan bare gjelde for ett organisasjonshierarki. Du kan for eksempel ha ett hierarki som kalles Geografisk og ett som kalles Avdeling, og har en forskjellig innkjøpspolicy for hver av dem.  
    * Velg en organisasjon som policyen skal gjelde for.  
4. Klikk pilen for å legge til den valgte organisasjonen.
    * Du kan gjenta denne prosessen for å legge til flere organisasjoner.  

## <a name="add-a-policy-rule"></a>Legge til en policyregel
1. Velg Regel for rekvisisjonsformål i listen Type policyregel.
    * Du oppretter en regel som setter standardformål for rekvisisjonen til Forbruk, men tillater at Etterfylling-typen velges i stedet.  
2. Klikk Opprett policyregel.
3. Velg Ja i feltet Tillat manuell overstyring.
4. Klikk Lukk.
    * Nå kan du definere andre policyregler for innkjøpspolicyen.   Legg merke til at en policyregeltype ikke kan ha overlappende regler som er aktive samtidig i én enkelt innkjøpspolicy.  
5. Lukk siden.
6. Lukk siden.

