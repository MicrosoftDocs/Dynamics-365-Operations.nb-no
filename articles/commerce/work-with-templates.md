---
title: Arbeide med maler
description: Dette emnet beskriver hvordan du arbeider med maler i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4ed3b6797127113450949aa957437125f37394f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995722"
---
# <a name="work-with-templates"></a>Arbeide med maler


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du arbeider med maler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Som diskutert i [Oversikt over maler og oppsett](templates-layouts-overview.md) definerer maler settet med alternativer som er tilgjengelig for nedstrømsforfattere. Maler er nyttige for en bedrifts webredigeringsgruppe av flere årsaker, og godt strukturerte maler kan hjelpe deg med alle disse målene:

- Forenkle redigeringsopplevelsen for daglige innholdsredigeringsroller.

    - Alternativer for filtermodul slik at bare relevante moduler vises for en bestemt sideinndeling. (En markedsføringsdel i en mal kan for eksempel konfigureres til å filtrere ut irrelevante moduler som aldri skal brukes i denne konteksten, og som bare vil forvanske innholdsredigeringsoppgaver hvis de vises.)
    - Konfigurer standard modulinnstilling for å forbedre redigeringseffektiviteten.
    - Definer standard sidefragmenter for å forbedre redigeringseffektiviteten. (Topp- og bunntekstfragmenter i en mal vil for eksempel automatisk vises på hver nedstrømsside.)

- Hold virksomhetsområder merkevarebaserte ved å definere et godkjent sett med modulordnings- og konfigurasjonsalternativer.

    > [!TIP] 
    > Vellykkede e-handelsområder gir kundene kunnskap om utformingsmønstre som er velkjente, kan gjentas og er merkevarebaserte. Ved å bruke maler bidrar du til å kontrollere konsekvensen på tvers av området.

- Forbedre resultater for søkemotoroptimaliseringe ved å sikre gjentatte og programmatisk definerte sidedefinisjoner og metadata.

> [!NOTE]
> Selv om maler er utformet for å styre konsekvensen på tvers av et område, kan de i teorien konfigureres slik at de ikke gjennomfører konsekvens. Merke- og områdeadministratorer kan definere et hvilket som helst variasjonsnivå for sidene på sitt område. En mal kan for eksempel være helt åpen, slik at innholdsforfattere kan opprette en hvilken som helst sideutforming. I dette tilfellet gjelder ingen av fordelene i foregående liste.

## <a name="modify-a-template"></a>Endre en mal

Maler endres ved hjelp av redigeringsprogrammet for maler.

Bruk en av en av fremgangsmåtene nedenfor for å åpne malredigeringsprogrammet:

- Velg **Maler** i navigasjonsruten for området, og velg deretter malen du vil endre.
- Velg toppnoden i disposisjonstreet til venstre i sideredigeringen for en eksisterende side. Deretter velger du **Rediger mal** i egenskapsruten til høyre.

Disposisjonstrevisningen til venstre viser modulalternativene og strukturene som er tilgjengelige for underordnede oppsett og sider. Når du velger en modul i disposisjonstreet, kan du vise malegenskapene for den valgte modulen i egenskapsruten til høyre. Noen av disse egenskapene er unike for malredigering. Tabellen nedenfor beskriver disse egenskapene.

| Egenskapsnavn | Beskrivelse |
|---|---|
| Minimum antall forekomster | Denne egenskapen definerer det minste antallet forekomster av den valgte modulen. Hvis for eksempel verdien er satt **1**, kreves modulen for nedstrømsforfattere, mens hvis verdien settes til **0** (null), er modulen valgfri. |
| Maksimalt antall forekomster | Denne egenskapen definerer det største antallet forekomster av den valgte modulen. Hvis for eksempel verdien er satt til **1**, kan modulen legges til bare én gang. |
| Minimumsmoduler (containere) | For moduler som inneholder andre moduler (det vil si for *containermoduler*), definerer denne egenskapen det minste antallet totale moduler som skal legges til som underordnet. For en karusellmodul kan for eksempel verdien være satt til et tall som er mer enn 1. |
| Maksimumsmoduler (containere) | For containermoduler definerer denne egenskapen det maksimale antallet totale moduler som skal legges til som underordnet. For en karusellmodul kan for eksempel verdien være satt til et tall som er mindre enn 10. |
| Låst | En **låst** boolsk kontroll vises ved siden av alle kjernemodulegenskaper. Den lar malforfatteren låse en modulinnstilling i malen. En modulinnstilling som er låst, kan ikke overstyres av underordnede oppsett eller sider. Den blir en sentralt redigerbar egenskapsverdi for alle oppsett og sider som bruker malen. |

## <a name="create-a-new-template"></a>Opprett en ny mal

Hvis du vil opprette en ny mal, følger du trinnene nedenfor.

