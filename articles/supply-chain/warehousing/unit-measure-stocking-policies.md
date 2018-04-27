---
title: "Måleenhet og lagringspolicyer"
description: Denne artikkelen beskriver hvordan standardenheter, enhetssekvenser og enhetskonverteringer brukes i lagerprosesser.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0a22e07f5a0e5bc30c8ad9dc87c5a506d62847d
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="unit-of-measure-and-stocking-policies"></a>Måleenhet og lagringspolicyer

[!INCLUDE [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan standardenheter, enhetssekvenser og enhetskonverteringer brukes i lagerprosesser.

Sekvensgrupper for enhet definerer sekvensen av enheter som kan brukes i lageroperasjoner. De opprettes på siden **Sekvensgrupper for enhet**. Sekvensen viser forholdet mellom de forskjellige enhetene. Du lagrer for eksempel paller som inneholder bokser som inneholder individuelle varedeler. I så fall må du angi tre ulike enhetene og den logiske rekkefølgen på lagene. Med sekvensgrupper for enhet kan du definere policyer for gruppering av nummerskilt, og standardenhetene som skal brukes for ulike lagerprosesser. Denne artikkelen gjelder for både den avanserte datalagerstyringsløsningen som er tilgjengelig i Lagerstyring, og den mer grunnleggende datalagerstyringsløsningen som er tilgjengelig i Beholdningsstyring.

## <a name="unit-sequence-groups-for-released-products"></a>Sekvensgrupper for enhet for frigitte produkter
Hvis du vil bruke frigitte produkter i lagerarbeidsprosesser, må en sekvensgruppe for enhet tilordnes til dem. Hvis du validerer et produkt som er tilknyttet en lagringsdimensjonsgruppe, og alternativet **Bruk lagerstyringsprosesser** for lagringsdimensjonsgruppen er satt til **Ja**, får du en feilmelding hvis en sekvensgruppe-ID for enhet ikke er definert for produktet. Hvis sekvensgruppen for enhet som du bruker, inneholder flere linjer (og derfor flere enheter), må du definere en enhetsomregning mellom enhetene. Du fullfører dette oppsettet på siden **Enhetsomregninger**. Den minste enheten i en gruppe i rekkefølgen som du knytter til et frigitt produkt, må samsvare med lagerenheten som er definert for det tilhørende produktet. Lagerenheten er enheten som brukes til grunnleggende beregninger av lagerbeholdningen. Du kan også definere måleenhetskonverteringer for produktvarianter av produktstandarder ved hjelp av alternativet **Aktiver måleenhetskonverteringer**.

## <a name="license-plate-grouping"></a>Gruppering av nummerskilt
Du kan angi om mottak av mindre enn eller flere enn én bestemt enhet skal grupperes i ett nummerskilt eller deles inn i et eget nummerskilt for hver enhet. Hvis du vil konfigurere dette, kan du bruke alternativet **Gruppering av nummerskilt** i **Linjedetaljer**-kategorien på siden **Sekvensgrupper for enhet**. Hvis du vil bruke nummerskiltgrupperingen når arbeid behandles av en mobilenhet, må du velge alternativet **Gruppering av nummerskilt** på menyelementet **Mobilenhet**. Du bruker for eksempel en mobilenhet til å registrere en vare som er tilknyttet en sekvensgruppe for enhet med to linjer. Den første linjen er for stykker, og **Gruppering av nummerskilt** er satt til **Ja**. Den andre linjen er for pallenhet, og **Gruppering av nummerskilt** er satt til **Nei**. I dette tilfellet kan systemet automatisk lede oppdelingen og opprettingen av nummerskilt per 100 enheter.

## <a name="units-for-cycle-counting"></a>Enheter for syklustelling
For å definere hvilke enheter som skal brukes som en del av prosesser for syklustelling, velger du alternativet **Bruk enhet for syklustelling** på siden **Sekvensgrupper for enhet**. Du kan velge maksimalt fire enheter i sekvensgruppen. Hvis du velger flere enn fire enheter, vises de ikke på mobilenheten.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Standardenheter for mottaksprosesser for mobilenhet
Hvis du vil angi standardenhetene som skal brukes for mottaksprosesser på mobilenheter, kan du aktivere alternativene **Standardenhet for innkjøp og overføring** og **Standardenhet for produksjon** på siden **Sekvensgrupper for enhet**. Du kan for eksempel angi at systemet som standard skal bruke pallantall når du mottar bestillingslagerbeholdning ved hjelp av en mobilenhet, men at lagringsenheten skal være stykker. For å få omregningen for antall stykker som hver pall inneholder, må du definere en enhetskonvertering, for eksempel 100 stk. = 1 PL.

## <a name="default-order-settings"></a>Standard ordreinnstillinger
Som en del av opprettelsen av frigitte produkter må du velge standardenheter for innkjøp, salg og lager for å behandle de forskjellige ordrene. Du kan angi standardenheter og -antall for de ulike kildedokumenter på sidene **Standard ordreinnstillinger** og **Områdespesifikke ordreinnstillinger**. Du får tilgang til disse sidene fra siden **Frigitte produkter**.




