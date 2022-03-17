---
title: Kundesertifikater og -hemmeligheter
description: Dette emnet forklarer hvordan du konfigurerer kundesertifikater og -hemmeligheter i elektronisk fakturering.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1325cad95e9a6dc470691f5f168439fccaaa78e1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371688"
---
# <a name="customer-certificates-and-secrets"></a>Kundesertifikater og -hemmeligheter

[!include [banner](../includes/banner.md)]

Hvis du allerede har en Microsoft Azure Key Vault-referanse i Regulatory Configuration Service (RCS), kan du opprette referanser til Key Vault-sertifikatene og -hemmelighetene. Hvis du ikke har en Key Vault-referanse ennå, kan du se [Tjenestemiljøer](e-invoicing-service-environments.md) hvis du vil ha informasjon om hvordan du oppretter den.

## <a name="create-certificates-and-secrets"></a>Opprette sertifikater og hemmeligheter

Følg denne fremgangsmåten for å opprette og konfigurere sertifikater og hemmeligheter.

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.
3. Velg **Tjenestemiljøer** i handlingsruten på siden **Miljøoppsett**.
4. Velg **Key Vault-parametere** i handlingsruten på **Tjenestemiljøer**-siden.
5. Velg en Key Vault-referanse på siden **Key Vault-parametere**, og velg deretter **Legg til** i **Sertifikater**-delen.
6. I **Navn**-feltet angir du navnet på Key Vault-sertifikatet eller -hemmeligheten. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure-lagringskonto i Azure-portalen](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Angi en beskrivelse i **Beskrivelse**-feltet.
8. Velg **Sertifikat** i **Type**-feltet hvis du refererer til sertifikatet som er lagret i nøkkehvelvet. Velg **Hemmelighet** hvis du refererer til hemmeligheten som er lagret i nøkkelhvelvet.
9. Velg **Lagre**.

> [!NOTE]
> I noen scenarioer må du bruke offentlige sertifikater som har filtypen CER. Key Vault støtter imidlertid ikke import og lagring av sertifikater av denne typen som Key Vault-sertifikater. I disse scenarioene bør du lagre CER-filen som en Base-64-kodet X.509-streng (CER). Lagre deretter strengen som vises mellom linjen **BEGIN CERTIFICATE** og linjen **END CERTIFICATE** i filen, i en Key Vault-hemmelighet. Du bør likevel opprette en referanse i tjenestemiljøet til Key Vault-posten og angi **Sertifikat** i **Type**-feltet.

## <a name="create-a-chain-of-certificates"></a>Opprette en sertifikatkjede

Hvis land-/områdespesifikke fakturaer krever at en sertifikatkjede bruker digitale signaturer eller opprette en sikker (Secure Sockets Layer \[SSL\])-tilkobling til eksterne nettjenester, oppretter du en sertifikatkjede der sertifikatene er i følgende rekkefølge:

1. Rotsertifikater
2. Mellomliggende sertifikater
3. Sluttbrukersertifikater

Rotsertifiseringsinstanser er en klarert kilde for sertifikater. Mellomliggende sertifiseringsinstanssertifikater kobler sluttbrukersertifikatene til rotsertifiseringsinstanssertifikater.

Følg denne fremgangsmåten for å opprette og konfigurere en sertifikatkjede.

1. Velg **Sertifikatkjede** i handlingsruten på siden **Key Vault-parametere**.
2. Velg **Ny** for å opprette en kjede av sertifikater.
3. I **Navn**-feltet angir du navnet på sertifikatkjeden.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.
6. Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden. Ha rotsertifiseringsinstanssertifikatet øverst i listen og sluttbrukersertifikatet nederst.
7. Velg **Lagre**.

Du kan opprette så mange Key Vault-referanser i RCS som du vil. Husk at hemmeligheten for tokenet for signatur for delt tilgang (SAS) for lagring brukes til å koble et gitt tjenestemiljø til Key Vault-referansen. Du kan referere til Key Vault-sertifikatene og -hemmelighetene som er lagret i et nøkkelhvelv som også inneholder hemmeligheten for SAS-tokenet for lagring som du bruker når du konfigurerer tjenestemiljøet.
