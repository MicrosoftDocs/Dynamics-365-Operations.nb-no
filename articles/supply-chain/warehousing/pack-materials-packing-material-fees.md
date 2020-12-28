---
title: Pakkematerialer og -gebyrer
description: Dette emnet gir informasjon om emballasjematerialegebyr som betales til resirkuleringsfirmaer ved bestemte intervaller.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1061f336701461df7a2cf78661788e4c6100c84d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434292"
---
# <a name="packing-materials-and-fees"></a>Pakkematerialer og -gebyrer

[!include [banner](../includes/banner.md)]

Emballasjematerialegebyrer betales til et resirkuleringsfirma med spesifikke intervaller. Et beløp betales per vektenhet for hvert materiale som en emballasjeenhet består av. Selv om emballasjematerialegebyrer beregnes og rapporteres, posteres ingen finanstransaksjoner fordi gebyrene ikke regnes som avgifter som må betales til en myndighet.

Emballasjevekt og -gebyrer beregnes for både salgsordrelinjer og bestillingslinjer.

Du kan definere én eller flere emballasjeenheter for én enkelt vare, for en varegruppe (pakkegruppe) eller for alle varer. En emballasjeenhet består av emballasjematerialer, vekt og antall varer som er tatt med i emballasjeenheten. En emballasjekode er tilordnet til hver type emballasje som er definert. Basert på emballasjekoden kan du angi en pris for en spesifikk periode. Emballasjegebyret beregnes basert på denne informasjonen.

> [!NOTE]
> Selv om firmaet ikke betaler emballasjegebyrer, kan du bruke funksjonaliteten til å beregne statistikk for emballasjevekt.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Definere tildeling for emballasjemateriale

Før du kan beregne emballasjematerialevekt, emballasjematerialegebyrer eller begge deler, må du aktivere beregningen og definere hvilke materialer og gebyrer varene skal gjelde for.

1. Gå til **Lagerstyring \> Oppsett \> Parametere for beholdnings- og lagerstyring**.
1. I kategorien **Generelt**, i delen **Emballasjemateriale**, angir du **Beregn emballasjegebyrer** til **Ja**.
1. Gå til **Lagerstyring \> Oppsett \> Emballasjemateriale \> Emballasjegrupper**, og opprett alle emballasjegruppene du bruker. Alle varene i en emballasjegruppe vil bruke samme emballasjematerialefordeling. Hvis du ikke bruker emballasjegrupper, kan du hoppe over dette trinnet.

    > [!TIP]
    > Når du har opprettet emballasjegruppene, kan du tilordne en gruppe til hvert produkt slik du ønsker. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**, velg et produkt, og gå deretter til hurtigfanen **Administrer lager** og feltet **Emballasjegruppe**, og velg den aktuelle emballasjegruppen.

1. Gå til **Lagerstyring \> Oppsett \> Emballasjemateriale \> Emballasjematerialekoder**, definer hver type emballasjemateriale som du bruker, og angi enheten som emballasjematerialet forbrukes i, når du klargjør forsendelser.
1. Gå til **Lagerstyring \> Oppsett \> Emballasjemateriale \> Emballasjematerialegebyrer**, og angi et gebyr for hver type emballasjemateriale som du akkurat har definert. Gebyrer beregnes på grunnlag av prisen per enhet som er brukt.
1. Hvis du vil tilordne emballasjemateriale til varer, går du til **Lagerstyring \> Oppsett \> Emballasjemateriale \> Tildeling av emballasje** og oppretter tildelinger. Du kan opprette så mange tildelinger du vil. Du kan tilordne emballasjematerialer for enkeltvarer, grupper av varer (emballasjegrupper) eller alle varer, avhengig av hvor detaljert fordelingene skal være.

    For hver tildeling du har opprettet, gjør du følgende.

    1. Angi følgende felt i hurtigfanen **Generelt**:

        - **Varekode** – Velg omfanget for tildelingen:

            - **Tabell** – Opprett en tildeling for en enkelt bestemt vare.
            - **Gruppe** – Opprett en tildeling for alle varene som tilhører en emballasjegruppe, som er definert på siden **Emballasjegrupper**.
            - **Alle** – Opprett en tildeling for alle varer.

            > [!NOTE]
            > Vanligvis bør du utføre alle tildelingene på samme nivå (**tabell**, **gruppe** eller **alle**). Hvis du bruker mer enn ett nivå, vil den mest spesifikke samsvarende tildelingen bli brukt for hver vare. (**Tabell**-nivået har prioritet over **Gruppe**-nivået, og begge nivåer har forrang over **Alle**-nivået.)

        - **Varerelasjon** – Hvis du tildeler for en enkelt vare, velger du varen. Hvis du tildeler for en gruppe varer, velger du emballasjegruppen. Hvis du tildeler for alle varer, lar du dette feltet stå tomt.
        - **Konfigurasjon**, **Størrelse**, **Farge** og **Stil** – Angi verdier for disse dimensjonene som du trenger, for å definere varen du tildeler for.
        - **Emballasjeenhet** – Velg enheten som varen pakkes inn i, når emballasjematerialet brukes. Denne enheten kan avvike fra enheten som varen kjøpes og lagres i.
        - **Emballasjeenhetsfaktor** – Angi omregningsfaktoren som skal brukes til å konvertere fra lagerenheten til emballasjeenheten. (Konverteringen bruker formelen *Emballasjeenheter* = *Vareenheter* × *Emballasjeenhetsfaktor*.)

    1. I hurtigfanen **Emballasjemateriale** legger du til en linje for hvert stykke emballasjemateriale som trengs for den gjeldende tildelingen. På hver linje angir du materialetypen (som definert på siden **Emballasjematerialekoder**) og hvor mye av den som forbrukes for hver sendte enhet av den gjeldende varen.

