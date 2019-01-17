---
title: "Lageroppslag på salgsstedet"
description: "Dette emnet beskriver alternativene som er tilgjengelige for å vise lagerinformasjon på salgsstedet (POS)."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.contentlocale: nb-no
ms.lasthandoff: 01/04/2019

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Lageroppslag på salgsstedet

[!include [banner](includes/banner.md)]

Lageroppslag på salgsstedet gjør det enklere for forhandlere å oppnå driftskvalitet i sanntid og få innsikt ved å koble sammen butikker, salgssted og back office. Denne funksjonaliteten gir nøyaktig sanntidsvisning av produktlageret på tvers av butikker og distribusjonssentre. Den hjelper også forhandlerne med å øke effektiviteten og kostnadsbesparelsene ved å forbedre lagerplanlegging i sanntid.

En nøyaktig sanntidsvisning av lageret i en organisasjon hjelper butikkansatte med å gi en rask og god kundeservice. Øyeblikket som betyr mest, er når kunden er klar til å ta en kjøpsbeslutning. Det er viktig at kasserere i butikken har sanntidsinformasjon om lageret lett tilgjengelig, slik at de kan gi riktig informasjon om produktlevering og plukking.

Du kan åpne **Lageroppslag**-siden fra **Moderne salgssted for detaljhandel**-arbeidsområdet eller **Skybasert salgssted for detaljhandel**-arbeidsområdet.

![Lageroppslag-flisen på hjemmesiden for salgssted](media/POSHomepage.png)

På **Lageroppslag**-siden kan du kan bruke det numeriske tastaturet til å angi et produktnummer. Du kan deretter vise antallet på lager for flere butikker og lagre.

![Oppslagsiden for standardoppsett](media/InventoryLookUp.png)

Antall for **Reservert** og **Bestilt** vises også for hver lokasjon.

- **Reservert** – Dette antallet refererer til **Fysisk reservert**-verdien fra back office for det angitte produktnummeret på lokasjonen.
- **Bestilt** – Dette antallet refererer til **Bestilt i alt**-verdien fra back office for det angitte produktnummeret på lokasjonen.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Lokasjoner som lagertilgjengelighetsinformasjon vises for

Listen over lokasjoner inneholder to typer enheter:

- **Detaljhandelbutikker** – Listen viser butikkene som er konfigurert ved hjelp av butikklokatorgruppen for gjeldende butikk i detaljhandelshovedkontoret.
- **Distribusjonssentre** – Forskjellige typer distribusjonssentre (for eksempel lagre) kan konfigureres i Microsoft Dynamics 365 for Retail. Listen viser imidlertid bare informasjon om tilgjengelig lager for distribusjonssentre av standardtypen **Standard**.

    > [!NOTE]
    > Informasjon om lagertilgjengelighet vises ikke for lagre av typen **Transitt**, **Karantene** og **Varer i ruten** for salgsstedet.

På **Lageroppslag**-siden kan du vise tilgjengelig for ordre (ATP)-antall for hver butikk, i tillegg til gjeldende lagerbeholdningsantall, reservert antall og bestilt antall. Velg butikken du vil vise informasjon om ATP for, og velg deretter **Vis butikktilgjengelighet**.

