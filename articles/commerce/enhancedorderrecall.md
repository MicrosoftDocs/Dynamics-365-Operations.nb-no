---
title: Tilbakekall ordre-operasjon i POS
description: Dette emnet inneholder funksjoner som er tilgjengelige for forbedrede sider for tilbakekalling av ordrer i POS.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799113"
---
# <a name="recall-order-operation-in-pos"></a>Tilbakekall ordre-operasjon i POS

[!include [banner](includes/banner.md)]

**Tilbakekall ordre**-operasjonen i Commerce-salgsstedet (POS) inneholder oppdaterte funksjoner for ordresøk og -filtrering og ordrespesifikk informasjon. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.15 og nyere.

Hvis du vil aktivere denne funksjonaliteten, aktiverer du funksjonen **Forbedret tilbakekall ordre-operasjon i POS** i arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters. Når du har aktivert funksjonen, bør du vurdere å oppdatere [skjermoppsettene](pos-screen-layouts.md) i POS for å dra nytte av noen av de endrede funksjonene.

Konfigurasjon av knappen for **Tilbakekall ordre**-operasjonen lar organisasjoner distribuere operasjonen med en forhåndsdefinert visning.

![Konfigurasjon for knappegruppe](media/recallorderbuttongrid.png)

Visningsalternativene er som følger:
- **Ingen** – Dette alternativet distribuerer operasjonen uten en bestemt visning. Når en bruker åpner operasjonen med denne konfigurasjonen, blir de bedt om å søke etter og finne ordrer, eller velge fra et forhåndsdefinert ordrefilter.
- **Ordrer som skal oppfylles** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som skal oppfylles av brukerens gjeldende butikk. Disse ordrene er konfigurert for henting i butikk eller butikkforsendelse, og linjene i disse ordrene er ennå ikke plukket eller pakket.
- **Ordrer som skal hentes** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for henting i butikk i brukerens gjeldende butikk.
- **Ordrer som skal leveres** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for levering fra brukerens gjeldende butikk.

Når du starter **Tilbakekall ordre**-operasjonen fra POS og visningen er konfigurert til **Ingen**, kan en bruker søke etter og hente ordrer på én av måtene nedenfor.
- Skanne ordrestrekkoder. Dette søker etter samsvarende felt for ordrenummer, kanalreferanse og kvitterings-ID.
- Velg **Søk etter ordrer**- eller **Søk og filtrer**-ikonet på applinjen for å bruke filtreringsmekanismen til å finne ordrer som oppfyller filterkriteriene.
- Velg fra et forhåndsdefinert filter fra rullegardinmenyen **Vis ordrer** (ordrer som skal oppfylles, ordrer som skal hentes, eller ordrer som skal leveres).

![RecallOrderMainMenu](media/recallordermain.png)

Når søkekriteriene er brukt, vil appen vise en liste over samsvarende salgsordrer. Det er viktig å merke seg at når du bruker søke-/filteralternativene, trenger ikke ordrene som hentes, være ordrer som er koblet til brukerens gjeldende butikk. Denne søkeprosessen henter og viser alle kundeordrer som samsvarer med søkekriteriene, selv om ordren ble opprettet eller angitt til å bli utført av en annen butikk/kanal eller lagerlokasjon.

![RecallOrderDetail](media/orderrecalldetail.png)

En bruker kan velge en ordre i listen for å vise flere detaljer. Informasjonspanelet til høyre på skjermen viser informasjon om den valgte ordren, inkludert ordrelinjedetaljer, leveringsdetaljer og oppfyllingsdetaljer.

Fra applinjen kan en bruker velge en operasjon. Det kan hende at bestemte operasjoner ikke er aktivert, avhengig av statusen for ordren.

- **Retur** – Starter prosessen med å opprette en retur for alle de fakturerte produktene på den valgte kundeordren.

- **Avbryt** – Utsteder en fullstendig annullering av den valgte salgsordren. Dette alternativet er ikke tilgjengelig for ordrer som startes via en samtalesenterkanal, og kan ikke brukes til å avbryte en ordre delvis.

- **Oppfyll** – Overfører brukeren til siden for ordreoppfylling som blir forhåndsfiltrert for den valgte ordren. Bare ordrelinjer som er åpne for oppfyllelse av brukerens butikk for den valgte ordren, vises.

- **Rediger** – Lar brukere gjøre endringer i den valgte kundeordren. Ordrer kan bare redigeres i [bestemte scenarioer](customer-orders-overview.md#edit-an-existing-customer-order).

- **Henting** – Dette alternativet vil være tilgjengelig hvis ordren har én eller flere linjer angitt for henting i brukerens gjeldende butikk. Denne operasjonen starter henteflyten, slik at brukeren kan velge hvilke produkter som skal hentes, og opprette salgstransaksjoner for hentingen.

## <a name="add-notifications-to-the-recall-order-operation"></a>Legge til meldinger i operasjonen for tilbakekalling av ordre

I versjon 10.0.18 og senere kan du konfigurere POS-meldinger og direkte flisvarslinger for operasjonen **Tilbakekalling av ordre** hvis dette er ønskelig. Hvis du vil ha mer informasjon, kan du se [Vise ordrevarslinger på salgsstedet](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