## <a name="packing-units-on-sales-order-lines"></a>Emballasjeenheter på salgsordrelinjer

Når du har [aktivert beregningen for emballasjegebyrer og satt opp tildelingene dine](#allocations), kontrollerer systemet at emballasjeenhetene er angitt for hver vare som legges til i en salgsordre. Deretter beregnes eventuelle gebyrer som kreves. Når en vare legges til en salgsordre, skjer ett av følgende:

- **Hvis en emballasjetildeling gjelder for varen:** Systemet oppdaterer salgsordrelinjen med den angitte emballasjeenheten og antallet for emballasjeenheten. (Antallet for emballasjeenheten beregnes etter formelen *Emballasjeenhetsantall* = *Bestilt antall* ÷ *Antall varer i den valgte emballasjeenheten*.)
- **Hvis ingen emballasjetildeling gjelder for varen:** Du kan angi en emballasjeenhet manuelt og et antall for emballasjeenhet på salgsordrelinjen.

Du kan også endre emballasjeenheten og antallet for emballasjeenhet når du posterer salgsordrelinjen. Denne funksjonen aktuell hvis salgsordrelinjen bare er delvis levert eller delvis fakturert.

Når du fakturerer salgsordren, oppretter systemet emballasjetransaksjoner. Emballasjetransaksjoner inneholder vekt for emballasjematerialer for salgslinjen. Du kan endre transaksjonene etter at du har fakturert dem. Du kan deretter opprette de nye transaksjonene.

## <a name="packing-units-on-purchase-order-lines"></a>Emballasjeenheter på bestillingslinjer

Systemet oppretter ikke emballasjematerialetransaksjoner for bestillingslinjer. I stedet oppretter du transaksjoner for fakturerte bestillingslinjer manuelt på siden **Emballasjematerialetransaksjoner**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Definere lisensnumre for kunder som er belastet for emballasjematerialegebyrer

Hvis salgsordrene for en bestemt kunde skal ta med tillegg for emballasjematerialene som brukes for hver ordre, følger du denne fremgangsmåten.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden som skal belastes for emballasjematerialer.
1. Angi følgende felt i hurtigfanen **Faktura og levering**:

    - I delen **Merverdiavgift**, feltet **Lisensnummer for emballasjeavgift**, angir du firmaets lisensnummer.
    - I delen **Emballasjematerialegebyr**, feltet **Lisensnummer**, angir du firmaets lisensnummer.

Når du nå oppretter og fakturerer en salgsordre som inkluderer én eller flere varer som bruker emballasjematerialer, viser fakturaen emballasjematerialegebyrene.

For kunder som ikke skal betale emballasjematerialegebyr, følger du den samme fremgangsmåten, men fjerner lisensnumrene fra feltene **Lisensnummer for emballasjeavgift** og **Lisensnummer**. Fakturaer for kunder som ikke betaler emballasjematerialegebyrer, viser vekten til emballasjematerialet, men de viser ikke gebyrene.

Hvis du vil generere en rapport som viser alle emballasjematerialegebyrene som firmaet skal skylde for en bestemt periode, går du til **Lagerstyring \> Forespørsler og rapporter \> Emballasjerapporter \> Beregning av emballasjegebyr**, angi et datoområde, og velg deretter **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Skrive ut emballasjematerialets vekt på fakturaer

Du kan skrive ut emballasjematerialets vekten på en faktura og angi hvem som betaler de relaterte gebyrene. Vekten summeres etter emballasjekode.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
1. På fanen **Oppdateringer**, på hurtigfanen **Faktura**, angir du **Skriv ut emballasjevekt** til **Ja**.
