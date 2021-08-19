---
title: Opprette og vedlikeholde en lagerblokkering
description: Dette emnet beskriver hvordan du bruker lagerblokkering til å forhindre at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d602abe4491f6cbbd0fce25a566acf97a25f3bf1e6214e95c80fda2638d14dde
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773282"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opprette og vedlikeholde en lagerblokkering

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du bruker lagerblokkering til å forhindre at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter. Du må ha en vare som fysisk lagerbeholdning er tilgjengelig for, før du starter denne fremgangsmåten.

## <a name="block-inventory"></a>Sperr beholdning

Følg denne fremgangsmåten for å opprette en lagerblokkeringspost, slik at lageret er sperret.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.
1. Velg **Ny** i handlingsruten.
1. Angi hodet i den nye blokkeringsposten, angi feltet **Varenummer** til varen du vil blokkere, og angi en beskrivelse.
1. Skriv inn et antall elementer som skal blokkeres, i hurtigfanen **Generelt** i feltet **Antall**.
1. Angi området og lageret der varene du vil blokkere, for øyeblikket finnes i hurtigkategorien **Lagerdimensjoner**.
1. Velg **Lagre** i handlingsruten.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Oppdatere betingelsene for lagerblokkeringen

Følg denne fremgangsmåten for å oppdatere en lagerblokkeringspost.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.
1. I listeruten velger du den relevante blokkeringsposten.
1. Rediger posten etter behov. Du kan for eksempel endre verdien i feltet **Forventet dato** for å angi når det blokkerte lageret forventes å bli tilgjengelig for reservasjon. Hvis alternativet **Forventede mottak** er valgt, vises datoen på den forventede transaksjonen. (Alternativet **Forventede mottak** velges som standard når du oppretter en blokkeringspost manuelt.)
1. Velg **Lagre** i handlingsruten.

## <a name="unblock-inventory"></a>Oppheve blokkering av lager

Følg denne fremgangsmåten for å fjerne en lagerblokkeringspost, slik at sperring av lageret oppheves.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerblokkering**.
1. I listeruten velger du den relevante blokkeringsposten.
1. Velg deretter **Slett** i handlingsruten.
1. Du blir bedt om å bekrefte operasjonen. Klikk på **Ja** for å fortsette.
1. Lukk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
