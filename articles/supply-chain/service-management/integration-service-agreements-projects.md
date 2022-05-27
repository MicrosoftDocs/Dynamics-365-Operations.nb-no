---
title: Integrering for serviceavtaler og prosjekter
description: Når du jobber med serviceavtaler og serviceavtalelinjer, bruker du data som er definert i områdene delen Prosjektstyring og regnskap.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7252de08b40aa0668d3ce801b4cbd6f3a53ef12f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673585"
---
# <a name="integration-for-service-agreements-and-projects"></a>Integrering for serviceavtaler og prosjekter 

[!include [banner](../includes/banner.md)]


Når du jobber med serviceavtaler og serviceavtalelinjer, bruker du data som er definert i følgende områder i delen **Prosjektstyring og regnskap**.

## <a name="project-prices"></a>Prosjektpriser

Kostnaden og salgsprisen for en serviceavtaletransaksjon er avledet fra kostprisoppsettet som gjelder for prosjektet som er knyttet til serviceavtalen. Kost- og salgspriser kan settes opp per prosjekt, ansatt og kategori. 

## <a name="project-validation"></a>Prosjektvalidering

Prosjektene, de ansatte og kategoriene som kan velges på en serviceavtalelinje kan begrenses av valideringsoppsettet i delen **Prosjektstyring og regnskap**. Ved å bruke valideringsoppsettet kan du kombinere ansatte, prosjekter og kategorier for kontrolltilgang. 

## <a name="project-line-properties"></a>Prosjektlinjeegenskaper

En linjeegenskap angis automatisk for en serviceavtalelinje.

Linjeegenskaper opprettes i skjemaet **Linjeegenskaper** i **Prosjektstyring og regnskap**. Linjeegenskapen som er angitt på en serviceavtale knyttes til prosjektet som er valgt for serviceavtalen, og deretter arves av serviceavtalelinjen. 

## <a name="default-offset-accounts"></a>Standard motkontoer

Hvis du angir en utgiftstransaksjon, velges en standard motkonto automatisk for transaksjonen. Standard motkonto settes opp for prosjektet som er knyttet til gjeldende serviceavtale.

## <a name="project-categories"></a>Prosjektkategorier

Kategoriene som er tilgjengelige for serviceavtalelinjer er definert i skjemaet **Prosjektkategorier** i delen **Prosjektstyring og regnskap**. 

> [!NOTE]
> <P>Kategorier der det er merket av for <STRONG>Aktiv i journaler</STRONG> på fanen <STRONG>Prosjekt</STRONG> i skjemaet <STRONG>Prosjektkategorier</STRONG>, kan velges. Imidlertid hvis det er merket av for <STRONG>Inaktive kategorier</STRONG> på fanen <STRONG>Journaler</STRONG> i skjemaet <STRONG>Parametere for prosjektstyring og regnskap</STRONG>, alle kategorier er tilgjengelige for valg.</P>

## <a name="project-parameters"></a>Prosjektparametere

Hvis feltet **Fratrådte arbeidere** på fanen **Journaler** i skjemaet **Parametere for prosjektstyring og regnskap** er valgt, kan du velge inaktive ansatte og aktive ansatte i skjemaene **Serviceavtaler** og **Serviceordrer**.

Du kan også aktivere feltene **Starttidspunkt** og **Sluttidspunkt** i **Prosjekt**-fanen i skjemaet **Serviceordrer** for å angi start- og sluttidspunktene på serviceordrelinjer.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Aktivere start- og sluttidspunktfunksjonen for serviceordrer

1.  Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.

2.  Klikk på fanen **Journaler**, og velg deretter **Vis start/sluttidspunkt**.

3.  Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Journaler** \> **Journalnavn**.

4.  Velg journalnavnet som er tilknyttet serviceordren.

5.  Klikk på fanen **Generelt**, og velg deretter **Vis start/sluttidspunkt**.


> [!NOTE]
> <P>Velg journalnavnet for serviceordren i <STRONG>Time</STRONG>-feltet på fanen <STRONG>Journaler</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]