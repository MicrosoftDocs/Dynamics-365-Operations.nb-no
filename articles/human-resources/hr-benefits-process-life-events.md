---
title: Behandle levetidshendelser
description: I løpet av den ansattes livssyklus i Microsoft Dynamics 365 Human Resources kan hver ansatt støte på forskjellige endringer av levetidshendelser.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42b7e2606bca4bb5eda1c9bfc7940f9067c4b943
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113669"
---
# <a name="process-life-events"></a>Behandle levetidshendelser

I løpet av den ansattes livssyklus i Microsoft Dynamics 365 Human Resources kan hver ansatt støte på forskjellige endringer av levetidshendelser. For eksempel giftermål, endring i ansettelse eller endring av avhengig/mottaker. Hvis du vil bruke levetidhendelser, må du aktivere levetidshendelser i skjemaet for fordelsparametere, definere livshendelsestyper og konfigurere livshendelsesalternativer for plantyper.

Før du kan behandle livshendelser, må du allerede kjøre åpen registrering minst én gang i løpet av en tidsramme for ansettelsen. I USA blir det vanligvis åpen registrering én gang per år. Utenfor USA kan åpen registrering kjøres på ansettelsestidspunktet. En arbeider trenger ikke å velge en fordelsplan for at levetidshendelser skal behandles, men de må være inkludert i åpen registreringsbehandling. 

Bruk behandling av levetidshendelser når du har arbeidere som har livshendelser som inntreffer på en fremtidig dato. Denne hendelsen behandler alle levetidshendelser som ikke er behandlet (for eksempel fremtidige levetidshendelser, eller levetidshendelser som ikke er spesifikke for én arbeider – ett eksempel er en ny fordel). Livshendelser i sanntid skjules.

Hvis for eksempel i dag er 1. februar, og den 14. februar er arbeideren Jon Nilsen planlagt å endre juridiske enheter, hvis du kjører behandling av levetid for den 15. februar, behandler systemet alle hendelsene inntil 15. februar. 

1. I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av levetidshendelse**.

2. I dialogboksen **Kjør prosess for levetidshendelse** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Registreringsperiode** | Registreringsperioden som det skal behandles levetidshendelser for. |
   | **Juridisk enhet** | Den juridiske enheten som det skal behandles levetidshendelser for. |
   | **Levetidshendelsesdato** | Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen. |
   | **Arbeider** | Arbeideren som det skal behandles levetidshendelser for. Hvis du lar dette feltet stå tomt, blir livshendelser behandlet for alle arbeidere. |

3. Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for prosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Prosessen vil kjøre med parameterne du angir.

4. Velg **OK**.
