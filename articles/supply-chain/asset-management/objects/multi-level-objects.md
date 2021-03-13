---
title: Aktiva på flere nivåer
description: Dette emnet forklarer hvordan du oppretter og sletter aktiva på flere nivåer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4da57c3849095909226db53c23b3c25301acdc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021328"
---
# <a name="multi-level-assets"></a>Aktiva på flere nivåer

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du oppretter og sletter aktiva på flere nivåer. Du kan opprette aktiva og relaterte underaktiva i en hierarkisk trestruktur. På denne måten kan du vise relasjoner og avhengigheter blant aktiva. Vedlikeholdsjobber kan knyttes til alle nivåer i trestrukturen. Statistikk kan også opprettes for et enkeltnivå eller som en sum for alle underaktivanivåer.

På listesiden **Alle aktiva** (**Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**) vises aktiva i hierarkisk rekkefølge i kolonnen **Aktiva**. Kolonnen **Overordnet** viser det tilknyttede overordnede objektet. Hvis det allerede er opprettet aktiva og under aktiva, viser i tillegg **Aktivatre**-delen i ruten **Beslektet informasjon** aktivaene i en trestruktur.

Se [Opprette et aktivum](../objects/create-an-object.md) hvis du vil ha mer informasjon om hvordan du oppretter et aktivum. Hvis du vil opprette et underordnet aktivum, velger du det overordnede objektet i feltet **Overordnet** på hurtigfanen **Generelt**.

## <a name="copy-an-asset-or-asset-structure"></a>Kopiere en aktivastruktur

Hvis firmaet har flere lignende aktivastrukturer, kan du bruke kopieringsfunksjonen i Aktivastyring til å opprette dem raskt.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.
2. På listesiden **Alle aktiva** velger du aktivumet du vil kopiere. Hvis du for eksempel vil kopiere hele aktivastrukturen, inkludert underordnede aktiva, velger du et overordnet objekt.
3. Velg **Kopier aktivum**. I **Kopier fra**-delen er **Aktivum**-feltet satt til aktivumet du valgte på listesiden.
4. I **Kopier til**-delen i **Aktiva**-feltet angir du navnet på det nye aktivumet.
5. Hvis aktivumet du oppretter, skal være en del av en eksisterende aktivastruktur, går du til delen **Overordnet objekt**, **Aktiva**-feltet, og velger en overordnet ID.
6. Velg **OK**. Den nye aktivastrukturen vises på listesiden **Alle aktiva**. Alle aktivaattributter, vedlikeholdsplaner og vedlikeholdsrunder som er relatert til aktivumet du kopierte, overføres til den nye aktivumet eller aktivastrukturen.

Når du kopierer en aktivastruktur, har de underordnede aktivaene i den nye strukturen samme navn som de underordnede aktivaene du kopierte. Når kopieringsprosedyren er fullført, kan du enkelt endre navnet og andre innstillinger for et aktivum. Velg aktivumet på listesiden **Alle aktiva**, og velg deretter **Rediger**-knappen.

> [!NOTE]
> Når du kopierer en aktivastruktur, tilbakestilles livssyklustilstanden til de nye aktivaene til uansett status du definerte som start lilvsløpsstatus for aktiva. Arbeidsstedet tilbakestilles til standard arbeidssted.

## <a name="delete-an-asset-or-asset-structure"></a>Slette et aktivum eller en aktivastruktur

Hvis et aktivum har relaterte underordnede aktiva, kan du bare slette det hvis det er registrert meldinger, arbeidsordrejobber, feilregistreringer eller betingelsesvurderinger for noen av aktivaene.

1. På listesiden **Alle aktiva** velger du aktivumet du vil slette.
2. Velg **Slett**.

> [!NOTE]
> Hvis du ikke kan slette et aktivum ved hjelp av denne fremgangsmåten, er det en annen måte å håndtere sletting på, ved å definere en livssyklustilstand for et aktivum Du kan for eksempel definere en **kassert** eller **slettet** livssyklustilstand på siden **Livssyklustilstander for aktiva**.
