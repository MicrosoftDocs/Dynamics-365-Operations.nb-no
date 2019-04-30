---
title: Hva er nytt eller endret i Dynamics 365 for Talent (7. februar 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b89fc15130755a80b56f26cf7c61674a26f43e36
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "858934"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (7. februar 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="interview-scheduling-enhancements"></a>Forbedringer i intervjuplanlegging
Det er gjort forbedringer i ende-til-ende-intervjuplanleggingsopplevelsen. Nå kan nå se kalendertilgjengeligheten til en intern kandidat og bruke den interne kandidatens kalender til å planlegge anbefalinger. Hvis du vil ha mer informasjon, se [Planlegging og tilbakemelding for intervju](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Jobbpostering til LinkedIn – problem med manglende firmasamsvar er løst
Et problem er løst der jobber som er postert til LinkedIn fra Attract, ble vist under feil firmanavn. Hvis du vil ha mer informasjon, se [Opprette, godkjenne og postere jobber i Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>URL-adresse for karriereområde vises i Admin-innstillinger
URL-adresse til hjemmeside for karriereområde vises nå i **Administrasjonsinnstillinger** under **Karrierestedsledelse**.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

**Build 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Flere kompensasjonsnivåer støttes for jobber
Denne endringen medfører at mer enn ett kompensasjonsnivå defineres i et prosjekt, som muliggjør faste kompensasjonsområder for ansatte, som kan variere fra plan til plan ved bruk av den samme jobben. 

For eksempel:    
*Jobb* – Kontoadministrator *Tilknyttede kompensasjonsnivåer:* B1 og B2 – Hvert nivå har et definert verdiområde. T1 = min 50 000, middels 60 000, maksimalt 75 000 og B2 = min 65 000, middels 74 000, maksimalt 85 000. Når du oppretter fast kompensasjon for ansatte basert på rettighetsreglene som er definert, kan hver faste plan nå peke til samme jobb og til ulike nivåer i jobben. Dette gjør at planer kan defineres i forskjellige regioner/firmaer og peke på den samme jobben, men forskjellige områder, uten å duplisere jobber for å ta hensyn til disse forskjellene.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Kompensasjonsnivåfelt er lagt til enheten Fast kompensasjon for ansatt 
Med denne oppdateringen er enheten for fast kompensasjon for ansatt oppdatert for å inkludere **Kompensasjonsnivå**-feltet. Dette tillegget gjør det enklere å oppdatere de ansattes faste kompensasjonsplaner. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Oppdatere jobbfamilie ved oppdatering og oppretting av nye stillinger
Når du endrer jobben for en stilling, vil **Jobbfamilie** nå angis som standard basert på jobben som er valgt.

### <a name="performance-improvements-when-rendering-workspaces"></a>Ytelsesforbedringer ved gjengivelse av arbeidsområder
Analyse-kategorier for arbeidsområder lastes nå bare ved tilgang til disse sidene. En indikator vises under den innledende gjengivelsen av siden i øvre venstre hjørne på siden.
