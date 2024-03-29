---
title: Tilbakeføre posterte leietransaksjoner
description: Denne artikkelen beskriver hvordan du tilbakefører en postert leietransaksjon. Alle transaksjoner som opprettes gjennom aktivaleie, kan tilbakeføres.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4f23b6cca6ddf4da7a0232a5bc61785dbd451d55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908074"
---
# <a name="reverse-posted-lease-transactions"></a>Tilbakeføre posterte leietransaksjoner

[!include [banner](../includes/banner.md)]

Alle transaksjoner som opprettes gjennom aktivaleie, kan tilbakeføres. Transaksjoner som tilbakeføres gjennom aktivaleie, oppdaterer leiedataene. Derfor oppdaterer du også de bærende verdiene for leieforpliktelse og bruksrettseiendel.

Hvis du vil opprette en tilbakeføringstransaksjon for en leieavtale, følger du denne fremgangsmåten.

1. På siden **Aktivatransaksjoner** eller **Gjeldstransaksjoner** velger du transaksjonen, og deretter velger du **Tilbakefør transaksjon**.
2. I dialogboksen som vises, kan du redigere datoen for postering av tilbakeføringsoppføringen. Som standard er **Dato**-feltet satt til transaksjonsposteringsdatoen for transaksjonen som er valgt. Tilbakeføringsoppføringen kan ikke posteres tidligere enn den opprinnelige posteringsdatoen for den valgte transaksjonen.
3. Velg **OK**. En journaloppføring posteres, som reverserer posten du har valgt. Tilbakeføringen vises på siden **Aktivatransaksjoner** eller **Gjeldstransaksjoner**, og nettosummen for gjeldende saldo som vises på siden, oppdateres.

Når du velger **Tilbakeført sporing**, blir det vist en dialogboks der det vises både de opprinnelige transaksjonene og de tilbakeførte transaksjonene sammen med et koblet nummer som kalles et *sporingsnummer*. Hvis du vil gjøre tilbakeføringene enklere å forstå og forbedre synligheten, kan du også spore tilbakeføringer ved hjelp av leieplaner.

Feltet **Siste journalnummer** på siden **Tidsplan** viser journalnumrene til transaksjoner. Når en transaksjon tilbakeføres, oppdateres dette feltet med journalnummeret til en tilbakeføringstransaksjon. I tillegg er avmerkingsboksen **Tilbakeført** for å angi at transaksjonen er tilbakeført, og at feltet **Postert** er valgt.

## <a name="revoke-a-reversed-transaction"></a>Oppheve en tilbakeført transaksjon

Følg denne fremgangsmåten for å oppheve en tilbakeført transaksjon.

1. På siden **Tidsplan** eller **Transaksjoner** velger du en opprinnelig transaksjon.
2. Følg ett av disse trinnene:

    - Hvis du valgte transaksjonen på siden **Tidsplan**, følger du fremgangsmåten for å opprette en journal i [Opprette månedlige journaloppføringer i en bunke](create-monthly-journals-batch.md). Du må postere journalen manuelt.
    - Hvis du valgte transaksjonen på **Transaksjoner**-siden, velger du **Tilbakefør transaksjon**. Du får en melding som sier at denne opphevelsen er en opphevelse av en tidligere tilbakeføring, og at du kan redigere posteringsdatoen for denne opphevelsen. Generelle forretningsvalideringer påvirker imidlertid datoene som kan registreres i **Dato**-feltet. 

3. Velg **OK**. En journaloppføring posteres, som reverserer posten du har valgt. Tilbakeføringen vises på **Transaksjoner**-siden, og nettosummen for gjeldende saldo gjenopprettes til hva den var før den første tilbakeføringen. Derfor vil innvirkningen som tilbakeføringen hadde på saldoene, negeres.

Når du velger **Tilbakeført sporing**, blir det vist en dialogboks der det vises både de opprinnelige transaksjonene og de tilbakeførte transaksjonene sammen med et koblet sporingsnummer.

Du kan også spore opphevelser ved å bruke den riktige **Tidsplaner**-siden. Merket fjernes i **Tilbakefør**-feltet, mens **Journal postert** velges. I tillegg oppdateres feltet **Siste journalnummer** med journalnummeret til den opphevede transaksjonen, og feltet **Journalnummer** oppdateres med tilbakeføringsjournalnummeret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
