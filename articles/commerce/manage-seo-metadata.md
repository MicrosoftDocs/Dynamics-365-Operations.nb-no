---
title: Behandle metadata for søkemotor
description: Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794217"
---
# <a name="manage-seo-metadata"></a>Behandle metadata for søkemotor

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.

Søkemotormetadata for et område kan administreres ved hjelp av områdekart og sidemetadata.
    
## <a name="site-maps"></a>Områdekart

Et områdekart er en maskinlesbar liste, i XML-format, på sidene på webområdet. Den er ment å brukes av søkemotorer, slik at de kan gi bedre søkeresultater fra området ditt. Områdekart kan tas inn manuelt ved hjelp av søkemotorer eller publiseres i en robots.txt-fil.

Dynamics 365 Commerce støtter automatisk generering av områdekart. Områdekart oppdateres automatisk når sider publiseres og publisering fjernes.

### <a name="turn-on-site-map-generation"></a>Aktivere generering av områdekart

1. Logge på redigeringsverktøyet.
1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Områdebehandling** i navigasjonsruten til venstre.
1. Kontroller at **Områdekart aktivert** er aktivert.

## <a name="page-metadata"></a>Sidemetadata

Dynamics 365 Commerce lar deg administrere søkemotormetadata for enkeltsider. Du kan vise og endre denne informasjonen i delen **Søkemotoregenskaper** i en sidecontainer. Følgende søkemotormetadataegenskaper støttes:

- Stillingstittel
- Beskrivelse
- Søkemotornøkkelord
- ARIA-etiketter
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Endre sidemetadata

Hvis du vil endre sidemetadata, følger du disse trinnene.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Sider** i navigasjonsruten til venstre.
1. Velg startsiden for å åpne den i sideredigeringsprogrammet.
1. På kommandolinjen velger du **Rediger**.
1. Velg **Standard metakoder** i egenskapsruten til høyre.
1. Hvis du vil legge til en ny metakode, velger du **Legg til**, og deretter angir du koden i feltet. Hvis du vil fjerne en eksisterende metakode, velger du papirkurvsymbolet til høyre for den.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. I feltet **Kommentarer** angr du **Oppdaterte metakoder**, og deretter velger du **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise siden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
