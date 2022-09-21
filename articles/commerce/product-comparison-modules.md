---
title: Produktsammenligningsmoduler
description: Denne artikkelen beskriver produktsammenligningsmoduler og hvordan du implementerer dem slik at kunder kan gjøre produktsammenligninger på Microsoft Dynamics 365 Commerce-netthandelssider.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474133"
---
# <a name="product-comparison-modules"></a>Produktsammenligningsmoduler

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver produktsammenligningsmoduler og hvordan du implementerer dem slik at kunder kan gjøre produktsammenligninger på Microsoft Dynamics 365 Commerce-netthandelssider.

> [!NOTE]
> Modulene for produktsammenligningen og produktsammenligningsknapp er tilgjengelige fra Dynamics 365 Commerce 10.0.29-versjonen. De kan brukes både for nettsteder for bedrift-til-kunde (B2C) og bedrift-til-bedrift-nettsteder (B2B).

Med produktsammenligningsfunksjonalitet kan kundene sammenligne produktdetaljer på en produktsammenligningsside slik at de kan ta bedre kjøpsavgjørelser. Denne funksjonaliteten konfigureres i Commerce Site Builder ved hjelp av produktsammenligningsmodulen. På produktlistesider (PLP-er), for eksempel kategoriresultater, søkeresultater og produktsamlingssider, kan du konfigurere en knapp for produktsammenligning der kundene kan legge til produkter i sammenligningssammenligning. Denne funksjonaliteten konfigureres i områdebyggeren ved hjelp av produktsammenligningsknappmodulen, som fungerer som [hurtigvisningsmodulen](quick-view-module.md).

Når nettstedsbrukere legger til produkter for sammenligning ved å merke dem på produktfliser, vises det en sammenligningssammenligning nederst på siden. Sammenligningshastigheten viser produktene som kjøperen for øyeblikket sammenligner, sammen med korte forhåndsvisninger av produktene. Nettstedsbrukere kan også legge til produkter fra produktdetaljsider (PDP-er), og de kan legge til bestemte produktvarianter som sammenlignes med produktstandarder.

Når kundene har lagt til et par produkter i sammenligningssammenligningssiden, kan de velge **Sammenlign** som skal omdirigeres til en produktsammenligningsside. Produktsammenligningssiden viser produktdetaljer for hvert valgte produkt, slik at kunder kan sammenligne bilder, priser, produktdimensjoner (størrelse, stil og farge), akkumulert vurderingsinformasjon og andre produktattributter.

Illustrasjonen nedenfor viser eksempler på produktknappen for sammenligning, fjern fra sammenligningsknappen, sammenligningsforløpet og produktsammenligningssiden.

