---
title: Vanlige spørsmål om styring av teknisk endring
description: Dette emnet gir svar på vanlige spørsmål om funksjonen for styring av teknisk endring.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69232eed8520bafeb734ffad43b333bf9e36909e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018691"
---
# <a name="engineering-change-management-faq"></a>Vanlige spørsmål om styring av teknisk endring

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om funksjonen for styring av teknisk endring.

## <a name="should-i-track-the-version-in-transactions"></a>Bør jeg spore versjonen i transaksjoner?

Når du oppretter en kategori for teknisk endring, gir siden **Detaljer for kategori for teknisk endring** et alternativ som kalles **Spor versjon i transaksjoner**. Hva er denne innstillingen, og hva gjør den?

- Hvis du setter alternativet **Spor versjon i transaksjoner** til *Ja*, blir feltet for **Dimensjonsgruppe** filtrert, slik at det bare viser dimensjonsgrupper der versjon er en aktiv dimensjon.
- Hvis du setter alternativet **Spor versjon i transaksjoner** til *Nei*, blir feltet for **Dimensjonsgruppe** filtrert, slik at det bare viser dimensjonsgrupper der versjonsdimensjonen **ikke** er en aktiv dimensjon.

### <a name="if-you-track-the-version-in-transactions"></a>Hvis du sporer versjonen i transaksjoner

For tekniske kategorier der du har valgt en dimensjonsgruppe der versjonen er en aktiv dimensjon, kan du spore versjoner i transaksjoner for produkter i denne kategorien. I dette tilfellet er det tekniske produktet en produktstandard, og hver versjon av produktet vil være en produktvariant som bruker versjonsdimensjonen. Andre dimensjoner kan brukes sammen med versjonsdimensjonen.

I så fall behandles hver ingeniørversjon som en variant i alle prosesser. Hvis du har en bestemt variant i en transaksjon (slik at du kan bestemme hvilken variant som ble solgt eller kjøpt), må du derfor administrere beholdningen for hver versjon, hovedplanleggingen vil planlegge forsyning for hver versjon og så videre. Hvis du trekker tilbake en versjon fra markedet, må du manuelt justere gjelder fra-datoene og gyldig til-datoene, slik at de gjenspeiler endringen. Du må også administrere beholdningen for å være sikker på at du ikke har ubrukte versjoner av varer i lagrene.

Selv om dette alternativet krever mer styringsinnsats, anbefaler vi det hvis du krever høy sporbarhet for de spesifikke versjonene som brukes i hver transaksjon.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Hvis du ikke sporer versjonen i transaksjoner

For tekniske kategorier der du har valgt en dimensjonsgruppe der versjonen **ikke** er en aktiv dimensjon, kan du **ikke** spore versjoner i transaksjoner for produkter i denne kategorien. Hvis du ikke bruker noen annen dimensjon, vil i så fall det tekniske produktet være et spesifikt produkt. Produktet vil fortsatt bli versjonsgenerert, og du kan styre informasjon om bestemte versjoner (for eksempel stykklisten \[BOM] og ruten), men du kan ikke spore hvilken bestemt versjon som ble brukt i hver transaksjon. Gyldig fra-datoen og gyldig til-datoene angir gyldigheten av hver versjon.

Dette alternativet er mye enklere å administrere, fordi hvis du vil endre fra én versjon til en annen, må du bare gjøre de nødvendige endringene i en endringsrekkefølge, og deretter oppdatere gyldig fra- og gyldig til-datoene i den tekniske versjonen. Produksjonsprosessene vil deretter plukke opp den nødvendige stykklisten og ruten for produktet (og den spesifikke versjonen).

De fleste organisasjoner velger dette alternativet fordi det gir versjons- og endringsbehandling, men de legger ikke til de ekstra administrasjonskostnadene for å spore versjonen i hver transaksjon, på lager og under hovedplanlegging.

## <a name="which-fields-are-copied-to-the-released-item-template"></a>Hvilke felt kopieres til den frigitte varemalen?

