---
title: Produktdimensjoner
description: Det finnes fem produktdimensjoner – farge, konfigurasjon, størrelse, stil og versjon. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.
author: t-benebo
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: acfd9be044818ab0f40171c25a8fc9e760173aa8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867934"
---
# <a name="product-dimensions"></a>Produktdimensjoner

[!include [banner](../includes/banner.md)]

Det finnes fem produktdimensjoner: farge, konfigurasjon, størrelse, stil og versjon. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.

Produktdimensjoner er egenskaper som brukes til å identifisere en produktvariant. Du kan bruke kombinasjoner av produktdimensjoner til å definere produktvariantene. Du må definere minst én produktdimensjon for en produktstandard for å opprette en produktvariant.

## <a name="product-variants"></a>Produktvarianter

Produktvarianter omtales også som varer. En vare er et materielt produkt, som ikke er det samme som en tjeneste. Det er også mulig å definere en produktstandard tjenestetypen. Når du bruker tjenestetypen, kan du angi produktvarianter som omfatter tjenester. Du kan for eksempel angi en produktstandard for konsulentarbeid og produktvarianter for arbeid som utføres av seniorkonsulenter og juniorkonsulenter.

## <a name="product-dimensions"></a>Produktdimensjoner

En produktvariant kan genereres basert på produktdimensjonsverdiene.

Produktdimensjonsverdier for dimensjonene størrelse, farge og stil kan opprettes på følgende steder:

- **Størrelse**-siden (**Behandling av produktinformasjon \> Oppsett \> Dimensjons- og variantgrupper \> Størrelser**)
- **Farge**-siden (**Behandling av produktinformasjon \> Oppsett \> Dimensjons- og variantgrupper \> Farger**)
- **Stil**-siden (**Behandling av produktinformasjon \> Oppsett \> Dimensjons- og variantgrupper \> Stiler**)

Produktdimensjonsverdier for konfigurasjonsdimensjonen opprettes vanligvis ved hjelp av produktkonfiguratoren eller den dimensjonsbaserte konfiguratoren. 

Produktversjoner opprettes vanligvis for bestemte versjoner etter hvert som produktet utvikles i løpet av livssyklusen. Produktversjoner dekkes i detalj senere i denne artikkelen.

Produktdimensjoner kan også opprettes og vedlikeholdes på **Produktdimensjoner**-siden, som er tilgjengelig fra følgende steder:

- Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**. I handlingsruten velger du **Produktdimensjoner**.
- Gå til **Behandling av produktinformasjon \> Produkter \> Alle produkter og produktstandarder**. Velg en produktstandard. I handlingsruten velger du **Produktdimensjoner**.
- Gå til **Behandling av produktinformasjon \> Frigitte produkter**. Velg en produktstandard. I handlingsruten, i **Produkt**-fanen og **Produktstandard**-gruppen, velger du **Produktdimensjoner**.

Antallet varianter du kan opprette for en vare, er begrenset av antallet mulige kombinasjoner av produktdimensjoner.

> [!TIP]
> Når du for eksempel bruker et produkt på en ordrelinje, velger du produktdimensjonene for å identifisere produktvarianten du vil arbeide med.

## <a name="example"></a>Eksempel

Et firma selger dongeribukser. Varen *dongeribukser* bruker produktdimensjonene for farge og størrelse. Dongeribuksene selges i tre forskjellige farger og seks forskjellige størrelser. Fargene er blå, svart og brun. Størrelsene er XS, S, M, L, XL og XXL. Ikke alle størrelser er tilgjengelige i alle tre fargene. Hvis alle kombinasjonene hadde vært tilgjengelige, hadde det blitt 18 forskjellige typer dongeribukser. I dette eksemplet produseres imidlertid bare de følgende ni produktvariantkombinasjonene.

