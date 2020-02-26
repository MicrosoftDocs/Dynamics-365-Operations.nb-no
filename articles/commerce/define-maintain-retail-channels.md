---
title: Definere og vedlikeholde detaljhandelskanaler
description: Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles butikker i Dynamics 365 Commerce. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en butikk.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 63639d69af90c6aa37bbf7af7868bca71942063f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023503"
---
# <a name="define-and-maintain-retail-channels"></a>Definere og vedlikeholde detaljhandelskanaler

[!include [banner](includes/banner.md)]

Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles butikker i Dynamics 365 Commerce. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en butikk.

Handel støtter flere kanaler, for eksempel nettbutikker, telefonsentre og fysiske butikker. En fysisk butikk kalles en butikk. Hver butikk kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte. Du må definere alle disse elementene for en butikk, før du oppretter den. Når du har opprettet en butikk, tilordner du produktene du vil den skal føre. Du tilordner også ansatte, kasser og kunder til butikken. Til slutt legger du til den nye butikken i et organisasjonshierarki.

## <a name="setting-up-stores"></a>Sette opp butikker

Før du kan definere en butikk i Handel, må du fullføre noen nødvendige oppgaver. Du kan deretter opprette butikken og legge til detaljer.

### <a name="prerequisites"></a>Forutsetninger

Du må fullføre følgende oppgaver før du kan definere en butikk:

1. Konfigurer organisasjonsstrukturen, og definer organisasjonshierarkier for detaljhandelssortimenter, -etterfylling og -rapportering.
2. Definere et lager som representerer butikken.
3. Definer nummerserier for butikker, butikkutdrag og utdragsbilag.
4. Konfigurer parametere for Handel.
5. Definer betalingsmåtene butikken godtar.
6. Hvis du vil behandle kredittkorttransaksjoner i kasser på salgssteder, kan du også konfigurere betalingstjenester.
7. Definer mva-grupper.
8. Definer detaljprodukter. Som en del av denne oppgaven definerer du også produkthierarkier, produktvarianter og produktsortimenter.
9. Definer produktgrupper.
10. Sett opp produktprising. Som en del av denne oppgaven definerer du også prisjusteringer, rabatter og rabattperioder.
11. Definere stabsmedlemmer.

    > [!NOTE]
    > Du må også tilordne aktuelle tillatelser til arbeiderne, slik at de kan logge på og utføre oppgaver ved hjelp av salgsstedssystemet.

12. Konfigurer salgsstedsprofiler som skal tilordnes butikken. Denne oppgaven omfatter mange andre oppgaver, for eksempel å definere kasser, definere frakoblede profiler og definere kvitteringsformater og -profiler.

Se gjennom alle oppgavene som er inkludert i forutsetningene, og fullfør bare de oppgavene som gjelder for deg.

### <a name="set-up-a-store"></a>Sette opp en butikk

Når du har fullført de nødvendige oppgavene, må du fullføre disse oppgavene for å definere detaljene for butikken:

1. Opprett en butikk.
2. Tilordne en mva-gruppe til butikken.
3. Tilordne de godtatte betalingsmåtene til butikken.
4. Legg til detaljer i produktbeskrivelsene for produkter du tilbyr i butikkene. Du kan for eksempel legge til rik tekst og bilder. Disse produktdetaljene vises i ulike kontekster, for eksempel på kassen på salgsstedet eller på utskrevne etiketter.
5. Legg til butikken som standard organisasjonshierarki som er tilordnet formålet **Detaljhandelsortiment**, **Detaljhandeletterfylling** eller **Detaljhandelsrapportering**.

### <a name="after-you-set-up-a-store"></a>Etter at du har satt opp en butikk

Når du har angitt detaljene for butikken, fullfører du disse oppgavene for å sende dataene for den nye butikken til salgsstedet.

1. Konfigurer salgsstedskassene for butikken.
2. Tilordne produktsortimenter til butikken.
3. Behandle sortimenter for å generere listen over produkter som er inkludert i sortimentet og gjøre varene tilgjengelige i butikken.
4. Sende data, for eksempel nummerserier, maskinvareprofiler, og skjermoppsett for salgssted til salgsstedskassene.
5. Publiser butikken hvis du vil sende butikkdata til salgsstedet.
6. Kjør jobbene for å sende butikkdataene til salgsstedet.

## <a name="organization-hierarchies"></a>Organisasjonshierarkier

Handel bruker organisasjonshierarkier til å strukturere kanaler. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten. Når du definerer butikker, kan du legge dem til i et organisasjonshierarki. Butikken lagrer og deler data som brukes for sortimenter, etterfylling og rapportering.

> [!NOTE]
> Konfigurasjonsnøkkelen for **Flere forsendelsesadresser** må være aktivert for å bruke funksjonalitet for detaljhandelsalg. Denne konfigurasjonsnøkkelen kan finnes i nøklene for **Handelskonfigurasjon** under **Systemadministrasjon**\> **Oppsett** \> **Lisenskonfigurasjon**. Dette er nødvendig på grunn av Retail-funksjonalitet som utfører forskjellige valideringer basert på leveringsadressen som er konfigurert på salgsordrelinjenivå.

