---
title: Opprett en Azure Storage-konto og en Key Vault
description: Dette emnet forklarer hvordan du oppretter en Azure Storage-konto og en Key Vault.
author: gionoder
ms.date: 02/12/2021
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
ms.openlocfilehash: b7df4933c1373893e00f48ea3a21bd5af40719a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840226"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="5c697-103">Opprett en Azure Storage-konto og en Key Vault</span><span class="sxs-lookup"><span data-stu-id="5c697-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="5c697-104">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="5c697-104">Prerequisites</span></span>

<span data-ttu-id="5c697-105">Før du kan fullføre trinnene i dette emnet, må du sørge for at følgende oppgaver er fullført:</span><span class="sxs-lookup"><span data-stu-id="5c697-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="5c697-106">Opprette en nøkkelhvelvressurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="5c697-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="5c697-107">Hvis du vil ha mer informasjon om mål, se [Om Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="5c697-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="5c697-108">Opprett en Azure Storage-konto (Blob Storage).</span><span class="sxs-lookup"><span data-stu-id="5c697-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="5c697-109">Hvis du vil ha mer informasjon, se [Vedlikeholde Azure Storage-konto](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="5c697-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="5c697-110">Oversikt</span><span class="sxs-lookup"><span data-stu-id="5c697-110">Overview</span></span>

<span data-ttu-id="5c697-111">I dette emnet fullfører du to hovedtrinn:</span><span class="sxs-lookup"><span data-stu-id="5c697-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="5c697-112">Konfigurer Azure Storage-kontoen for å hente URI for lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="5c697-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="5c697-113">Konfigurer Key Vault for å lagre lagringskonto-URIen.</span><span class="sxs-lookup"><span data-stu-id="5c697-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="5c697-114">Konfigurere Azure Storage-kontoen for å hente URIen for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="5c697-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="5c697-115">Åpne lagringskontoen du har tenkt å bruke med elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="5c697-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="5c697-116">Gå til **Blob service** \> **Containere**, og opprett en ny container.</span><span class="sxs-lookup"><span data-stu-id="5c697-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="5c697-117">Angi et navn på beholderen, og sett feltet **Offentlig tilgangsnivå** til **Privat (ingen anonym tilgang)**.</span><span class="sxs-lookup"><span data-stu-id="5c697-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="5c697-118">Åpne beholderen, og gå til **Innstillinger \> Tilgangspolicy**.</span><span class="sxs-lookup"><span data-stu-id="5c697-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="5c697-119">Velg **Legg til policy** for å legge til en lagret tilgangspolicy.</span><span class="sxs-lookup"><span data-stu-id="5c697-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="5c697-120">Angi feltene **Identifikator** og **Tillatelser** etter behov.</span><span class="sxs-lookup"><span data-stu-id="5c697-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="5c697-121">I **Tillatelser**-feltet må du velge alle tillatelser.</span><span class="sxs-lookup"><span data-stu-id="5c697-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Gi tillatelse til Blob Storage](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="5c697-123">Angi start- og utløpsdatoer.</span><span class="sxs-lookup"><span data-stu-id="5c697-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="5c697-124">Utløpsdatoen må være i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="5c697-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="5c697-125">Velg **OK** for å lagre policyen, og lagre endringene i containeren.</span><span class="sxs-lookup"><span data-stu-id="5c697-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="5c697-126">Gå tilbake til lagringskontoen, og åpne **Lagringsutforsker (forhåndsversjon)**.</span><span class="sxs-lookup"><span data-stu-id="5c697-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="5c697-127">Høyreklikk containeren, og velg deretter **Hent delt tilgangssignatur**.</span><span class="sxs-lookup"><span data-stu-id="5c697-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="5c697-128">I dialogboksen **Delt tilgangssignatur** kopierer og lagrer du verdien i **URI**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c697-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="5c697-129">Denne verdien brukes i den neste prosedyren og refereres til som *URI for delt tilgangssignatur*.</span><span class="sxs-lookup"><span data-stu-id="5c697-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Velge og kopiere URI-verdien](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="5c697-131">Konfigurere Key Vault for å lagre lagringskonto-URIen</span><span class="sxs-lookup"><span data-stu-id="5c697-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="5c697-132">Åpne Key Vault du har tenkt å bruke med elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="5c697-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="5c697-133">Gå til **Innstillinger** \> **Hemmeligheter**, og velg deretter **Generer/Importer** for å opprette en ny hemmelighet.</span><span class="sxs-lookup"><span data-stu-id="5c697-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="5c697-134">På siden **Opprett en hemmelig**, i feltet **Opplastingsalternativer**, velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="5c697-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="5c697-135">Angi navnet på hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="5c697-135">Enter the name of the secret.</span></span> <span data-ttu-id="5c697-136">Dette navnet vil bli brukt under installasjonen av tjenesten i RCS (Regulatory Configuration Service) og refereres til som *hemmelig Key Vault-navn*.</span><span class="sxs-lookup"><span data-stu-id="5c697-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="5c697-137">I **Verdi**-feltet velger du **URI for delt tilgangssignatur**, og deretter velger du **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="5c697-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="5c697-138">Angi at tilgangspolicyen skal gi elektronisk fakturering det riktige nivået for sikker tilgang til hemmeligheten du opprettet.</span><span class="sxs-lookup"><span data-stu-id="5c697-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="5c697-139">Gå til **Innstillinger \> Tilgangspolicy**, og velg **Legg til tilgangspolicy**.</span><span class="sxs-lookup"><span data-stu-id="5c697-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="5c697-140">Angi de hemmelige tillatelsene for **Hente**- og **Liste**-operasjonene.</span><span class="sxs-lookup"><span data-stu-id="5c697-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Gi tjenestetilgang](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="5c697-142">Angi sertifikattillatelsene for **Hent**- og **Liste**-operasjonene.</span><span class="sxs-lookup"><span data-stu-id="5c697-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Gi sertifikattillatelse](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="5c697-144">I feltet **Velg sikkerhetskontohaver** velger du **Ingen valgt**.</span><span class="sxs-lookup"><span data-stu-id="5c697-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="5c697-145">I dialogboksen **Sikkerhetskontohaver** velger du sikkerhetskontohaveren ved å legge til **E-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="5c697-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="5c697-146">Velg **Legg til**, og velg deretter **Lagre Key Vault-endringer**.</span><span class="sxs-lookup"><span data-stu-id="5c697-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="5c697-147">På siden **Oversikt** kopierer du **DNS-navn**-verdien for Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5c697-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="5c697-148">Denne verdien vil bli brukt under konfigurasjon av tjenesten i RCS, og vil bli referert til som *Key Vault-URI*.</span><span class="sxs-lookup"><span data-stu-id="5c697-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

