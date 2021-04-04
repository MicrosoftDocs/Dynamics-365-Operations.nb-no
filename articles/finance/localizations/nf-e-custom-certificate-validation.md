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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240585"
---
# <a name="nf-e-custom-certificate-validation"></a>Validering av egendefinert NF-e-sertifikat

[!include [banner](../includes/banner.md)]

Når du aktiverer funksjonen for bekreftelse av egendefinert NF-e-sertifikat, tillater egendefinert validering en tilkobling til webtjenestene. Denne tilkoblingen kreves for å overføre NF-e og motta godkjenning fra SEFAZ.

**Godkjenningsformål for server**-egenskapen fra sertifikatet V5 utstedes av den brasilianske rotsertifiseringsinstansen. Denne egenskapen er som standard deaktivert og må aktiveres manuelt. I enkelte tilfeller kan den automatiske sertifikatoppdateringen endre denne egenskapen slik at den ikke lenger er aktivert. Hvis dette skjer påvirkes TLS-tilkoblingen, og den er ikke lenger klarert. Muligheten til å utstede NF-e i produksjonsmiljøer for delstatene Minas Gerais (MG) og Paraná (PR) påvirkes også.

Denne oppdateringen gjør det mulig å bruke en alternativ løsning for sertifikatvalideringen, noe som betyr at det er mulig å opprette sikker kommunikasjon.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]