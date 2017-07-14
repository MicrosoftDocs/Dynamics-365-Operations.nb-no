---
title: "Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS"
description: "Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0b7e5ed451497aea1c2ce798af2b717705538d47
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017



---

# Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS
<a id="set-up-extended-logon-functionality-for-cloud-pos-and-mpos" class="xliff"></a>

[!include[banner](includes/banner.md)]


Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel.

Definere utvidet pålogging
<a id="setting-up-extended-logon" class="xliff"></a>
=========================

Du kan finne oppsettet for strekkodemasker på **Retail** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Funksjonalitetsprofiler**. Hurtigkategorien **Funksjoner** inneholder følgende alternativer som er knyttet til utvidet pålogging.

### Strekkodepålogging for stab
<a id="staff-bar-code-logon" class="xliff"></a>

Når alternativet **Strekkodepålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en strekkode.

### Stabspålogging med strekkode krever passord
<a id="staff-bar-code-logon-requires-password" class="xliff"></a>

Når alternativet **Stabspålogging med strekkode krever passord** er aktivert, velger stabspålogging med strekkode bare arbeideren som er tilordnet til den utvidede påloggingen som vises. Arbeidere må fremdeles angi passord når dette alternativet er aktivert.

### Kortpålogging for stab
<a id="staff-card-logon" class="xliff"></a>

Når alternativet **Kortpålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en kortleser.

### Stabspålogging med kort krever passord
<a id="staff-card-logon-requires-password" class="xliff"></a>

Når alternativet **Stabspålogging med kort krever passord** er aktivert, velger stabspålogging med kort bare arbeideren som er tilordnet til den utvidede påloggingen som vises. Arbeidere må fremdeles angi passord når dette alternativet er aktivert.

Tilordne en utvidet pålogging
<a id="assigning-an-extended-logon" class="xliff"></a>
===========================

Som standard kan bare ledere tilordne utvidet pålogging til arbeidere. Hvis du vil tilordne utvidet pålogging, kan du gå til **Utvidet pålogging** i POS. Søk deretter etter en arbeider ved å angi hans eller hennes operatør-ID i søkefeltet. Velg arbeideren, og klikk deretter **Tilordne**. Dra eller skann utvidet pålogging for å tilordne arbeideren på neste side. Hvis dra eller skanning blir lest, blir **OK**-knappen tilgjengelig. Klikk **OK** for å lagre den utvidede påloggingen for denne arbeideren.

Slette en utvidet pålogging
<a id="deleting-an-extended-logon" class="xliff"></a>
==========================

Du kan slette den utvidede påloggingen som er tilordnet til en arbeider, ved å søke etter arbeideren ved hjelp av **Utvidet pålogging** operasjonen. Velg arbeideren, og klikk deretter **Ikke tilordnet**. All utvidet påloggingslegitimasjon som er knyttet til denne arbeider fjernes.

Utvide utvidet pålogging
<a id="extending-extended-logon" class="xliff"></a>
========================

Påloggingstjenesten kan utvides for å støtte flere utvidede påloggingsenheter, for eksempel håndholdte skannere. Hvis du vil ha mer informasjon, kan du se i dokumentasjonen for utvidelsesmuligheter for salgssted.

Bruke utvidet pålogging
<a id="using-extended-logon" class="xliff"></a>
====================

Når utvidet pålogging er konfigurert, og en arbeider er tilordnet til en strekkode eller magnetstripe, trenger arbeideren bare å dra eller skanne hans eller hennes kort mens Salgsstedets påloggingsside vises. Hvis et passord kreves også før pålogging kan fortsette, blir arbeideren bedt om å angi passordet sitt.




