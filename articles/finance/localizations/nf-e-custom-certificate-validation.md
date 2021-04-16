---
title: Validering av egendefinert NF-e-sertifikat
description: Dette emnet inneholder informasjon om hvordan du aktiverer og bruker det egendefinerte NF-e-sertifikatet.
author: gionoder
ms.date: 10/06/2020
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813974"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="948b1-103">Validering av egendefinert NF-e-sertifikat</span><span class="sxs-lookup"><span data-stu-id="948b1-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="948b1-104">Når du aktiverer funksjonen for bekreftelse av egendefinert NF-e-sertifikat, tillater egendefinert validering en tilkobling til webtjenestene.</span><span class="sxs-lookup"><span data-stu-id="948b1-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="948b1-105">Denne tilkoblingen kreves for å overføre NF-e og motta godkjenning fra SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="948b1-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="948b1-106">**Godkjenningsformål for server**-egenskapen fra sertifikatet V5 utstedes av den brasilianske rotsertifiseringsinstansen.</span><span class="sxs-lookup"><span data-stu-id="948b1-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="948b1-107">Denne egenskapen er som standard deaktivert og må aktiveres manuelt.</span><span class="sxs-lookup"><span data-stu-id="948b1-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="948b1-108">I enkelte tilfeller kan den automatiske sertifikatoppdateringen endre denne egenskapen slik at den ikke lenger er aktivert.</span><span class="sxs-lookup"><span data-stu-id="948b1-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="948b1-109">Hvis dette skjer påvirkes TLS-tilkoblingen, og den er ikke lenger klarert.</span><span class="sxs-lookup"><span data-stu-id="948b1-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="948b1-110">Muligheten til å utstede NF-e i produksjonsmiljøer for delstatene Minas Gerais (MG) og Paraná (PR) påvirkes også.</span><span class="sxs-lookup"><span data-stu-id="948b1-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="948b1-111">Denne oppdateringen gjør det mulig å bruke en alternativ løsning for sertifikatvalideringen, noe som betyr at det er mulig å opprette sikker kommunikasjon.</span><span class="sxs-lookup"><span data-stu-id="948b1-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]