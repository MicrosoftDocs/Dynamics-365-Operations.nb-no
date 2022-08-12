---
title: Katalogvelgermodul
description: Denne artikkelen dekker katalogvelgermoduler og beskriver hvordan du legger dem til i e-handelsområder av typen bedrift-til-bedrift (B2B) i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136947"
---
# <a name="catalog-picker-module"></a>Katalogvelgermodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker katalogvelgermoduler og beskriver hvordan du legger dem til i e-handelsområder av typen bedrift-til-bedrift (B2B) i Microsoft Dynamics 365 Commerce.

En katalogvelgermodul er en spesiell beholder som brukes til å vise alle produktkatalogene som er tilgjengelige for B2B-områdebrukere for handel. Flere kataloger støttes i øyeblikket bare for B2B-områder.

Illustrasjonen nedenfor viser et eksempel på en katalogvelgermodul.

![Eksempel på en katalogvelgermodul med tre produktkataloger.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Legg til en katalogvelgermodul på nettstedet ditt

Følg denne fremgangsmåten for å legge til en katalogvelgermodul på nettstedet ditt i Commerce-områdebyggeren.

### <a name="create-a-catalog-picker-page"></a>Opprett en katalogvelgerside

Opprett først en katalogvelgerside.

1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du **Katalogvelger**.
1. Under **URL-adresse for side**, angir du en URL-adresse for siden og velger deretter **Neste**.

    ![Dialogboksen Opprett en ny side.](./media/Create-catalog-picker-page.png)

1. Velg **Generelt innhold** under **Velg en mal**, og velg deretter **Neste**.
1. Velg **Fleksibelt oppsett** under **Velg et oppsett**, og velg deretter **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du må redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**.
1. Under **Katalogvelger** velger du **Hovedspor**, velger ellipsen (**...**) og velger deretter **Legg til modul**.

    ![Legge til en modul i hovedsporet under Katalogvelger.](./media/Author-web-page-catalog-picker-1.png)

1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. Velg **Beholder**-sporet, velg ellipsen (**…**), og velg deretter **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Katalogvelger**-modulen, og deretter velger du **OK**.
1. I egenskapsruten **Katalogvelger**, under **Overskrift**, velger du **Kataloger** og skriver deretter inn en overskrift for katalogvelgersiden.
1. Under **Overskriftsnivå** velger du et overskriftsnivå og velger deretter **OK**.
1. Under **Rik tekst** angir du tekst som skal vises øverst på katalogvelgersiden.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="add-a-link-on-your-account-page"></a>Legg til en kobling på kontosiden

Deretter legger du til en referanse til katalogvelgersiden på **Min konto**-siden.

1. Gå til **Sider**, finn og velg områdets **Min konto**-side, og velg deretter **Rediger**.
1. Under **Hoved**-sporet på siden velger du sporet **Generell kontoflis**. 
1. I egenskapsruten **Generell kontoflis**, under **Koblinger**, velger du **Legg til handlingskobling** og deretter **Handlingskobling**.
1. I dialogboksen **Handlingskobling**, under **Koblingstekst**, skriver du inn koblingsteksten for koblingen til katalogvelgersiden.
1. Under **Koblingsmål** velger du **Legg til en kobling**.
1. Velg **Egendefinert side** i dialogboksen **Legg til en kobling**, og velg deretter **Neste**.
1. Under **Navn** velger du katalogvelgersiden, velger **Bruk** og velger deretter **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Illustrasjonen nedenfor viser et eksempel på en kontoside med en referanse til katalogsiden.

![Mine kontoer-side med kobling til katalog.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Legg til en kobling fra overskriften

Til slutt legger du til en kobling fra overskriften til nettstedet i katalogene.

1. Gå til **Fragmenter**, finn og velg overskriftsfragmentet til nettstedet, og velg deretter **Rediger**.
1. Velg **Topptekst**-sporet. 
1. I egenskapsruten **Overskrift**, under **Min konto-koblinger**, velger du **Legg til handlingskobling** og deretter **Handlingskobling**.
1. I dialogboksen **Handlingskobling**, under **Koblingstekst**, skriver du inn koblingsteksten for koblingen til katalogvelgersiden.
1. Under **Koblingsmål** velger du **Legg til en kobling**.
1. Velg **Egendefinert side** i dialogboksen **Legg til en kobling**, og velg deretter **Neste**.
1. Under **Navn** velger du katalogvelgersiden, velger **Bruk** og velger deretter **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn topptekstfragmentet, og velg deretter **Publiser** for å publisere det.

Illustrasjonen nedenfor viser et eksempel på en overskrift på nett e-handelsnettsted med en kobling til B2B-katalogen.

![Overskrift på e-handelsnettsted med rullegardinkobling til katalog.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Tilleggsressurser 

[Opprett handelskataloger for B2B-områder](catalogs-b2b-sites.md)

[Påvirkning av handelskataloger for B2B-tilpasninger](catalogs-b2b-sites-dev.md)

[Vanlige spørsmål om handelskataloger for B2B](catalogs-b2b-sites-FAQ.md)

[Kontobehandlingssider og -moduler](account-management.md)

[Topptekstmodul](author-header-module.md)
