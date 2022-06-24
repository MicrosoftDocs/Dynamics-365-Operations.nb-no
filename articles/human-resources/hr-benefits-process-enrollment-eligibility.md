---
title: Fordelsregistreringsrettighet
description: Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c01d7a6f456514fc9da1889ccaff5af1ae7c0f52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877750"
---
# <a name="process-enrollment-eligibility"></a>Fordelsregistreringsrettighet


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

2.  Følgende felter er angitt på siden **Prosessresultater**:

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
