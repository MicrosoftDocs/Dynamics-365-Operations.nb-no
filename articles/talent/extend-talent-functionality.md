---
title: Utvide funksjonaliteten i Microsoft Dynamics 365 for Talent
description: Hvis du har opprettet en Microsoft PowerApps, kan du starte disse programmene fra koblinger i Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: nb-no
ms.lasthandoff: 03/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Utvide funksjonaliteten i Microsoft Dynamics 365 for Talent

[!include [banner](includes/banner.md)]

Hvis du har opprettet en Microsoft PowerApps, kan du starte disse programmene fra koblinger i Microsoft Dynamics 365 for Talent. Hvis du vil konfigurere tilgang til programmene, må du angi informasjon i Talent på en konfigurasjonsside som kan åpnes fra **Systemadministrasjon**-arbeidsområdet.

## <a name="configuring-embedded-powerapps-within-talent"></a>Konfigurere innebygd PowerApps i Talent
Bruk **Angi innebygd Microsoft PowerApps**-siden til å konfigurere Talent-sider for å starte PowerApps-programmer. Hvis du skal åpne **Angi innebygd Microsoft PowerApps**-siden, åpner du **Systemadministrasjon**-arbeidsområdet og åpner deretter **Koblinger**-fanen. Velg **Microsoft PowerApps** fra **Oppsett**-gruppen. 

Følgende informasjon angis på denne siden: 

 -  Et beskrivende navn eller en identifikator for hver PowerApps-applikasjon.
 -  En unik identifikator (GUID) for hvert program som du legger til på en Talent-side. Program-ID-en er tilgjengelig på PowerApps-området [powerapps.com](http://powerapps.com/). 
 -  Siden som brukere kan åpne et program eller en rapport fra. Ikke alle Talent-sider støtter innebygde PowerApps- og Power BI-rapporter. 

 > [!NOTE]
 >  Angi det interne navnet på siden, i stedet for visningsnavnet som vises øverst på siden. Hvis du vil finne det interne navnet, åpner du siden som du trenger det interne navnet for, og høyreklikker hvor som helst på siden. Når menyen åpnes, holder du pekeren over **Skjemainformasjon**-elementet. Det interne skjemanavnet vises ved siden av **Skjemainformasjon**-elementet på menyen.
 
-   Angi skjemakontrollen som programmet kan hente kontekstdata fra. Et program kan for eksempel bruke data om en arbeider. Hvis du angir **Arbeider**-siden i **Kontekst**-feltet, åpnes **Arbeider**-siden når du starter programmet. En oppføring i **Kontekstfelt** er valgfritt. 
-   Angi størrelsen på dialogboksen som PowerApps-programmet skal kjøre. Dialogboksene angis som "små" eller "stor" for å optimalisere brukergrensesnittet når programmet skal kjøre på en telefon eller en større enhet, henholdsvis. 


Du kan også angi hvilke juridiske enheter et program skal være tilgjengelig for, eller du kan gjøre det tilgjengelig for alle dine juridiske enheter. PowerApps-programmer er som standard tilgjengelige for alle juridiske enheter.

## <a name="opening-an-application"></a>Åpne et program
Når du har konfigurert innebygde PowerApps-programmer, legges koblinger til programmene du har angitt, på sidene i Talent. Klikk på en kobling for å åpne et program. 



