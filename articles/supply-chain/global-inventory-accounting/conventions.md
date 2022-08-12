---
title: Konvensjoner
description: Denne artikkelen beskriver hvordan du definerer konvensjoner for å fastsette hvordan kostnader skal beregnes i Globalt lagerregnskap.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f148d4c6ece543c8a11eee3e6dcdff47b3767936
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135513"
---
# <a name="conventions"></a>Konvensjoner

[!include [banner](../includes/banner.md)]

En konvensjon er en container for et sett med policyer som påvirker systemvirkemåten. På grunnlag av forretningskravene må du definere konvensjoner ved å bruke en kombinasjon av de forskjellige policyene som fastsetter hvordan kostnader skal regnskapsførers i globalt lagerregnskap. Du kan knytte hver konvensjon til én eller flere finansmoduler for å sikre konsekvens i regnskapspolicyer som gjelder i alle finansmodulene.

Hvis du vil definere konvensjonene, kan du gå til **Globalt lagerregnskap \> Oppsett \> Konvensjoner**. For hver konvensjon angir du feltene nedenfor:

- **Navn** – Angi navnet på konvensjonen.
- **Beskrivelse** – Angi en beskrivelse av konvensjonen.
- **Kostnadsobjektpolicy** – Velg en kostnadsobjektpolicy. Disse policyene bestemmer detaljnivået som systemet bruker til å beregne og vedlikeholde lagerverdien. Følgende forhåndsdefinerte alternativer er tilgjengelige:

    - Produkt
    - Produkt – Område
    - Produkt – Område – Lager

    Hvis du for eksempel velger *Produkt – Område* for hver lagerbevegelse (innflyt eller utflyt), beregner og vedlikeholder systemet lagerkostnaden for hvert produkt på områdenivå. Lagerbevegelser på lavere nivåer, for eksempel lagernivå, påvirker derfor ikke lagerverdien. (Et eksempel på en lagernivåoverføring er en vareoverføring mellom to lagre i ett område.) På samme måte kan du ikke vise lagerkostnaden på et lavere nivå, for eksempel lagernivået.

- **Policy for målingsgrunnlag for inndata** – Velg en policy for målingsgrunnlag for inndata. Disse policyene bestemmer kostnadene som skal flyte inn i lagerkontoen, og kostnadene som skal belastes. Følgende alternativer er relevante for handelsselskaper:

    - **Normal historisk** – Alle kostnadskomponentene flyter til lagerkontoen.
    - **Standard** – Standard kostnadsflyt til lagerkontoene, og forskjellen mellom brukte kostnader og de faktiske kostnadene belastes avvikskontoene. Hvis du vil opprette en *Standard* policy for måling av inndata, må du først opprette en prisliste der policyen kan slå opp varens standardkost.
    - **Prislister** – Globalt lagerregnskap støtter henting av varepriser fra flere juridiske enheter. Du kan definere en prisliste som policy for målingsgrunnlag for inndata skal bruke. På denne måten vet systemet hvor du skal slå opp vareprisen. Følg disse trinnene for å konfigurere prislister:

        1. Angi et navn i **Navn**-feltet.
        1. Angi en beskrivelse i **Beskrivelse**-feltet.
        1. I feltet **Kosttype** velger du kosttype (*Standardkostnad* eller *Planlagt kostnad*).
        1. I **Pristype**-feltet velger du en pristype (*Kostnad*, *Innkjøp* eller *Salgspris*).
        1. Legg til en kostnadsversjon.
        1. Velg **Pris** i handlingsruten for å validere vareprisene i prislisten.

- **Policy for kostnadsflytforutsetning** – Velg en policy for kostnadsflytforutsetning. Disse policyene bestemmer hvordan kostnader fjernes fra lageret og rapporteres som solgte varers kost. Følgende forhåndsdefinerte alternativer er tilgjengelige:

    - Gjennomsnitt
    - Spesifikk – parti

    > [!NOTE]
    > Globalt lagerregnskap er et permanent lagersystem. Derfor sporer systemet lagerverdien transaksjon for transaksjon.

- **Kostnadselementpolicy** – Du kan definere kostnadselementpolicyer og koble dem til dette feltet. Et *kostnadselement* er kostnaden for en ressurs som forbrukes av en hendelse. Du kan bruke kostnadselementer til å spore og kategorisere kostnader. Hvis du vil opprette policyer for kostnadselementer, angir du informasjon på følgende steder:

    - **Navn**-felt
    - **Beskrivelse**-felt
    - **Kostnadselement**-liste
    - **Regler**-rutenett

    Hvis du ikke vil dele inn lagerverdien ytterligere, må du likevel opprette en kostnadselementliste som har ett enkelt kostnadselement. Deretter må du opprette en policy for kostnadselement for å tilordne alle de relevante målingstypene (kostnadskomponentene) til kostnadselementet.
