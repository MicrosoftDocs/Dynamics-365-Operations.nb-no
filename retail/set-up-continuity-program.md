---
title: Definere et kontinuitetsprogram for et telefonsenter
description: Denne artikkelen beskriver hvordan du setter opp et kontinuitetsprogram for et telefonsenter.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c0a9eec6bdf67deca885b30082b958869e64aae2
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017



---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Definere et kontinuitetsprogram for et telefonsenter

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver hvordan du setter opp et kontinuitetsprogram for et telefonsenter.

I et kontinuitetsprogram, som også kalles et program for regelmessige ordrer, mottar kunder regelmessige produktforsendelser i henhold til en forhåndsdefinert tidsplan. Hver forsendelse kan inneholde et forskjellig produkt, som for eksempel månedens bok i en bokklubb, eller det samme produktet kan sendes gjentatte ganger. Du må fullføre følgende oppgaver hvis du vil definere et kontinuitetsprogram.

1.  Angi kontinuitetsparametere på siden **Telefonsenterparametere**.
2.  Opprett deretter et kontinuitetsprogram som angir detaljer, for eksempel betalingsplanen, tidfestingen av forsendelsene, og om det faktureres på forhånd. Du må også legge til en liste over produkter som er inkludert i kontinuitetsprogrammet. Hvert produkt mottar et hendelses-ID-nummer som tilordnes sekvensielt fra 1. Hendelses-ID-er bestemmer rekkefølgen som produktene sendes i.
    -   Hvis kunder mottar forskjellige produkter i hver forsendelse, sendes produktene i rekkefølge basert på deres hendelses-ID fra og med gjeldende hendelse.
    -   Hvis kunder mottar det samme produktet i hver forsendelse, inneholder listen bare ett produkt som har én hendelses-ID. Samme hendelse forekommer gjentatte ganger. Du kan angi hvor mange ganger hver hendelse gjentas.

3.  Opprett et overordnet produkt som representerer kontinuitetsprogrammet du opprettet i oppgave 2. Hvis du legger til dette produktet i en salgsordre, åpnes siden **Kontinuitet**. Du kan deretter bruke denne siden til å opprette den faktiske kontinuitetsordren. Det overordnede produktet angir ikke enkeltproduktene som kunden mottar i hver forsendelse.

Når du har definert et kontinuitetsprogram som beskrevet ovenfor, kan du opprette en kontinuitetsordre for en kunde. Du må kanskje også utføre følgende ekstra vedlikeholdsoppgaver.

-   **Oppdatere gjeldende hendelsesperiode for kontinuitet** – Konfigurer en satsvis jobb som angir for systemet hva gjeldende hendelsesperiode er.
-   **Opprett underordnede kontinuitetsordrer** – Opprett underordnede ordrer fra den overordnede kontinuitetsordren.
-   **Behandle kontinuitetsbetalinger** – Behandle fakturering og varsler for betalinger som er knyttet til kontinuitetssalgsordrer.
-   **Utvid kontinuitetslinjer** (om nødvendig) – Utvid antall ganger en kontinuitetshendelse kan gjentas. Gjentakelsen av forsendelser kan deretter gå utover grensen som er angitt i feltet **Terskel for kontinuitetsgjentakelse** i telefonsenterparameterne.
-   **Utfør en kontinuitetsoppdatering** (om nødvendig) – Synkroniser endringer mellom kontinuitetsprogrammet og de overordnede kontinuitetssalgsordrene.
-   **Lukk overordnede kontinuitetslinjer og -ordrer** – Lukk kontinuitetsordrer.





