---
title: Aktivere og konfigurere automatiske avregninger etter kanal
description: Dette emnet forklarer hvordan du aktiverer og konfigurerer automatiske gebyrer per kanal i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d905819d1e0c8223c74509bfb357b3aaa51d20305a2857061eadb0b0ff8f6b9b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727636"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Aktivere og konfigurere automatiske avregninger etter kanal

Dette emnet forklarer hvordan du aktiverer og konfigurerer automatiske gebyrer per kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Du kan ha scenarioer der resirkuleringsgebyrer eller andre gebyrer må brukes på en gruppe produkter som selges i alle eller enkelte butikker i en bestemt delstat (for eksempel California). Med funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** i Commerce kan du angi automatiske gebyrer per kanal (for eksempel en bestemt fysisk kanal). Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.10 og senere.

Du må fullføre følgende oppgaver for å aktivere og konfigurere automatiske gebyrer per kanal:

- Aktiver funksjonen **Aktiver filtrering av automatiske gebyrer per kanal**.
- Konfigurer formålet for organisasjonshierarki.
- Definer automatiske gebyrer per kanal.

> [!NOTE]
> Funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** fungerer bare hvis funksjonen for avanserte automatiske gebyrer også er aktivert. Hvis du vil ha informasjon om hvordan du aktiverer funksjonen for avanserte automatiske gebyrer, kan du se [Avanserte automatiske gebyrer for omnikanal](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Aktivere funksjonen Aktiver filtrering av automatiske gebyrer per kanal

Følg denne fremgangsmåten for å aktivere automatiske gebyrer per kanal i Commerce.

1. Gå til **Systemadministrator \> Arbeidsområder \> Funksjonsbehandling**.
1. I kategorien **Ikke aktivert**, i listen **Funksjonsnavn** finner og velger du **Aktiver filtrering av automatiske gebyrer per kanal**.
1. Velg **Aktiver nå** i hjørnet nederst til høyre. Når funksjonen er slått på, vil den vises i listen i kategorien **Alle**.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. I venstre rute finner du og velger jobben **1110** (**Global konfigurasjon**).
1. Velg **Kjør nå** i handlingsruten for å overføre konfigurasjonsendringene.

> [!WARNING]
> Hvis du deaktiverer funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** etter at du allerede har brukt den, vises ikke feltet **Relasjon med detaljhandelskanal** under **Automatiske gebyrer** lenger, og du mister alle eksisterende konfigurasjoner. Hvis fjerning av konfigurasjonene for **Relasjon med detaljhandelskanal** forårsaker duplisering av regler for automatiske gebyrer, vil et forsøk på å deaktivere funksjonen mislykkes. Før du slår av funksjonen, må du passe på å se gjennom alle regler for automatiske gebyrer og foreta eventuelle endringer som kreves.

## <a name="configure-the-organization-hierarchy-purpose"></a>Konfigurere formålet for organisasjonshierarki

Et nytt formål for organisasjonshierarki kalt **Automatisk gebyr for detaljhandel** er opprettet for å administrere hierarkiet for automatiske gebyrer per kanal.

Følg denne fremgangsmåten for å tilordne et standardhierarki til et formål for organisasjonshierarki i Commerce.
        
1. Gå til **Organisasjonsstyring \> Organisasjoner \> Formål for organisasjonshierarkier**.
1. I den venstre ruten velger du **Automatisk gebyr for detaljhandel**.
1. Under **Tilordnede hierarkier** velger du **Legg til**.
1. I dialogboksen **Organisasjonshierarkier** velger du et organisasjonshierarki (for eksempel **Detaljhandelbutikker etter område**), og deretter velger du **OK**.
1. Under **Tilordnede hierarkier** velger du **Bruk som standard**.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. I venstre rute finner du og velger jobben **1040** (**Produkter**).
1. Velg **Kjør nå** i handlingsruten.
1. Gjenta de to forrige trinnene for å kjøre jobbene **1070** (**Kanalkonfigurasjon**) og **1110** (**Global konfigurasjon**).

![Konfigurasjon av formålet for automatisk gebyr for detaljhandel per organisasjonshierarki.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Definere automatiske gebyrer per kanal

Når du har aktivert funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** og konfigurert formålet **Automatisk gebyr for detaljhandel** for organisasjonshierarki, kan automatiske gebyrer per kanal defineres på ordrehodenivå eller ordrelinjenivå.

Følg denne fremgangsmåten for å definere automatiske gebyrer per kanal i Commerce.

1. Gå til **Kunder \> Oppsett for tillegg \> Automatiske gebyrer**.
1. I den venstre ruten, i **Nivå**-feltet, velger du enten **Hode** eller **Linje**, alt etter forretningskravene dine.
1. I feltet **Detaljhandelskanalkode** velger du den aktuelle kanalkoden (for eksempel **Tabell** eller **Gruppe**). Hvis standardinnstillingen **Alle** er brukt, brukes gebyrregler på alle kanaler.

    - Hvis du velger **Gruppe**, må du kontrollere at en gebyrgruppe for detaljhandelskanal opprettes under **Retail og Commerce \> Kanaloppsett \> Gebyrer \> Gebyrgrupper for detaljhandelskanal**.
    - Hvis du velger **Tabell**, kan du velge en bestemt kanal (for eksempel **San Francisco**) i feltet **Relasjon med detaljhandelskanal**.

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. I venstre rute finner du og velger jobben **1040** (**Produkter**).
1. Velg **Kjør nå** i handlingsruten.
1. Gjenta de to forrige trinnene for å kjøre jobbene **1070** (**Kanalkonfigurasjon**) og **1110** (**Global konfigurasjon**).
    
![Automatiske gebyrer definert per kanal.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Eksempelscenario

I følgende eksempel vises fremgangsmåten som kreves for å konfigurere et produkt, slik at resirkuleringsgebyrer belastes når produktet selges via en fysisk kanal i San Francisco. Eksemplet viser også hvordan de automatiske gebyrene vises i POS-appen (salgssted) i Commerce.

Organisasjonen definerer en gebyrkode som heter **RESIRKULERING**, som vist i følgende illustrasjon.

![Gebyrkoden RESIRKULERING.](media/Auto-charges-charge-code.png)

Et automatisk gebyr opprettes på linjenivå. Det har følgende konfigurasjon:

- Feltet **Kontokode** settes til **Alle**.
- Feltet **Varekode** settes til **Tabell**.
- Feltet **Varerelasjon** settes til produkt-ID **91001**.
- Feltet **Kode for leveringsmåte** settes til **Alle**.
- Feltet **Detaljhandelskanalkode** settes til **Tabell**.
- Feltet **Relasjon med detaljhandelskanal** settes til butikken i **San Francisco**.

En linje for automatiske gebyrer opprettes. Det har følgende konfigurasjon:

- Feltet **Valuta** settes til **USD**.
- Feltet **Tilleggskode** settes til **RESIRKULERING**.
- Feltet **Kategori** settes til **Fast**.
- Feltet **Gebyrer** settes til **USD 6,25**.

![Konfigurasjon av automatisk gebyr på linjenivå og linjen for automatiske gebyrer.](media/Auto-charges-recyclingfee-line-fee.png)

I POS-appen opprettes det en salgsordre i butikkanalen **San Francisco**. Linjen **Gebyrer** viser resirkulasjonsgebyret på **USD 6,25**.

Ved å velge **Transaksjonsalternativer \> Gebyrer \> Behandle gebyrer** i POS-appen kan du vise gebyrkoden og beskrivelsen for resirkuleringsgebyret.

![Resirkuleringsgebyr i POS-appen.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Avanserte automatiske tillegg for omnikanal](omni-auto-charges.md)

[Fordele hodegebyrer til samsvarende salgslinjer](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]