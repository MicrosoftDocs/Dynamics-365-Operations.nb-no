---
title: Opprette forhåndsdefinerte produktvarianter
description: Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a90e0eb469b823368c1140421fc9c92ccfe69a3b7bac73f762170c0da43e3eee
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747895"
---
# <a name="predefined-product-variants"></a>Forhåndsdefinerte produktvarianter

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Eksempelscenario: Opprette forhåndsdefinerte produktvarianter

Dette eksempelscenarioet viser hvordan du oppretter produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å følge dette scenarioet ved å bruke verdiene som er foreslått her, må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten *USMF*.

### <a name="step-1-create-a-product-master"></a>Trinn 1: Opprette en produktstandard

Slik opprettes en produktstandard:

1. Gå til **Behandling av produktinformasjon > Produkter > Produktstandarder**.
1. Velg **Ny**.
1. Hvis **Produktnummer**-feltet ikke allerede viser et tall, angir du en verdi. Dette er bare nødvendig hvis ingen nummerserie er definert for dette feltet.
1. Angi et navn i feltet **Produktnavn**.
1. I feltet **Produktdimensjonsgruppe** velger du produktdimensjonsgruppen *SizeCol* (Størrelse og farge).
1. Velg **OK** for å opprette og åpne den nye produktstandard.

### <a name="step-2-add-product-dimensions"></a>Trinn 2: Legge til produktdimensjoner

Dette eksemplet viser hvordan du manuelt angir produktdimensjoner. Du kan også velge en størrelse, farge eller stilgruppe som inkluderer produktdimensjonsverdiene du vil bruke.

Slik legger du til produktdimensjoner:

1. Når den nye produktstandarden fremdeles er åpen, velger du **Produktdimensjoner** i handlingsruten.
1. Åpne kategorien **Størrelse**, og velg **Ny** på verktøylinjen for å legge til en rad i rutenettet. Gjør følgende innstillinger for den nye raden:
    - **Størrelse:** Velg en størrelsesverdi.
    - **Navn:** Angi et navn for størrelsen.
1. Velg **Ny** på verktøylinjen, og legg til en ny størrelse i rutenettet med ny **Størrelse** og nytt **Navn**.
1. Åpne kategorien **Farger**, og velg **Ny** på verktøylinjen for å legge til en rad i rutenettet. Gjør følgende innstillinger for den nye raden:
    - **Farge:** Velg en fargeverdi.
    - **Navn:** Angi et navn for fargen.
1. Velg **Ny** på verktøylinjen, og legg til en ny farge i rutenettet med ny **Farge** og nytt **Navn**.
1. Velg **Lagre**.
1. Lukk siden for å gå tilbake til den nye produktstandarden.

### <a name="step-3-generate-product-variants"></a>Trinn 3: Generere produktvarianter

> [!NOTE]
> Denne delen beskriver hvordan du genererer produktvarianter når funksjonen *Forbedringer for variantforslagssiden* ikke er aktivert. I neste del finner du informasjon om hvordan du genererer produktvarianter når denne funksjonen er tilgjengelig.

Slik genererer du produktvarianter:

1. Når den nye produktstandarden fremdeles er åpen, velger du **Produktvarianter** i handlingsruten.
1. Velg **Variantforslag** i handlingsruten.
1. Systemet genererer en liste med alle mulige kombinasjoner av størrelsene og fargene du definerte for produktet. Velg **Velg alle** på verktøylinjen.
    - I dette eksemplet velger du alle mulige varianter. Hvis du bare vil bruke et delsett av de mulige produktdimensjonskombinasjonene, merker du bare av i de obligatoriske avmerkingsboksene etter behov.  
1. Velg **Opprett**.
1. Velg **Lagre**.

## <a name="improved-variant-suggestions"></a>Forbedrede variantforslag

Funksjonen *Forbedringer for variantforslagssiden* forbedrer **Variantforslag** for å adressere ytelses- og brukervennlighetsproblemer for firmaer som har et høyt antall produktdimensjonskombinasjoner. Den utvidede prosessen for valg av produktdimensjonsverdier som du kan generere variantforslag for, gjør det raskere og enklere å identifisere og frigi det relevante settet med produktvarianter.

Følgende forbedringer er lagt til av denne funksjonen:

- **Utsatt generering av variantforslag:** **Variantforslag**-siden viser ikke lenger forslag når du åpner den første gang. I stedet må du uttrykkelig velge hvilke verdier du trenger, og deretter velge **Foreslå**-knappen for å generere kombinasjonene. Dette gjør prosessen mer synlig og interaktiv.
- **Valg av dimensjonsverdier:** Når du har mange dimensjonsverdier, er du vanligvis interessert i å generere variantforslag som bare omfatter noen få av dem (for eksempel når du introduserer et nytt sett med farger eller stiler). Med den forbedrede utformingen kan du velge dimensjonsverdiene du vil generere produktvariantforslag for. Dette øker relevansen av de foreslåtte variantene betydelig og forbedrer både systemets ytelse og brukerproduktivitet.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Aktivere funksjonen Forbedringer for variantforslagssiden

Før du kan bruke funksjonen *Forbedringer for variantforslagssiden* må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Behandling av produktinformasjon*
- **Funksjonsnavn:** *Forbedringer for variantforslagssiden*

### <a name="work-with-the-improved-variant-suggestions"></a>Arbeide med de forbedrede variantforslagene

For å generere produktvariantforslag når funksjonen *Forbedringer for variantforslagssiden* er aktivert:

1. Åpne eller opprett en produktstandard, og legg til de nødvendige produktdimensjonene, som beskrevet i forrige del.
1. Når den produktstandarden er åpen, velger du **Produktvarianter** i handlingsruten.
1. Velg **Variantforslag** i handlingsruten.
1. Velg verdiene du vil bruke for hver av dimensjonene.
1. På verktøylinjen velger du **Foreslå**.
1. Systemet genererer en liste med alle mulige kombinasjoner av størrelsene og fargene du valgte. I hurtigkategorien **Foreslåtte varianter** merker du av for hver produktdimensjonskombinasjon du vil bruke, eller velger **Velg alle** på verktøylinjen for å velge alle.  
1. Velg **Opprett** for å legge til variantene i gjeldende produktstandard.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
