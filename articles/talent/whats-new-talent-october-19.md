---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (16. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551709"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (16. oktober 2018)

[!include[banner](includes/banner.md)]

**Build 8.1.1067**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Tillate ledere å oppdatere fraværsforespørsler

Fraværsforespørsler fra ansatte må oppdateres etter at de godkjennes gjennom arbeidsflyten. I mange tilfeller gjør lederen disse oppdateringene på vegne av den ansatte. Denne nye funksjonen gjør det mulig for ledere å oppdatere fravær eller avbryte fraværsforespørsler på vegne av de ansatte. Denne funksjonen styres av parameteren **Arbeid på vegne av** som kan angis på siden **Personalparametere**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Tillate HR å oppdatere fraværsforespørsler

På samme måte som funksjonen ovenfor, må fraværsforespørsler fra ansatte kanskje oppdateres av HR etter at de tidligere er godkjent via arbeidsflyten. Denne funksjonen gjør det mulig for HR å oppdatere fraværsforespørsler. Funksjonaliteten aktiveres i **Mennesker**-arbeidsområdet og på siden **Arbeider** ved hjelp av et nytt alternativ som kalles **Vis fridager**. På disse sidene kan HR-brukere vise forespørsler og oppdatere fraværestransaksjoner, på lignende måte som ledere kan utføre disse handlingene.

Sikkerhetsplikten som styrer tilgang til denne funksjonaliteten er:
- Plikt: Opprettholde arbeiderspesifikke permisjons- og fraværsprosesser.
- Rettighet: Opprettholde forespørsler om permisjon og fravær for alle arbeidere.

## <a name="other-changes"></a>Andre endringer
Følgende oppdateringer er gjort i denne versjonen:
- Endringer i arbeideransettelseshandlinger, slik at de ikke lenger "sitter fast" i **Arbeidsflyt fullført**-tilstanden.
- Ansettelsesposten kan nå opprettes uten en startdato for ansettelse.
- Dynamics 365 Talent-registreringsdatoen for et kurs i Ansattselvbetjening bruker nå tidssoneforskyvningen på datoen.
- Excel-filer kan importeres flere ganger uten feil ved hjelp av **Ansattenhet**.

## <a name="known-issue"></a>Kjent problem

- **Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene. 
- **Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket. Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert. (Dette problemet vil bli løst i neste plattformoppdatering.)
