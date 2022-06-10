---
title: Vurderinger for søkemotoroptimalisering (SEO) for området
description: Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 2f90581766dba3d3a671df52ec08339a1a0fd7dc
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806411"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Vurderinger for søkemotoroptimalisering (SEO) for området


[!include [banner](includes/banner.md)]

Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.

## <a name="a-site-that-is-under-development"></a>Et område som er under utvikling

For å sikre at søkeresultater ikke indekserer et område under utvikling, bør alle områdesider ha **noindex** og **nofollow** metakodene. Det er en god fremgangsmåte å opprette et fragment basert på [Modul for metakoder](metatags-module.md) som inneholder følgende metakodeoppføring, og sørge for at fragmentet legges til i HTML \<head\>-delen i alle maler som brukes på området.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Myk lansering av et område

Under en "myk lansering" er et webområde gjort tilgjengelig for en begrenset målgruppe eller et begrenset marked før den fullstendige oppstarten skjer. Hvis du gjør en myk lansering av webområdet, bør du vurdere å la metakodene **noindex** bli værende. På denne måten bidrar du til å sikre at den myke oppstarten forblir begrenset til den begrensede målgruppen du vil nå.

## <a name="a-site-that-is-in-production"></a>Et område som er i produksjon

Når et område er i produksjon, bør du kontrollere at alle områdesidene er riktig kodet. Microsoft Dynamics 365 Commerce bruker informasjonen som er angitt for en side, til å gjengi all søkemotorinformasjon på den aktuelle siden. Følgende moduler inneholder denne funksjonaliteten: kategorisidesammendrag, listesidesammendrag og produktsidesammendrag.

For å optimalisere søkemotorindeksering bruker gjengivelsesrammeverket både opplysningene fra søkemotoregenskapene som er konfigurert i Dynamics 365 Commerce, og modulspesifikk informasjon. For et område som er i produksjon, bør du kontrollere at robots.txt-filen tillater indeksering av hele området, og at det inneholder koblinger til det publiserte områdekartdokumentet. Du bør slå på funksjonen for generering av områdekart på **Områdeinnstillinger \> Områdekart aktivert**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Innstillinger for sidesøkemotor for intern forhåndsvisning, begrenset målgruppe og alle målgrupper

Fordi Dynamics 365 Commerce støtter WYSIWYG-forhåndsvisning i visuell sidebygger(det du ser, er det du får), kan forfattere klargjøre sideinnholdet uten å bekymre seg om at informasjonen blir synlig for besøkende på webområdet. Hvis en side må publiseres, men eksponeringen må begrenses, skal den ha metakoden **noindex**, slik at den ikke vil bli indeksert av søkemotorer. Når siden er klar for alle målgrupper, bør alle de grunnleggende søkemotormetadataene være til stede for å maksimere effektiviteten av søkmotorindeksering. I tillegg bør metakoden **nolimit** fjernes.

## <a name="additional-resources"></a>Tilleggsressurser

[Behandle brukere og roller for e-handel](manage-ecommerce-users-roles.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

[Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
