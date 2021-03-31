---
title: Automatisk autorisasjon med planleggingsoptimalisering
description: Dette emnet beskriver hvordan du bruker automatisk autorisasjon med planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227802"
---
# <a name="autofirming-with-planning-optimization"></a>Automatisk autorisasjon med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Automatisk autorisasjon gjør det mulig å autorisere planlagte bestillinger som en del av hovedplanlegging-prosessen. Når planlagte bestillinger autoriseres, blir de omgjort til faktiske bestillinger, overføringsordrer eller produksjonsordrer. Når planleggingsoptimalisering brukes, blir planlagte bestillinger autorisert under en hovedplanlegging som kjøres når ordredatoen (det vil si startdatoen) er innenfor tidshorisonten for autorisasjon.

> [!NOTE]
> Automatisk autorisasjon av et bestillingsforslag kan bare skje hvis varen er knyttet til en leverandør.

## <a name="turn-on-autofirming"></a>Aktivere automatisk autorisering

Følg denne fremgangs måten for å aktivere automatisk autorisering.

1. I arbeidsområdet **Funksjonsbehandling** i **Ny**-fanen velger du **Automatisk autorisasjon med planleggingsoptimalisering** i listen. Hvis funksjonen ikke vises i **Ny**-fanen, ser du i fanene **Ikke aktivert** og **Alle**.
1. Velg **Aktiver nå**. Du kan også velge **Tidsplan**, og deretter velge tidspunktet når du vil at funksjonen skal aktiveres.

## <a name="set-up-the-firming-time-fence"></a>Definer autorisasjonshorisonten

Autorisasjonshorisonten beregnes fremover fra og med kjøringsdatoen for hovedplanlegging. Den er definert av antall dager du angir. Du kan styre autorisasjonshorisonten på følgende måter:

- Hvis du vil definere standard autorisasjonshorisonten for en dekningsgruppe, går du til **Hovedplanlegging** \> **Oppsett** \> **Dekning** \> **Dekningsgrupper**, og velger en dekningsgruppe. Deretter angir du antall dager i feltet **Horisont for automatisk autorisasjon (dager)** i hurtigfanen **Annet**.
- Hvis du vil overskrive autorisasjonshorisonten som er definert for dekningsgruppen for en bestemt vare, går du til **Behandling av produktinformasjon** \> **Frigitte produkter**, og deretter velger du **Plan** og **Varedekning** i handlingsruten. I fanen **Generelt** velger du deretter **Overstyr horisont** og angir antall dager i feltet **Horisont for automatisk autorisasjon (dager)**.
- Hvis du vil overskrive autorisasjonshorisonten som er definert for dekningsgruppen og varedekningen for en bestemt hovedplan, går du til **Hovedplanlegging** \> **Oppsett** \> **Hovedplanlegging**, og velger en hovedplan. Deretter setter du **Autorisasjon** til **Ja** i hurtigfanen **Horisont i antall dager**, og angir antall dager.

Hvis automatisk autorisering er aktivert for en kjøring av hovedplanlegging som bruker planleggingsoptimalisering, utføres automatisk autorisering i henhold til oppsettet for automatisk autorisasjon. Hvis automatisk autorisering ikke er aktivert, eller hvis planlegging startes fra **Nettobehov** -siden, hoppes den automatiske autorisasjonsprosessen over.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planleggingsoptimalisering vs. den innebygde planleggingsmotoren Supply Chain Management.

Både planleggingsoptimalisering og planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management, kan brukes til automatisk autorisering av planlagte bestillinger. Det er imidlertid noen viktige forskjeller. Mens planleggingsoptimalisering for eksempel bruker ordredatoen (det vil si startdatoen) for å bestemme hvilke planlagte bestillinger som skal autoriseres, bruker den innebygde planleggingsmotoren Supply Chain Management behovsdatoen (det vil si sluttdatoen). Her er et sammendrag av forskjellene.

**Planleggingsoptimalisering**

- Automatisk autorisasjon er basert på ordredatoen (startdato).
- Fordi ordredatoen (Startdato) utløser autorisering, trenger du ikke å ta hensyn til leveringstiden som en del av autorisasjonshorisonten.
- Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være én uke.

**Innebygd planleggingsmotor for Supply Chain Management**

- Automatisk autorisasjon er basert på behovsdatoen (sluttdato).
- Hvis du vil ha hjelp til å sikre at ordrer blir autorisert innen forfallstid, må autorisasjonshorisonten være lenger enn leveringstiden.
- Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være leveringstiden pluss én uke.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]