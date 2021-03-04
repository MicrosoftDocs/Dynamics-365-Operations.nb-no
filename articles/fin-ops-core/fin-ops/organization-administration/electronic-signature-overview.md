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
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df7f842477ddfb88662f37ae311215f08c6b0173
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693190"
---
# <a name="electronic-signatures-overview"></a>Oversikt over elektroniske signaturer

[!include [banner](../includes/banner.md)]

Denne artikkelen emnet gir en oversikt over elektroniske signaturer, og beskriver hvordan de brukes.

## <a name="what-is-an-electronic-signature"></a>Hva er en elektronisk signatur?

En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess. I noen bransjer er en elektronisk signatur like bindende som er håndskrevet signatur.

Elektroniske signaturer er et krav til samsvar med lovgivning for flere regulerte industrier, for eksempel legemiddelindustrien, matvareindustrien og romfarts- og forsvarsindustrien. De er også nødvendig for samsvar med lovgivningen i 21 CFR Part 11 som er utstedt av Food and Drug Administration (FDA) i USA.

> [!NOTE]
> En elektronisk signatur alene er ikke det samme som en digital signatur. En elektronisk signatur er bare en erstatning for en håndskrevet signatur, mens en digital signatur gir flere sikkerhetstiltak. En digital signatur kan hjelpe med å identifisere om en annen bruker eller prosess har endret dataene på en ulovlig måte. En digital signatur kan også verifiseres, og denne verifiseringen kan ikke imøtegås av eieren av sertifikatet som ble brukt til å signere dataene. Som beskrevet nedenfor har elektroniske signaturer innebygd funksjonalitet for digital signatur.

## <a name="electronic-signatures"></a>Elektroniske signaturer

Du kan du bruke elektroniske signaturer for viktige forretningsprosesser. Noen prosesser har innebygde funksjoner for elektronisk signatur. Du kan også opprette egendefinerte signaturkrav for en hvilken som helst databasetabell og et hvilket som helst felt.

Elektroniske signaturer har innebygd funksjonalitet for digital signatur. Alle brukere som signerer dokumenter, må ha et gyldig kryptografisk sertifikat. Når et dokument signeres, valideres den private nøkkelen som er tilordnet dette sertifikatet. Informasjon om elektronisk signatur registreres i en logg for å angi et revisjonsspor. Hvis du vil definere elektroniske signaturer, kan du se [Opprette elektroniske signaturer](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Brukere som trenger tilgang til elektroniske signaturer

Tre typer brukere krever vanligvis sikkerhetstilgang til elektroniske signaturer: administratorer for elektroniske signaturer, signatarer og revisorer for elektroniske signaturer.

### <a name="electronic-signature-administrator"></a>Administrator for elektronisk signatur

Administratoren for elektronisk signatur oppretter signaturkrav, generelle parametere og godkjennere, og mottar varsler når signaturer ikke kan verifiseres. En bruker som tilhører sikkerhetsrollen **IT-sjef** som standard, har tillatelse til å administrere elektroniske signaturer.

### <a name="signer"></a>Signatar

En signatar angir elektroniske signaturer for dokumenter og prosesser som krever signaturer. En bruker som tilhører sikkerhetsrollen **Systembruker** som standard, har tillatelse til å signere dokumenter elektronisk.

> [!NOTE]
> Det kan hende at signataren trenger flere tillatelser før det gis tilgang til dataene som er relatert til dokumentet eller prosessen som blir signert. En brukere som gjøre endringer i dataene og deretter må signere for disse endringene, må ha tillatelse til å endre dataene. En bruker som signerer på vegne av en annen bruker trenger ikke tilgang til dataene. Et eksempel på denne typen bruker er en ansvarlig som signerer for ansattes endringer.

### <a name="electronic-signature-auditor"></a>Revisor for elektronisk signatur

Revisoren for elektronisk signatur ser gjennom databaseloggen og gjenomgangsloggen for signatur som er tilgjengelige i databaseloggen. En bruker som tilhører sikkerhetsrollen **IT-sjef** som standard, har tillatelse til å revidere elektroniske signaturer.

Hvis du bruker en annen rolle enn **IT-sjef**, må du passe på at rollen er tilordnet følgende rettigheter:

- Vis feil for elektronisk signatur
- Vis databaselogg

## <a name="signing-documents-electronically"></a>Signere dokumenter elektronisk

### <a name="get-a-certificate"></a>Hente et sertifikat

Før du signerer dokumenter elektronisk, må hver signatar be om et sertifikat.

> [!NOTE]
> Microsoft SQL Server-funksjoner brukes til å opprette sertifikater og aktivere elektronisk signering. Det kreves ikke et ekstra sertifikat eller en infrastruktur for offentlig nøkkel (PKI).

Når du ber om et sertifikat, opprettes det en offentlig og en privat nøkkel for deg. Den private nøkkelen krypteres ved hjelp av et passord som bare du kjenner. Når du signerer et dokument elektronisk, verifiseres identiteten din når du angir passordet.

Hvis du vil be om et sertifikat, går du til siden **Alternativer** og kategorien **Kontoer**, og klikker  **Hent sertifikat**.

Du må deretter angi og bekreft passordet som du vil bruke for signering. Passordet brukes til å beskytte din private nøkkel og autorisere bruk av sertifikatet ditt. Dette passordet lagres ikke i databasen, og er ikke tilgjengelig for noen andre, selv ikke administrator.

Hvis du glemmer passordet som er knyttet til sertifikatet, må dette sertifikatet tilbakestilles. Hvis du tilbakestiller sertifikatet, berøres ikke dokumentet du signerte med det forrige sertifikatet. Hvis du vil tilbakestille et sertifikat, går du til siden **Alternativer** og klikker **Tilbakestill sertifikat**.

### <a name="sign-a-document-electronically"></a>Signere et dokument elektronisk

Siden **Signer dokument** vises når du gjør en endring som krever en elektronisk signatur.

1. Klikk kategorien **Dokument** på siden **Signer dokument** for å gå gjennom endringene i dokumentet.
2. Velg en årsakskode i kategorien **Signatur**.
3. Angi en kommentar hvis det kreves en kommentar.
4. Hvis bruker-ID-en ikke vises i **Signatar**-feltet, velger du den i listen.
5. Angi plasseringen din, hvis denne informasjonen er nødvendig.
6. Klikk **OK**.

### <a name="sign-for-another-users-changes"></a>Signere for en annen brukers endringer

Noen ganger kan det hende at du vil at en bruker skal signere for en annen brukers endringer. Det kan for eksempel kreves at en arbeidsleder signerer for endringer som en ansatt gjør i stykklister. Bruk fremgangsmåten nedenfor til å angi en bruker som signatar for en annen bruker.

> [!NOTE]
> Når en bruker signerer for en annen brukers endring, må signaturen angis på arbeidsstasjonen til brukeren som gjorde endringen. Brukeren kan ikke lagre endringen før signaturen er angitt.

Hvis du vil angi godkjennere, følger du denne fremgangsmåten.

1. På siden **Alternativer** i kategorien **Kontoer**, klikker du **Angi godkjenner**.
2. I feltet **Bruker-ID for godkjenner** velger du ID-en for brukeren som må signere for en annen brukers endringer.
3. I feltet **Signer for bruker-ID** velger du ID-en til brukeren som har endringer det må signeres for.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]