---
title: Autorisere samhandling med webtjenester for ID-porten og Altinn
description: Dette emnet forklarer hvordan du autoriserer samhandling mellom Microsoft Dynamics 365 Finance-miljøet og nettjenestene ID-porten og Altinn.
author: liza-golub
ms.author: elgolu
ms.date: 11/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.search.validFrom: 2022-11-18
ms.openlocfilehash: 498085108eceec1a9411ccd84b108c1c51ff6e94
ms.sourcegitcommit: a11e8f4e764ff0bb210875401ae0671bc6412bde
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7866807"
---
# <a name="authorize-interoperation-with-id-porten-and-altinn-web-services"></a>Autorisere samhandling med webtjenester for ID-porten og Altinn

[!include [banner](../includes/banner.md)]

Før du begynner å autorisere Microsoft Dynamics 365 Finance-miljøet til å fungere sammen med webtjenestene ID-porten og Altinn, må du sørge for at du har [registrert et integreringspunkt i ID-porten](emea-nor-vat-return-integration-point.md). I tillegg må du kontrollere at feltet **Gyldig(e) redirect uri-er** for integreringspunktet er satt til Internett-adressen (URL) på siden **Webprogrammer** i den juridiske enheten som du vil samhandle med ID-porten- og Altinn-webtjenestene fra.

Følg denne fremgangsmåten for å autorisere Finance-miljøet i ID-porten- og Altinn-webtjenester, og gjør det klart for samarbeid mellom dem.

1. Gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**, og velg webprogrammet **NO ID-Porten** i listen til venstre.
2. Kontroller at feltet **URL-adresse for omadressering** er satt til URL-adressen for gjeldende side (**Webprogrammer**). Denne URL-adressen må samsvare med URL-adressen du angav i feltet **Gyldig(e) omdirigerings-uri-er** for integreringspunktet i webportalen for ID-porten.
3. Kontroller at feltet for **Klient-ID** er satt til klient-IDen for integreringspunktet, og at feltet **Klienthemmelighet** er satt til klienthemmelighet.
4. Velg **Få autorisasjonskode** i handlingsruten.
5. I dialogboksen **Parametere for elektronisk rapport**, i feltet for **Forespurt språk i brukergrensesnittet** angir du **en**, og deretter velger du **OK**.

    Du blir sendt videre til ID-porten for brukerautorisering. Brukeren som er autorisert i ID-porten, må ha rettighetene som er nødvendige for å fullføre og sende mva-returer.

6. Når autorisasjonen er vellykket, blir du sendt tilbake til Finance, og en ny webleserkategori viser **Vellykket**-siden. Lukk webleserkategorien, og gå tilbake til webleserkategorien som viser siden **Webprogrammer**, der du kan starte autorisasjonsprosessen.
7. Velg **Få tilgangstoken** i handlingsruten.

    > [!NOTE]
    > Du må fullføre dette trinnet umiddelbart etter at du har fått autorisasjonskoden. Hvis ikke kan du få følgende feilmelding:
    >
    > > Webtjeneste returnerte feilkode 400 ({"feil":"invalid_grant","error_description":"invalid_grant (korrelasjons-ID: 08ede4e5-4720-5edb-8fd2-a4f6a1902b74)"}).
    >
    > Hvis du får denne feilmeldingen, kan du gå tilbake til trinn 4. Velg **Få tilgangstoken** umiddelbart etter at du har fått autorisasjonskoden.

8. I dialogboksen **Parametere for elektronisk rapportering** velger du **OK**.

    Når du har fått et tilgangstoken, får du melding om at tilgangstokenet ble hentet. I tillegg oppdateres verdiene i feltene **Innvilget område** og **Tilgangstoken utløper om**.

    ![Innvilget område og Tilgangstoken utløper i felt som er oppdatert for NO ID-Porten-webprogrammet på webapplikasjonssiden.](media/emea-nor-vat-return-no-authorization.png)

9. Velg webprogrammet **NO Altinn** i listen til venstre.
10. Velg **Få tilgangstoken** i handlingsruten.
11. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.

    Når du har fått et tilgangstoken, får du melding om at tilgangstokenet ble hentet. I tillegg oppdateres verdiene i feltene **Innvilget område** og **Tilgangstoken utløper om**.

> [!IMPORTANT]
> Godkjenning av Finance-miljøet i integreringspunktet i ID-porten er gyldig for ett kalenderår. Denne perioden defineres av feltet **Authorization levetid (sekunder)** for [integreringspunktet](emea-nor-vat-return-integration-point.md). Du må autorisere Finance-miljøet på nytt før autorisasjonen utløper.

> [!IMPORTANT]
> Godkjenning av Finance-miljøet i integreringspunktet i ID-porten er *brukerspesifikk*. På grunn av dette lagrer Finance også informasjon om hvilken bruker som har hentet autorisasjonskoden i ID-porten. Innsending av mva-retur fra Finance er bare tillatt for denne brukeren. Hvis en annen bruker må sende inn en mva-retur, må de gå gjennom autorisasjonsprosessen før de kan sende mva-returen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
