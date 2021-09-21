---
title: Feil i sertifiseringsbane når du konfigurerer apptilkobling
description: Hvis Warehouse Management-appen viser feilen "Finner ikke klareringsanker for sertifiseringsbane", kan du bruke denne siden til å løse eller omgå problemet.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477203"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Finner ikke klareringsanker for sertifiseringsbane ved konfigurasjon av apptilkobling

## <a name="symptoms"></a>Symptomer

Når du prøver å koble til Supply Chain Management, kan det hende at Warehouse Management-appen viser følgende feilmelding:

> java.security.cert.certPathValidatorException: Finner ikke klareringsanker for sertifiseringsbane.

Dette problemet kan påvirke enheter med følgende egenskaper:

- **OS-versjon**: Android 4.4.x (f.eks. Zebra TC55). Dette gjelder ikke nylige Android versjoner.
- **Supply Chain Management-plassering**: Cloud
- **Tilkoblingsmodus**: Klienthemmelighet eller -sertifikat

## <a name="possible-cause"></a>Mulig årsak

Microsoft kan ha oppdatert SSL-sertifikatene som brukes av Supply Chain Management. Derfor kan rotsertifikatet og/eller et av de midlertidige sertifikatene være endret, så det nye finnes ikke på listen over klarerte systemsertifikater for mobilenheten. Nyere versjoner av Android oppdaterer automatisk listene over klarerte sertifikater, men Android 4.4.x gjør ikke.

## <a name="resolution"></a>Løsning

Du omgår dette problemet ved å gjøre ett av følgende:

- Bruk omgåelsen som beskrives i neste del, til å oppdatere hver relevante enhet.
- Det *kan* være mulig å ta kontakt med Zebra eller Google for å få en oppdatering av CA-sertifikatene (systemklarerte sertifiseringsmyndigheter). Vi har imidlertid ikke bekreftet dette.
- Hvis mulig bør du vurdere å erstatte eldre enheter med enheter som kjører en nyere versjon av Android (der klarerte CA-sertifikater oppdateres automatisk).

### <a name="workaround"></a>Løsning

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Trinn 1: Eksporter det nye rotsertifikatet fra Supply Chain Management

Last ned det nye rotsertifikatet manuelt ved hjelp av webleseren ved å gjøre følgende:

1. Logg deg på Dynamics Supply Chain Management, og åpne forsiden.

1. Velg låsikonet på adresselinjen i webleseren for å åpne dialogboksen **Plasseringen er sikker**.
1. I dialogboksen velger du **Sertifikat (gyldig)** for å åpne **Sertifikat**-vinduet for dette sertifikatet.
1. Åpne kategorien **Sertifiseringsbane** i **Sertifikat**-vinduet.
1. Velg det øverste sertifikatet som vises i hierarkiet. (dette er rotsertifikatet).
1. Åpne kategorien **Detaljer** i **Sertifikat**-vinduet.
1. Velg **Kopier til fil**-knappen nederst i kategorien **Detaljer**.
1. **Veiviseren for sertifikateksport** åpnes. Klikk **Neste** for å fortsette.
1. Siden **Eksporter filformat** åpnes. Velg **DER-kodet binær X.509 (.CER)**. Klikk på **Neste** for å fortsette.
1. Siden **Filer som skal eksporteres** åpnes, og du kan angi et filnavn og en plassering. Klikk på **Neste** for å fortsette.
1. Siden **Veiviser for utfylling av sertifikateksport** åpnes og viser resultatet av eksporten. Velg **Fullfør**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Trinn 2: Installer det nedlastede sertifikatet på de berørte enhetene

Installer det nedlastede sertifikatet ved å gjøre følgende:

1. Overfør sertifikatet du lastet ned i forrige trinn, til enheten du vil oppdatere. Du kan for eksempel bruke et SD-kort eller en nettverkstilkobling til å gjøre filen tilgjengelig for enheten.
1. Åpne sikkerhetsinnstillingene for enheten, og velg menyalternativet for å installere et sertifikat fra en fil. (De nøyaktige trinnene for dette varierer basert på enhet og OS-versjon.)
1. Det nye sertifikatet skal nå vises i kategorien **Bruker** for klarerte sertifikater.
1. Gjenta denne fremgangsmåten for hvert berørt produkt.
