---
title: Blandet modus-planlegging – Kombinere separat, prosess og lean-leverandører
description: Dette emnet inneholder informasjon om blandet modus-planlegging.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c16cf5bf1346cad7d5310a74b84c199ae2c71a4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434253"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Blandet modus-planlegging – Kombinere separat, prosess og lean-leverandører

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om blandet modus-planlegging. I blandet modus-planlegging kan du utforme forsyningskjeden etter materialflyten. Dynamics 365 Supply Chain Management sørger for at materialflyten følger modellene dine, uavhengig av forsyningspolicyen som er valgt (kanbaner, produksjonsordrer, bestillinger, partiordrer eller overføringsordrer). 

Du kan velge den overordnede strategien for å forsyne et produkt, uavhengig av produktstrukturen.  

Du kan for eksempel ha kanban-kontroll i monteringen, der materialer forsynes til monteringsverkstedet etter produksjonsordrer, Kanbaner, overføringer, partiordrer, eller en kombinasjon som passer for kjennetegnene til forsyningskjeden, men kan du fremdeles ha full oversikt over forsyninger. Denne funksjonen fører til optimale forsyningskjedeprosesser og forbedret oversikt i forsyningskjeden.  

Detaljene for forsyningspolicyene som brukes i hovedplanlegging, avhenger av lagringsdimensjonene som er aktivert som dekningsdimensjoner. Hvis du vil aktivere hovedplanlegging for å kontrollere etterfylling og forsyning for ulike typer lokasjoner (for eksempel ved å skille produksjonen for forskjellige produksjonsenheter, eller ved å skille ulike typer lagre for materialer og ferdigvarer), anbefaler vi at du aktiverer Område og lager som dekningsdimensjoner. Du kan alternativt utelate lager som dekningsdimensjon. I så fall når du bruker avanserte lagerstyring, kontrolleres alle bevegelser på lageret av lagerarbeid, mens all flytting på tvers av lagre styres av uttak-Kanbaner.

## <a name="supply-policies"></a>Forsyningspolicyer
Blandet modus-planlegging styrer hvordan et produkt angis og, basert på forsyningen, hvordan avledede behov (forbruk av varer fra en stykkliste \[BOM\]) utstedes. Avhengig av bestillingstypen tilfører systemet automatisk materialer for å oppfylle kravene.  

Forsyningspolicyer kan defineres på produktnivå eller på alle nivåer som støtter dine behov. Du definerer detaljene for forsyningspolicyer på siden **Standard ordreinnstillinger**.  

Forsyningspolicyer kan være kontrollert etter produkt, varedimensjoner (konfigurasjon, farge og størrelse), område og lager. Dette oppsettet blir utført på siden **Varedekning**.  

Standard ordretype styrer hvilken rekkefølge Hovedplanlegging genererer.  

Uansett hvordan forsyningskjeden er modellert støtter Supply Chain Management din blanding av forsyningspolicyer. Du kan ha produksjonsordrer fra Kanbaner som kilde. Du kan alternativt ha en partiordre som krever et produkt som forsynes av overføringer eller Kanbaner.  

Supply Chain Management sørger for at materialflyt følger modellen.  

Lageret til plukking av materiale tilordnes dynamisk under kjøring, etter forsyningspolicyen er definert.  

Vanligvis opprettes Kanbaner ikke for fremtidige datoer, fordi en kanban har en kort livssyklus. For å gi full oversikt over forsyningskjeden har vi innført det nye planleggingskonseptet med en "planlagt kanban," som brukes til å beregne avledede behov, og hjelper deg med å sikre at kravene forsynes basert på den samme logikken som brukes når den faktiske Kanbanen opprettes.  

Den samme logikken gjelder for alle andre typer forsyningspolicyer. Langsiktig materialplanlegging er derfor basert på den samme logikken som du forventer å kjøre med de faktiske ordrene etter produksjon og forsyning er godkjent.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Policy for materialtildeling mellom forsyning – ressursforbruk i stykklister
Ressursforbruk er en viktig funksjonalitet. Med ressursforbruk kan et lager for plukking av materialer velges dynamisk basert på forsyningspolicyen (ordretype), og vedlikehold av stamdata blir enklere.  

Ressursforbruk krever at lageret som materialer plukkes fra, tilordnes basert på måten produktet forsynes på. Ved kjøretid finner med andre ord systemet ressursene som skal brukes for produksjon. Basert på disse ressursene, finner systemet deretter plukklageret.  

For arbeid som er uavhengig av en policy for forsyning, trenger du ikke endre informasjon på Stykklisten Hvis forsyningen endres. For ad hoc-endringer sørger Supply Chain Management for at materialer forsynes fra lageret som er riktig.

## <a name="process-manufacturing--the-production-type"></a>Prosessproduksjon – Produksjonstypen
Vi anbefaler at du bruker produksjonstype stykklister for alle produkter for full fleksibilitet i blandet modus. Du kan deretter bruke produksjonsordrer, kanbaner, overføringsordrer eller bestillinger for å levere et produkt. For prosessproduksjon må du bruke produksjonstypen **formel**, **koprodukt**, **biprodukt** eller **planleggingselement**. Kanbaner og produksjonsordrer kan ikke brukes for disse typene for produksjon.



