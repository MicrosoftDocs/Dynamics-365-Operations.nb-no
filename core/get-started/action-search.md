---
title: "Handlingssøk"
description: "Denne artikkelen beskriver handlingssøkefunksjonen i Microsoft Dynamics 365 for Finance and Operations. Handlingssøk hjelper deg med å finne og kjøre handlinger på en side."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: cd024f2bc06fca9c21ea41fbed44efbc519cee94
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Handlingssøk
<a id="action-search" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver handlingssøkefunksjonen i Microsoft Dynamics 365 for Finance and Operations. Handlingssøk hjelper deg med å finne og kjøre handlinger på en side.

Introduksjon
<a id="introduction" class="xliff"></a>
------------

Sider i Microsoft Dynamics 365 for Finance and Operations viser hovedsakelig kommandoer i handlingsruter, både standard handlingsruten som vises øverst på en side, og verktøylinjene som vises i ulike deler av siden. I tidligere versjoner gir en funksjon for nøkkeltips deg rask tilgang til alle knapper i en handlingsrute ved å trykke Alt-tasten og deretter en serie med bokstaver. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) I den gjeldende versjonen av Finance and Operations er imidlertid ikke nøkkeltips lenger tilgjengelige, men er erstattet med handlingssøkefunksjonen. Denne nye funksjonen lar deg raskt søke etter og kjøre en knapp fra en hvilken som helst synlig handlingsrute.

## Bruke handlingssøk
<a id="using-action-search" class="xliff"></a>
Når du skal bruke handlingssøkfunksjonen, følger du disse trinnene.

1.  I handlingsruten klikker du i feltet for **handlingssøk**. (Feltet for **handlingssøk** inneholder et forstørrelsesglassikon.)
2.  Skriv inn hele eller deler av navnet på knappen du vil kjøre. Du kan også søke ved hjelp av ord fra knappens "bane". (Hvis du vil ha mer informasjon, se den neste delen av denne artikkelen.) En knapp vises vanligvis øverst i resultatlisten etter at du har skrevet inn to til fire tegn.
3.  Finn og kjør knappen i resultatlisten (ved hjelp av musen eller tastaturet).

Når knappen er kjørt, returnerer fokuset til den siste posisjonen på siden, slik at du kan fortsette å arbeide. 

[![handling-søk-felt](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøket ved å trykke Ctrl +/ eller Alt + Q. Trykk hurtigtasten på nytt for å returnere fokuset til den siste posisjonen på siden.

## Forstå resultatlisten
<a id="understanding-the-results-list" class="xliff"></a>
I Finance and Operations må du ofte vite både plasseringen og konteksten til en knapp for å fullt ut forstå formålet med denne knappen. Derfor vises tilleggsinformasjon for hvert element i listen over resultater, som forklarer nøyaktig hvilke knapper som vises i listen. Spesielt vises "banen" for knappen. Denne banen kan inkludere etikettene for følgende grensesnittelementer, etter behov:

-   Handlingsrutekategori
-   Knappegruppe
-   Menyknapp (hvis knappen er i en menyknapp)
-   Menyskillelinje (hvis knappen er i en navngitt gruppe i en menyknapp)
-   Gruppen eller kategorien på siden (for eksempel navnet på en hurtigfane)

Du tastet for eksempel **tot** i feltet for **handlingssøk**, og undersøker nå resultatlisten. Den første oppføringen, for en knapp som heter **Totaler**, er uthevet. En knapp i banen til **Salgsordre** &gt; **Vis** vises også. Delen **Salgsordre** for banen samsvarer med kategorien **Salgsordre** i handlingsruten, og delen **Vis** samsvarer med gruppen **Vis** i denne kategorien. På samme måte vil banen til knappen **Sluttrabatt** (**Selg** &gt; **Beregn**) fortelle deg at denne knappen er plassert i **Beregn**-gruppen i **Selg**-kategorien i handlingsruten. Derfor kan denne informasjonen hjelpe deg med å forstå nøyaktig hvilken knapp som vil utløses av handlingssøk (hvis du velger denne knappen i resultatlisten). 

[![handling-søk-felt-med-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

I det forrige eksemplet viste handlingssøk resultatene fra standardhandlingsruten øverst på en side. Handlingssøk viser imidlertid også resultater fra synlige verktøylinjer som er plassert andre steder på siden. Du søker for eksempel etter knappen **Lagerbeholdning** som er plassert i hurtigfanen **Salgsordrelinjer**. I dette tilfellet informerer knappebanen i resultatlisten (**Salgsordrelinjer** &gt; **Beholdning** &gt; **Vis**) deg om at denne knappen er plassert under overskriften **Vis** på **Beholdning**-menyknappen i hurtigfanen **Salgsordrelinjer**. 

[![lager-beholdning](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## Handlingssøk kontra navigasjonssøk
<a id="action-search-vs-navigation-search" class="xliff"></a>
Mens handlingssøk skal søke etter og kjøre handlinger på en side, er det en egen søkemekanisme for å finne og navigere til sider i Finance and Operations. Hvis du vil ha mer informasjon om denne funksjonen, kan du se artikkelen [Navigasjonssøk](navigation-search.md).




