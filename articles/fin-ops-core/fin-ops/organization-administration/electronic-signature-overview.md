---
title: Oversikt over elektroniske signaturer
description: Denne artikkelen emnet gir en oversikt over elektroniske signaturer, og beskriver hvordan de brukes.
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e5144517a880c41cf04998ed53a826a75ecefb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179309"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="af71a-103">Oversikt over elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="af71a-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af71a-104">Denne artikkelen emnet gir en oversikt over elektroniske signaturer, og beskriver hvordan de brukes.</span><span class="sxs-lookup"><span data-stu-id="af71a-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="af71a-105">Hva er en elektronisk signatur?</span><span class="sxs-lookup"><span data-stu-id="af71a-105">What is an electronic signature?</span></span>

<span data-ttu-id="af71a-106">En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess.</span><span class="sxs-lookup"><span data-stu-id="af71a-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="af71a-107">I noen bransjer er en elektronisk signatur like bindende som er håndskrevet signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="af71a-108">Elektroniske signaturer er et krav til samsvar med lovgivning for flere regulerte industrier, for eksempel legemiddelindustrien, matvareindustrien og romfarts- og forsvarsindustrien.</span><span class="sxs-lookup"><span data-stu-id="af71a-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="af71a-109">De er også nødvendig for samsvar med lovgivningen i 21 CFR Part 11 som er utstedt av Food and Drug Administration (FDA) i USA.</span><span class="sxs-lookup"><span data-stu-id="af71a-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="af71a-110">En elektronisk signatur alene er ikke det samme som en digital signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="af71a-111">En elektronisk signatur er bare en erstatning for en håndskrevet signatur, mens en digital signatur gir flere sikkerhetstiltak.</span><span class="sxs-lookup"><span data-stu-id="af71a-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="af71a-112">En digital signatur kan hjelpe med å identifisere om en annen bruker eller prosess har endret dataene på en ulovlig måte.</span><span class="sxs-lookup"><span data-stu-id="af71a-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="af71a-113">En digital signatur kan også verifiseres, og denne verifiseringen kan ikke imøtegås av eieren av sertifikatet som ble brukt til å signere dataene.</span><span class="sxs-lookup"><span data-stu-id="af71a-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="af71a-114">Som beskrevet nedenfor har elektroniske signaturer innebygd funksjonalitet for digital signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="af71a-115">Elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="af71a-115">Electronic signatures</span></span>

<span data-ttu-id="af71a-116">Du kan du bruke elektroniske signaturer for viktige forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="af71a-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="af71a-117">Noen prosesser har innebygde funksjoner for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="af71a-118">Du kan også opprette egendefinerte signaturkrav for en hvilken som helst databasetabell og et hvilket som helst felt.</span><span class="sxs-lookup"><span data-stu-id="af71a-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="af71a-119">Elektroniske signaturer har innebygd funksjonalitet for digital signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="af71a-120">Alle brukere som signerer dokumenter, må ha et gyldig kryptografisk sertifikat.</span><span class="sxs-lookup"><span data-stu-id="af71a-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="af71a-121">Når et dokument signeres, valideres den private nøkkelen som er tilordnet dette sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="af71a-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="af71a-122">Informasjon om elektronisk signatur registreres i en logg for å angi et revisjonsspor.</span><span class="sxs-lookup"><span data-stu-id="af71a-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="af71a-123">Hvis du vil definere elektroniske signaturer, kan du se [Opprette elektroniske signaturer (oppgaveveiledning)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="af71a-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="af71a-124">Brukere som trenger tilgang til elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="af71a-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="af71a-125">Tre typer brukere krever vanligvis sikkerhetstilgang til elektroniske signaturer: administratorer for elektroniske signaturer, signatarer og revisorer for elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="af71a-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="af71a-126">Administrator for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="af71a-126">Electronic signature administrator</span></span>

