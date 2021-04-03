---
title: Fordelsregistreringsrettighet
description: Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 25699d643b3e74fe7118884457ab17314d1f9132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466308"
---
# <a name="process-enrollment-eligibility"></a>Fordelsregistreringsrettighet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.

1. I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av registreringsrettighet**.

2. I dialogboksen **Kjør prosess for fordelsregistreringsrettighet** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Registreringsperiode** | Registreringsperioden som det skal behandles registreringsrettigheter for. |
   | **Juridisk enhet** | Den juridiske enheten som det skal behandles registreringsrettigheter for. |
   | **Arbeider** | Arbeideren som det skal behandles registreringsrettigheter for. Hvis du lar dette feltet stå tomt, blir registreringsrettigheten behandlet for alle arbeidere. |
   | **Fordelsplan** | Fordelsplanen som det skal behandles registreringsrettigheter for.

3. Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for prosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Prosessen vil kjøre med parameterne du angir.

4. Velg **OK**.

## <a name="view-process-results"></a>Vis prosessresultater

Denne artikkelen beskriver hvordan du viser resultater av en rettighetsprosess.

1.  I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Prosessresultater**.

2.  Følgende felt er angitt i skjemaet **Prosessresultater**:

   | Felt | beskrivelse |
   | --- | --- |
   | **Prosess-ID** | Den unike ID-en for kombinasjonen av arbeider, juridisk enhet og prosesskjøring. |
   | **Prosesstype** | Dette identifiserer prosessen som ble kjørt. Eksempel: Registrering. |
   | **Tidsangivelse** | Tidspunktet da rettighetsprosessen ble kjørt. |
   | **Juridisk enhet** | Den juridiske enheten som ble angitt under registreringsprosessen. |
   | **Worker** | Arbeideren som ble behandlet. |
   | **Plan | Fordelsplanen som registreringen ble forsøkt utført for. |
   | **Rettighetsregel** | Rettighetsregelen som ble behandlet. Hvis det oppstod en feil før rettigheten ble kjørt, vil dette være tomt. Eksempel: Hvis kompensasjon ikke er definert for en arbeider, kan ikke rettighetsprosessen kjøres, og dette feltet blir stående tomt. |
   | **Resultatstatus** | Dette vil være Kvalifisert eller Ikke kvalifisert. Resultatstatusen vil være Ikke kvalifisert hvis arbeideren ikke oppfyller rettighetsregelkriteriene, hvis arbeideren mangler nødvendig informasjon, for eksempel en betalingsfrekvens eller fast kompensasjon, eller hvis det mangler informasjon i fordelsplanen, og som forhindrer at arbeidere registreres. |
   | **Resultatmelding** | Indikerer hvorfor en arbeider ikke er kvalifisert for en fordelsplan, eller om rettighetsregelen ble bestått. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]