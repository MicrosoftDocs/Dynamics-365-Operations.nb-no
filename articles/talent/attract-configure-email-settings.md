---
title: Konfigurere e-postinnstillinger i Microsoft Dynamics 365 for Talent - Attract
description: Dette emnet beskriver hvordan konfigurerer innstillinger for e-post som sendes av Microsoft Dynamcis 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 360937b807ea149edb2f16ad6799d74791d599b5
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729795"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-for-talent---attract"></a>Konfigurere e-postinnstillinger i Microsoft Dynamics 365 for Talent - Attract
[!include[banner](../includes/banner.md)]

Varemerket ditt vekker tillit og hjelper deg å utvikle et forhold til kandidater selv før de søker på stillinger. Positive oppfatninger av varemerket tiltrekker de største talentene og øker lojaliteten til eksisterende ansatte. Microsoft Dynamics 365 for Talent: Attract gjør at du kan konfigurere e-postmeldinger slik at de gjenspeiler firmaets varemerke. Derfor kan du gi jobbkandidater en konsekvent opplevelse etter hvert som de går gjennom søknadsprosessen.

Med Attract kan du utføre følgende handlinger:

- Konfigurer e-postinnstillinger slik at firmaets e-posttjenestekonto i Microsoft Exchange brukes. På denne måten vet kandidater at e-postmeldingene kommer fra firmaet. Du kan for eksempel konfigurere innstillingene slik at kandidater mottar e-postmeldinger fra `recruiting@contoso.com` i stedet for `contoso@microsoft.com`.
- Opprett konsekvent varemerking for alle e-postmeldingene ved å angi en global topptekst og bunntekst for e-postmaler. 

> [!NOTE]
> Hvis du vil konfigurere Attract slik at det bruker firmaets e-posttjenestekonto til å sende e-post, trenger du tillegget for omfattende ansettelse.

## <a name="connect-an-email-service-account"></a>Koble til en e-posttjenestekonto

Når du kobler til firmaets e-posttjenestekonto, kan du skape en varemerket e-postopplevelse for jobbkandidatene. Hvis du ikke kobler til firmakontoen, bruker Attract den standard Microsoft-varemerkede e-posttjenestekontoen.

1. Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.
2. Velg **Koble til en firmakonto** under **E-posttjenestekontoer** i fanen **E-postinnstillinger**.

    ![Koble til firmaets e-posttjenestekonto i Attract](./media/attract-admin-email-service-accounts.png)

    Hvis du vil ha mer informasjon om hvordan du oppretter en delt e-postkonto, kan du se [Delte postbokser i Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. I påloggingsvinduet for Microsoft logger du på ved å bruke firmalegitimasjonen.
4. Hvis du ikke har konfigurert en e-posttjenestekonto, eller hvis du vil legge til en ny, velger du **Legg til ny tjenestekonto**, og angi deretter e-postinformasjonen. Hvis du allerede har konfigurert e-posttjenestekontoen du vil bruke, velger du den.

Når e-posttjenestekontoen er konfigurert, vises den under **E-posttjenestekontoer**.

## <a name="disconnect-an-email-service-account"></a>Koble fra en e-posttjenestekonto

Hvis du vil slutte å bruke firmaets domene i e-postkommunikasjon via Attract, kan du koble fra en e-posttjenestekonto.

1. Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.
2. Under **posttjenestekontoer** i fanen **E-postinnstillinger** velger du **Mer**-knappen (tre loddrette prikker) ved siden av e-posttjenestekontoen du vil koble fra.
3. Velg **Koble fra e-postkonto**.

    ![Koble fra firmaets e-posttjenestekonto](./media/attract-admin-disconnect-email-account.png)

4. Når du blir bedt om å bekrefte operasjonen, velger du **Koble fra**.

    ![Bekrefte frakoblingen av firmaets e-posttjenestekonto](./media/attract-admin-email-confirm-disconnect.png)

Hvis du ikke kobler til en annen e-posttjenestekonto, bruker e-postmeldinger som sendes fra Attract, den standard Microsoft-varemerkede e-posttjenestekontoen.

## <a name="configure-email-template-settings"></a>Konfigurere innstillinger for e-postmal

Du kan laste opp et bilde av firmaets logo og annen informasjon som en varemerket topptekst for e-postmeldingene. Du kan også ha koblinger til personvernpolicy og vilkår for bruk i bunntekst i e-post.

> [!NOTE]
> Du må overholde alle gjeldende lover i landet eller området ditt samt landet eller området som styrer e-postmottakeren. Disse lovene omfatter forskrifter for søppelpost.

1. Velg **Innstillinger** (tannhjulsikonet i øvre høyre hjørne), og velg deretter **Administrasjonssenter**.
2. Under **Innstillinger for e-postmal** i fanen **postinnstillinger** drar du bildet du vil bruke som topptekst i e-postmeldinger, til bildeboksen, eller du klikker i bildeboksen for å bla gjennom etter filen. Hvis du vil erstatte et eksisterende bilde, må du først velge **Fjern** ved siden av det. Bildet må være en JPEG-, JPG-, PNG- eller SVG-fil. Den anbefalte størrelsen for bilder er mellom 25 og 800 piksler bredt og mellom 25 og 150 piksler høyt. Den maksimale filstørrelsen for toppteksten er 1 megabyte (MB).

    ![Legge til et bilde for firmaets topptekst i e-postmeldinger](./media/attract-admin-email-header.png)

3. Under **Din personvernerklæring for kommunikasjon** kan du oppgi en kobling til firmaets personvernpolicy. Under **Dine vilkår og betingelser for kommunikasjon** kan du angi en kobling til firmaets vilkår for bruk.

    ![Legge til koblinger i firmaets personvernpolicy og vilkår for bruk for bunnteksten i e-postmeldinger](./media/attract-admin-email-footer.png)

4. Velg **Lagre** for å lagre innstillingene for e-postmal.
