---
title: Flytte, erstatte og installere aktiva
description: Dette emnet forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aad94f17d6efadf7c520c021354963e7135d6d4da1426774925ce877f705e01a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769641"
---
# <a name="move-replace-and-install-assets"></a>Flytte, erstatte og installere aktiva

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling. Du kan opprette individuelle aktiva som ikke har noen relasjoner til andre aktiva, eller du kan opprette en aktivastruktur som inkluderer et overordnet objekt (aktiva på øverste nivå) og relaterte underordnede aktiva (underobjekter). I Aktivabehandling er det tre tilnærminger til flytting og endre plasseringen av et aktivum:

- **Flytte** – Flytt et aktivum til en annen aktivastruktur eller et annen sted i den samme aktivastrukturen.
- **Erstatt** – Midlertidig fjern et aktivum fra en aktivastruktur slik at den kan repareres eller pusses opp, og deretter legge til det renoverte aktivumet tilbake til aktivastrukturen senere. Du kan også erstatte et brukt aktivum permanent med et nytt aktivum.
- **Installer** – Installer et overordnet objekt og tilknyttede underordnede aktiva på et arbeidssted.

> [!NOTE]
> aktivumet du flytter, erstatter eller installerer, kan være relatert til et annet arbeidssted. I så fall kan aktivumet bruke finansdimensjoner for arbeidsstedet. På siden **Arbeidsstedstyper** definerer du håndteringen av finansdimensjoner på arbeidssteder.

## <a name="move-asset"></a>Flytt aktivum

Bruk **Flytt aktivum**-funksjonen til å flytte et aktivum til en annen aktivastruktur eller et annet sted i den samme aktivastrukturen. Du kan også flytte et aktivum ut av en aktivastruktur slik at det blir et frittstående aktivum som ikke har noen strukturrelasjoner.

> [!NOTE]
> Ikke bruk denne funksjonen hvis aktiva repareres eller byttes ut midlertidig. Bruk i stedet funksjonen **Erstatt aktivum** som er beskrevet senere i dette emnet.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. Velg aktivumet som skal flyttes, fra listen. Hvis aktivumet har underordnede aktiva, flytter du også disse.
3. Velg **Flytt aktivum**.
4. Hvis du vil flytte aktivumet slik at det blir en del av en aktivastruktur, velger du det nye overordnede objektet i feltet **Overordnet objekt**. Hvis du flytter et underordnet aktivum og vil gjøre det til et frittstående aktivum som ikke har noen strukturrelasjoner, lar du feltet **Overordnet objekt** stå tomt.
5. Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett. Du kan imidlertid velge en annen dato og klokkeslett som flyttingen av aktivumet skal være gyldig fra.
6. Velg **OK**.

## <a name="replace-asset"></a>Erstatt aktivum

Bruk funksjonen **Erstatt aktivum** i forbindelse med reparasjoner, oppussing eller permanent utskifting av et utslitt aktivum med et nytt aktivum. Denne funksjonen brukes til å erstatte underordnede aktiva i en aktivastruktur. For overordnede objekter (det vil si aktiva som for øyeblikket ikke har et overordnet objekt), utføres denne erstatningen på et arbeidssted. Hvis du vil ha mer informasjon om hvordan du erstatter overordnede objekter på et arbeidssted, kan du se [Installere aktiva på arbeidssteder](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Hvis et verksted er knyttet til produksjonsavdelingen, kan du opprette arbeidssteder som **Reparasjon**, **Svinn** og **Lager** for å håndtere reparasjon og utskifting av aktiva.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. Velg det underordnede aktivumet som skal erstattes, fra listen. Hvis aktivumet har underordnede aktiva, erstatter du også disse.
3. Velg **Erstatt aktivum**.

    Feltet **Strukturendring** viser siste dato og klokkeslett da det valgte aktivumet og tilknyttede underordnede aktiva ble flyttet i aktivastrukturen.

4. I delen **Valgte aktiva** i feltet **Målarbeidssted** velger du arbeidsstedet du vil flytte aktivumet til. Velg for eksempel stedet **Reparasjon** eller **Svinn**.

    I delen **Overordnet objekt** viser feltet **Gyldighet** den siste datoen og klokkeslettet da det overordnede objektet og relaterte underordnede aktiva ble installert eller flyttet på det gjeldende arbeidsstedet.

5. I delen **Nytt aktivum** i **Aktivum**-feltet velger du aktivumet som skal settes inn som en midlertidig eller permanent erstatning for det valgte aktivumet. Dette aktivumet kan for øyeblikket være plassert på et annet arbeidssted, for eksempel **Lager**.
7. I delen **Gyldig fra** settes feltet **Gyldighet** til gjeldende dato og klokkeslett som standard. Du kan imidlertid velge en annen dato og klokkeslett som erstatningen av aktivumet skal være gyldig fra.
8. Velg **OK**.

## <a name="install-asset"></a>Installer aktivum

Bruk funksjonen **Installer aktivum** til å installere en aktivastruktur på et arbeidssted.

> [!NOTE]
> Velg alltid et overordnet objekt. Det overordnede objektet og tilknyttede underordnede aktiva vil bli flyttet til det valgte arbeidsstedet.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. I listen velger du det overordnede objektet som skal installeres på et annet arbeidssted.
3. Velg **Installer aktivum**.

    I **Attributter**-delen vises aktivaattributtene som er definert på det overordnede objektet.

4. Velg det nye arbeidsstedet i **Arbeidssted**-feltet.
5. Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett. Du kan imidlertid velge en annen dato og klokkeslett som installeringen av aktivastrukturen skal være gyldig fra.
6. Velg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]