Når et teknisk firma oppretter et teknisk produkt, opprettes dette produktet som et frigitt produkt i det tekniske firmaet. Det frigitte produktet som opprettes, er basert på den valgte *frigitte varemalen*. (Den frigitte varemalen er i seg selv et eksisterende frigitt produkt.) Den frigitte varemalen brukes også når produktet frigis til et driftsfirma. I hvert tilfelle definerer den frigitte varemalen de fleste feltverdiene for det frigitte produktet, og disse verdiene kommer fra siden **Frigitt produktdetaljer**.

Følgende tabeller viser feltene som kopieres i løpet av disse prosessene.

| Hurtigfane | Felt som kopieres ved produktopprettelse i ingeniørfirmaet | Felt som kopieres ved frigivelse til et driftsfirma |
|---|---|---|
| **Generelt** | Alle felt i **Administrasjon**-delen | De samme feltene som kopieres for ingeniørfirmaet |
| **Kjøp** | Alle felt | Alle felt unntatt **Enhet** |
| **Selg** | Alle felt i følgende deler: **Salgsordre**, **Administrasjon**, **Avgiftsnivå**, **Prisoppdatering**, **Grunnleggende salgspris**, **Tillegg**, **Rabatter** og **Alternativt produkt** | Alle de samme feltene som kopieres for ingeniørfirmaet, unntatt **Enhet** |
| **Utenrikshandel** | Alle felt | Alle felt |
| **Administrer lager** | Alle felt og deler *unntatt* **Fysiske dimensjoner** og **Faktisk vekt** | Alle de samme feltene som kopieres for ingeniørfirmaet, unntatt **Enhet** |
| **Ingeniør**, **Planlegg**, **Styr kostnader**, **Administrer prosjekter**, **Finansdimensjoner** og **Lager** | Alle felt | Alle felt unntatt **Stykklisteenhet** |
| **Produktvarianter** | Alle felt i delen **Standard produktvariant** | De samme feltene som kopieres for ingeniørfirmaet |

I tillegg til feltene som vises i den forrige tabellen, kopieres alle standard ordreinnstillinger fra den frigitte varemalen, både når produktet blir opprettet i ingeniørfirmaet, og når det frigis til et driftsfirma. (Hvis du vil vise standard ordreinnstillinger for en frigitt varemal, åpner du den relevante siden **Detaljer om frigitt produkt**, og deretter, på handlingssiden i kategorien **Administrer lager**, velger du **Standard ordreinnstillinger**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Bør jeg opprette en separat juridisk enhet for tekniske produkter eller bruke en eksisterende juridisk enhet?

Forretningskravene bestemmer om du skal opprette en ny juridisk enhet for tekniske produkter.

Ved å opprette et separat ingeniørfirma, kan du holde tekniske data separate, og deretter legge til endringer etter behov for de lokale driftsfirmaene. På denne måten kan du oppnå følgende mål:

- Ha en egen enhet der de tekniske produktene opprettes og administreres.
- Hindre at tekniske produkter vises sammen med resten av de frigitte produktene til de er klare og frigitte.
- Tydelig skille data som styres av tekniske og lokale data.

På den annen side bør du sannsynligvis bruke en eksisterende juridisk enhet som et teknisk firma hvis følgende betingelser gjelder for deg:

- Du har bare én juridisk enhet i systemet, og/eller du trenger ikke et klart skille mellom produkter som er under konstruksjon.
- Du vil ikke duplisere noen data, for eksempel ressursgrupper, ressurser, operasjoner og (kanskje) områder.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Hva er terminologien for tekniske versjoner og varianter?

Terminologien for ingeniørprodukter og produktvarianter fungerer på følgende måte:

- For ingeniørproduktet (det spesifikke produktet hvis ingen dimensjoner brukes, eller produktstandarden hvis en dimensjon brukes), blir nummerregelterminologien definert i kategorien for teknisk produkt. Der har du muligheten til å bruke en nummerserie, tekstkonstanter og attributtnavn og verdier.
- For hver variant av et ingeniørprodukt (hvis det tekniske produktet er en produktstandard, defineres varianter i kategorien for teknisk produkt der du angir dimensjonsgruppen) defineres nummerregelterminologien for hver variant i dimensjonsgruppen. I dette tilfellet kan du bruke produkt-IDen for malen samt dimensjonsverdier og -navn.