![ATP-antall](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Åpne dimensjonsbasert matrisevisning for å vise alle varianter

På **Produktdetaljer**-siden i en produktstandard eller på **Lageroppslag**-siden velger du **Vis alle varianter** fra programfeltet nederst på siden. **Dimensjonsbasert matrise**-visningen for den første oppstarten fra disse sidene viser lagertilgjengelighetsinformasjon for alle varianter av et produkt for gjeldende butikk.

> [!NOTE]
> **Vis alle varianter**-knappen er bare tilgjengelig for vareproduktstandarder som har produktvarianter. Den er ikke tilgjengelig for frittstående produkter eller pakker.

![Vis alle varianter-knappen på Lageroppslag-siden](media/StandardToMatrix.png)

Velg **Vis alle varianter** på **Produktdetaljer**-siden i en produktstandard, eller på **Lageroppslag**-siden, uten å velge en plassering, for å gå til **Dimensjonsbasert matrise**-visningen og vise lagertilgjengelighetsinformasjon for alle varianter av et produkt for gjeldende butikk.

![Dimensjonsbasert matrisevisning for Lageroppslag-siden](media/Matrix.png)

> [!NOTE]
> I forrige illustrasjon er visningsrekkefølgen for dimensjonene alfabetisk, fordi visningsrekkefølgen for dimensjoner ikke ble konfigurert for det valgte produktet.

I **Dimensjonsbasert matrise**-visningen inkluderer cellene for produktvariantene en beholdningsverdi i nedre høyre hjørne. Tabellen nedenfor forklarer betydningen av ulike verdier.

| Beholdningsverdi                            | beskrivelse |
|------------------------------------------|-------------|
| Numerisk verdi som er større enn 0 (null) | En variant er frigitt til den valgte plasseringen, og du kan utføre flere handlinger i cellen. (Disse handlingene beskrives nærmere i senere i dette emnet.) |
| **0** (null)                             | En variant er frigitt til den valgte plasseringen, men varen er ikke tilgjengelig på den valgte plasseringen. Du kan imidlertid utføre flere handlinger i cellen. (Disse handlingene beskrives nærmere i senere i dette emnet.) |
| **i/t** eller en inaktiv celle              | En variant er ikke frigitt til den valgte plasseringen, og du kan ikke utføre flere handlinger i cellen. |

Du kan også endre pivot for dimensjoner ved å velge den nye dimensjonen som skal brukes.

![Endre pivot](media/ChangePivot.png)

![Pivot endret](media/PivotChanged.png)

> [!NOTE]
> I de foregående illustrasjonene er visningsrekkefølgen for dimensjonene for det valgte produktet egendefinert (ikke-alfabetisk). Den er basert på visningsrekkefølgen for dimensjoner som er angitt i back office.

I tillegg i **Dimensjonsbasert matrise**-visningen kan flere handlinger utføres og bidra til å øke produktiviteten til butikkmedarbeidere. Her er noen eksempler:

- Endre butikkplasseringen for å slå opp varetilgjengeligheten til alle produktvarianter på andre lokasjoner. Disse plasseringene inkluderer andre butikker i butikklokatorgruppen og distribusjonssentrene for standardtypen **Standard**.
- Selg en individuell produktvariant til en kunde ved hjelp av hentesalg, henting i butikken eller levering til en adresse.
- Gi kunden ATP-informasjon for en enkelt produktvariant på et bestemt sted.

![Flere handlinger på variantfliser](media/VariantActions.png)

> [!NOTE]
> I forrige illustrasjon er visningsrekkefølgen for dimensjonene alfabetisk, fordi visningsrekkefølgen for dimensjoner ikke ble konfigurert for det valgte produktet.

Tabellen nedenfor inneholder mer informasjon om flere handlinger som er tilgjengelige.

| Handling               | beskrivelse |
|----------------------|-------------|
| Selg nå             | Legg til den valgte varevarianten i transaksjonen, og omdiriger brukeren til skjermbildet for transaksjonen. (Denne handlingen er ikke tilgjengelig når den valgte plasseringen er et distribusjonssenter.) |
| Hent i butikk     | Opprett en kundeordre for produktvarianten som plukkes fra den valgte plasseringen, og omdiriger brukeren til skjermbildet for transaksjonen. (Denne handlingen er ikke tilgjengelig når den valgte plasseringen er et distribusjonssenter.) |
| Send produkt         | Opprett en kundeordre for produktvarianten som sendes fra den valgte plasseringen, og omdiriger brukeren til skjermbildet for transaksjonen. |
| Tilgjengelighet         | Vis ATP-informasjonen for den valgte variantkombinasjonen for det valgte stedet. |
| Vis alle lokasjoner   | Bytt til visningen for standard lageroppslag, og uthev lagertilgjengelighetsinformasjon for varevarianten i alle butikkene i butikklokatorgruppen, og også i distribusjonssentre av typen **Standard**. |
| Vis produktdetaljer | Omdiriger brukeren til **Produktdetaljer**-siden for den tilknyttede produktstandarden. |