1. Velg **Maler** i navigasjonsruten for området for å åpne malinspeksjonsvisningen.
1. Velg **Ny mal**.
1. Skriv inn et navn og en beskrivelse av malen i dialogboksen for malopprettelse. Verdiene du angir, vises for forfattere når de oppretter nye sider. Derfor må du angi metadata som kan være nyttige for sideforfattere. Skriv for eksempel inn **Bruk denne malen for å opprette generelle markedsføringssider** som en beskrivelse. Disse metadataene kan redigeres senere.
1. Velg **OK** for å opprette den nye malen og åpne redigeringsprogrammet. Malredigeringsprogrammet viser et disposisjonstre til venstre og en egenskapsrute til høyre.
1. Utvid nodene i disposisjonstreet, og velg deretter **HTML-hode**-sporet.
1. Hvis det ikke finnes noen moduler i dette sporet ennå, velger du ellipseknappen (**...**) og deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Sammendrag av standardside**, og deretter velger du **OK**.
1. I disposisjonstreet velger du den nye modulen, og deretter, i egenskapsruten, angir du eventuelle standardinnstillinger som skal konfigureres automatisk for alle underordnede sider i malen. Hvis du ikke vil ha noen standardinnstillinger, lar du verdiene stå tomme.
1. Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen, og velg deretter **Legg til modul**.
1. Velg en sidecontainermodul (det kan hende at det bare er ett alternativ), og velg deretter **OK**.

Under den nye sidecontainermodulen vil du se et nytt sett med spor (**Topptekst**, **Hoved** og så videre). Her kan du legge til og konfigurere modulalternativene som skal være tilgjengelige for forfattere når de oppretter sider fra denne malen. Hvis du ikke legger til noen moduler i et spor, støttes som standard alle tilgjengelige modultyper for sporet.

Malen er nå teknisk gyldig, og den kan lagres, sjekkes inn og brukes til å opprette nye sider. De neste tre delene beskriver imidlertid noen andre standardinnstillinger som du kanskje vil konfigurere først.

## <a name="add-a-header-and-a-footer"></a>Legge til topptekst og bunntekst

Hvis området ditt allerede har et topptekstfragment, følger du denne fremgangsmåten for å legge til en topptekst og en bunntekst i en mal.

1. Utvid **Brødtekst**-sporet og dens underordnede sidemodul i disposisjonstreet.
1. Velg **Topptekst**-sporet.
1. Velg ellipseknappen for **Topptekst**-sporet, og velg deretter **Legg til fragment**.
1. Søk etter og velg topptekstfragmentet til området, og deretter **OK**.

Alle sider som bruker malen, arver nå dette topptekstfragmentet automatisk.

Hvis området ditt ikke har et topptekstfragment ennå, se [Opprette et fragment](work-with-fragments.md#create-a-fragment) for informasjon om hvordan du oppretter det, og fullfør deretter forrige prosedyre.

## <a name="change-the-template-theme"></a>Endre maltemaet

Følg denne fremgangsmåten for å angi standardtemaet for alle sider som bruker en mal.

1. Utvid **Brødtekst**-sporet i disposisjonstreet til venstre.
1. I **Brødtekst**-sporet velger du sidecontainermodulen (for eksempel **Standardside**).
1. I egenskapsruten til høyre velger du et tema i feltet **Tema**.

Alle nye sider vil nå bruke det valgte temaet som standard. Hvis du vil hindre at sider overstyrer denne innstillingen på oppsett- eller sidenivået, setter du den boolske kontrollen **Låst** til **Sann**.

## <a name="add-a-script-to-a-template"></a>Legge til et skript i en mal

Du kan legge til HTML-**&lt;skript&gt;**-elementer som inneholder JavaScript, i malen din. På denne måten kan du gi standard skriptkodeoppførsel til HTML-hodet og start- og sluttdelen av brødteksten på sidene dine.

Hvis du vil legge til et skript i en mal, følger du disse trinnene.

1. I disposisjonstreet til venstre velger du sporet der du vil legge til **&lt;skript&gt;**-elementet (for eksempel HTML-hodet og start- og sluttdelen av brødteksten).
1. Velg ellipseknappen for sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du en skriptmodul (for eksempel **Eksternt skript** eller **Innebygd skript**).
1. I egenskapsruten til høyre, i den gjeldende skriptegenskapskontrollen (for eksempel **Innebygd skript** eller **Skriptkoder**), angir du skriptet.
1. I egenskapsruten angir du eventuelle andre valgfrie innstillinger du vil konfigurere.

> [!TIP]
> Hvis du vil bruke noen av skriptmodulene på nytt for andre maler, kan du konvertere dem til fragmenter. På denne måten gjør du redigeringsprosessen mer effektiv, og du desentraliserer oppdateringsprosessen. Hvis du vil ha informasjon om hvordan du konverterer en skriptmodul til et fragment, se [Lagre en eksisterende modulkonfigurasjon som et fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Lagre, sjekke inn, forhåndsvise og publisere en mal

Hvis du vil lagre og sjekke inn en mal, følger du disse trinnene:

1. Velg **Lagre** øverst i malredigeringsprogrammet. Lagrede endringer påvirker ikke nedstrømssider før de er sjekket inn.
1. Velg **Fullfør redigering**. Dine endringer er nå synlige for nedstrøms arbeidsflyter.

Hvis du vil forhåndsvise endringene, kan du enten åpne en eksisterende side som bruker malen, eller opprette en ny side fra malen.

Når du har forhåndsvist endringene i malen, følger du en av disse fremgangsmåtene for å publisere malen på ditt aktive område:

* Gå til **Maler**, velg malen, og velg deretter **Publiser**.
* Velg oppsettnavnet for å åpne redigeringsprogrammet for oppsett, og velg deretter **Publiser**.
* Publiser en side som refererer til den upubliserte malen. Malen publiseres automatisk.

> [!WARNING]
> Når en mal eller en annen CMS-vare (Content Management System) er publisert, er den synlig på Internett. Ikke publiser dokumenter eller aktiva før du er klar til å offentliggjøre dem. Dokumentversjoner som er lagret og sjekket inn, men som ikke er publisert, er bare synlige for godkjente systembrukere.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)
