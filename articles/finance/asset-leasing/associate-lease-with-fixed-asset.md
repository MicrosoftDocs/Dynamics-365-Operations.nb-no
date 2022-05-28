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
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0ae7a850ceb13cb41ee5adc406e71105cdad4fe
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712153"
---
# <a name="associate-fixed-assets-with-leases"></a>Knytte anleggsmidler til leieavtaler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

Når en leie er knyttet til et anleggsmiddel, oppdateres **Levetid**-feltet i anleggsmiddelboken slik at det justeres til den minste verdien av følgende kriterier: 

 - Anleggsmiddelets levetid
 - Leievilkårene fra den tilknyttede leieboken

Hvis feltet **Overføring av eierskap** er satt til **Ja** for leieboken, blir verdien i **Levetid**-feltet alltid levetiden til aktivumet. 
 
Levetiden blir oppdatert hver gang leien justeres for å sikre at bruksrettseiendelen blir avskrevet i løpet av leieperioden, som om det ble avskrevet i leie av anleggsmidler.

> [!NOTE]
> Hvis du knytter et anleggsmiddel til en leieavtale, deaktiveres knappene **Avskrivning av anleggsmiddel** og **Verdiforringelse for leieavtale** i Aktivaleie. Du kan vise transaksjoner for avskrivning av aktiva og verdiforringelse for leieavtale fra Anleggsmidler. Knappen **Aktivatransaksjoner**, som brukes til å åpne et forespørselsskjema, blir også deaktivert. Du kan også åpne forespørselsskjemaet **Aktivatransaksjoner** i Anleggsmidler.  

Sidene **Anleggsmidler** og **Anleggsmiddeltablå** viser leie-ID-en som er knyttet til et anleggsmiddel. Hvis et anleggsmiddel er knyttet til en leieavtale, vises leie-ID-en og leiebeskrivelsen i hurtigkategorien **Leieinformasjon** på **Anleggsmidler**-siden. Når det gjelder anleggsmiddelbøker som er knyttet til leiebøker, viser feltene **Leie-ID**, **Leiebeskrivelse** og **Tablåtype** informasjon om det valgte anleggsmiddeltablået på hurtigfanen **Leieinformasjon**, for å angi at den er knyttet til en leiebok.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
