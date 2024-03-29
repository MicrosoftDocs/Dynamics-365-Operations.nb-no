---
title: Søkebanemodul
description: Denne artikkelen dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fe5dfea7e579d54d11be35eb657a1c1f617a5724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277092"
---
# <a name="breadcrumb-module"></a>Søkebanemodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Brødsmulemoduler brukes til å levere sekundær navigasjon på områdesider. De vises vanligvis øverst på en side, under overskriften. Selv om brødsmulemoduler kan legges til på en hvilken som helst side, brukes de oftest på sider for produktdetaljer (PDP-sider) for å vise produktkategorihierarkiet og gi en rask metode for å bevege seg rundt på et område. En brødsmulemodul kan også brukes til å vise en "Tilbake til resultatene"-kobling når en bruker åpner en PDP fra en søke- eller listeside. På denne måten kan brukere raskt gå tilbake til den filtrerte listesiden for å fortsette å handle.

På sider som inneholder produktkategorikontekst, for eksempel PDP-er og kategorisider, viser brødsmulekategorier kategorihierarkiet. På sider som ikke inneholder kategorikontekst, viser brødsmulemoduler **&lt;Områderot&gt; / &lt;Gjeldende side&gt;** som standard. Brødsmulemoduler kan også konfigureres manuelt på andre typer områdesider for å vise koblinger til bestemte sider på området.

> [!NOTE]
> Brødsmulemodulen er tilgjengelig i Dynamics 365 Commerce 10.0.12-versjonen.

Bildet nedenfor viser et eksempel på en brødsmulemodul som viser kategorihierarkiet på en PDP.

![Eksempel på en brødsmulemodul.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Innstillinger for brødsmulemoduler

Brødsmulemodulen er avhengig av **Brødsmulevisningstype på PDP**-innstillingen, som er angitt på **Områdeinnstillinger \> Utvidelser** i områdebygger. Denne innstillingen har tre mulige verdier:

- **Vis kategorihierarki** – Når denne verdien er valgt, viser brødsmulemodulen det fullstendige kategorihierarkiet for produktet som vises på PDP.
- **Vise tilbake til resultater** – Når denne verdien er valgt, vil brødsmulemodulen vise en "Tilbake til resultater"-kobling på en PDP hvis brukeren åpnet PDP-en fra en modul som tillater en "Tilbake til resultater"-kobling. Denne funksjonaliteten er tilgjengelig når brukere navigerer fra listesider for kategorier, søk, lister og anbefalinger. For å støtte denne funksjonaliteten har modulene for produktinnsamling og søkeresultater en egenskap som heter **Tillat tilbake til resultater på PDP**. Denne egenskapen gir deg fleksibilitet til å definere hvilke moduler som støtter koblingsfunksjonen "Tilbake til resultatene" på PDP-en. Når for eksempel **Vis tilbake til resultater** er valgt for **Brødsmulevisningstype på PDP**-innstillingen i brødsmulemodulen, og **Tillat tilbake til resultater på PDP** er valgt for søkeresultatmodulen for søkesiden, vises en kobling for "Tilbake til resultater" når brukere navigerer fra søkesiden til en PDP.
- **Vis kategorihierarki og tilbake til resultater** – denne verdien er en kombinasjon av de foregående to. Når denne verdien er valgt, vil brødsmulemodulen vise både hele kategorihierarkiet og en "Tilbake til resultater"-kobling (hvis den er konfigurert) på en PDP.

> [!IMPORTANT]
> Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.12-versjonen. Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Egenskaper for brødsmulemoduler

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Rot | Tekst eller kobling| Denne valgfrie egenskapen angir koblingstekst og et koblingsmål for roten til brødsmuleområdet. Hvis denne egenskapen ikke er konfigurert, blir det ikke definert noen rot. |
| Brødsmulekobling | Sammenkobling | Denne valgfrie egenskapen angir koblinger for en manuelt konfigurert brødsmule, hvis disse koblingene er nødvendige. Koblingene vises i den rekkefølgen de er oppført i. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Legge til en brødsmulemodul på en ny side

Hvis du vil legge til en brødsmulemodul på en PDP og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Områdeinnstillinger \> Utvidelser**, finn **Brødsmulevisningstype på PDP**-innstillingen og velg **Vis kategorihierarki**.
1. Gå til **Maler**, og velg PDP-malen.
1. I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søkebane**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne en PDP som bruker PDP-malen. Hvis en PDP ennå ikke finnes, oppretter du en.
1. I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søkebane**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for **Brødsmule**-sporet, under **Rot**, velger du **Koblingstekst**.
1. I **Koblingstekst**-dialogboksen skriver du **Hjem**,og under **Koblingsmål** velger du **Legg til en kobling**.
1. Velg en kobling til brødsmuleroten i dialogboksen **Legg til en kobling**, og velg deretter **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Navigasjonsmenymodul](nav-menu-module.md)

[Områdevelgermodul](site-selector.md)

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Produktsamlingsmoduler](product-collection-module-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
