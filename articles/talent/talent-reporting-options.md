---
title: Rapporteringsalternativer i Talent
description: Dette emnet forklarer hvordan du løser problemet der en kunde ønsker å tilpasse Microsoft Dynamics 365 Talent-rapporter eller opprette nye rapporter.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897954"
---
# <a name="reporting-options-in-talent"></a>Rapporteringsalternativer i Talent

**Miljødetaljer**

Dette problemet gjelder for alle miljøer.

**Symptom**

Kunden ønsker å tilpasse Microsoft Dynamics 365 Talent-rapporter eller opprette nye rapporter.

**Avgang**

Brukeren kan ikke tilpasse de innebygde Microsoft Power BI-rapportene.

**Løsning**

- Core HR-dataene som flyter til Common Data Service, kan rapporteres via Power Apps Common Data Service-koblingen til Power BI Desktop. Legg merke til at Common Data Service inneholder et delsett med Core HR-data. Hvis du vil ha mer informasjon om Power BI og instrumentbord, kan du se [Opprette Power BI-rapporter og -instrumentbord med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronisk rapportering (ER) er tilgjengelig for noen av rapportene i Talent. Kundedrevne tilpasninger kan gjøres via ER-konfigurasjonsalternativene.
- Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjelp av ulike dataenheter som leveres av Talent via Microsoft Office-integreringen.

**Langsiktig løsning**

Flere Power BI-alternativer er tilgjengelige, og mer data og enheter vil være en del av Common Data Service.