| Farge | Størrelse |
|-------|------|
| Blå  | XS   |
| Blå  | L    |
| Blå  | M    |
| Svart | M    |
| Svart | L    |
| Svart | XL   |
| Brun | L    |
| Brun | XL   |
| Brun | XXL  |

## <a name="the-version-product-dimension"></a>Produktdimensjonen versjon

Versjon er en produktdimensjon som er ment å hjelpe deg med å vedlikeholde og spore flere versjoner av et produkt gjennom hele forsyningskjeden. Versjonssporing er avgjørende for produsenter som arbeider i en verden med stadig kortere produktlivssykluser, økt kvalitet og pålitelighetskrav og økt fokus på produktsikkerhet.

Som en standard produktdimensjon vil versjon oppføre seg på samme måte som de eksisterende produktdimensjonene (størrelse, stil, farge og konfigurasjon). Derfor kan du bruke den til andre formål enn å spore produktversjoner.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Aktivere versjonsdimensjonen

#### <a name="before-you-turn-on-the-version-dimension"></a>Før du aktiverer versjonsdimensjonen

Når du aktiverer versjonsdimensjonen, kan noe funksjonalitet bli ødelagt eller slutte å fungere som forventet hvis du har installert andre løsninger som legger til tilpasninger i beholdningsdimensjonene. For at versjonsdimensjonen skal fungere som den skal, må du kanskje oppdatere disse løsningene slik at de inkluderer versjonsdimensjonen i referansene til beholdningsdimensjonene.

Når du tester løsningene for å sikre kompatibilitet med versjonsdimensjonen, kan du se etter følgende elementer:

1. **Funksjonalitet:** Det viktigste er at eventuelle tilpasninger som involverer beholdningsdimensjonene, må vurderes for å sikre at de kan arbeide sammen med versjonsdimensjonen.
1. **Referanser til beholdningsdimensjonene:** Se etter referanser til beholdningsdimensjonene (det vil si steder der dimensjonene eksplisitt er referert). Referanser til `InventDimId` skal fungere som standard, men se etter referanser til stil eller farge. Du kan for eksempel kontrollere følgende elementer:

    - API-kall i utvidede klasser
    - Alle referanser til bestemte beholdningsdimensjoner i utvidelseskode (denne koden må flyte versjonsdimensjonen sammen med dimensjonene for stil, farge og størrelse).

1. **Referanser til foreldede API-kall:** I innføringen av versjonsdimensjonen har Microsoft forsøkt å gjøre så få API-er som mulig foreldet. De få API-ene som er blitt foreldet, vil gi en advarsel når du aktiverer konfigurasjonsnøkkelen **Produktdimensjon – versjon**. Kall til disse API-ene må rettes opp i de utvidede løsningene før du aktiverer versjonsdimensjonen i et produksjonssystem. Her er de versjonsspesifikke foreldede API-ene:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Tilordninger:** Hvis noen tilordninger bruker beholdningsdimensjonene, må den tilsvarende relasjonstilordningen til disse tilordningene oppdateres, slik at de inkluderer versjonsdimensjonen. I den utvidede modellen eller tabellutvidelser må du se etter tabeller der feltene omfatter beholdningsdimensjoner.
1. **Microsoft Dynamics 365 Commerce-funksjonalitet:** Når versjonsdimensjonen er aktivert, vil den vises i hele den Commerce-spesifikke koden i Dynamics 365 Supply Chain Management. Versjonsdimensjonen støttes imidlertid ikke av Commerce-kanaldatabasen eller i salgssteds- (POS) eller e-handelsapper. Disse Commerce-spesifikke programmene støtter ikke brukere som selger/sender eller returnerer/mottar lager etter versjonsdimensjon. Oppslagsfunksjoner for lagertilgjengelighet vil ikke skjelne lageret etter versjonsdimensjon i Commerce-apper. Denne virkemåten ligner på den gjeldende virkemåten til konfigurasjonsdimensjonen i hele Commerce.

