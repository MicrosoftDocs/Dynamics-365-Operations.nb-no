---
title: Definere et lager ved hjelp av en mal for lagerkonfigurasjon
description: Dette emnet forklarer hvordan du definerer et lager ved hjelp av en mal for lagerkonfigurasjon.
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 66fdc26b0b967a04a3c6a6e3444e00b1372dc504
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434660"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Definere et lager ved hjelp av en mal for lagerkonfigurasjon

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du definerer et lager ved hjelp av en mal for lagerkonfigurasjon. Det finnes flere forhåndsdefinerte konfigurasjonsmaler som du kan bruke. Hvis du vil ha informasjon om hvordan du bruker disse malene, se [Konfigurasjonsdatamaler](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Scenarier der konfigurasjonsmaler kan være nyttige

Konfigurasjonsmaler kan være nyttige i mange scenarier. Her er noen eksempler:

- Du har fullført og testet et konfigurasjonsoppsett i et testmiljø, og nå vil du kopiere oppsettet til et produksjonsmiljø.
- Du vil rulle lageroppsettet ut til flere juridiske enheter eller opprette et nytt lager i den samme juridiske enheten.
- Du vil klargjøre en demonstrasjon av funksjonen for lageret raskt.
- Du vil at eksisterende elementer og lagre skal bruke funksjonaliteten i Lagerstyring i stedet for funksjonaliteten i Beholdningsstyring.

Dette emnet fokserer på det første av disse scenariene. Det viser hvordan du kan bruke en konfigurasjonsmal til å kopiere et konfigurasjonsoppsett fra et testmiljø til et produksjonsmiljø.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Kopiere et konfigurasjonsoppsett fra et testmiljø til et produksjonsmiljø

I dette scenariet finnes konfigurasjonsoppsettet for et lager og enkelte transaksjonsprosesser allerede i et testmiljø. Nå ønsker du å kopiere konfigurasjonsoppsettet for lageret fra testmiljøet til et produksjonsmiljø.

> [!NOTE]
> Det er viktig at du tar med andre relaterte oppsettdata når du kopierer et konfigurasjonsoppsett. Du kan for eksempel definere produkter ved å kopiere oppsettet fra et testmiljø. Du kan imidlertid definere et fast plukksted for et produkt før produktet blir opprettet. Selv om enkelte konfigurasjonsmaler ikke støtter denne typen avhengighet, finnes det standard datamaler som støtter dette. Du kan enkelt inkludere disse standard datamalene i en konfigurasjonsprosess.

### <a name="export-a-default-warehouse-template"></a>Eksportere en standardmal for lager 

1. Åpne arbeidsområdet **Databehandling**.

    > [!NOTE]
    > Hvis du bruker dette arbeidsområdet for første gang, må du laste inn alle dataenhetene før du fortsetter.

2. Velg flisen **Maler**, og velg deretter **Last standardmaler** for å laste inn standardmalene.

    > [!NOTE]
    > **Last standardmaler** er bare tilgjengelig i **Utvidet**-visningen. Velg **Rammeverkparametere**, og deretter i feltet **Vis standarder** velger du **Utvidet visning**.

3. Når standardmalene er lastet inn, kan du endre dem slik at de overholder dine forretningskrav.

    > [!NOTE]
    > Hvis du vil laste inn standardmaler og importere maler, må du ha administratortilgang for systemet. Dette kravet bidrar til å sikre at alle enheter er riktig lastet inn i malen.

4. Kontroller at du er i den juridiske enheten du vil eksportere de bedriftsspesifikke dataene fra.
5. I arbeidsområdet, velger du **Eksporter**.
6. Opprett et nytt eksportprosjekt.
7. Velg **+ Legg til mal**, og finn standardmalen **400 - WMS** for lageret. Denne malen legger til dataenheter for lagerkonfigurasjonen.

    > [!NOTE]
    > Hvis dataene som du eksporterer, må filtreres (du ønsker for eksempel å eksportere bare dataene som er knyttet til et bestemt lager), må du evaluere hver dataenhet og legge til filtrering via en spørring. Du kan også eksportere alle dataene og deretter slette postene som ikke er påkrevd i målfilene.

8. Velg **Eksporter**. Data som er knyttet til alle dataenhetene i prosjektet, eksporteres.

Du kan laste ned en zip-fil for datapakken. Denne filen inneholder alle dataene i det valgte formatet (for eksempel et Excel-format). Som nevnt, må enkelte poster i datapakkefilene kanskje oppdateres før du kan importere dem til produksjonsmiljøet. Hvis du oppdaterer en post, må du kontrollere at du ikke endrer filnavnet.

### <a name="import-a-warehouse-configuration-setup"></a>Importere et konfigurasjonsoppsett for lager

1. I målmiljøet må du kontrollere at du er i firmaet der du vil importere lagerdataene.

    > [!NOTE]
    > Før du gjør importen, må du identifisere dataavhengigheter. Malen **Lagerstyring** inneholder for eksempel en dataenhet som heter **Disposisjonskoder for lager**. Denne enheten inneholder data som er knyttet til oppsettsiden **Disposisjonskoder** (**Lagerstyring** > **Oppsett** > **Mobilenhet** > **Disposisjonskoder**). Hvis et eksisterende oppsett allerede håndterer prosessen for salgsordrer, inneholder feltet **Returdisposisjonskode** en verdi for feltet. Disposisjonskoden i dette feltet er knyttet til dataenheten **Disposisjonskode**, som er en del av malen **Salg og markedsføring**. Hvis dataene fra dataenheten **Disposisjonskode** ikke er importert før dataene fra feltet **Disposisjonskoder for lager**, vil importen mislykkes.

2. I arbeidsområdet **Databehandling** velger du **Importer**.
3. Opprett et nytt importprosjekt.
4. Velg **+ Legg til fil**, og last opp zip-filen for datapakken.
5. Velg **Import**. I **Utvidet**-visningen kan du bruke **Filter**-alternativet for raskt å få oversikt over problemer som kan oppstå under importen.

**Vis utførelseslogg** gir deg detaljert informasjon om hver dataenhet som importeres. Du kan bruke oppsamling datavisningen for å gå raskt til målet dataene. På denne måten kan du se hva de importerte dataene ser slik på de tilknyttede sidene i programmet. Når du bruker standard datamalene, fungerer importsekvensen for hver dataenhet på den forhåndsdefinerte måten, for å garantere at alle avhengige data importeres først. Hvis egendefinerte enheter inngår i prosjektet, må du kontrollere at den riktige rekkefølgen er definert. Hvis du vil ha mer informasjon, kan du se [Konfigurasjonsdatamaler](../../dev-itpro/data-entities/configuration-data-templates.md).

Hvis du vil vite mer om hvordan du bruker lagermalen for å kopiere konfigurasjonen for et lager fra ett firma til et nytt selskap i samme forekomst, kan du se denne 3-minutters lange YouTube-videoen om [hvordan du bruker lagermalen til å kopiere konfigurasjonen for Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-topic"></a>Relaterte emne

[Konfigurasjonsdatamaler](../../dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]