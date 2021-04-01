---
title: Konsernintern planlegging
description: Dette emnet beskriver konsernintern planlegging og forklarer hvordan du konfigurerer konsernintern planlegging med planleggingsoptimalisering i Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd498489e18eaba81720757faa14c0bf7b7d67f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263404"
---
# <a name="intercompany-planning"></a>Konsernintern planlegging

[!include [banner](../../includes/banner.md)]

For noen organisasjoner er logistikkoperasjoner avhengige av andre juridiske enheter (firmaer) i organisasjonen. Disse operasjonene håndteres ved hjelp av konserninterne salg og innkjøp, fordi hver juridiske enhet har en egen kontoplan.

Dette emnet beskriver konsernintern planlegging og forklarer hvordan du konfigurerer konsernintern planlegging med planleggingsoptimalisering i Microsoft Dynamics 365 Supply Chain Management.

Dette emnet bruker følgende viktige, konserninterne vilkår:

- **Oppstrøms** – En relativ referanse i en autorisasjons- eller forsyningskjede. Den viser bevegelse i retningen til råvareleverandøren.
- **Nedstrøms** – En relativ referanse i en autorisasjons- eller forsyningskjede. Den viser bevegelse i retningen til kunden.
- **Planlagt konsernintern etterspørsel** – Planlagt etterspørsel for et produkt i et firma, basert på planlagt etterspørsel for produktet fra et nedstrømsfirma.

I hovedplanlegging kan en plan i ett firma omfatte planlagt konsernintern etterspørsel som er knyttet til planlagte ordrer fra en plan i et annet firma. Denne muligheten er nyttig, fordi den gir full oversikt over planlagte ordrer på tvers av firmaer. Det sikrer også at alle nødvendige planlagte forsyningsordrer opprettes, men uten at det kreves at planlagte ordrer autoriseres for den konsernintern etterspørselen.

Hvis du kjører hovedplanlegging fra en hovedplan som inkluderer planlagt nedstrømsetterspørsel, vil planlagte ordrer fra de relaterte konserninterne leverandørene bli tatt med i planen som etterspørsel.

## <a name="required-setup"></a>Obligatorisk oppsett

Hvis du vil bruke konsernintern planlegging, må du klargjøre systemet på følgende måte:

1. De relevante produktene må frigis i alle de relevante firmaene. Hvis du vil ha mer informasjon, kan du se [Konfigurer og bruk konsernintern handel i Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.
1. Nedstrømsetterspørsel må dekkes av innkjøp fra en leverandør som har en konsernintern relasjon til oppstrømsfirmaet, og relevante standard lagerdimensjoner (område og lager) på kunden. Hvis du vil ha mer informasjon, kan du se [Konfigurer og bruk konsernintern handel i Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.
1. Hovedplanen i oppstrømsfirmaet må inkludere planlagt nedstrømsetterspørsel, og det relevante firmaet og hovedplanen må være angitt i nedstrømsplanene.

## <a name="include-planned-downstream-demand"></a>Inkluder planlagt nedstrøms etterspørsel

Følg denne fremgangsmåten for å konfigurere hovedplanen slik at den inneholder planlagt nedstrømsetterspørsel.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg eller opprett en hovedplan.
1. Angi følgende felt i hurtigfanen **Konsertintern planlegging**:

    - **Inkluder planlagt nedstrømsetterspørsel** – Sett dette alternativet til *Ja* for å aktivere konsernintern planlegging for hovedplanen.
    - **Nedstrømsplaner** – Hvis du setter alternativet **Inkluder planlagt nedstrømsetterspørsel** til *Ja*, bruker du verktøylinjen og rutenettet til å legge til de ønskede hovedplanene fra andre firmaer.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Utlign på tvers av firmaer ved bruk av flernivå utligning

I utligning på flere nivåer kan du vise utligning på tvers av firmaer for å se den innledende kilden for etterspørsel som dekkes av en forsyning.

Følg disse trinnene for å vise informasjon om utligning på flere nivåer.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**.
1. Velg eller åpne en planlagt ordre.
1. På handlingsruten, i fanen **Vis** i **Krav**-gruppen, velger du **Utligning på flere nivåer**.

### <a name="intercompany-example-that-involves-two-companies"></a>Konserninternt eksempel som omfatter to firmaer

I dette eksemplet opprettes det en produksjonsordre i USMF-firmaet for å dekke en salgsordre i DEMF-firmaet. I USMF er direkte etterspørsel planlagt konsernintern etterspørsel. Hvis du vil at denne forespørselen skal vises i USMF, kjøres hovedplanlegging først i DEMF og deretter i USMF.

Illustrasjonen nedenfor viser hvordan dette eksemplet kan vises på siden **Utligning med flere nivåer** for den planlagte produksjonsordren.

![Konserninternt eksempel som omfatter to firmaer](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Konserninternt eksempel som omfatter tre firmaer

I dette eksemplet opprettes det et bestillingsforslag i USMF-firmaet for å dekke en salgsordre i FRRT-firmaet. I DEMF- og USMF-firmaer er direkte etterspørsel planlagt konsernintern etterspørsel. Hvis du vil at denne etterspørselen skal vises i USMF, kjøres hovedplanlegging først i FRRT, deretter i DEMF og til slutt USMF.

Illustrasjonen nedenfor viser hvordan dette eksemplet kan vises på siden **Utligning med flere nivåer** for den planlagte produksjonsordren.

![Konserninternt eksempel som omfatter tre firmaer](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]