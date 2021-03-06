---
title: Opprett en Azure Storage-konto og en Key Vault
description: Dette emnet forklarer hvordan du oppretter en Azure Storage-konto og en Key Vault.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963245"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Opprett en Azure Storage-konto og en Key Vault

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet, må du sørge for at følgende oppgaver er fullført:

- Opprette en nøkkelhvelvressurs i Azure. Hvis du vil ha mer informasjon om mål, se [Om Azure Key Vault](/azure/key-vault/general/overview).
- Opprett en Azure Storage-konto (Blob Storage). Hvis du vil ha mer informasjon, se [Vedlikeholde Azure Storage-konto](/azure/storage/blobs/).

## <a name="overview"></a>Oversikt

I dette emnet fullfører du to hovedtrinn:

- Konfigurer Azure Storage-kontoen for å hente URI for lagringskonto.
- Konfigurer Key Vault for å lagre lagringskonto-URIen.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Konfigurere Azure Storage-kontoen for å hente URIen for lagringskonto

1. Åpne lagringskontoen du har tenkt å bruke med elektronisk fakturering.
2. Gå til **Blob service** \> **Containere**, og opprett en ny container.
3. Angi et navn på beholderen, og sett feltet **Offentlig tilgangsnivå** til **Privat (ingen anonym tilgang)**.
4. Åpne beholderen, og gå til **Innstillinger \> Tilgangspolicy**.
5. Velg **Legg til policy** for å legge til en lagret tilgangspolicy.
6. Angi feltene **Identifikator** og **Tillatelser** etter behov. I **Tillatelser**-feltet må du velge alle tillatelser.

    ![Gi tillatelse til Blob Storage](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Angi start- og utløpsdatoer. Utløpsdatoen må være i fremtiden.
8. Velg **OK** for å lagre policyen, og lagre endringene i containeren.
9. Gå tilbake til lagringskontoen, og åpne **Lagringsutforsker (forhåndsversjon)**.
10. Høyreklikk containeren, og velg deretter **Hent delt tilgangssignatur**.
11. I dialogboksen **Delt tilgangssignatur** kopierer og lagrer du verdien i **URI**-feltet. Denne verdien brukes i den neste prosedyren og refereres til som *URI for delt tilgangssignatur*.

    ![Velge og kopiere URI-verdien](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Konfigurere Key Vault for å lagre lagringskonto-URIen

1. Åpne Key Vault du har tenkt å bruke med elektronisk fakturering.
2. Gå til **Innstillinger** \> **Hemmeligheter**, og velg deretter **Generer/Importer** for å opprette en ny hemmelighet.
3. På siden **Opprett en hemmelig**, i feltet **Opplastingsalternativer**, velger du **Manuell**.
4. Angi navnet på hemmeligheten. Dette navnet vil bli brukt under installasjonen av tjenesten i RCS (Regulatory Configuration Service) og refereres til som *hemmelig Key Vault-navn*.
5. I **Verdi**-feltet velger du **URI for delt tilgangssignatur**, og deretter velger du **Opprett**.
6. Angi at tilgangspolicyen skal gi elektronisk fakturering det riktige nivået for sikker tilgang til hemmeligheten du opprettet. Gå til **Innstillinger \> Tilgangspolicy**, og velg **Legg til tilgangspolicy**.
7. Angi de hemmelige tillatelsene for **Hente**- og **Liste**-operasjonene.

    ![Gi tjenestetilgang](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Angi sertifikattillatelsene for **Hent**- og **Liste**-operasjonene.

    ![Gi sertifikattillatelse](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. I feltet **Velg sikkerhetskontohaver** velger du **Ingen valgt**.
10. I dialogboksen **Sikkerhetskontohaver** velger du sikkerhetskontohaveren ved å legge til **E-faktureringstjeneste**.
11. Velg **Legg til**, og velg deretter **Lagre Key Vault-endringer**.
12. På siden **Oversikt** kopierer du **DNS-navn**-verdien for Key Vault. Denne verdien vil bli brukt under konfigurasjon av tjenesten i RCS, og vil bli referert til som *Key Vault-URI*.

> [!NOTE]
> Hvis du vil ha mer sikkerhet på lagringskontoen, konfigurerer du Azure Defender for Storage.
> 
> Hvis du vil ha mer informasjon, kan du se [Innføring i Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
