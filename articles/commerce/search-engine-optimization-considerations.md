---
title: Vurderinger for søkemotoroptimalisering (SEO) for området
description: Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414727"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Vurderinger for søkemotoroptimalisering (SEO) for området


[!include [banner](includes/banner.md)]

Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.

## <a name="a-site-that-is-under-development"></a>Et område som er under utvikling

Mens et område er under utvikling, skal alle områdesidene ha metakodene **NOINDEX** og **NOFOLLOW**, slik at søkemotorene ikke indekserer sidene og lagrer utviklingsversjoner av området i hurtigbufferen. Hvis du vil gjøre denne konfigurasjonen, må du legge til standard metakodemoduler i områdesidemalen. Standardegenskapene for metakoder vil da være tilgjengelige i delen om søkemotoregenskaper i sideredigeringsprogrammet. Du kan bruke disse egenskapene til å administrere metakodene.

## <a name="soft-launch-of-a-site"></a>Myk lansering av et område

Under en "myk lansering" er et webområde gjort tilgjengelig for en begrenset målgruppe eller et begrenset marked før den fullstendige oppstarten skjer. Hvis du gjør en myk lansering av webområdet, bør du vurdere å la metakodene **NOINDEX** bli værende. På denne måten bidrar du til å sikre at den myke oppstarten forblir begrenset til den begrensede målgruppen du vil nå.

## <a name="a-site-that-is-in-production"></a>Et område som er i produksjon

Når et område er i produksjon, bør du kontrollere at alle områdesidene er riktig kodet. Microsoft Dynamics 365 Commerce bruker informasjonen som er angitt for en side, til å gjengi all søkemotorinformasjon på den aktuelle siden. Følgende moduler inneholder denne funksjonaliteten: kategorisidesammendrag, listesidesammendrag og produktsidesammendrag.

For å optimalisere søkemotorindeksering bruker gjengivelsesrammeverket både opplysningene fra søkemotoregenskapene som er konfigurert i Dynamics 365 Commerce, og modulspesifikk informasjon. For et område som er i produksjon, bør du kontrollere at robots.txt-filen tillater indeksering av hele området, og at det inneholder koblinger til det publiserte områdekartdokumentet. Du bør slå på funksjonen for generering av områdekart på **Områdeinnstillinger \> Områdekart aktivert**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Innstillinger for sidesøkemotor for intern forhåndsvisning, begrenset målgruppe og alle målgrupper

Fordi Dynamics 365 Commerce støtter WYSIWYG-forhåndsvisning i visuell sidebygger(det du ser, er det du får), kan forfattere klargjøre sideinnholdet uten å bekymre seg om at informasjonen blir synlig for besøkende på webområdet. Hvis en side må publiseres, men eksponeringen må begrenses, skal den ha metakoden **NOINDEX**, slik at den ikke vil bli indeksert av søkemotorer. Når siden er klar for alle målgrupper, bør alle de grunnleggende søkemotormetadataene være til stede for å maksimere effektiviteten av søkmotorindeksering. I tillegg bør metakoden **NOLIMIT** fjernes.

## <a name="additional-resources"></a>Tilleggsressurser

[Behandle brukere og roller for e-handel](manage-ecommerce-users-roles.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

[Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]