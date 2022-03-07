---
title: Komme i gang med Elektronisk fakturering
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med Elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 3a62f68718a9bd46cdf15146bbb6a4e5166bfcc7abcf99b24d3fbc7e3e6c94ab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732987"
---
# <a name="get-started-with-electronic-invoicing"></a>Komme i gang med Elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering. Dette emnet leder deg gjennom de vanlige konfigurasjonstrinnene i RCS (Regulatory Configuration Services) og Dynamics 365 Finance, og beskriver trinnene du må følge for å sende forretningsdokumenter og gjennomgå behandlingsresultatene.

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:

- Konfigurer Microsoft Dynamics Lifecycle Services (LCS), RCS (Regulatory Configuration Service) og Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljøet ditt. Hvis du vil ha mer informasjon, kan du se [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Opprett en konfigurasjonsleverandør for organisasjonen. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importere en funksjon for elektronisk fakturering fra Microsoft-konfigurasjonsleverandøren 

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Velg **Importer**, og velg deretter **Synkroniser**.
4. Filtrer **Konfigurasjonsleverandør**-kolonnen etter termen **Microsoft**.
5. Velg navnet på en funksjon for elektronisk fakturering fra tabellen i begynnelsen av dette emnet, og velg deretter **Importer**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Opprette en funksjon for Elektronisk fakturering under organisasjonsleverandøren

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. Velg **Legg til** > **Basert på eksisterende funksjon**, og i feltet **Navn** angir du navnet på funksjonen for Elektronisk fakturering.
3. I **Beskrivelse**-feltet skriver du inn en beskrivelse av funksjonen.
4. I **Basefunksjonsfeltet** velger du den importerte funksjonen for elektronisk fakturering fra Microsofts konfigurasjonsleverandør.
5. Velg **Opprett funksjon**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering

Avhengig av landet eller området kan det hende at funksjonen for Elektronisk fakturering krever spesifikk konfigurasjon. 

Hvis du vil ha mer informasjon om disse trinnene, kan du se i "Komme i gang"-dokumentasjonen som er tilgjengelig for landet eller området ditt.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Importer konfigurasjoner av modelltilordning fra elektronisk rapportering

1. Velg arbeidsområdet **Elektronisk rapportering** i RCS.
2. Fra listen over **Microsoft**-konfigurasjonsleverandører velger du **Repositorier**.
3. Velg **Globalt**, og velg deretter **Åpne** i handlingsruten.
4. Importer modelltilordningskonfigurasjonene i henhold til følgende tabell etter funksjonsnavn.

| Funksjonsnavn                         | Modelltilordningskonfigurasjon |
|--------------------------------------|-----------------------------|
| Østerrikske elektroniske fakturaer (AT)    | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Belgisk elektronisk faktura (BE)      | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Brasiliansk NF-e (BR)                  | <p>Kontekstmodell for kundefaktura</p><p>Regnskapsdokumenter</p><p>Svarmeldingsmodell</p> |
| Brasiliansk NFS-e ABRASF Curitiba (BR) | <p>Kontekstmodell for kundefaktura</p><p>Regnskapsdokumenter</p><p>Svarmeldingsmodell</p> |
| Dansk elektronisk faktura (DK)       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Egyptisk elektronisk faktura (EG)     | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p><p>Svarmeldingsmodell</p> |
| Estisk elektronisk faktura (EE)     | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Finsk elektronisk faktura (FI)       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Fransk elektronisk faktura (FR)       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Tysk elektronisk faktura (DE)       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| FatturaPA (IT)                       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Meksikansk CFDI Interfactura (MX)       | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p><p>Svarmeldingsmodell</p> |
| Nederlandsk elektronisk faktura (NL)        | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Norsk elektronisk faktura (NO)    | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Spansk elektronisk faktura (ES)      | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |
| Elektronisk faktura i PEPPOL-format            | <p>Kontekstmodell for kundefaktura</p><p>Fakturamodell</p> |


## <a name="configure-the-application-setup"></a>Konfigurere programoppsettet

1. Velg funksjonen for Elektronisk fakturering som du opprettet.
2. Velg **Programoppsett** i kategorien **Oppsett**.
3. Velg tilkoblingen som er knyttet til forekomsten av Finance eller Supply Chain Management i feltet **Koble til program**.
4. I delen **Elektroniske dokumenttyper** velger du **Legg til**.
5. Velg og angi en verdi for **Tabellnavn** i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Tabellnavn |
    |--------------------------------------|-------------------|------------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | Regnskapsdokument |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste | Regnskapsdokument |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Kundefakturajournal |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |

7. For hvert tabellnavn du oppretter, velger og angir du en kontekstverdi i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Kontekst |
    |--------------------------------------|-------------------|---------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | <p>Kontekstmodell for kundefaktura – regnskapsdokumentkontekst</p><p>Kontekstmodell for kundefaktura – FD-korreksjonsbrevkontekst</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste| Kontekstmodell for kundefaktura – regnskapsdokumentkontekst |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Kontekstmodell for kundefaktura – kundefakturakontekst |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |

8. For hvert taballnavn og kontekst velger og angir du en verdi for tilordning av forretningsdokument i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Tilordning av forretningsdokument |
    |--------------------------------------|-------------------|---------------------------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | <p>Regnskapsdokumenttilordning – regnskapsdokumenttilordning</p><p>Regnskapsdokumenttilordning – korreksjonsbrevtilordning</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste | Regnskapsdokumenttilordning – regnskapsdokumenttilordning |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Fakturamodelltilordning – kundefaktura |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Landspesifikk konfigurasjon av programoppsett

Avhengig av landet eller området kan det hende at programoppsettet krever spesifikk konfigurasjon. 

Hvis du vil ha mer informasjon om disse trinnene, kan du se i "Komme i gang"-dokumentasjonen som er tilgjengelig for landet eller området ditt.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Distribuere funksjonen for elektronisk fakturering til servicemiljø

1. Velg versjonen av funksjonen for Elektronisk fakturering du vil distribuere, i kategorien **Versjoner**.
2. Velg **Endre status** \> **Fullført**.
3. Velg **Endre status** \> **Publiser**.
4. Velg **Distribuer**.
5. Sett alternativet **Distribuer til tilkoblet program** til **Nei**.
6. Sett alternativet **Distribuer til servicemiljø** til **Ja**.
7. I feltet **Servicemiljø** velger du servicemiljøet for Elektronisk fakturering der du vil distribuere funksjonen for Elektronisk fakturering.
8. I **Fra dato**-feltet velger du datoen da funksjonen for Elektronisk fakturering må bli gyldig i Elektronisk fakturering.
9. Velg **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Distribuere funksjonen for elektronisk fakturering til et tilkoblet program

1. Velg en versjon av funksjonen for Elektronisk fakturering du vil distribuere, i kategorien **Versjoner**.
4. Velg **Distribuer**.
5. Sett alternativet **Distribuer til tilkoblet program** til **Ja**.
6. Velg tilkoblingen som er knyttet til forekomsten av Finance eller Supply Chain Management i feltet **Koble til program**.
7. Sett alternativet **Distribuer til servicemiljø** til **Nei**.
10. Velg **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Slå på funksjonen for Elektronisk fakturering i Finance eller Supply Chain Management

1. Logg deg på Finans eller Supply Chain Management, og kontroller at du er i riktig juridisk enhet.
2. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Parametere for elektronisk dokument**.
3. I fabeb **Funksjoner** velger du den land-/områdespesifikke funksjonen for å aktivere funksjonen for elektronisk fakturering for Finance eller Supply Chain Management. Følgende tabell inneholder en liste over funksjonene for elektronisk fakturering som er tilgjengelige for bestemte land/områder. 

    | Funksjonsnavn                                          | Land/område  |
    |-------------------------------------------------------|-----------------|
    | Østerrikske elektroniske fakturaer (AT)                     | Østerrike         |
    | Belgisk elektronisk faktura (BE)                       | Belgia         |
    | CFDI Meksikansk elektronisk faktura (MX)                  | Mexico          |
    | Dansk elektronisk faktura (DK)                        | Danmark         |
    | Nederlandsk elektronisk faktura (NL)                         | Nederland |
    | Egyptisk elektronisk faktura (EG)                      | Egypt           |
    | Estisk elektronisk faktura (EE)                      | Estland         |
    | Finsk elektronisk faktura (FI)                       | Finland         |
    | Fransk elektronisk faktura (FR)                        | Frankrike          |
    | Tysk elektronisk faktura (DE)                        | Tyskland         |
    | Italiensk elektronisk faktura (IT)                       | Italia           |
    | NF-e Føderal – Brasiliansk elektronisk faktura (BR)      | Brasil          |
    | NFS-e – Elektronisk faktura for brasiliansk tjeneste (by)   | Brasil          |
    | Norsk elektronisk faktura (NO)                     | Norge          |
    | Elektronisk faktura i PEPPOL-format                             | Globalt          |
    | Spansk elektronisk faktura (ES)                       | Spania           |

4. Velg **Lagre**.

## <a name="issue-electronic-invoices"></a>Utstede elektroniske fakturaer

1. Gå til **Organisasjonsstyring** \> **Periodiske** \> **Elektroniske dokumenter** \> **Send elektroniske dokumenter**.
2. Velg **Filtrer** i hurtigfanen **Post som skal inkluderes** .
3. Velg **Legg til** for å legge til et tabellnavn i spørringsfilteret.
4. Velg tabellen som inneholder fakturaene.

    > [!NOTE]
    > Tabellnavnet må vises i tabellen i delen [Konfigurere programoppsettet](#configure-the-application-setup) tidligere i dette emnet.

5. Velg feltnavnet fra tabellen du vil spørre.
6. Angi tabellnavnet og feltnavnet for kriteriene du skal spørre på.
7. Gjenta trinn 5 og 6 hvis du vil legge til flere felt og kriterier i spørringen, og velg deretter **OK**.
8. Velg **OK**.

## <a name="view-submission-logs"></a>Vise sendelogger

1. Gå til **Organisasjonsstyring** \> **Periodisk** \> **Elektroniske dokumenter** \> **Sendingslogg for elektronisk dokument**.
2. Velg tabellen som inneholder fakturaene, i **Dokumenttype**-feltet.

    > [!NOTE]
    > Tabellnavnet må vises i tabellen i delen [Konfigurere programoppsettet](#configure-the-application-setup) tidligere i dette emnet.

3. Velg en faktura i rutenettet, og velg deretter **Forespørsel om** \> **Innsendingsdetaljer**.


## <a name="related-topics"></a>Relaterte emner

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering for Brasil](e-invoicing-bra-get-started.md)
- [Komme i gang med Elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Komme i gang med Elektronisk fakturering for Italia](e-invoicing-ita-get-started.md)
- [Elektroniske fakturaer for kunde i Egypt](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
