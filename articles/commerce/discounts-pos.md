---
title: Vis rabatter i salgssted
description: I denne artikkelen finner du informasjon om hvordan Microsoft Dynamics 365 Commerce hjelper selgere med å lære om kampanjer og hvordan de kan brukes for krysssalg- og videresalgsbevegelser.
author: ShalabhjainMSFT
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, Commerce
ms.search.form: ''
ms.openlocfilehash: 706c13bf090b2ad3826d17bbbeda8a2fa7733f2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287715"
---
# <a name="show-discounts-in-pos"></a>Vise rabatter i POS

[!include [banner](includes/banner.md)]

Kampanjer spiller en viktig rolle i motivering av kunder som foretar innkjøpsavgjørelser. Ferier kan for eksempel produsere det høyeste antallet salg for forhandlere, fordi hele detaljmarkedet blir oversvømt med kampanjer og rabatter. Hvis butikkforbindelser vet om og forstår tilgjengelige kampanjer, kan de enkelt dra nytte av disse kampanjene for å oppnå kryss- og mersalg. I denne artikkelen finner du informasjon om hvordan Microsoft Dynamics 365 Commerce hjelper selgere med å lære om kampanjer og hvordan de kan brukes for krysssalg- og videresalgsbevegelser.

## <a name="learn-about-store-discounts"></a>Lær mer om butikkrabatter

Commerce inkluderer en operasjon med navnet Vis alle rabatter. Denne operasjonen viser alle rabattene som i øyeblikket kjøres i en butikk. Operasjonen Vis alle rabatter kan tilordnes en knapp i salgsstedet (POS), og denne knappen kan legges til på **velkomstsiden** eller **transaksjonssiden**. Illustrasjonen nedenfor viser et eksempel på siden **Alle rabatter** som åpnes.

![Siden Alle rabatter.](./media/View_all_discounts.png "Siden Alle rabatter")

For å vise rabatter ser systemet etter alle rabattene som samsvarer med én eller flere av følgende betingelser:

- Prisgruppen for rabatten samsvarer med prisgruppen for butikken.
- Prisgruppen for rabatten tilordnes til et tilknytnings- eller fordelsprogram.
- Prisgruppen for rabatten tilordnes til en katalog som er knyttet til butikken.

Siden **Alle rabatter** viser bare enkelte kupongbaserte rabatter, fordi forhandlere vanligvis oppretter tusenvis av kuponger og korresponderende rabatter for unike kunder, og denne siden er ikke ment å vise kundespesifikke rabatter. Kupongbaserte rabatter vises bare hvis alternativet **Bruk uten en kupongkode** er aktivert i hver kuponghode. I så fall kan kasserere bruke kupongen uten å måtte angi eller skanne noen kupongkode eller strekkode.

Når alternativet **Bruk uten en kupongkode** er aktivert, blir ulike scenarier tilgjengelige. Kasserere kan for eksempel gi flere rabatter til kunder for økt kundetilfredshet eller på grunn av produktfeil. Utskrevne kupongkoder eller strekkoder må ikke distribueres til kasserere. Kasserere kan i stedet velge **Bruk kupong**-knappen. Kupongen brukes deretter automatisk på transaksjonen. Hvis det finnes flere kuponger for et kuponghode, vil systemet automatisk velge den første aktive kupongen på transaksjonen.

På siden **Alle rabatter** kan salgsforbindelser også søke i rabatter etter nøkkelord. Nøkkelordsøk søker i feltene som inneholder rabattnavnet og rabattbeskrivelsen. Salgsforbindelser kan også filtrere rabatter på grunnlag av om en rabatt krever en kupongkode.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Kryss- og mersalg ved hjelp av rabatter

Samkjøpsrabatter, for eksempel kvantumsrabatter, samlerabatter og terskelrabatter, er en fin måte å motivere kunder til å kjøpe flere produkter på for å få større rabatter. De bidrar derfor også til å øke størrelsen på kundens handlevogn og detaljomsetning. Disse rabattene kan publiseres på webområder for e-handel, sosiale medier og bannere i butikken.

Selv når alle disse reklamemetodene brukes, kan det hende at kundene går glipp av muligheten til å dra nytte av kampanjer. For å gjøre det lettere for salgsmedarbeidere å finne ut hvilke kampanjer som gjelder for en valgt linje, eller til og med hele handlekurven, kan forhandlerne legge til knappen for **"Vis tilgjengelige rabatter"**-operasjonen i knappegruppen på siden **Transaksjon**. Dette gjør at en salgsmedarbeider kan velge en transaksjonslinje, og deretter velge knappen for å vise alle rabattene som er tilgjengelige for den valgte linjen. Salgsmedarbeideren kan også velge en annen kategori for å vise rabatter som gjelder for hele transaksjonen. Det er viktig å legge merke til at **Vis tilgjengelige rabatter** ikke viser rabatter som allerede er brukt på salgslinjen, fordi rabattinformasjonen allerede vises på salgslinjen. Formålet med dette scenariet er å bare vise rabattene som ennå ikke er brukt. Unntaket til dette er rabattene som brukes basert på en kupong som er merket som "Bruk uten en kupongkode". Dette gjør det enkelt for salgsmedarbeideren å fjerne fjerne kupongen de har brukt.

Siden **Alle rabatter** viser bare rabatter som ikke konkurrerer med noen av de brukte rabattene. Denne virkemåten bidrar til å sikre at hvis en salgsmedarbeider gir en kunde informasjon om rabatt, og kunden utfører den nødvendige handlingen (for eksempel kjøper kunden en vare til for å få 10 prosent rabatt), brukes rabatten på transaksjonen. De kupongbaserte rabattene vises bare hvis alternativet **Bruk uten en kupongkode** er aktivert.

I et enkelt scenario der alle rabatter har samme prioritet, blir samtidighetsmodus for rabatt **Sammensatt**, og samtidighetskontroll for rabatt er satt til **Beste pris og sammensatt i prioritet, aldri sammensatt på tvers av prioriteter**, viser **Alle rabatter**-siden alle tilgjengelige rabatter for et produkt, fordi alle rabattene er sammensatte og ikke konkurrerer med hverandre.

Illustrasjonene nedenfor viser logikken som bestemmer hvilke rabatter som vises i avanserte scenarier, for eksempel et scenario der samtidighetsmodus for rabatt er **Beste pris** eller **Eksklusiv**, og to eller flere prioriteringer brukes. I disse scenariene påvirkes også rabattene som vises, basert på om samtidighetskontrollen for rabatt er satt til **Beste pris og sammensatt i prioritet, aldri sammensatt på tvers av prioriteter** eller **Beste pris bare innen prioritet, alltid sammensatt på tvers av prioriteter**.

Følgende illustrasjon viser logikken som brukes når samtidighetskontrollen for rabatt er satt til **Beste pris og sammensatt i prioritet, aldri sammensatt på tvers av prioriteter**.

![Logikk for Beste pris og sammensatt i prioritet, aldri sammensatt på tvers av prioriteter.](./media/Model_1.png "Logikk for Beste pris og sammensatt i prioritet, aldri sammensatt på tvers av prioriteter").

Følgende illustrasjon viser logikken som brukes når samtidighetskontrollen for rabatt er satt til **Beste pris bare innen prioritet, alltid sammensatt på tvers av prioriteter**.

![Logikk for Beste pris bare innen prioritet, alltid sammensatt på tvers av prioriteter.](./media/Model_2.png "Logikk for Beste pris bare innen prioritet, alltid sammensatt på tvers av prioriteter").


[!INCLUDE[footer-include](../includes/footer-banner.md)]
