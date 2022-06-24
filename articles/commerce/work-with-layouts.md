---
title: Arbeide med forhåndsinnstilte oppsett
description: Denne artikkelen beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 34b9cb15dd77e6317208e6468fbfb60e804f5e8f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896847"
---
# <a name="work-with-preset-layouts"></a>Arbeide med forhåndsinnstilte oppsett

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.

Før du fullfører prosedyrene i denne artikkelen, må du lese [Forhåndsinnstilte og egendefinerte oppsett](templates-layouts-overview.md#preset-and-custom-layouts). Du finner en generell oversikt i [Oversikt over maler og oppsett](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Opprette et nytt forhåndsinnstilt oppsett

Det finnes to metoder for å opprette en forhåndsinnstilt oppsett. Du kan lagre et eksisterende egendefinert oppsett som et nytt forhåndsinnstilt oppsett, eller du kan opprette et forhåndsdefinert oppsett fra grunnen av.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett

Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett.

1. Åpne en eksisterende side som ikke bruker et forhåndsinnstilt oppsett, og som har en modulstruktur som du vil bruke på nytt for andre sider på området.
1. Velg **Rediger** for å sjekke ut siden.
1. Velg **Lagre som nytt oppsett**. Dialogboksen **Lagre som nytt oppsett** vises.
1. Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet. Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem. Derfor må du angi verdier som kan være nyttige for sideforfattere.
1. Velg **OK**.

Det forhåndsinnstilte oppsettet vil nå være tilgjengelig når du oppretter nye sider eller velger et annet oppsett for en side i samme malhierarki.

> [!TIP]
> Hvis du raskt vil se om en bestemt side er bundet til et forhåndsinnstilt oppsett, velger du siden i sidelistevisningen og undersøker metadataene for oppsett i egenskapsruten til høyre.

### <a name="create-a-new-preset-layout"></a>Opprette et nytt forhåndsinnstilt oppsett

Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra bunnen av.

1. Velg **Oppsett** i navigasjonsruten til venstre.
1. Velg **Nytt oppsett**. Dialogboksen **Nytt oppsett** vises.
1. Velg malen som skal brukes for det forhåndsinnstilte oppsettet.
1. Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet. Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem. Derfor må du angi verdier som kan være nyttige for sideforfattere.
1. Velg **OK** for å opprette det nye forhåndsinnstilte oppsettet, og åpne redigeringsprogrammet for oppsett.
1. I oppsettredigering legger du til og konfigurerer moduler ved å bruke disposisjonstreet til venstre og egenskapsruten til høyre. (Prosessen ligner på prosessen for å legge til og konfigurere moduler for en mal i malredigeringsprogrammet.) Ordningen av moduler og eventuelle låste standardinnstillinger blir sentralisert modulkonfigurasjon for alle sider som bruker dette forhåndsinnstilte oppsettet.

## <a name="modify-a-preset-layout"></a>Endre et forhåndsinnstilt oppsett

Følg disse trinnene for å endre et forhåndsinnstilt oppsett.

1. Velg **Oppsett** i navigasjonsruten til venstre.
1. Velg modulen du vil endre, i disposisjonstreet til venstre i oppsettredigering. Følg deretter et av disse trinnene:

    - Hvis du vil flytte en modul opp eller ned i det overordnede elementet, velger du ellipseknappen (**...**) for modulen, og deretter velger du **Flytt opp** eller **Flytt ned**.
    - Hvis du vil endre standardinnstillingene for en modul, kan du bruke egenskapsruten til å angi standardverdier og eventuelt låse dem for alle nedstrømssider.
    - Hvis du vil legge til nye moduler eller fragmenter i containermoduler, velger du ellipseknappen og deretter **Legg til modul** eller **Legg til fragment**.
    - Hvis du vil fjerne en modul fra oppsettet, velger du ellipseknappen og deretter **Slett**.

## <a name="change-a-preset-layout-theme"></a>Endre et forhåndsinnstilt oppsettema

En vanlig praksis er å angi et standardtema for alle sider som bruker et forhåndsinnstilt oppsett.

Hvis du vil angi eller endre temaet for alle underordnede sider som bruker det forhåndsinnstilte oppsettet, følger du disse trinnene.

1. Velg sidecontainermodulen i disposisjonstreet til venstre i oppsettredigering. (Denne modulen er vanligvis den andre noden og kalles **Standardside**.)
1. I egenskapsruten til høyre velger du et tema i feltet **Tema**.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Lagre, sjekke inn, forhåndsvise og publisere et forhåndsinnstilt oppsett

Hvis du vil lagre og sjekke inn det forhåndsinnstilte oppsettet, følger du disse trinnene:

1. Velg **Lagre** øverst i oppsettredigeringsprogrammet. Lagrede endringer påvirker ikke nedstrømssider før de er sjekket inn.
1. Velg **Fullfør redigering**. Dine endringer er nå synlige for nedstrøms arbeidsflyter.

Hvis du vil forhåndsvise endringene, kan du enten åpne en eksisterende side som bruker det forhåndsinnstilte oppsettet, eller opprette en ny side fra oppsettet.

Når du har forhåndsvist endringene i det forhåndsinnstilte oppsettet, følger du en av disse fremgangsmåtene for å publisere oppsettet på ditt aktive område:

1. Gå til **Oppsett**, velg oppsettet, og velg deretter **Publiser**.
1. Velg oppsettnavnet for å åpne redigeringsprogrammet for oppsett, og velg deretter **Publiser**.
1. Publiser en side som refererer til det upubliserte oppsettet. Oppsettet vil automatisk bli publisert.

> [!WARNING]
> Du kan referere til forhåndsinnstilte oppsett på flere sider. Når du publiserer et forhåndsinnstilt oppsett, må du være oppmerksom på at du kan påvirke oppsettet på flere sider.

## <a name="rename-a-preset-layout"></a>Gi nytt navn til et forhåndsinnstilt oppsett

Hvis du vil gi et nytt navn til et forhåndsinnstilt oppsett i områdebygger, følger du denne fremgangsmåten.

1. Velg **Oppsett** i navigasjonsruten til venstre.
1. Velg navnet på oppsettet du vil gi nytt navn til.
1. Velg **Rediger** for å begynne å redigere oppsettet.
1. Velg pennesymbolet ved siden av navnet på oppsettet i egenskapsruten.
1. Rediger navnet på oppsettet etter behov.
1. Merk av for å bekrefte navneendringen.
1. Velg **Fullfør redigering**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med maler](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
