---
title: Behandle metadata for søkemotor
description: Denne artikkelen beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4b04d675a903279e667e1f5fcee387f05d979e81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276835"
---
# <a name="manage-seo-metadata"></a>Behandle metadata for søkemotor

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.

Søkemotormetadata for et område kan administreres ved hjelp av områdekart og sidemetadata.
    
## <a name="site-maps"></a>Områdekart

Et områdekart er en maskinlesbar liste, i XML-format, på sidene på nettstedet. Den er ment å brukes av søkemotorer, slik at de kan gi bedre søkeresultater fra området ditt. Områdekart kan tas inn manuelt ved hjelp av søkemotorer eller publiseres i en robots.txt-fil.

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
1. I sideredigeringsprogrammet, øverst på sidedisposisjonskontroll til venstre, velger du **alternativet for disposisjonsmodus** (tannhjulsymbol) og velger deretter **Avansert disposisjonsvisning**.
1. I disposisjonsvisningen utvider du trekontrollene for å vise innholdet i **HTML-hodesporet**.
1. I **HTML-hodesporet** velger du ønsket SEO-modul (for eksempel **Sidesammendrag**, **Produktsidesammendrag**, **Kategorisidesammendrag** eller **Metakoder**).
1. I egenskapsruten til høyre redigerer du de ønskede SEO-dataene for den valgte SEO-modulen (for eksempel **Tittel**, **Beskrivelse** eller **Delingsbilde**).
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. I feltet **Kommentarer** angr du **Oppdaterte SEO-data**, og deretter velger du **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise siden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.

> [!TIP]
> Forfattere kan bruke **alternativet for disposisjonsmodus** (tannhjulsymbol) øverst på venstre disposisjonskontroll i sideredigeringsprogrammet for å bytte mellom **grunnleggende disposisjonsvisning** og **avansert disposisjonsvisning**. **Grunnleggende disposisjonsvisning** er standardinnstillingen og filtrerer omrisset slik at det bare viser moduler i **Brødtekst-HTML**-spor for en side. **Avansert disposisjonsvisning** viser hele sidemodulen, inkludert **HTML-hode**, **brødtekststart** og **brødtekstslutt**. Denne visningen er nyttig når forfattere må redigere bestemte SEO- eller skriptmodulinnstillinger for en side.

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
