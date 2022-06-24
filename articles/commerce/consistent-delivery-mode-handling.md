---
title: Aktiver konsekvent leveringsmåtehåndtering i e-handelskanaler
description: Denne artikkelen beskriver hvordan du aktiverer konsekvent leveringsmåtehåndtering for å ta hånd om mulige problemer som er knyttet til tilleggsflyt i e-handelskanaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885591"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Aktiver konsekvent leveringsmåtehåndtering i e-handelskanaler 

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du aktiverer konsekvent leveringsmåtehåndtering for å ta hånd om mulige problemer som er knyttet til tilleggsflyt i e-handelskanaler i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce blir ikke ufordelte tillegg på hodenivå brukt i e-handelskanaler som standard. Denne funksjonaliteten kan føre til det ene av eller begge problemene i e-handelskanaler som følger:

- Ufordelte tillegg på hodenivå vises ikke.
- Tillegg for leveringsmåter er ikke konsekvent mellom valget av leveringsmåte og ordresammendraget i kassen.

For å kunne løse disse problemene må du aktivere funksjonen **Aktiver konsekvent leveringsmåtehåndtering i kanal**. Denne funksjonen sikrer at ufordelte tillegg på hodenivå vises i e-handelskanaler, og at leveringsinformasjon for salgsordrer håndteres konsekvent av samme arbeidsflyt for forespørsel.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Aktiver funksjonen Aktiver konsekvent leveringsmåtehåndtering i kanal

Følg denne fremgangsmåten for å aktivere funksjonen **Aktiver konsekvent leveringsmåtehåndtering i kanal** i Commerce Headquarters.

1. Åpne arbeidsområdet **Funksjonsbehandling** (**Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**).
1. Søk etter og velg **Aktiver konsekvent leveringsmåtehåndtering i kanal** i listen over tilgjengelige funksjoner.
1. Velg **Aktiver nå** i høyre rute.
