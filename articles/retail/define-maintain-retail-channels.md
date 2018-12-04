---
title: Definere og vedlikeholde detaljhandelskanaler
description: "Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles detaljhandelsbutikker i Microsoft Dynamics 365 for Retail. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en detaljhandelsbutikk."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: b6dd6d929d771e0b1fc2604b90a2a1522447e168
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---

# <a name="define-and-maintain-retail-channels"></a>Definere og vedlikeholde detaljhandelskanaler

[!include [banner](includes/banner.md)]

Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles detaljhandelsbutikker i Microsoft Dynamics 365 for Retail. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en detaljhandelsbutikk.

Dynamics 365 for Retail støtter flere detaljhandelskanaler, for eksempel nettbutikker, telefonsentre og fysiske butikker. En fysisk butikk kalles detaljhandelbutikk. Hver detaljhandelsbutikk kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte. Du må definere alle disse elementene for en detaljhandelsbutikk, før du oppretter den. Når du har opprettet en detaljhandelsbutikk, tilordner du produktene du vil den skal føre. Du tilordner også ansatte, kasser og kunder til butikken. Til slutt legger du til den nye butikken i et organisasjonshierarki.

## <a name="setting-up-retail-stores"></a>Definere detaljhandelsbutikker
Før du kan definere en detaljhandelsbutikk i Dynamics 365 for Retail, må du fullføre noen nødvendige oppgaver. Du kan deretter opprette detaljhandelsbutikken og legge til detaljer.

### <a name="prerequisites"></a>Nødvendig programvare

Du må fullføre følgende oppgaver før du kan definere en detaljhandelsbutikk:

1.  Konfigurer organisasjonsstrukturen, og definer organisasjonshierarkier for detaljhandelssortimenter, -etterfylling og -rapportering.
2.  Definere et lager som representerer detaljhandelsbutikken.
3.  Definer nummerserier for detaljhandelsbutikker, butikkutdrag og utdragsbilag.
4.  Konfigurer parametere for Detaljhandel.
5.  Definer betalingsmåtene butikken godtar.
6.  Hvis du vil behandle kredittkorttransaksjoner i kasser på salgssteder, kan du også konfigurere betalingstjenester.
7.  Definer mva-grupper.
8.  Definer detaljprodukter. Som en del av denne oppgaven definerer du også detaljprodukthierarkier, produktvarianter og produktsortimenter.
9.  Definer produktgrupper.
10. Definer produktpriser for detaljhandel. Som en del av denne oppgaven definerer du også prisjusteringer, rabatter og rabattperioder.
11. Definere stabsmedlemmer. **Obs!** Du må også tilordne aktuelle tillatelser til arbeiderne, slik at de kan logge på og utføre oppgaver ved hjelp av Dynamics 365 for Retail for Retail POS-systemet.
12. Konfigurer Retail POS-profilene som skal tilordnes butikken. Denne oppgaven omfatter mange andre oppgaver, for eksempel å definere kasser, definere frakoblede profiler og definere kvitteringsformater og -profiler.

Se gjennom alle oppgavene som er inkludert i forutsetningen, og fullfør bare de oppgavene som gjelder for deg.

### <a name="set-up-a-retail-store"></a>Angi en detaljhandelsbutikk

Når du har fullført de nødvendige oppgavene, må du fullføre disse oppgavene for å definere detaljene for detaljhandelsbutikken:

1.  Opprett en detaljhandelsbutikk.
2.  Tilordne en mva-gruppe til butikken.
3.  Tilordne de godtatte betalingsmåtene til butikken.
4.  Legg til detaljer i produktbeskrivelsene for produkter du tilbyr i detaljhandelsbutikkene. Du kan for eksempel legge til rik tekst og bilder. Disse produktdetaljene vises i ulike kontekster, for eksempel på kassen på salgsstedet eller på utskrevne etiketter.
5.  Legg til butikken som standard organisasjonshierarki som er tilordnet formålet **Detaljhandelsortiment**, **Detaljhandeletterfylling** eller **Detaljhandelsrapportering**.

### <a name="after-you-set-up-a-retail-store"></a>Når du har opprettet en detaljhandelsbutikk

Når du har angitt detaljene for detaljhandelsbutikken, fullfører du disse oppgavene for å sende de nye dataene for detaljhandelsbutikken til Retail POS:

1.  Konfigurer salgsstedskassene for butikken.
2.  Tilordne produktsortimenter til butikken.
3.  Behandle sortimenter for å generere listen over produkter som er inkludert i sortimentet og gjøre varene tilgjengelige i detaljhandelsbutikken.
4.  Sende data, for eksempel nummerserier, maskinvareprofiler, og skjermoppsett for salgssted til Retail POS-kassene.
5.  Publiser detaljhandelsbutikken hvis du vil sende butikkdata til Retail POS.
6.  Kjør jobbene for å sende butikkdataene til Retail POS.

## <a name="organization-hierarchies"></a>Organisasjonshierarkier
Retail bruker organisasjonshierarkier til å strukturere detaljhandelskanaler. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten. Når du definerer butikker, kan du legge dem til i et organisasjonshierarki. Butikken lagrer og deler data som brukes for sortimenter, etterfylling og rapportering.




