---
title: Komme i gang med Elektronisk fakturering-tillegget for Egypt
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Egypt i Finance and Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592604"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Komme i gang med Elektronisk fakturering-tillegget for Egypt

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Egypt. Emnet veileder deg gjennom konfigurasjonstrinnene som er landavhengige i RCS (Regulatory Configuration Services), og utfyller trinnene som beskrives i emnet [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering for egyptisk elektronisk faktura (EG)

Det er noen trinn som skal fullføres for å konfigurere funksjonen for elektronisk fakturering for egyptisk elektronisk faktura (EG). Noen av parameterne fra konfigurasjonene publiseres med standardverdier, så de må gjennomgås og oppdateres slik at de passer bedre til forretningsoperasjonen.

### <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre prosedyren i denne delen, må du:

- Opprette en digital sertifikathemmelighet, som beskrevet i delen **Opprett digital sikkerhetshemmelighet** i [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md). Av testformål gir skattemyndigheten spesifikke testinfraktsertifikater som bare må brukes under test- og løsningsvalideringsfaser. Hvis du vil ha mer informasjon, kan du se nettstedet til de egyptiske skattemyndighetene ved hjelp av koblingen [SDK for egyptisk e-fakturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Opprette en egyptisk elektronisk faktura (EG) Funksjon for elektronisk fakturering for organisasjonen, som beskrevet i delen **Opprette en funksjon for elektronisk fakturering under organisasjonsleverandøren** i [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **egyptisk elektronisk faktura (EG)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. Velg oppsett for funksjonen **Salgsfaktura** i rutenettet i fanen **Oppsett**.
5. Velg **Rediger**, og i feltgruppen **Handlinger** i fanen **Handlinger** velger du **Signer JSON-dokument for egyptisk skattemyndighet**.
6. I feltgruppen **Parametere** velger du parameteren, **Sertifikatnavn** og deretter navnet på det digitale sertifikatet som er opprettet for bruk med funksjonen for elektronisk fakturering.
7. I feltgruppen **Handlinger** velger du **Integrer med egyptisk ETA-tjeneste**. Gjenta dette trinnet for de to forekomstene av denne handlingen.
8. I feltgruppen **Parametere** velger du **URL for webtjeneste** og **URL for påloggingstjeneste** og, om nødvendig, går gjennom URL-parameterne. Gå til nettstedet til de egyptiske skattemyndighetene for å finne URL-adressen til testing og produksjon ved hjelp av koblingen [SDK for egyptisk e-fakturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Velg **Lagre** og lukk siden.
10. Hvis du vil konfigurere programoppsettet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsettet for funksjon for elektronisk fakturering for egyptisk elektronisk faktura (EG)

Konfigurasjonen av programoppsettet for funksjon for elektronisk fakturering for **egyptisk elektronisk faktura (EG)** krever at bestemte trinn utføres. Du må utføre de trinnene før du distribuerer funksjonen for elektronisk fakturering til tilleggsmiljøet for elektronisk fakturering.

### <a name="prerequisites"></a>Forutsetninger

Før du fullfører prosedyren i denne delen, oppretter og starter du en funksjon for elektronisk fakturering for **egyptisk elektronisk faktura (EG)** for å konfigurere programoppsettet for funksjonen for elektronisk fakturering for **egyptisk elektronisk faktura (EG)**, som beskrevet i delen **Konfigurere programoppsettet** i emnet [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **egyptisk elektronisk faktura (EG)**, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. I fanen **Oppsett** velger du **Programopsett**, og i feltet **Tilkoblet program** velger du programmet der du vil distribuere.
5. I feltet **Tabellnavn** kontrollerer du at kundens fakturajournal er valgt.
6. Velg **Svartyper**, og velg deretter **Ny**.
7. I feltet **Svartype** angir du "Svar", og i feltet **Beskrivelse** skriver du inn "Beskrivelse".
8. I feltet for **innsendingsstatus** velger du **Venter**.
9. I feltet **Modelltilordning** velger du **Modelltilordning fra svarmelding** med **(Forhåndsversjon) Format for import av svarmelding**, og deretter velger du **Lagre**.
10. Velg **Ny**, og i feltet **Svartype** angir du "Svardata" som en fast verdi. Angi "Beskrivelse" i feltet **Beskrivelse**.
11. I feltet for **innsendingsstatus** velger du **Venter**.
12. I feltet **Navn på dataenhet** velger du **Salgsfakturahoder V2**.
13. I feltet **Modelltilordning** velger du **Import av egyptiske svardata** med **(Forhåndsversjon) Import av egyptiske svardata**, og deretter velger du **Lagre**.
14. Hvis du vil distribuere funksjonen for elektronisk fakturering, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Personvernerklæring

Aktivering av funksjonen for **egyptisk elektronisk faktura (EG)** krever kanskje å sende begrensede data, inkludert registrerings-IDen for organisasjonen. Disse dataene vil bli overført til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. En administrator kan aktivere og deaktivere funksjonen ved å gå til **Organisasjonsstyring** > **Oppsett** > **Parametere for elektronisk dokument**. I fanen **Funksjoner** velger du raden som inneholder funksjonen **Egyptisk elektronisk faktura (EG)**, og deretter foretar du det riktige valget. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over tillegg for elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering-tillegget](e-invoicing-get-started.md)
- [Elektroniske fakturaer for kunde i Egypt](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