<span data-ttu-id="af71a-127">Administratoren for elektronisk signatur oppretter signaturkrav, generelle parametere og godkjennere, og mottar varsler når signaturer ikke kan verifiseres.</span><span class="sxs-lookup"><span data-stu-id="af71a-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="af71a-128">En bruker som tilhører sikkerhetsrollen **IT-sjef** som standard, har tillatelse til å administrere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="af71a-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="af71a-129">Signatar</span><span class="sxs-lookup"><span data-stu-id="af71a-129">Signer</span></span>

<span data-ttu-id="af71a-130">En signatar angir elektroniske signaturer for dokumenter og prosesser som krever signaturer.</span><span class="sxs-lookup"><span data-stu-id="af71a-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="af71a-131">En bruker som tilhører sikkerhetsrollen **Systembruker** som standard, har tillatelse til å signere dokumenter elektronisk.</span><span class="sxs-lookup"><span data-stu-id="af71a-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="af71a-132">Det kan hende at signataren trenger flere tillatelser før det gis tilgang til dataene som er relatert til dokumentet eller prosessen som blir signert.</span><span class="sxs-lookup"><span data-stu-id="af71a-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="af71a-133">En brukere som gjøre endringer i dataene og deretter må signere for disse endringene, må ha tillatelse til å endre dataene.</span><span class="sxs-lookup"><span data-stu-id="af71a-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="af71a-134">En bruker som signerer på vegne av en annen bruker trenger ikke tilgang til dataene.</span><span class="sxs-lookup"><span data-stu-id="af71a-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="af71a-135">Et eksempel på denne typen bruker er en ansvarlig som signerer for ansattes endringer.</span><span class="sxs-lookup"><span data-stu-id="af71a-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="af71a-136">Revisor for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="af71a-136">Electronic signature auditor</span></span>

<span data-ttu-id="af71a-137">Revisoren for elektronisk signatur ser gjennom databaseloggen og gjenomgangsloggen for signatur som er tilgjengelige i databaseloggen.</span><span class="sxs-lookup"><span data-stu-id="af71a-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="af71a-138">En bruker som tilhører sikkerhetsrollen **IT-sjef** som standard, har tillatelse til å revidere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="af71a-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="af71a-139">Hvis du bruker en annen rolle enn **IT-sjef**, må du passe på at rollen er tilordnet følgende rettigheter:</span><span class="sxs-lookup"><span data-stu-id="af71a-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="af71a-140">Vis feil for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="af71a-140">View electronic signature failures</span></span>
- <span data-ttu-id="af71a-141">Vis databaselogg</span><span class="sxs-lookup"><span data-stu-id="af71a-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="af71a-142">Signere dokumenter elektronisk</span><span class="sxs-lookup"><span data-stu-id="af71a-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="af71a-143">Hente et sertifikat</span><span class="sxs-lookup"><span data-stu-id="af71a-143">Get a certificate</span></span>

