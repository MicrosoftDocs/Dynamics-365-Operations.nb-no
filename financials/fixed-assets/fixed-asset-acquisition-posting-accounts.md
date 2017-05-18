---
title: Posteringskontoer for anskaffelse av anleggsmidler
description: "Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 124aa1aec7ff2cee51128ab0bc10e7f679414157
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Posteringskontoer for anskaffelse av anleggsmidler

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler.

Kontoene som brukes for postering av anskaffelse av anleggsmidler, kan variere avhengig av metoden som brukes til å ansaffe anleggsmidlet. På siden Posteringsprofiler for anleggsmidler, i kategorien Finanskontoer, velger du Anskaffelse og Anskaffelsesjustering for å definere anleggsmiddelkontoer som posteres til finans. 

I journalen og på bestillinger er Finanskonto vanligvis balansekontoen, der anskaffelsesverdien til det nye anleggsmiddelet debiteres. Denne kontoen vises ikke i journalen og kan ikke erstattes i transaksjoner. 

Motkonto er også en balansekonto. I den generelle journalen og anleggsmiddeljournalen brukes ofte denne kontoen som bankkontoen til å betale for anskaffelsen av varen. Motkontoen er en standardkonto, noe som foreslås i journalen. I journalen kan du endre den til enhver konto fra kontoplanen eller til en leverandørkonto hvis anleggsmidlet ble kjøpt fra en leverandør. 

Når Fakturajournal eller Bestillinger i Leverandører brukes til anskaffelse av anleggsmidler, erstattes motkontoen for anleggsmiddeltransaksjonen av leverandørkontoen som er valgt for transaksjonen.

Når det gjelder anskaffelser som er postert via journalen Lager til anleggsmidler i Økonomimodul, blir ikke anleggsmidlene kjøpt fra ekstern kilder, men overføres fra firmaets eget lager. Derfor er motkontoen en lageravgangskonto for lagervaren i Lagerstyring.

Hvis du vil ha mer informasjon, se [Skaffe anleggsmidler ved hjelp av innkjøp](acquire-assets-procurement.md).




