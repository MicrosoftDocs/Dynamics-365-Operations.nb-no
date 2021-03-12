---
title: Validering av egendefinert NF-e-sertifikat
description: Dette emnet inneholder informasjon om hvordan du aktiverer og bruker det egendefinerte NF-e-sertifikatet.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
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
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990092"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="b2d9e-103">Validering av egendefinert NF-e-sertifikat</span><span class="sxs-lookup"><span data-stu-id="b2d9e-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2d9e-104">Når du aktiverer funksjonen for bekreftelse av egendefinert NF-e-sertifikat, tillater egendefinert validering en tilkobling til webtjenestene.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="b2d9e-105">Denne tilkoblingen kreves for å overføre NF-e og motta godkjenning fra SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="b2d9e-106">**Godkjenningsformål for server**-egenskapen fra sertifikatet V5 utstedes av den brasilianske rotsertifiseringsinstansen.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="b2d9e-107">Denne egenskapen er som standard deaktivert og må aktiveres manuelt.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="b2d9e-108">I enkelte tilfeller kan den automatiske sertifikatoppdateringen endre denne egenskapen slik at den ikke lenger er aktivert.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="b2d9e-109">Hvis dette skjer påvirkes TLS-tilkoblingen, og den er ikke lenger klarert.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="b2d9e-110">Muligheten til å utstede NF-e i produksjonsmiljøer for delstatene Minas Gerais (MG) og Paraná (PR) påvirkes også.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="b2d9e-111">Denne oppdateringen gjør det mulig å bruke en alternativ løsning for sertifikatvalideringen, noe som betyr at det er mulig å opprette sikker kommunikasjon.</span><span class="sxs-lookup"><span data-stu-id="b2d9e-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


