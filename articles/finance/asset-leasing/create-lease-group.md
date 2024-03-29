---
title: Opprett en leiegruppe
description: Denne artikkelen forklarer hvordan du konfigurerer leiegrupper. Leiegrupper kreves for å opprette nye leieavtaler.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd1a6f61346233bf205657917c65fccd82167f7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895029"
---
# <a name="create-a-lease-group"></a>Opprett en leiegruppe

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer leiegrupper. Leiegrupper kreves for å opprette nye leieavtaler. Leietablåer er knyttet til hver leiegruppe. Leietablåer fastsetter standardtablåene som må opprettes for hver leieavtale. Du kan tilordne bestemte kontoer til en leiegruppe på siden **Parametere for leiepostering**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Opprette et leietablå og legge til en leiegruppe

1. Gå til **Aktivaleie \> Oppsett \> Leiegrupper**.
2. I handlingsruten velger du **Ny** for legge til en leiegruppe. Det blir lagt til en linje i rutenettet.
3. Angi en verdi i feltet **Leiegruppe** på den nye linjen.
4. Angi en verdi i feltet **Beskrivelse**.

Informasjonen du nettopp har registrert, legges til i feltet **Leiegruppe** på siden **Legg til leieavtale**.

## <a name="associate-a-book-with-a-lease-group"></a>Knytte et tablå til en leiegruppe

Etter at du har opprettet leiegrupper, kan du tilordne tablåer til hver gruppe. Når du oppretter en leieavtale og tilordner den til en leiegruppe, oppretter systemet et sett med tidsplaner for hvert tablå som er tilknyttet denne leiegruppen.

> [!NOTE]
> Tablåer må konfigureres før de kan tilordnes til en leiegruppe.

1. Gå til **Aktivaleie \> Oppsett \> Leiegruppe**.
2. Velg en leiegruppe, og velg deretter **Tablåer**.
3. Velg **Nytt**, og velg deretter tablået som skal tilordnes til leiegruppen, i feltet **Tablåtype**. Du kan tilordne flere tablåer til en leiegruppe hvis en leieavtale må gjøres rede for på forskjellige måter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