<span data-ttu-id="af71a-144">Før du signerer dokumenter elektronisk, må hver signatar be om et sertifikat.</span><span class="sxs-lookup"><span data-stu-id="af71a-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="af71a-145">Microsoft SQL Server-funksjoner brukes til å opprette sertifikater og aktivere elektronisk signering.</span><span class="sxs-lookup"><span data-stu-id="af71a-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="af71a-146">Det kreves ikke et ekstra sertifikat eller en infrastruktur for offentlig nøkkel (PKI).</span><span class="sxs-lookup"><span data-stu-id="af71a-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="af71a-147">Når du ber om et sertifikat, opprettes det en offentlig og en privat nøkkel for deg.</span><span class="sxs-lookup"><span data-stu-id="af71a-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="af71a-148">Den private nøkkelen krypteres ved hjelp av et passord som bare du kjenner.</span><span class="sxs-lookup"><span data-stu-id="af71a-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="af71a-149">Når du signerer et dokument elektronisk, verifiseres identiteten din når du angir passordet.</span><span class="sxs-lookup"><span data-stu-id="af71a-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="af71a-150">Hvis du vil be om et sertifikat, går du til siden **Alternativer** og kategorien **Kontoer**, og klikker  **Hent sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="af71a-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="af71a-151">Du må deretter angi og bekreft passordet som du vil bruke for signering.</span><span class="sxs-lookup"><span data-stu-id="af71a-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="af71a-152">Passordet brukes til å beskytte din private nøkkel og autorisere bruk av sertifikatet ditt.</span><span class="sxs-lookup"><span data-stu-id="af71a-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="af71a-153">Dette passordet lagres ikke i databasen, og er ikke tilgjengelig for noen andre, selv ikke administrator.</span><span class="sxs-lookup"><span data-stu-id="af71a-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="af71a-154">Hvis du glemmer passordet som er knyttet til sertifikatet, må dette sertifikatet tilbakestilles.</span><span class="sxs-lookup"><span data-stu-id="af71a-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="af71a-155">Hvis du tilbakestiller sertifikatet, berøres ikke dokumentet du signerte med det forrige sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="af71a-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="af71a-156">Hvis du vil tilbakestille et sertifikat, går du til siden **Alternativer** og klikker **Tilbakestill sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="af71a-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="af71a-157">Signere et dokument elektronisk</span><span class="sxs-lookup"><span data-stu-id="af71a-157">Sign a document electronically</span></span>

<span data-ttu-id="af71a-158">Siden **Signer dokument** vises når du gjør en endring som krever en elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="af71a-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="af71a-159">Klikk kategorien **Dokument** på siden **Signer dokument** for å gå gjennom endringene i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="af71a-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="af71a-160">Velg en årsakskode i kategorien **Signatur**.</span><span class="sxs-lookup"><span data-stu-id="af71a-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="af71a-161">Angi en kommentar hvis det kreves en kommentar.</span><span class="sxs-lookup"><span data-stu-id="af71a-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="af71a-162">Hvis bruker-ID-en ikke vises i **Signatar**-feltet, velger du den i listen.</span><span class="sxs-lookup"><span data-stu-id="af71a-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="af71a-163">Angi plasseringen din, hvis denne informasjonen er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="af71a-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="af71a-164">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="af71a-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="af71a-165">Signere for en annen brukers endringer</span><span class="sxs-lookup"><span data-stu-id="af71a-165">Sign for another user's changes</span></span>

<span data-ttu-id="af71a-166">Noen ganger kan det hende at du vil at en bruker skal signere for en annen brukers endringer.</span><span class="sxs-lookup"><span data-stu-id="af71a-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="af71a-167">Det kan for eksempel kreves at en arbeidsleder signerer for endringer som en ansatt gjør i stykklister.</span><span class="sxs-lookup"><span data-stu-id="af71a-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="af71a-168">Bruk fremgangsmåten nedenfor til å angi en bruker som signatar for en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="af71a-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="af71a-169">Når en bruker signerer for en annen brukers endring, må signaturen angis på arbeidsstasjonen til brukeren som gjorde endringen.</span><span class="sxs-lookup"><span data-stu-id="af71a-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="af71a-170">Brukeren kan ikke lagre endringen før signaturen er angitt.</span><span class="sxs-lookup"><span data-stu-id="af71a-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="af71a-171">Hvis du vil angi godkjennere, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="af71a-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="af71a-172">På siden **Alternativer** i kategorien **Kontoer**, klikker du **Angi godkjenner**.</span><span class="sxs-lookup"><span data-stu-id="af71a-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="af71a-173">I feltet **Bruker-ID for godkjenner** velger du ID-en for brukeren som må signere for en annen brukers endringer.</span><span class="sxs-lookup"><span data-stu-id="af71a-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="af71a-174">I feltet **Signer for bruker-ID** velger du ID-en til brukeren som har endringer det må signeres for.</span><span class="sxs-lookup"><span data-stu-id="af71a-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
