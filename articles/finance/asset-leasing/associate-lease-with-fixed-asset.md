---
title: Knytte anleggsmidler til leieavtaler
description: Emnet forklarer hvordan du knytter et eksisterende anleggsmiddel til en ny leieavtale.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881354"
---
# <a name="associate-fixed-assets-with-leases"></a>Knytte anleggsmidler til leieavtaler

[!include [banner](../includes/banner.md)]

Emnet forklarer hvordan du knytter et eksisterende anleggsmiddel til en ny leieavtale. Når du knytter et anleggsmiddel til en leieavtale, er verdien til bruksrettseiendelen ved opprinnelig føring anskaffelseskostnaden til anleggsmidlet.

Før du kan knytte et anleggsmiddel til en leieavtale, må du opprette en post for anleggsmidlet i Anleggsmidler. På siden **Leiesammendrag** må du deretter opprette en leieavtale og koble anleggsmiddelet til denne leieavtalen.

1. Legg til en leieavtale ved å følge trinnene i [Legge til eller kopiere leieavtaler](add-lease.md). I feltet **Anleggsmiddelnummer** på siden **Legg til leieavtale** velger du anleggsmidlet som ennå ikke er anskaffet.
2. Velg **Tablåer** og bekreft betalingsplanen.
3. Velg **Opprinnelig føring**.
4. Velg **Journal for aktivaleie**.

    Journaloppføringen for opprinnelig føring for leieavtalen debiterer anleggsmidlet for beløpet som vanligvis debiteres til kontoen for bruksrettseiendel.

    Du kan nå vise transaksjonstypen og tablået for anleggsmidlet.

5. Velg **Journaldetaljer**.
6. Velg **Linjer** for å vise enkeltlinjene for journaloppføringen.
7. Velg journallinjen som inneholder anleggsmidlet, og velg deretter fanen **Anleggsmidler**.

    Fanen **Anleggsmidler** viser transaksjonstypen og tablået. Feltet **Transaksjonstype** er som standard satt til **Anskaffelse**, og **Tablå**-feltet settes til gjeldende tablå for anleggsmidlet.

Når du har postert journaloppføringen for opprinnelig føring, vises transaksjonen som en anskaffelsestransaksjon for anleggsmidlet. Hvis du vil vise transaksjonstabellen, kan du gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**, velge det aktuelle aktivumet og deretter velge **Vurderinger**. Du skal se at journaloppføringen for opprinnelig føring har opprettet en anskaffelsestransaksjon for det angitte anleggsmidlet.

Anleggsmidlet kan nå avskrives ved hjelp av standard avskrivningsfunksjonalitet i Anleggsmidler. Hvis du vil ha mer informasjon om avskrivning, kan du se [Avskrivningsmetoder og -konvensjoner](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Hvis du knytter et anleggsmiddel til en leieavtale, deaktiveres knappene **Avskrivning av anleggsmiddel** og **Verdiforringelse for leieavtale** i Aktivaleie. Du kan vise transaksjoner for avskrivning av aktiva og verdiforringelse for leieavtale fra Anleggsmidler. Knappen **Aktivatransaksjoner**, som brukes til å åpne et forespørselsskjema, blir også deaktivert. Du kan også åpne forespørselsskjemaet **Aktivatransaksjoner** i Anleggsmidler.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
