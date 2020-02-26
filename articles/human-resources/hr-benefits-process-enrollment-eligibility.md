---
title: Fordelsregistreringsrettighet
description: Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010017"
---
# <a name="process-enrollment-eligibility"></a>Fordelsregistreringsrettighet

[!include [banner](includes/preview-feature.md)]

Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.

1. I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av registreringsrettighet**.

2. I dialogboksen **Kjør prosess for fordelsregistreringsrettighet** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | Registreringsperiode | Registreringsperioden som det skal behandles registreringsrettigheter for. |
   | Juridisk enhet | Den juridiske enheten som det skal behandles registreringsrettigheter for. |
   | Arbeider | Arbeideren som det skal behandles registreringsrettigheter for. Hvis du lar dette feltet stå tomt, blir registreringsrettigheten behandlet for alle arbeidere. |
   | Fordelsplan | Fordelsplanen som det skal behandles registreringsrettigheter for.

3. Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for prosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Prosessen vil kjøre med parameterne du angir.

4. Velg **OK**.
