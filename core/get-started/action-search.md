---
title: "Handlingssøk"
description: "Denne artikkelen beskriver søkefunksjonen handling i Microsoft Dynamics 365 for operasjoner. Handling ved hjelp av Søk etter og Kjør handlinger på en side."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Handlingssøk

Denne artikkelen beskriver søkefunksjonen handling i Microsoft Dynamics 365 for operasjoner. Handling ved hjelp av Søk etter og Kjør handlinger på en side.

<a name="introduction"></a>Innledning
------------

Sider i Microsoft Dynamics 365 for operasjoner utsette hovedsakelig kommandoer på handling-ruter, både standard handlingsruten som vises øverst på en side og verktøylinjene som vises i ulike deler av siden. En nøkkel Tips-funksjonen kan du raskt få tilgang til en hvilken som helst knapp i en handlingsrute ved å trykke Alt-tasten og deretter en rekke bokstaver i tidligere versjoner. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) imidlertid i den gjeldende versjonen av Dynamics 365 for operasjoner nøkkel Tips er ikke lenger tilgjengelig, men har blitt erstattet av handlingen søkefunksjonen. Denne nye funksjonen lar deg raskt søke etter og kjøre en knapp fra en hvilken som helst synlig handlingsrute.

## <a name="using-action-search"></a>Bruke handlingssøk
Når du skal bruke handlingssøkfunksjonen, følger du disse trinnene.

1.  I handlingsruten klikker du i feltet for **handlingssøk**. (Feltet for **handlingssøk** inneholder et forstørrelsesglassikon.)
2.  Skriv inn hele eller deler av navnet på knappen du vil kjøre. Du kan også søke ved hjelp av ord fra knappen "bane". (Hvis du vil ha mer informasjon, se den neste delen av denne artikkelen.) En knapp vil vanligvis vises nær toppen av listen over søkeresultater etter at du har skrevet inn to til fire tegn.
3.  Finn og kjør knappen i resultatlisten (ved hjelp av musen eller tastaturet).

Når knappen er kjørt, returnerer fokuset til den siste posisjonen på siden, slik at du kan fortsette å arbeide. 

[![handlingen søkefeltet](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøket ved å trykke Ctrl +/ eller Alt + Q. Trykk hurtigtasten på nytt for å returnere fokuset til den siste posisjonen på siden.

## <a name="understanding-the-results-list"></a>Forstå resultatlisten
Ofte må Dynamics 365 for operasjoner, du vite at både plasseringen og konteksten til en knapp for å fullt ut forstå hensikten med denne knappen. Derfor vises tilleggsinformasjon for hvert element i listen over søkeresultater kan hjelpe deg med å forstå nøyaktig hvilke knapper som vises i listen. Spesielt vises "banen" for knappen. Denne banen kan inkludere etikettene for følgende grensesnittelementer, etter behov:

-   Handlingsrutekategori
-   Knappegruppe
-   Menyknapp (hvis knappen er i en menyknapp)
-   Menyskillelinje (hvis knappen er i en navngitt gruppe i en menyknapp)
-   Gruppen eller kategorien på siden (for eksempel navnet på en hurtigfane)

Du tastet for eksempel **tot** i feltet for **handlingssøk**, og undersøker nå resultatlisten. Den første oppføringen, for en knapp som heter **totaler**, er uthevet. En knapp banen til **ordre**&gt;**Vis** blir også vist. Den **ordre** samsvarer med en del av banen i **ordre** kategorien i handlingsruten og **Vis** samsvarer med en del av banen i **Vis** grupper i denne kategorien. På samme måte, banen til den **Sluttrabatt** knappen (**selge**&gt;**Beregn**) informerer deg om at denne knappen er plassert i den **Beregn** gruppen på den **selge** i kategorien i handlingsruten. Derfor denne informasjonen hjelper deg å forstå nøyaktig hvilken knapp utløses av handlingen Søk (Hvis du velger denne knappen i resultatlisten). 

[![handling-Søk-feltet-med-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

I det forrige eksemplet viste handlingssøk resultatene fra standardhandlingsruten øverst på en side. Handlingssøk viser imidlertid også resultater fra synlige verktøylinjer som er plassert andre steder på siden. Hvis du for eksempel søker etter den **lagerbeholdningen** knappen som er plassert på den **salgsordrelinjer** hurtigfanen. I dette tilfellet knappen banen i resultatlisten (**salgsordrelinjer**&gt;**lager**&gt;**Vis**) informerer deg om at denne knappen er plassert de **Vis** overskriften på den **lager** -menyknapp i den **salgsordrelinjer** hurtigfanen. 

[![på--lager](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Handlingssøk kontra navigasjonssøk
Mens handlingen søk er beregnet til å finne og kjøre handlinger på en side, er det en egen søkemekanisme for å søke etter og navigere til sider i Dynamics 365 for operasjoner. Hvis du vil ha mer informasjon om denne funksjonen, se den [navigasjon Søk](navigation-search.md) artikkelen.


