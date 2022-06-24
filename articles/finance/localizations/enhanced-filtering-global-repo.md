---
title: Forbedret RCS-filtrering i RCS/det globale repositoriet
description: Denne artikkelen beskriver forbedrede filtreringsfunksjoner for det det globale repositoriet RCS som er forbedret for å inkludere tilleggsfiltrene.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a343b9f1af68a727cb2a8d1e390f85e10aab2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901219"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Forbedrede RCS-filtreringsalternativer for å finne konfigurasjoner i RCS/det globale repositoriet

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver forbedrede filtreringsfunksjoner for det det globale repositoriet Regulatory Configuration Services (RCS) som er forbedret for å inkludere muligheten til å filtrere med følgende kriterier: 
- **Land/område**– basert på ISO-landskoder  
- **Kode**-typer for:
  - Funksjonelt område
  - Funksjonsområde
  - Bransje 
  - Forretningsdokument 

Du kan bruke filtre, enten individuelt eller i grupper, for å gjøre det lettere å finne bestemte eller relaterte konfigurasjoner. Hvis du for eksempel vil finne en enkelt type konfigurerbare forretningsdokumenter som er relatert til leverandørfakturaer, kan du bruke et **Forretningsdokumenttype**-filter for å søke etter denne dokumenttypen. 

[![Filterdel for det globale repositoriet.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Du kan finjustere søket ytterligere ved å velge dokumenttype, for eksempel "leverandørfaktura", og klikke **Bruk filter**. Følgende eksempel viser resultatene ved filtrering på **Forretningsdokumenttype** med dokumenttypen lagt til. 

[![Brukte filter og import for forretningsdokumenttype.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrerte resultater kan importeres til en brukers RCS-repositorium eller et Dynamics 365 Finance-miljø, enten individuelt eller som et sett. Dette gjør du ved å velge konfigurasjonsgruppen og klikke **Importer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]