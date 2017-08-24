--- 
title: " Konfigurere maskinlæringsbaserte produktanbefalinger"
description: "Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> Konfigurere maskinlæringsbaserte produktanbefalinger

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Systemadministrasjon > Oppsett > Enhetsbutikk.
2. Finn og velg posten RetailSales i listen.
3. Klikk Oppdater.
4. Klikk OK.
5. Lukk siden.
6. Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.
7. Klikk kategorien Maskinlæring.
8. Velg Ja i feltet Aktiver produktanbefalinger.
    * Hvis du får meldingen Kan ikke hente anbefalingsmodellene, er det fordi du nylig oppdaterte enhetsbutikken og systemet er kanskje ikke ferdig med å assimilere de nye dataene. Vent 2–3 timer, og prøv på nytt.  
9. Klikk Lagre.
10. Lukk siden.


