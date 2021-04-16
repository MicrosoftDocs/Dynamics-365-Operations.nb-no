---
title: Salgsstedsforbedringer for serialiserte produkter
description: Dette emnet inneholder forbedringer som er gjort på serialiserte produkter, slik at du kan spare tid og være mer produktiv.
author: ShalabhjainMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 45376e43c00116d403f00c58772aefba6fa33eeb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794025"
---
# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Salgsstedsforbedringer for serialiserte produkter

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Oversikt

Basert på innstillingene i Commerce-hovedkontoret kan produktene klassifiseres som serialiserte eller ikke-serialiserte. Når produktene er serialiserte, kan hvert element tildeles et unikt nummer som hjelper til med å spore garantier, spore elementer og bekrefte eierskap. lv om muligheten til å gi serienumre for serielle produkter eksisterte i våre Modern/Cloud Point of Sale (POS), har det blitt lagt til noen forbedringer for å hjelpe kasserere å spare tid og være mer produktive.

## <a name="pos-improvements"></a>POS-forbedringer

- **Serienummer er ikke påkrevd før i kassen** – Tidligere måtte en kasserer som la et serialisert produkt til transaksjonen oppgi et serienummer. Dette kravet ble et problem i kundescenarier, hvis kasserere og salgsforbindelser hadde mulighet til å selge produkter. Frem til betalingstrinnet ble produktene ofte oppdatert i handlekurven. Hver gang en kasserer la til et nytt produkt, ba systemet derfor om å få serienummeret. Dialogboksen for serienummer har nå en **Legg til senere**-knapp. Derfor kan salgsorganisasjonen legge til et element til transaksjonen, men kan oppgi serienummeret senere. Salgsorganisasjonen kan raskt legge til og erstatte serialiserte produkter i handlekurven, og deretter gi serienummer rett før utsjekking. Hvis serienummeret ikke er oppgitt for et serialisert produkt, vil en kasserer motta en feilmelding når den prøver å fullføre transaksjonen. Disse meldingene forteller at kassereren må gi de manglende serienumrene før han eller hun kan fortsette.

    For hvert serialisert element der man hoppet over serienummeret, vises en kommentar under transaksjonslinjen. Kommentaren forteller at serienummer ikke er oppgitt for denne artikkelen. Derfor kan kassereren raskt finne produkter som mangler serienummer.

    En ny **Legg til serienummer**-operasjoner gir også serienummeret for produkter som mangler et serienummer. Etter at serienummer er gitt kan det ikke redigeres. Kassereren må annullere linjen og legge til produktet på nytt.
    
- **Serienummer er ikke påkrevd for å plassere kundeordrer** – Kundeordrer kan plasseres i en butikk og oppfylles fra en annen butikk. En kasserer som plasserer en kundeordre trenger ikke å oppgi serienummeret. Serienummeret vil gis under henting eller i hente-trinnet. Imidlertid må det oppgis et serienummer for alle linjeposter hvor leveringstypen er valgt som **Gjennomført**. Hvis ikke kan ikke transaksjonen fullføres.
- **Serialiserte produkter samles ikke på transaksjonsskjermbildet**. – Innstillingen for **Aggregate produkter** i feltgruppen **Terminal** på siden **Funksjonalitetsprofil** lar deg aggregere de samme ikke-serielle produktene på transaksjonsskjermen. Når de samme produktene er aggregert, er de lettere å se i transaksjonsnettverket. Men fordi serienumrene generelt er unike, og salgsmedarbeidere ikke trenger å skrive inn serienumre til kassa, gjelder ikke innstillingen for **Aggregerte produkter** ved serialiserte produkter. Derfor blir ikke serielle produkter samlet på transaksjonsskjermbildet hvis innstillingen for **Aggreger produkter** er valgt.
- **Muligheten til å søke i journaler etter serienummer** – Det er nå også mulig å søke etter serienummer i journalene. Hvis du vil gjøre dette, åpner du operasjonen "Journaler" og trykker på knappen "Avansert søk" i feltet i appen. Ved hjelp av knappen "Legg til filter" kan et filter brukes for å søke etter serienumrene også.


[!INCLUDE[footer-include](../includes/footer-banner.md)]