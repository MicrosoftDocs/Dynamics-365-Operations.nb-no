---
title: "Sette opp utvidet pålogging funksjonaliteten for skyen POS- og MPOS"
description: "Denne wikien dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Sette opp utvidet pålogging funksjonaliteten for skyen POS- og MPOS

Denne wikien dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel.

<a name="setting-up-extended-logon"></a>Definere utvidet pålogging
=========================

Kan du finne oppsettet for strekkodemasker på **detaljhandel og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**Funksjonalitetsprofiler**. Hurtigkategorien **Funksjoner** inneholder følgende alternativer som er knyttet til utvidet pålogging.

### <a name="staff-bar-code-logon"></a>Strekkodepålogging for stab

Når alternativet **Strekkodepålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en strekkode.

### <a name="staff-bar-code-logon-requires-password"></a>Stabspålogging med strekkode krever passord

Når alternativet **Stabspålogging med strekkode krever passord** er aktivert, velger stabspålogging med strekkode bare arbeideren som er tilordnet til den utvidede påloggingen som vises. Arbeidere må fremdeles angi passord når dette alternativet er aktivert.

### <a name="staff-card-logon"></a>Kortpålogging for stab

Når alternativet **Kortpålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en kortleser.

### <a name="staff-card-logon-requires-password"></a>Stabspålogging med kort krever passord

Når alternativet **Stabspålogging med kort krever passord** er aktivert, velger stabspålogging med kort bare arbeideren som er tilordnet til den utvidede påloggingen som vises. Arbeidere må fremdeles angi passord når dette alternativet er aktivert.

<a name="assigning-an-extended-logon"></a>Tilordne en utvidet pålogging
===========================

Som standard kan bare ledere tilordne utvidet pålogging til arbeidere. Hvis du vil tilordne utvidet pålogging, kan du gå til **utvidet Logg på** i POS. Deretter Søk for en arbeider ved å angi hans eller hennes operatør-ID i søkefeltet. Velg arbeideren, og klikk deretter **Tilordne**. Dra eller skann utvidet pålogging for å tilordne arbeideren på neste side. Hvis dra eller skanning blir lest, blir **OK **-knappen tilgjengelig. Klikk **OK** for å lagre den utvidede påloggingen for denne arbeideren.

<a name="deleting-an-extended-logon"></a>Slette en utvidet pålogging
==========================

Du kan slette den utvidede påloggingen som er tilordnet til en arbeider, ved å søke etter arbeideren ved hjelp av **Utvidet pålogging** operasjonen. Velg arbeideren, og klikk deretter **Ikke tilordnet**. All utvidet påloggingslegitimasjon som er knyttet til denne arbeider fjernes.

<a name="extending-extended-logon"></a>Utvide utvidet pålogging
========================

Påloggingstjenesten kan utvides for å støtte flere utvidede påloggingsenheter, for eksempel håndholdte skannere. Hvis du vil ha mer informasjon, kan du se i dokumentasjonen for utvidelsesmuligheter for salgssted.

<a name="using-extended-logon"></a>Bruke utvidet pålogging
====================

Når utvidet pålogging er konfigurert, og en arbeider er tilordnet til en strekkode eller magnetstripe, trenger arbeideren bare å dra eller skanne hans eller hennes kort mens Salgsstedets påloggingsside vises. Hvis et passord kreves også før pålogging kan fortsette, blir arbeideren bedt om å angi passordet sitt.


