---
title: Aktiver konsekvent leveringsmåtehåndtering i e-handelskanaler
description: Dette emnet beskriver hvordan du aktiverer konsekvent leveringsmåtehåndtering for å ta hånd om mulige problemer som er knyttet til tilleggsflyt i e-handelskanaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349953"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Aktiver konsekvent leveringsmåtehåndtering i e-handelskanaler 

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer konsekvent leveringsmåtehåndtering for å ta hånd om mulige problemer som er knyttet til tilleggsflyt i e-handelskanaler i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce blir ikke ufordelte tillegg på hodenivå brukt i e-handelskanaler som standard. Denne funksjonaliteten kan føre til det ene av eller begge problemene i e-handelskanaler som følger:

- Ufordelte tillegg på hodenivå vises ikke.
- Tillegg for leveringsmåter er ikke konsekvent mellom valget av leveringsmåte og ordresammendraget i kassen.

For å kunne løse disse problemene må du aktivere funksjonen **Aktiver konsekvent leveringsmåtehåndtering i kanal**. Denne funksjonen sikrer at ufordelte tillegg på hodenivå vises i e-handelskanaler, og at leveringsinformasjon for salgsordrer håndteres konsekvent av samme arbeidsflyt for forespørsel.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Aktiver funksjonen Aktiver konsekvent leveringsmåtehåndtering i kanal

Følg denne fremgangsmåten for å aktivere funksjonen **Aktiver konsekvent leveringsmåtehåndtering i kanal** i Commerce Headquarters.

1. Åpne arbeidsområdet **Funksjonsbehandling** (**Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**).
1. Søk etter og velg **Aktiver konsekvent leveringsmåtehåndtering i kanal** i listen over tilgjengelige funksjoner.
1. Velg **Aktiver nå** i høyre rute.
