---
title: "Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS"
description: "Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 499fd5947a96f4a44f09883d5dd0d6124758e47a
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS

[!include[banner](includes/banner.md)]


Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel.

<a name="setting-up-extended-logon"></a>Definere utvidet pålogging
=========================

Du kan finne oppsettet for strekkodemasker på **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Funksjonalitetsprofiler**. Hurtigkategorien **Funksjoner** inneholder følgende alternativer som er knyttet til utvidet pålogging.

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

Som standard kan bare ledere tilordne utvidet pålogging til arbeidere. Hvis du vil tilordne utvidet pålogging, kan du gå til **Utvidet pålogging** i POS. Søk deretter etter en arbeider ved å angi hans eller hennes operatør-ID i søkefeltet. Velg arbeideren, og klikk deretter **Tilordne**. Dra eller skann utvidet pålogging for å tilordne arbeideren på neste side. Hvis dra eller skanning blir lest, blir **OK**-knappen tilgjengelig. Klikk **OK** for å lagre den utvidede påloggingen for denne arbeideren.

<a name="deleting-an-extended-logon"></a>Slette en utvidet pålogging
==========================

Du kan slette den utvidede påloggingen som er tilordnet til en arbeider, ved å søke etter arbeideren ved hjelp av **Utvidet pålogging** operasjonen. Velg arbeideren, og klikk deretter **Ikke tilordnet**. All utvidet påloggingslegitimasjon som er knyttet til denne arbeider fjernes.

<a name="extending-extended-logon"></a>Utvide utvidet pålogging
========================

Påloggingstjenesten kan utvides for å støtte flere utvidede påloggingsenheter, for eksempel håndholdte skannere. Hvis du vil ha mer informasjon, kan du se i dokumentasjonen for utvidelsesmuligheter for salgssted.

<a name="using-extended-logon"></a>Bruke utvidet pålogging
====================

Når utvidet pålogging er konfigurert, og en arbeider er tilordnet til en strekkode eller magnetstripe, trenger arbeideren bare å dra eller skanne hans eller hennes kort mens Salgsstedets påloggingsside vises. Hvis et passord kreves også før pålogging kan fortsette, blir arbeideren bedt om å angi passordet sitt.