![Oversikten over produktsammenligning viser produktknappen for sammenligning, fjern fra sammenligningsknappen, sammenligningsskuffpanelet og produktsammenligningssiden.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Produktsammenligningssiden sammenligner et standardsett med produktegenskaper og alle attributter som kan vises på en PDP for et angitt produkt.
> - Egenskaper som leveringsmåte, lagerbeholdning og måleenhet kan ikke vises på en produktsammenligningsside.
> - Kunder kan legge til produkter fra ulike kategorier i sammenligningssammenligningen, forutsatt at produktene er fra den samme katalogen.
> - Funksjonaliteten for produktsammenligning er i øyeblikket begrenset til å sammenligne produkter i en enkeltkatalog. Nettstedsbrukere kan ikke sammenligne på tvers av kataloger.
> - Du bør sikre at egenskapen **Gjengi modulklientside** er fjernet for alle produktsammenligningsmoduler.
> - Du bør sikre at hurtigbufring på sidenivå er deaktivert for alle sider der produktsammenligningsmodulen brukes. Disse sidene inneholder PDP-er, PLP-er og produktsammenligningssider. Hvis du vil ha mer informasjon, kan du se [Konfigurer sidebufring](e-commerce-extensibility/page-caching.md).

Illustrasjonen nedenfor viser et eksempel på en produktsammenligningsside.

![Produktsammenligningsside.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Legg til produktsammenligningsmodulen i en ny produktsammenligningsside

Du kan opprette en egen produktsammenligningsside ved å legge til en produktsammenligningsmodul i hoveddelen av en side. I tillegg til å gjøre det mulig for kunder å sammenligne produktdetaljer for ulike produkter, kan du konfigurere produktsammenligningsmodulen for å gi kunder muligheten til å raskt fullføre innkjøpet etter at de har sammenlignet produkter. Produktsammenligningsmodulen inneholder også et **tomt sammenligningsspor**, der du kan legge til en innholdsblokkmodul som beskriver tom tilstand (for eksempel Produktsammenligningen er tom).

Hvis du vil legge til en produktsammenligningsmodul på en ny produktsammenligningsside, følger du disse trinnene.

1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du et egnet sidenavn F.eks. **Produktsammenligning**, og deretter velger du **Neste**.
1. Under **Velg en mal** velger du den riktige malen (f.eks. malen som brukes av standard kategoriside), og deretter velger du **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du må redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**.
1. I **Hoved**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Produktsammenligning**-modulen, og deretter velger du **OK**.
1. Velg ellipseknappen (**...**) i **Hurtigvisningsknapp**-sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Produkthurtigvising**-modulen, og deretter velger du **OK**.
1. I egenskapsruten til høyre konfigurerer du egenskapene for modulen **Produkthurtigvisning**.
1. I **Tom sammenligning**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Innholdsblokk**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for **Innholdsblokk**-modulen i egenskapsruten til høyre: 
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Følgende illustrasjon viser et eksempel på en tom sammenligningsside i områdebyggeren.

![Produktsammenligningsmodul.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Legg til en produktsammenligningsknapp i produktfliser på søke- og kategoriresultatsider

Med knappen for produktsammenligning kan brukere raskt legge til et produkt i sammenligningsskuffen når de blar gjennom produkter på en listeside. De kan legge til et eller flere produkter i sammenligningssammenligningen fra en listeside uten å måtte gå til en PDP.

Produktsammenligningsknappen støttes av modulene for produktsamling, søkeresultater og PDP-kjøpsboks.

For å legge til en produktsammenligningsknapp i produktfliser på søke- og kategoriresultatsider følger du denne fremgangsmåten.

1. I områdebyggeren kan du gå til **Sider** og åpne kategorisiden der du vil legge til en produktsammenligningsknapp.
1. I **Hoved**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søkeresultater**-modulen, og deretter velger du **OK**.
1. På **Produktsammenligningsknapp**-sporet for modulen **Søkeresultater** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Produktsammenligningsknapp**-modulen, og deretter velger du **OK**.
1. I egenskapsruten til høyre konfigurerer du egenskapene for modulen **Produktsammenligningsknapp**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Angi maksimalt antall produkter som skal vises i sammenligningsskuffen

Du kan angi maksimalt antall produkter som skal vises i sammenligningsskuffen ved å gå til **Områdeinnstillinger \> Utvidelser** i områdebyggeren. Du kan konfigurere separate maksimumsgrenser for skrivebord- og mobil-/nettbrettvisninger. Som standard vil det ikke bli iverksatt en grense hvis det ikke er definert en maksimumsgrense.

> [!NOTE]
> For en optimal nettleseropplevelse anbefaler vi at du angir maksimalt antall produkter i sammenligningssammenligningen til **2** for den mobilvisningsporten og **4** for visningsporten for skrivebord for å redusere mengden vannrett rulling som kreves.

For å angi maksimalt antall produkter i sammenligningsskuffen følger du denne fremgangsmåten.

1. Gå til **Områdeinnstillinger \> Utvidelser** i områdebyggeren.
1. For egenskapen **Produkter i sammenligningsgrensen – skrivebordsenheter** legger du inn det maksimale antallet produkter som skal vises i sammenligningsskuffen for visningsporter for skrivebord.
1. For egenskapen **Produkter i sammenligningsgrensen – mobil- og nettbrettenheter** legger du inn det maksimale antallet produkter som skal vises i sammenligningsskuffen for visningsporter for mobil og nettbrett.
1. På kommandolinjen velger du **Lagre og publiser**.

![Områdeinnstillinger for å begrense produkter i sammenligningsskuffen.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
