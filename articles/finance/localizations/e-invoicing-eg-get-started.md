---
title: Komme i gang med Elektronisk fakturering for Egypt
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Egypt i Finance and Supply Chain Management.
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 03ccc18d4c767dbb2a314e2eb1076b1c6e9019e991c6de3fc80be65d765fdd36
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758806"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Komme i gang med Elektronisk fakturering for Egypt

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Egypt. Emnet veileder deg gjennom konfigurasjonstrinnene som er landavhengige i RCS (Regulatory Configuration Services), og utfyller trinnene som beskrives i [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering for egyptisk elektronisk faktura (EG)

Noen av parameterne fra funksjonen **Elektronisk fakturering for egyptisk (EG)** publiseres med standardverdier. Gå gjennom og oppdater om nødvendig verdiene slik at bedre gjenspeiler forretningsoperasjonen din, før du distribuerer funksjonen for elektronisk fakturering til servicemiljøet.

Denne delen utfyller delen **Landspesifikk konfigurasjon for funksjon for elektronisk fakturering** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre prosedyren i denne delen, må du:

- Opprette en digital sertifikathemmelighet, som beskrevet i delen **Opprett digital sikkerhetshemmelighet** i [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md). Av testformål gir skattemyndigheten spesifikke testinfraktsertifikater som bare må brukes under test- og løsningsvalideringsfaser. Hvis du vil ha mer informasjon, kan du se nettstedet til de egyptiske skattemyndighetene ved hjelp av koblingen [SDK for egyptisk e-fakturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **egyptisk elektronisk faktura (EG)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. Velg oppsett for funksjonen **Salgsfaktura** i rutenettet i fanen **Oppsett**.
5. Velg **Rediger**, og i feltgruppen **Handlinger** i fanen **Handlinger** velger du **Signer JSON-dokument for egyptisk skattemyndighet**.
6. I feltgruppen **Parametere** velger du parameteren, **Sertifikatnavn** og deretter navnet på det digitale sertifikatet som er opprettet for bruk med funksjonen for elektronisk fakturering.
7. I feltgruppen **Handlinger** velger du **Integrer med egyptisk ETA-tjeneste**. Gjenta dette trinnet for de to forekomstene av denne handlingen.
8. I feltgruppen **Parametere** velger du **URL for webtjeneste** og **URL for påloggingstjeneste** og, om nødvendig, går gjennom URL-parameterne. Gå til nettstedet til de egyptiske skattemyndighetene for å finne URL-adressen til testing og produksjon ved hjelp av koblingen [SDK for egyptisk e-fakturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Velg **Lagre** og lukk siden.
10. Hvis du vil distribuere funksjonen for elektronisk fakturering til servicemiljøet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsettet for funksjon for elektronisk fakturering for egyptisk elektronisk faktura (EG)

Fullfør disse trinnene før du distribuerer programoppsettet til det tilkoblede programmet i Finans eller Supply Chain Management.

Denne delen utfyller delen **Landspesifikk konfigurasjon for programoppsett** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **egyptisk elektronisk faktura (EG)**, er valgt.
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
14. Hvis du vil distribuere programoppsettet til det tilkoblede programmet i Finans eller Supply Chain Management , kan du se [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Personvernerklæring

Aktivering av funksjonen for **egyptisk elektronisk faktura (EG)** krever kanskje å sende begrensede data, inkludert registrerings-IDen for organisasjonen. Disse dataene vil bli overført til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. En administrator kan aktivere og deaktivere funksjonen ved å gå til **Organisasjonsstyring** > **Oppsett** > **Parametere for elektronisk dokument**. I fanen **Funksjoner** velger du raden som inneholder funksjonen **Egyptisk elektronisk faktura (EG)**, og deretter foretar du det riktige valget. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md)
- [Elektroniske fakturaer for kunde i Egypt](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
