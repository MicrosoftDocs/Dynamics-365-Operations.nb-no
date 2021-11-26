---
title: Forbedringer av ytelse for opprydding i salgshistorikk
description: Dette emnet beskriver forbedringer av ytelsen for funksjonen for salgshistorikkopprydding, og hvordan du aktiverer den.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d4eeee3c1228b278fea07464f35946c295c5aea8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679061"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Forbedringer av ytelse for opprydding i salgshistorikk

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!-- GA with 10.0.24 -->

Den periodiske satsvise jobben **Opprydding av salgsoppdateringshistorikk** kan ta lang tid hvis det kjøres sjelden i miljøer med høyt volum på salgsoppdateringer. I disse situasjonene kan funksjonen *Forbedringer av ytelse for opprydding i salgshistorikk* redusere varigheten til kjøringen og forbedre påliteligheten.

Funksjonen forbedrer den eksisterende oppryddingsjobben på følgende måter:

- Den deler oppryddingen i bunker (du kan endre bunkestørrelsen ved hjelp av tilpasninger).
- Den vil kjøre i maksimalt 2 timer (du kan endre varigheten ved hjelp av tilpasninger).
- Der det er mulig, vil den bruke databasefunksjoner for å minimere låsekonflikt og unngå å slå sammen transaksjonstabeller under opprydding.

Etter at funksjonen er aktivert, kjøres den satsvise jobben **Opprydding av salgoppdateringshistorikk** (**Salg og markedsføring \> Opprydding \> Periodeoppgaver \> Opprydding av salgsoppdateringshistorikk**) som den gjorde før, men med bedre ytelse og maksimum 2 timer. Det betyr at det kan hende at det må kjøres flere ganger for å rydde opp i alle dataene for en bestemt oppbevaringstidsramme.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Aktiver funksjonen for forbedringer av ytelse for opprydding i salgshistorikk

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Salg og markedsføring*
- **Funksjonsnavn:** *Forbedringer av ytelse for opprydding i salgshistorikk*