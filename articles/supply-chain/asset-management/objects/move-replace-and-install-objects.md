---
title: Flytte, erstatte og installere aktiva
description: Denne artikkelen forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling.
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
ms.openlocfilehash: 0a6b5a2904d21782ae422d06eaaf03c5d5e51ab9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015586"
---
# <a name="move-replace-and-install-assets"></a>Flytte, erstatte og installere aktiva

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling. Du kan opprette individuelle aktiva som ikke har noen relasjoner til andre aktiva, eller du kan opprette en aktivastruktur som inkluderer et overordnet objekt (aktiva på øverste nivå) og relaterte underordnede aktiva (underobjekter). I Aktivabehandling er det tre tilnærminger til flytting og endre plasseringen av et aktivum:

- **Flytte** – Flytt et aktivum til en annen aktivastruktur eller et annen sted i den samme aktivastrukturen.
- **Erstatt** – Midlertidig fjern et aktivum fra en aktivastruktur slik at den kan repareres eller pusses opp, og deretter legge til det renoverte aktivumet tilbake til aktivastrukturen senere. Du kan også erstatte et brukt aktivum permanent med et nytt aktivum.
- **Installer** – Installer et overordnet objekt og tilknyttede underordnede aktiva på en funksjonslokasjon.

> [!NOTE]
> aktivumet du flytter, erstatter eller installerer, kan være relatert til en annen funksjonslokasjon. I så fall kan aktivumet bruke finansdimensjoner for funksjonslokasjonen. På siden **Funksjonslokasjonstyper** definerer du håndteringen av finansdimensjoner på funksjonslokasjoner.

## <a name="move-asset"></a>Flytt aktivum

Bruk **Flytt aktivum**-funksjonen til å flytte et aktivum til en annen aktivastruktur eller et annet sted i den samme aktivastrukturen. Du kan også flytte et aktivum ut av en aktivastruktur slik at det blir et frittstående aktivum som ikke har noen strukturrelasjoner.

> [!NOTE]
> Ikke bruk denne funksjonen hvis aktiva repareres eller byttes ut midlertidig. Bruk i stedet funksjonen **Erstatt aktivum** som er beskrevet senere i denne artikkelen.

1. Velg **Aktivastyring** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. Velg aktivumet som skal flyttes, fra listen. Hvis aktivumet har underordnede aktiva, flytter du også disse.
3. Velg **Flytt aktivum**.
4. Hvis du vil flytte aktivumet slik at det blir en del av en aktivastruktur, velger du det nye overordnede objektet i feltet **Overordnet objekt**. Hvis du flytter et underordnet aktivum og vil gjøre det til et frittstående aktivum som ikke har noen strukturrelasjoner, lar du feltet **Overordnet objekt** stå tomt.
5. Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett. Du kan imidlertid velge en annen dato og klokkeslett som flyttingen av aktivumet skal være gyldig fra.
6. Velg **OK**.

## <a name="replace-asset"></a>Erstatt aktivum

Bruk funksjonen **Erstatt aktivum** i forbindelse med reparasjoner, oppussing eller permanent utskifting av et utslitt aktivum med et nytt aktivum. Denne funksjonen brukes til å erstatte underordnede aktiva i en aktivastruktur. For overordnede objekter (det vil si aktiva som for øyeblikket ikke har et overordnet objekt), utføres denne erstatningen på en funksjonslokasjon. Hvis du vil ha mer informasjon om hvordan du erstatter overordnede objekter på en funksjonslokasjon, kan du se [Installere aktiva på funksjonslokasjoner](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Hvis et verksted er knyttet til produksjonsavdelingen, kan du opprette funksjonslokasjoner som **Reparasjon**, **Svinn** og **Lager** for å håndtere reparasjon og utskifting av aktiva.

1. Velg **Aktivastyring** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. Velg det underordnede aktivumet som skal erstattes, fra listen. Hvis aktivumet har underordnede aktiva, erstatter du også disse.
3. Velg **Erstatt aktivum**.

    Feltet **Strukturendring** viser siste dato og klokkeslett da det valgte aktivumet og tilknyttede underordnede aktiva ble flyttet i aktivastrukturen.

4. I delen **Valgte aktiva** i feltet **Målfunksjonslokasjon** velger du funksjonslokasjonen du vil flytte aktivumet til. Velg for eksempel stedet **Reparasjon** eller **Svinn**.

    I delen **Overordnet objekt** viser feltet **Gyldighet** den siste datoen og klokkeslettet da det overordnede objektet og relaterte underordnede aktiva ble installert eller flyttet på den gjeldende funksjonslokasjonen.

5. I delen **Nytt aktivum** i **Aktivum**-feltet velger du aktivumet som skal settes inn som en midlertidig eller permanent erstatning for det valgte aktivumet. Dette aktivumet kan for øyeblikket være plassert på en annen funksjonslokasjon, for eksempel **Lager**.
7. I delen **Gyldig fra** settes feltet **Gyldighet** til gjeldende dato og klokkeslett som standard. Du kan imidlertid velge en annen dato og klokkeslett som erstatningen av aktivumet skal være gyldig fra.
8. Velg **OK**.

## <a name="install-asset"></a>Installer aktivum

Bruk funksjonen **Installer aktivum** til å installere en aktivastruktur på en funksjonslokasjon.

> [!NOTE]
> Velg alltid et overordnet objekt. Det overordnede objektet og tilknyttede underordnede aktiva vil bli flyttet til den valgte funksjonslokasjonen.

1. Velg **Aktivastyring** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. I listen velger du det overordnede objektet som skal installeres på en annen funksjonslokasjon.
3. Velg **Installer aktivum**.

    I **Attributter**-delen vises aktivaattributtene som er definert på det overordnede objektet.

4. Velg det nye funksjonslokasjonen i **Funksjonslokasjon**-feltet.
5. Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett. Du kan imidlertid velge en annen dato og klokkeslett som installeringen av aktivastrukturen skal være gyldig fra.
6. Velg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]