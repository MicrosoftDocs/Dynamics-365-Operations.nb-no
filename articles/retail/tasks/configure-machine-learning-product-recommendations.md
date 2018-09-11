--- 
title: " Konfigurere maskinlæringsbaserte produktanbefalinger"
description: "Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter."
author: ashishmsft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

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


