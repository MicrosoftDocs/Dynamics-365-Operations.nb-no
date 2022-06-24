---
title: Validering av egendefinert NF-e-sertifikat
description: Denne artikkelen inneholder informasjon om hvordan du aktiverer og bruker det egendefinerte NF-e-sertifikatet.
author: gionoder
ms.date: 07/29/2021
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
ms.openlocfilehash: 3d69aa9d6d0ce33fbed9ba1c7a7af441e14d0d07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875911"
---
# <a name="nf-e-custom-certificate-validation"></a>Validering av egendefinert NF-e-sertifikat

[!include [banner](../includes/banner.md)]

Egenskapen **Servergodkjenningsformål** fra sertifikatene som er utstedt av den brasilianske sertifiseringsmyndigheten for rotsertifikat, er deaktivert som standard, og må aktiveres manuelt. I enkelte tilfeller kan den automatiske sertifikatoppdateringen endre denne egenskapen slik at den ikke lenger er aktivert. Hvis dette skjer påvirkes TLS-tilkoblingen, og den er ikke lenger klarert. Muligheten til å utstede den brasilianske elektroniske regnskapsdokumentmodellen 55 (NF-e) i produksjonsmiljøer for delstatene Minas Gerais (MG) og Paraná (PR) påvirkes også.

Hvis du vil aktivere reparasjonen for **Egendefinert sertifikatvalidering for NF-e**, kan du gå til **Funksjonsbehandling**. Denne funksjonen gir en alternativ løsning for validering av V5- og V10-sertifikatet og gir tillatelse til en klarert forbindelse med nettjenestene, som kreves for sikker overføring av NF-e og mottak av autorisasjonen fra SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
