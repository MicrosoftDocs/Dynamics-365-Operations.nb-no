---
title: Behandle endringer i formler og ingrediensene
description: Dette emnet beskriver hvordan du behandler formelstyring og administrerer endringer for å behandle hoveddata for produksjon.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c65f929120d2501fa3873880179a9b53ab79c60c73fd4d597fb6151b1c5bb2b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720402"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Behandle endringer i formler og ingrediensene

[!include [banner](../includes/banner.md)]

Hvis du bruker prosessproduksjonsfunksjonene til Microsoft Dynamics 365 Supply Chain Management, kan du også bruke de relaterte formelstyringsfunksjonene til å administrere følgende endringer:

- **Formel- og planleggingselementer:** Behandle endringer i ingredienser i formler og koprodukter og biprodukter.
- **Koprodukter og biprodukter:** Rediger antall og annen informasjon om koproduktene og biproduktene i en formel.
- **Faktisk vekt-varer:** Administrer endringer i faktisk vekt-varer.

## <a name="turn-on-this-feature-in-your-system"></a>Aktivere denne funksjonen i systemet

Hvis du vil bruke denne funksjonen, må du utføre følgende oppgaver:

1. Aktiver funksjonen for *Styring av teknisk endring* og konfigurasjonsnøkkelen, som beskrevet i [Oversikt over styring av teknisk endring](product-engineering-overview.md). Som nevnt i det emnet må du også aktivere lisensnøkkelen for **Endringsstyring for prosessproduksjon**, som er nestet under lisensnøkkelen for **Behandling av teknisk endring**.
1. Slå på funksjonen *Behandle endringer i formler og ingredienser* i [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Navnekonvensjoner for funksjon

I brukergrensesnittet for Supply Chain Management (grensesnitt) og dokumentasjon er endringsbehandlingsfunksjonalitet vanligvis referert til som *teknisk endringsbehandling*, og de administrerbare produktene kalles vanligvis *tekniske produkter*. Selv om denne terminologien vanligvis ikke er knyttet til administrasjon av formler for prosessproduksjon, bør du tenke på teknisk endringsbehandling som ganske enkelt endringsbehandling, og du bør se på tekniske produkter som versjonsprodukter.

## <a name="work-with-formula-change-management-features"></a>Arbeide med funksjoner for formelendringsbehandling

Listen nedenfor gir et sammendrag av hvordan funksjoner for teknisk endringsbehandling gjelder for formelstyring. Her finner du også koblinger til mer informasjon. Siden behandling av formelendringer benytter seg av styringsfunksjonene for teknisk endringsbehandling, bør du lære hvordan administrasjon av tekniske endringer fungerer generelt, slik at du kan bruke det til å administrere formlene og ingrediensene.

- **Sentralisert produktdataadministrasjon** – Konfigurer en organisasjon som gjennom en administrert frigivelsesprosess sørger for at nøyaktige og relevante produktdata er tilgjengelige for brukere i hele organisasjonen. Hvis du vil ha mer informasjon, kan du se [Tekniske firmaer og dataeierskapsregler](engineering-org-data-ownership-rules.md).
- **Produktversjonering** – Spor endringer i produkter via produktversjoner, og kontroller produktet i alle stadiene i forsyningskjeden. På denne måten kan du spore endringene i skjemaene. Hvis du vil ha mer informasjon, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).
- **Administrasjon av produktlivssyklus** – Administrer synligheten til produktdata i hele organisasjonen, og kontroller tilgjengeligheten av produktversjoner i hvert trinn i forsyningskjeden. Du har detaljert kontroll over når en produktversjon kan brukes i bestemte forretningsprosesser, og du kan opprette dine egne statuser etter dine forretningsbehov. Hvis du vil ha mer informasjon, kan du se [Produktstatuser og transaksjoner](product-lifecycle-state-transactions.md).
- **Behandling av formelendringer** – Brukere i hele organisasjonen kan be om endringer i formler. Bruk endringsordrer til å vurdere og dokumentere virkningen av foreslåtte endringer. Legg til arbeidsflyter for å styre endringsprosessen og frigjøringen av nye versjoner av produktet og formelen. Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).
- **Beredskapskontroll** – Bruk systemkontroller og brukerveiledning (spørreskjemaer og kontrollister) for å sikre at alle nødvendige produktdata er fullstendig angitt før produktet frigis. Hvis du vil ha mer informasjon, kan du se [Produktklargjøring](product-readiness.md).
- **Forbedrede produktfrigivelsesfunksjoner** – Frigi fullstendig definerte versjoner av et produkt og formelen fra en organisasjon (juridisk enhet) til andre juridiske enheter. Du kan til og med bestemme om produktinformasjonen må gjennomgås eller redigeres før frigivelse. Hvis du vil ha mer informasjon, kan du se [Frigi produktstrukturer](release-product-structure.md).

Legg merke til at de fleste emnene som er koblet til i den forrige listen, inneholder eksempler som er basert på stykklister. Formler fungerer imidlertid på en lignende måte. Her er noen flere begreper det er nyttig å vite når du bruker endringsbehandling (eller bare formelendringsbehandling) til å administrere formler og stykklister:

- For hver [tekniske produktkategori](engineering-versions-product-category.md) kan du angi produksjonstypen (stykkliste, formel eller planleggingselement). Du kan også angi om støtte for faktisk vekt er nødvendig for produkter som bruker denne kategorien.
- Koprodukter og biprodukter er ikke tekniske produkter. Derfor har de ikke versjonsnummeret. Hvis du må endre dem, kan du bare opprette et nytt produkt. Denne fremgangsmåten gjør vedlikeholdet enklere.
- Du kan styre sluttvarer som er stykklister og som har underordnede formelvarer. Funksjonaliteten vil fungere for en hvilken som helst kombinasjon av stykklister som inneholder formler og/eller formler som inneholder stykklister.
