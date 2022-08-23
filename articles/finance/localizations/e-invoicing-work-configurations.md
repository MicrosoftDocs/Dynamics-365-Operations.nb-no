---
title: Arbeid med konfigurasjoner
description: Denne artikkelen gir en oversikt over hovedscenarioet for arbeid med konfigurasjoner for elektronisk rapportering (ER) fra arbeidsområdet for globaliseringsfunksjoner.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283063"
---
# <a name="work-with-configurations"></a>Arbeid med konfigurasjoner

[!include [banner](../includes/banner.md)]

Konfigurasjoner for elektronisk rapportering (ER) er et av hovedsettene med komponenter for funksjoner for elektronisk fakturering. En ER-konfigurasjon inneholder oppsettet for filstrukturen og et sett med transformasjonsregler for å transformere data på to måter:

- **Eksporter ER-formatkonfigurasjon** – Denne konfigurasjonen transformerer data fra den enhetlige interne strukturen (ER-modellen) til det elektroniske filformatet.
- **Importer ER-formatkonfigurasjon** – Denne konfigurasjonen transformerer data fra det elektroniske filformatet til den enhetlige interne strukturen (ER-modellen).

I tillegg til å generere utgående elektroniske filer i det forhåndsdefinerte formatet brukes ofte ER-konfigurasjoner til å dele opp innkommende meldinger fra eksterne nettjenester som svar. Denne funksjonaliteten bidrar til å bygge konfigurerbar logikk for å hente resultatene av kommunikasjon med eksterne kanaler, konvertere disse resultatene (koder, meldinger og logger) til strukturen som kan leses av brukere, og deretter sende denne informasjonen til klientprogrammet.

Hvis du vil begynne å bruke ER-konfigurasjoner i funksjonen for elektroniske fakturering, må du koble dem til funksjonen og gjøre dem tilgjengelige i **Konfigurasjoner**-fanen for gjeldende funksjonsversjon. Du kan arbeide med en koblet ER-konfigurasjon ved å velge **Legg til**, **Slett**, **Rediger** eller **Vis**.

Før du kan legge til en kobling i en ER-konfigurasjon, må konfigurasjonen finnes i Regulatory Configuration Service (RCS). Følg denne fremgangsmåten for å gå gjennom ER-konfigurasjonene som er tilgjengelige i RCS-repositoriet.

1. Logg på RCS-kontoen.
2. I delen **Konfigurasjoner** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.

Hvis du vil ha mer informasjon om hvordan du oppretter en ny ER-konfigurasjon eller importerer en eksisterende ER-konfigurasjon fra det globale repositoriet, kan du se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Hvis du vil justere en koblet ER-konfigurasjon, velger du **Rediger** i **Konfigurasjoner**-fanen for gjeldende funksjon for elektroniske fakturering. Systemet oppretter automatisk en versjon av ER-konfigurasjonen. Hvis den gjeldende versjonen ikke ble opprettet av den aktive konfigurasjonsleverandøren, oppretter systemet en avledet versjon som bruker konfigurasjonsleverandøren. Hvis den gjeldende versjonen ble opprettet av den aktive konfigurasjonsleverandøren, oppretter systemet en ny versjon. I begge tilfeller kan du endre versjonen som opprettes, og deretter utføre alle nødvendige oppdateringer automatisk.
