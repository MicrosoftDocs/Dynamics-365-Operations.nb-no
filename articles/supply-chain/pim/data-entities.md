---
title: Produktdataenheter
description: Denne artikkelen inneholder informasjon om de ulike enhetene som kan brukes til å importere og eksportere produktdata.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: e37e0928d8633a81d3a736527f2545cd61055a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859205"
---
# <a name="product-data-entities"></a>Produktdataenheter

[!include [banner](../includes/banner.md)]

Du må bruke dataenheter til å importere og eksportere produktdata. Tabellen nedenfor inneholder detaljer om de produktrelaterte dataenhetene og beskriver formålet med hver av dem.

| Enhet | Navn på applikasjonsobjekttre (AOT) (type) | Notater |
|--------|-------------------------------------------|-------|
| Produkter V2 | `EcoResProductV2Entity` | Denne enheten brukes til å importere og eksportere delte produkter, distinkte produkter og produktstandarder. Den muliggjør oppdateringer. Den støtter ikke settbaserte SQL-operasjoner. Den er aktivert for Open Data Protocol (OData). |
| Frigitte produkter V2 | `EcoResReleasedProductV2Entity` | Denne enheten brukes til å importere og eksportere utgitte produkter, distinkte produkter og produktstandarder. Den muliggjør oppdateringer. Den krever at det delte produktet allerede er opprettet. Når et nytt, frigitt produkt importeres, oppstår en utgivelse av det delte produktet. Det finnes også separate enheter som kan brukes til å importere og eksportere frigitte produktstandarder og frigitte forskjellige varianter. Denne enheten støtter ikke sett-baserte SQL-operasjoner eller sletteoperasjoner. Den er aktivert for OData. |
| Frigitt produktoppretting V2 | `EcoResReleasedProductCreationV2Entity` | Denne enheten brukes til å importere delte produkter og frigitte produkter i ett trinn. Selv om den støtter eksport, anbefales ikke denne bruken, fordi formålet med enheten er produktoppretting. Den støtter ikke oppdateringer. Den støtter et begrenset sett med felt (felt som er tilgjengelige i dialogboksen for produktoppretting). Den støtter ikke settbaserte SQL-operasjoner. Den er ikke eksponert gjennom OData. |
| Produktvarianter | `EcoResProductVariantEntity` | Denne enheten brukes til å importere og eksportere delte produktvarianter. Den muliggjør oppdateringer. Den krever at dimensjonsverdiene allerede er opprettet. Integreringsnøkkelen er produktstandarden pluss produktdimensjonene. Denne enheten støtter ikke settbaserte SQL-operasjoner. Den er aktivert for OData. Den støtter sletteoperasjoner. Den kan ikke utvides ved å legge til nye produktdimensjoner. |
| Produktvarianter etter produktnummeridentifikasjon | `EcoResProductNumberIdentifiedProductVariantEntity` | Denne enheten brukes til å importere og eksportere delte produktvarianter. Den muliggjør oppdateringer. Den krever at dimensjonsverdiene allerede er opprettet. Integreringsnøkkelen er produktnummeret (mens integreringsnøkkelen for enheten **Produktvarianter** er produktstandarden pluss produktdimensjonene). |
| Frigitte produktvarianter | `EcoResReleasedProductVariantEntity` | Denne enheten brukes til å importere og eksportere frigitte produktvarianter. Den muliggjør oppdateringer. Den krever at delte produktvarianter allerede er opprettet. Når en ny, frigitt produktvariant importeres, oppstår en utgivelse av den delte produktvarianten. Denne enheten støtter ikke settbaserte SQL-operasjoner. Den er aktivert for OData. Selv om den støtter sletteoperasjoner, fører denne bruken for øyeblikket til at data blir ødelagt på grunn av en feil i den gjeldende plattformen. Enheten kan ikke utvides ved å legge til nye produktdimensjoner. |
| Utgitte produktvarianter etter produktnummeridentifikasjon | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Enheten ligner på enheten **Frigitte produktvarianter**, men integreringsnøkkelen er produktnøkkelen i stedet for er produktstandarden pluss produktdimensjoner. Den kan utvides ved å legge til nye produktdimensjoner. |
| Salgbare frigitte produkter | `EcoResSellableReleasedProductEntity` | Denne enheten brukes til å eksportere bare salgbare produkter. salgbare produkter er produkter som inneholder informasjon som kreves for å kunne brukes på en salgsordre. De samme reglene gjelder når et produkt er bekreftet ved å bruke **Valider**-funksjonen på siden **Frigitte produkter**. |
| Frigitte spesifikke produkter V2 | `EcoResDistinctProductV2Entity` | Denne enheten brukes til å eksportere spesifikke produkter. Disse spesifikke produktene kan være produkter, undertypeprodukter og produktvarianter. |
| Frigitte produktstandarder V2 | `EcoResProductMasterV2Entity` | Denne enheten brukes til å importere og eksportere produktstandarder. Den er ikke aktivert for databehandling. |
| Vare – strekkode | `EcoResProductBarcodeEntityV3` | Denne enheten brukes til å eksportere produkter og strekkoder. Denne enheten tillater ikke endringssporing, oppdateringer eller slettinger. Hvis du vil bruke endringssporing, oppdateringer eller slettinger på strekkoder, må du bruke **Vare – strekkodetilknytning**. |
| Tilknytning for vare – strekkode | `EcoResProductBarcodeAssociationEntity` | Denne enheten brukes til å eksportere produkter og strekkoder. Den tillater endringssporing, oppdateringer og slettinger. Hvis du vil bruke enheten, må funksjonen *Vare – strekkodeforbedringer* være aktivert i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Enhetsnøkkelen er `AssociationID`, som oppretter tilknytningen mellom strekkoden og produktet. Hvis du vil legge til støtte for denne nøkkelen, blir `InventitemBarcodeAssociation`-tabellen fylt ut for eksisterende varestrekkodedata når du aktiverer funksjonen. Tabellen fylles ut ved hjelp av en satsvis jobb, og hvis strekkodetabellen har mange oppføringer, kan det ta lang tid å kjøre den satsvise jobben. Det anbefales derfor at du planlegger å aktivere funksjonen (og dermed kjøre den satsvise jobben) på et tidspunkt som passer forretningstidsplanen din. |
| Tilstander for produktlivssyklus | `EcoResProductLifecycleSateEntity` | Denne enheten brukes til å importere og eksportere de ulike produktlivssyklustilstandene som kan tilordnes til et produkt. |

> [!NOTE]
> Du kan bruke dataenheten **Frigitte produkter v2** til å importere produkter til systemet bare hvis det delte produktet allerede er opprettet. Hvis du vil importere produkter til systemet, må du ellers bruke dataenheten **Produktoppretting**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]