---
title: Elektronisk fakturering for Egypt
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med Elektronisk fakturering for Egypt i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
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
ms.openlocfilehash: e21c4ce4d676c3194665672a078dc1e3d0492799
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661729"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektronisk fakturering for Egypt

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Egypt. Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Service (RCS). Denne fremgangsmåten utfyller fremgangsmåten som beskrives i [Definere elektronisk fakturering](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Forutsetninger

Før du begynner fremgangsmåtene i dette emnet, må følgende forutsetninger være fullført:

- Gjør deg kjent med elektronisk fakturering slik det beskrives i [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md).
- Registrer deg for RCS, og definer elektronisk fakturering. Hvis du vil ha mer informasjon, kan du se følgende emner:

    - [Registrere deg for og installere tjenesten for elektronisk fakturering](e-invoicing-sign-up-install.md)
    - [Konfigurere Azure-ressurser for elektronisk fakturering](e-invoicing-set-up-azure-resources.md)
    - [Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktiver integreringen mellom programmet Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management og tjenesten for elektronisk fakturering slik det beskrives i [Aktivere og konfigurere integrering med elektronisk fakturering](e-invoicing-activate-setup-integration.md).
- Opprett en hemmelighet for digitalt sertifikat i Azure Key Vault, og konfigurer den som beskrevet i [Kundesertifikater og -hemmeligheter](e-invoicing-customer-certificates-secrets.md). Av testformål gir skattemyndigheten spesifikke testinfraktsertifikater som bare må brukes under test- og løsningsvalideringsfaser. Hvis du vil ha mer informasjon, kan du gå til nettstedet til de egyptiske skattemyndighetene ved hjelp av koblingen som er oppgitt i [SDK for egyptisk e-fakturering](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Landspesifikk konfigurasjon for funksjonen for egyptisk elektronisk faktura (EG)

Noen av parameterne fra den elektroniske faktureringsfunksjonen **Egyptisk elektronisk faktura (EG)** publiseres med standardverdier. Før du ruller ut den elektroniske faktureringsfunksjonen til tjenestemiljøet, går du gjennom standardverdiene og oppdaterer dem etter behov, slik at de bedre gjenspeiler forretningsoperasjonen.

1. Importer den nyeste versjonen av globaliseringsfunksjonen **Egyptisk elektronisk faktura (EG)** som beskrevet i [Importere funksjoner fra det globale repositoriet](e-invoicing-import-feature-global-repository.md).
2. Opprett en kopi av den importerte globaliseringsfunksjonen, og velg konfigurasjonsleverandøren for den, som beskrevet i [Opprette en globaliseringsfunksjon](e-invoicing-create-new-globalization-feature.md).
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. Velg konfigurasjonen for funksjonen **Salgsfaktura avledet** i rutenettet i **Konfigurasjoner**-fanen.
5. Velg **Rediger**.
6. Velg **Signer JSON-dokument for egyptiske skattemyndigheter** i delen **Datasamlebånd for behandling** i fanen **Datasamlebånd for behandling**.
7. Velg **Sertifikatnavn** i **Parametere**-delen, og velg deretter navnet på det digitale sertifikatet du opprettet.
8. I delen **Datasamlebånd for behandling** velger du **Integrer med egyptisk ETA-tjeneste**. Gjenta dette trinnet for de to forekomstene av denne handlingen.
9. Velg **Nettadresse for nettjeneste** og **Nettadresse for tjenestepålogging** i **Parametere**-delen. Gå deretter gjennom parameterne for nettadresse. Gå til nettstedet til de egyptiske skattemyndighetene for å få nettadressen til testing og produksjon ved hjelp av koblingen som er oppgitt i [SDK for egyptisk e-fakturering](https://sdk.invoicing.eta.gov.eg/faq/).
10. Velg **Lagre**, og lukk siden.
11. Gjenta trinn 4 til og med 10 for konfigurasjonen for funksjonen **Prosjektfaktura avledet**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Landspesifikk konfigurasjon for programmet Egyptisk elektronisk faktura (EG)

Det finnes parametere som må defineres i Finance- eller Supply Chain Management-miljøet. Du kan fullføre denne konfigurasjonen på ett av to steder:

- Direkte i Finance- eller Supply Chain Management-miljøet. Hvis du vil ha mer informasjon, kan du se [Konfigurere parametere for elektronisk fakturering](e-invoicing-set-up-parameters.md).
- I RCS. Når det gjelder konfigurasjon av funksjonen for elektronisk fakturering, kan du definere alle parametere og deretter rulle dem direkte ut til Finance- eller Supply Chain Management-miljøet når du ruller ut funksjonen for elektronisk fakturering.

Parameterne er de samme for begge alternativene. Hvis du konfigurerer den første funksjonen i tjenesten for elektronisk fakturering, anbefaler vi at du følger disse trinnene for å konfigurere parameterne i RCS og deretter rulle dem ut til det tilkoblede programmet.

> [!NOTE]
> Enkelte versjoner av funksjonen for elektronisk fakturering kan inneholde et forhåndsdefinert sett med programspesifikke parametere for Finance eller Supply Chain Management. I dette tilfellet bør du kontrollere at dataene er riktige. Ellers angir du parameterne manuelt.

1. Finn kopien av globaliseringsfunksjonen **Egyptisk elektronisk faktura (EG)** du opprettet.
2. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
3. Velg **Programoppsett** i kategorien **Oppsett**.
4. Velg programmet der du vil rulle ut parameterne, i **Tilkoblede programmer**.
5. Velg **Legg til** på siden **Elektroniske dokumenttyper** for å opprette en post.
6. Legg til **CustInvoiceJour** i **Tabellnavn**-feltet.
7. Legg til en referanse til tilordningsnavnet **Kundefakturakontekst** i **Kontekst**-feltet. Konfigurasjonen er **Kontekstmodell for kundefaktura**.
8. Legg til en referanse til tilordningsnavnet **Kundefakturakontekst** i feltet **Tilordning av elektronisk dokument**. Konfigurasjonen er **Fakturamodelltilordning**.
9. Velg **Lagre**.
10. Velg **Legg til** på **Svartyper**-siden.
11. I feltet **Svartype** angir du **Svar**.
12. I **Beskrivelse**-feltet angir du **Prosessvar**.
13. I feltet for **innsendingsstatus** velger du **Venter**.
14. Velg **Import av svarmelding** i feltet **Modelltilordning**. Konfigurasjonen er **Import av svarmelding for Egypt (EG)**.
15. Velg **Lagre**.
16. Velg **Legg til**.
17. I feltet **Svartype** angir du **ResponseData**.
18. I **Beskrivelse**-feltet angir du **Prosessvardata**.
19. I feltet for **innsendingsstatus** velger du **Venter**.
20. I feltet **Navn på dataenhet** velger du **SalesInvoiceHeaderV2Entity**.
21. Velg **Import av svardata** i feltet **Modelltilordning**. Konfigurasjonen er **Format for import av svardata for Egypt (EG)**.
22. Velg **Lagre**, og lukk siden.
23. Lukk siden.

Hvis du vil rulle ut en funksjon til tjenestemiljøet og en programkonfigurasjon til programmet som er koblet til Finance eller Supply Chain Management, kan du se [Fullføre, publisere og rulle ut en globaliseringsfunksjon](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Personvernerklæring

Hvis du aktiverer funksjonen **Egyptisk elektronisk faktura (EG)**, kan det hende at det må sendes begrensede data. Disse dataene inkluderer organisasjonens avgiftsregistrerings-ID. Dataene vil bli overført til tredjepartsleverandører som har blitt autorisert av skattemyndigheten til å sende elektroniske fakturaer til denne skattemyndigheten i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes nettjeneste. En administrator kan aktivere og deaktivere funksjonen ved å gå til **Organisasjonsstyring** \> **Oppsett** \> **Parametere for elektronisk dokument**. I fanen **Funksjoner** velger du raden som inneholder funksjonen **Egyptisk elektronisk faktura (EG)**, og deretter foretar du det riktige valget. Data som importeres fra eksterne systemer til denne Dynamics 365-nettjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delen «Personvernerklæring» i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md)
- [Elektroniske fakturaer for kunde i Egypt](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
