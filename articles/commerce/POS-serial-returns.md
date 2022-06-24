---
title: Returnere serienummerkontrollerte produkter i POS
description: Denne artikkelen beskriver funksjonene for validering av serialiserte varer som en del av returprosessen i Microsoft Dynamics 365 Commerce POS.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b2af301180dc2284400b887ce36357660bdd86fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860327"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Returnere serienummerkontrollerte produkter i POS

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver funksjonene for validering av serialiserte varer som en del av returprosessen i Microsoft Dynamics 365 Commerce POS.

> [!NOTE]
> Det er en ny funksjon kalt **Enhetlig returbehandling i POS** tilgjengelig i Commerce versjon 10.0.20 og nyere. Hvis du vil bruke serienummervalidering under returordrebehandling i POS, må du aktivere denne funksjonen. Hvis du vil ha informasjon om andre funksjoner denne funksjonen gir når den er aktivert, kan du se [Opprette returer i POS](POS-returns.md).
>
> Når funksjonen er aktivert, kan den ikke deaktiveres.

## <a name="options-for-validating-serialized-returns"></a>Alternativer for validering av serialiserte returer

Når funksjonen **Enhetlig returbehandling i POS** er aktivert, kan organisasjoner utføre en validering av returer av serienummerkontrollerte varer via POS. Denne funksjonen kan advare brukere hvis serienummeret som returneres, er forskjellig fra det opprinnelige serienummeret som ble solgt. Meldingen som brukere mottar i Commerce versjon 10.0.20 og nyere, er bare en advarsel. Brukere kan fortsette å behandle en retur mot et serienummer som er forskjellig fra serienummeret som opprinnelig ble solgt.

Hvis du vil konfigurere serienummervalidering for en organisasjon etter at funksjonen **Enhetlig returbehandling i POS** er aktivert, går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Handelsparametere** i Commerce Headquarters. Sett alternativet **Aktiver validering av serienumre for returer i POS** til **Ja** i hurtigfanen **Butikklageroperasjoner** i **Lager**-fanen.

## <a name="process-returns-for-serialized-items-in-pos"></a>Behandle returer for serialiserte varer i POS

Hvis alternativet **Aktiver validering av serienumre for returer i POS** er satt til **Ja** når en serienummerkontrollert vare returneres via POS, kan brukeren angi serienummeret for returlinjen i detaljruten på siden **Produkter som kan returneres**. Hvis serienummeret som angis, ikke samsvarer med det opprinnelige serienummeret som ble solgt for salgstransaksjonen, får brukeren en advarsel. Programmet forhindrer imidlertid ikke brukeren fra å fortsette å postere returen.

> [!NOTE]
> POS støtter for øyeblikket validering av serienumre bare på returlinjer der det opprinnelig bestilte antallet ikke er større enn én. Hvis den opprinnelige salgsordrelinjen ble opprettet i en ikke-POS-kanal, og hvis antallet som ble bestilt for den serialiserte varen på en angitt salgslinje, er større enn én, kan ikke varen returneres riktig via POS.

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette returer i POS](POS-returns.md)
