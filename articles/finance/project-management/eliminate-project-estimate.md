---
title: Eliminere et prosjektestimat
description: Dette emnet gir informasjon om å eliminere et prosjektestimat etter at det er fullført.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410250"
---
# <a name="eliminate-a-project-estimate"></a>Eliminere et prosjektestimat

[!include [banner](../includes/banner.md)]

Prosjektestimater gir en økonomisk visning for arbeid som er estimert og planlagt for et prosjekt. For å arbeide med estimater for et prosjekt må du knytte prosjektet til et estimatprosjekt. Et estimatprosjekt er alltid basert på et eksisterende prosjekt, men flere prosjekter kan referere til ett estimatprosjektet. Bare fastprisprosjekter og investeringsprosjekter kan knyttes til estimatprosjekter, og disse prosjektene må tilhøre samme prosjektgruppe som estimatprosjektet.

Hvis du vil eliminere et estimatprosjekt, må det være fullført. De følgende trinnene forklarer hvordan du eliminerer et estimat.

1. Gå til **Prosjektstyring og regnskap** > **Alle prosjekter**, og åpne prosjektet. 
2. På **Behandle**- fanen velger du **Estimater**, og på **Estimat**-siden velger du **Eliminer**.
3. På **Eliminer estimat**-siden i **Generelt**-kategorien angir du følgende alternativer:

   - **Periodekode**: Velg periodekoden for å velge de aktuelle forhåndsberegningsprosjektene. 
   - **Estimatdato**: Velg den aktuelle forhåndsberegningsdatoen for eliminering.
   - **Eliminer med VIA-varsler**: Aktiver dette alternativet for å gi beskjed når et estimat som er knyttet til et arbeid som pågår, blir eliminert. Når dette alternativet ikke er aktivert, kan ikke elimineringen fortsette hvis det finnes transaksjoner som ikke er estimert. 
   > [!NOTE]
   > Dette alternativet er bare tilgjengelig når eliminering brukes på et estimatprosjekt. Det er ikke tilgjengelig hvis du bruker periodiske posteringer. Denne innstillingen fungerer sammen med innstillingene i **Estimat**-kategorien på **Prosjektparametere**-siden i feltgruppen **Tillat eliminering når det finnes ikke-estimerte transaksjoner**.
   - **Sett trinnet til fullført**: Aktiver dette alternativet for å sette estimatprosjektet til fasen **Fullført** når du har kjørt elimineringen.
   - **Skriv ut estimatliste**: Velg informasjonen som skal tas med når estimatlisten skrives ut.
   - **Vis infologg**: Aktiver dette alternativet for å vise infologgen.
   - **Posteringsdato**: Velg finansposteringsdatoen for estimatet.

4.  Velg **OK**.
5. Når elimineringsprosessen er fullført, vises det eliminerte estimatprosjektet med en negativ verdi. 

Hvis du ikke vil eliminere et estimat, kan du velge det eliminerte estimatet og velge **Tilbakefør eliminering**.   
