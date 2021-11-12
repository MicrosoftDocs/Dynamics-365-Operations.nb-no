---
title: Posteringskontoer for anskaffelse av anleggsmiddel
description: Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7718ab6ad40dd135a79d2d07def19465aef68b33
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675030"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>Posteringskontoer for anskaffelse av anleggsmiddel

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler.

Kontoene som brukes for postering av anskaffelse av anleggsmidler, kan variere avhengig av metoden som brukes til å ansaffe anleggsmidlet. På siden Posteringsprofiler for anleggsmidler, i kategorien Finanskontoer, velger du Anskaffelse og Anskaffelsesjustering for å definere anleggsmiddelkontoer som posteres til finans. 

I journalen og på bestillinger er Finanskonto vanligvis balansekontoen, der anskaffelsesverdien til det nye anleggsmiddelet debiteres. Denne kontoen vises ikke i journalen og kan ikke erstattes i transaksjoner. 

Motkonto er også en balansekonto. I den generelle journalen og anleggsmiddeljournalen brukes ofte denne kontoen som bankkontoen til å betale for anskaffelsen av varen. Motkontoen er en standardkonto, noe som foreslås i journalen. I journalen kan du endre den til enhver konto fra kontoplanen eller til en leverandørkonto hvis anleggsmidlet ble kjøpt fra en leverandør. 

Når Fakturajournal eller Bestillinger i Leverandører brukes til anskaffelse av anleggsmidler, erstattes motkontoen for anleggsmiddeltransaksjonen av leverandørkontoen som er valgt for transaksjonen.

Når det gjelder anskaffelser som er postert via journalen Lager til anleggsmidler i Økonomimodul, blir ikke anleggsmidlene kjøpt fra ekstern kilder, men overføres fra firmaets eget lager. Derfor er motkontoen en lageravgangskonto for lagervaren i Lagerstyring.

Hvis du vil ha mer informasjon, se [Skaffe anleggsmidler ved hjelp av innkjøp](acquire-assets-procurement.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
