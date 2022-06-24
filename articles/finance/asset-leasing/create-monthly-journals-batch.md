---
title: Opprette månedlige journaloppføringer i en bunke
description: Denne artikkelen forklarer hvordan du oppretter journaloppføringer i en bunke for å øke effektiviteten når månedlige leieutgifter registreres.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb5c65b0a2c982171fa0ae88141d92c2f1ead6ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895000"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Opprette månedlige journaloppføringer i en bunke

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Denne artikkelen forklarer hvordan du oppretter journaloppføringer i en bunke for å øke effektiviteten når månedlige leieutgifter registreres. Satsvis behandling kan brukes til å opprette journaloppføringer fra flere tidsplaner. Disse journaloppføringene kan omfatte leiebetalinger, nedbetaling av gjeld, nedbetaling av bruksrettseiendel og fullbyrdelseskostnader. Du kan også bruke satsvis behandling til å gjøre den opprinnelige føringen av flere leieavtaler samtidig, eller til å opprette overgangsjusteringer for flere leieavtaler samtidig.

Hvis du vil konfigurere en satsvis jobb eller behandle betalingsfakturaer, avskrivning eller renter for flere leieavtaler, går du til **Aktivaleie \> Periodisk \> Opprettelse av bunkejournal**. I dialogboksen som vises, kan du velge tidsplanen som journaloppføringene skal opprettes fra. Du kan også angi om bunkeprosessen skal kjøres for bestemte enheter, leiegrupper eller leietablåer.

> [!NOTE]
> Påfølgende transaksjoner, for eksempel nedbetalingsplaner for gjeld, betalinger, avskrivning og utgifter, posteres bare etter at den opprinnelige føringen for tilsvarende leieavtaler er postert.
>
> Journaloppføringene opprettes, men de blir ikke postert før du velger **Kjør**-kommandoen.

Hvis du vil postere den opprinnelige journaloppføringen på en annen dato enn leiedatoen, velger du **Tilordne posteringsdato for første journaloppføring**. Et **Dato**-felt vises, der du kan angi riktig posteringsdato.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
