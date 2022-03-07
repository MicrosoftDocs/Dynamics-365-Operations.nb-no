---
title: Handlingssøk
description: Denne artikkelen beskriver funksjonen for handlingssøk. Handlingssøk hjelper deg med å finne og kjøre handlinger på en side.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb268c2643b45f6797793dbc5b7cc2e33d5218d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564220"
---
# <a name="action-search"></a>Handlingssøk

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjonen for handlingssøk. Handlingssøk hjelper deg med å finne og kjøre handlinger på en side.

## <a name="introduction"></a>Innledning

Sidene viser hovedsakelig kommandoer i handlingsruter, både standard handlingsruten som vises øverst på en side, og verktøylinjene som vises i ulike deler av siden. I tidligere versjoner gir en funksjon for nøkkeltips deg rask tilgang til alle knapper i en handlingsrute ved å trykke Alt-tasten og deretter en serie med bokstaver.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Handlingssøkefunksjonen erstatter Nøkkeltips, som ikke lenger er tilgjengelige. Denne nye funksjonen lar deg raskt søke etter og kjøre en knapp fra en hvilken som helst synlig handlingsrute.

## <a name="using-action-search"></a>Bruke handlingssøk

Når du skal bruke handlingssøkfunksjonen, følger du disse trinnene.

1. I handlingsruten klikker du i feltet for **handlingssøk**. (Feltet for **handlingssøk** inneholder et forstørrelsesglassikon.)
2. Skriv inn hele eller deler av navnet på knappen du vil kjøre. Du kan også søke ved hjelp av ord fra knappens "bane". (Hvis du vil ha mer informasjon, se den neste delen av denne artikkelen.) En knapp vises vanligvis øverst i resultatlisten etter at du har skrevet inn to til fire tegn.
3. Finn og kjør knappen i resultatlisten (ved hjelp av musen eller tastaturet).

Når knappen er kjørt, returnerer fokuset til den siste posisjonen på siden, slik at du kan fortsette å arbeide.

[![handling-søk-felt](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøket ved å trykke Ctrl +/ eller Alt + Q. Trykk hurtigtasten på nytt for å returnere fokuset til den siste posisjonen på siden.

## <a name="understanding-the-results-list"></a>Forstå resultatlisten

Du må ofte vite både plasseringen og konteksten til en knapp for å fullt ut forstå formålet med denne knappen. Derfor inneholder listen over resultater ytterligere informasjon som forklarer nøyaktig hvilke knapper som vises i listen. Spesielt vises "banen" for knappen. Denne banen kan inkludere etikettene for følgende grensesnittelementer, etter behov:

- Handlingsrutekategori
- Knappegruppe
- Menyknapp (hvis knappen er i en menyknapp)
- Menyskillelinje (hvis knappen er i en navngitt gruppe i en menyknapp)
- Gruppen eller fanen på siden (for eksempel navnet på en hurtigfane)

Du tastet for eksempel **tot** i feltet for **handlingssøk**, og undersøker nå resultatlisten. Den første oppføringen, for en knapp som heter **Totaler**, er uthevet. En knapp i banen til **Salgsordre** &gt; **Vis** vises også. **Salgsordre**-delen av banen korresponderer til **Salgsordre**-fanen på handlingspanelet, og **Vis**-delen av banen korresponderer til **Vis**-gruppen for denne fanen. Tilsvarende vil banen for **Total rabatt**-knappen (**Selg** &gt; **Beregne**) informere deg at denne knappen er lokalisert i **Kalkuler**-gruppen i fanen **Selg** i handlingspanelet. Derfor kan denne informasjonen hjelpe deg med å forstå nøyaktig hvilken knapp som vil utløses av handlingssøk (hvis du velger denne knappen i resultatlisten).

[![handling-søk-felt-med-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

I det forrige eksemplet viste handlingssøk resultatene fra standardhandlingsruten øverst på en side. Handlingssøk viser imidlertid også resultater fra synlige verktøylinjer som er andre steder på siden. Du søker for eksempel etter knappen **Lagerbeholdning** som er i hurtigfanen **Salgsordrelinjer**. I dette tilfellet informerer knappebanen i resultatlisten (**Salgsordrelinjer** &gt; **Beholdning** &gt; **Vis**) deg om at denne knappen er under overskriften **Vis** på **Beholdning**-menyknappen i hurtigfanen **Salgsordrelinjer**.

[![lager-beholdning](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Det finnes noen knapper som ikke vises i Handlingssøk. Disse inneholder nedtrekksdialogknapper og knapper fra delskjemaer. 

## <a name="action-search-vs-navigation-search"></a>Handlingssøk kontra navigasjonssøk

Mens handlingssøk skal søke etter og kjøre handlinger på en side, er det en egen søkemekanisme for å finne og navigere til sider. Hvis du vil ha mer informasjon om denne funksjonen, kan du se artikkelen [Navigasjonssøk](navigation-search.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]