#### <a name="turn-on-the-version-dimension"></a>Aktivere versjonsdimensjonen

Før du kan bruke versjonsdimensjonen, må den være aktivert i systemet. Denne oppgaven krever administrasjonstillatelser.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
1. Slå på funksjonen som heter *Produktdimensjonen versjon*. (Hvis du vil ha mer informasjon, kan du se [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Sett systemet i [vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. På fanen **Konfigurasjonsnøkler** utvider du **Handel** og merker deretter av for **Produktdimensjon – versjon**.
1. Deaktiver [vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Områder der versjonsdimensjonen ikke støttes

Følgende områder støtter ikke versjonsdimensjonen (du kan likevel bruke disse områdene, men du kan ikke legge til versjonsbaserte produkter (produkter der versjonsdimensjonen brukes) i dem). Du kan for eksempel ikke legge til en versjonsbasert vare i en leverandørkatalog. Årsaken er at hvis du legger til produkter med versjonsdimensjonen i disse områdene, kan det føre til oppdelingsendringer.

- Månedlig rapport for kostobjekt
- Oppgavebuffer for kostnadsobjekt
- MCR-salgsstatistikk per vare
- Leverandørkataloger
- EcoResProductDimensionGroupEntity

I tillegg støtter funksjonene for ordreoppretting og ordrebehandling i Commerce (for eksempel for POS, kundestøtte og e-handelsordrer) ikke versjonsdimensjonen. Det finnes ingen bekreftet tidslinje for når Commerce-ordrer blir forbedret for å støtte det.

### <a name="functional-characteristics-of-the-version-dimension"></a>Funksjonelle karakteristikker for versjonsdimensjonen

Versjonsdimensjonen fungerer på samme måte som de andre produktdimensjonene. På grunn av det bestemte formålet, og fordi den er ment å vedlikeholde og spore flere versjoner av et produkt, oppfører den seg litt forskjellig. Her er noen av forskjellene og likhetene:

- **Det finnes ingen versjonsgruppe.**

    Selv om gruppekonseptet finnes for størrelse, farge og stil (fargegruppe, størrelsesgruppe og stilgruppe), finnes det ikke noe versjonsgruppekonsept. Med grupper kan du forhåndsdefinere de aktuelle verdiene slik at når du for eksempel tilordner en fargegruppe til et produkt, vil produktet kunne bruke alle fargene i denne fargegruppen. Dette konseptet gjelder ikke for versjonsdimensjonen, fordi versjonene som et produkt tar, ikke er forhåndsdefinert når produktet skapes. I stedet blir versjoner opprettet i løpet av produktets levetid etter hvert som de er nødvendige. Hvis form, tilpasning og funksjon til produktet forblir lik, oppretter du vanligvis en ny versjon i stedet for et nytt produkt.

- **Forslag til produktvarianter fungerer slik de gjør for øyeblikket.**

    Forslag til produktvarianter vil opprette forslag for alle versjonsdimensjonsverdier, på samme måte som for andre dimensjoner. Prosessen med å opprette og lansere versjoner av produkter er den samme som for produkter som bruker andre dimensjoner. Når du oppretter et versjonsbasert produkt, opprettes den første versjonen (V1) som en produktdimensjon, og variantene lanseres. Etter hvert som produktet endres og en ny versjon er nødvendig, blir den nye versjonsverdien (V2) lagt til, og de nødvendige variantene vil bli utgitt. Det er ingen forventning om at alle versjonene (V1,Vv2 og V3) blir opprettet på forhånd for produktet.

> [!IMPORTANT]
> Hvis du aktiverer og bruker versjonsdimensjonen, kan det hende at noen løsninger som refererer til beholdningsdimensjonene, slutter å fungere som forventet. Du kan bekrefte og løse disse problemene ved å kontakte den uavhengige programvareleverandøren for de berørte løsningene. Hvis du vil ha mer informasjon, kan du se [Aktivere versjonsdimensjonen](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]