---
title: Opprette en URL-adresse for side
description: Dette emnet dekker de grunnleggende konseptene og prosedyrene for oppretting av en URL-adresse på området.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795697"
---
# <a name="create-a-page-url"></a>Opprette en URL-adresse for side

[!include [banner](includes/banner.md)]

Dette emnet dekker de grunnleggende konseptene og prosedyrene for oppretting av en URL-adresse på området.

Den fullstendige eller absolutte URL-adressen som peker til en side på området, består av forskjellige deler. For eksempel har URL-adressen `https://www.contoso.com/en-us/contactus` følgende deler:

- `https://www.contoso.com` – HTTP-protokollen og områdedomenet.
- `/en-us` – Områdets språkbane.
- `/contactus` – Den relative URL-adressen til siden **Kontakt oss**. En relativ URL-adresse kalles også en URL-*plassholder*.

Du bestemmer områdets domene og valgfri språkbane når du konfigurerer området. Du kan legge til flere domener og språkbaner til området via nettbutikkens side i områdeinnstillingene.

URL-plassholderen for en side finnes som en frittstående enhet i sideredigeringsmiljøet. En URL-adresse for side består av to deler: et navn som representerer URL-plassholderen, og en peker til en side på området eller et eksternt område. En URL-adresse for side kan også konfigureres til å fungere som en omadressering til en annen side, enten på området eller på et eksternt område.

## <a name="create-a-page-url"></a>Opprette en URL-adresse for side

Det finnes to måter å opprette side-URL-adresser på:

- Automatisk når du oppretter en side
- Manuelt fra siden **URL-adresser**

### <a name="create-a-page-url-when-you-create-a-page"></a>Opprette en URL-adresse for side når du oppretter en side

Hvis du angir et navn i feltet **URL-adresse** når du oppretter en ny side, opprettes det automatisk en side-URL-adresse som peker til denne siden på siden **URL-adresser**. Når du har publisert URL-adressen og siden den peker til, kan brukere av området (kundene) få tilgang til siden som er knyttet til URL-adressen.

> [!NOTE]
> Hvis du publiserer en URL-adresse uten å publisere siden den peker til, mottar områdebrukere en 404-feil når de prøver å få tilgang til siden. Hvis du publiserer en side uten å publisere URL-adressen som peker til den, får du ikke tilgang til siden ved hjelp av en URL-adresse.

### <a name="manually-create-a-page-url"></a>Opprette en URL-adresse for side manuelt

Når du oppretter nye sider, trenger du ikke angi en URL-adresse for side. Hvis du lar URL-feltet være tomt, opprettes siden i en ikke-koblet tilstand. I så fall får ikke kundene tilgang til siden, selv om den er publisert. Hvis du vil at siden skal være tilgjengelig, må du manuelt opprette URL-adressen og koble den til siden.

Hvis du vil opprette side-URL-adressen manuelt for en side, følger du denne fremgangsmåten.

1. Velg **Ny** på siden **URL-adresser**.
1. Velg områdesiden som URL-adressen skal knyttes til.
1. Angi URL-plassholderen, og velg deretter **OK**.

På dette tidspunktet er URL-adressen i utkasttilstand. Den må publiseres før områdebrukere kan få tilgang til den tilknyttede siden.

## <a name="update-a-page-url"></a>Oppdatere en URL-adresse for side

Hvis du vil oppdatere målsiden til en side-URL-adresse, følger du disse trinnene.

1. På siden **URL-adresser** velger du URL-adressen som skal oppdateres.
1. I egenskapsruten til høyre velger du ellipseknappen (**...**) ved siden av målsidefeltet.
1. I dialogboksen velger du en annen side, og deretter velger du **OK**.
1. Lagre og publiser URL-adressen.

## <a name="redirect-a-page-url"></a>Omadressere en URL-adresse for side

Noen ganger kan det hende at du vil at kundene skal vise en annen side når de ber om en bestemt URL-adresse. I disse tilfellene er beste og enkleste fremgangsmåte ofte å endre siden som URL-adressen peker til. Du kan imidlertid ha legitime årsaker til å bruke HTTP 301- eller 3023-omadresseringer for å omadressere forespørsler for en URL-adresse til en annen URL-adresse.

Hvis du vil omadressere en URL-adresse til en annen URL-adresse, følger du disse trinnene.

1. På siden **URL-adresser** velger du URL-adressen som skal oppdateres.
1. Deretter velger du **Omadresser** i egenskapsruten til høyre.
1. Velg en destinasjon for omadresseringen.

    - Hvis du vil peke til en annen side på området, velger du **Intern URL-adresse** og deretter ellipseknappen (**...**), og velg deretter URL-adressen det skal omadresseres til.
    - Hvis du vil peke til en side på det eksterne området, velger du **Ekstern URL**, og deretter angir du full URL-adresse for denne siden. Husk å ta med protokollen. Skriv for eksempel inn `https://domain.com/new/page`. Hvis URL-adressen allerede omadresseres til en intern URL-adresse, må du velge **Fjern utvalg** før du kan angi en ekstern URL-adresse.

1. Velg en omadresseringstype:

    - **Permanent omadressering (301)** – Velg dette alternativet når du vet at innholdet flyttes permanent og ikke går tilbake til den forrige URL-adressen. Søkemotorer tilordner verdien for søkemotoroptimaliseringen for URL-adressen for omadressering til URL-adressen som det omadresseres til, og oppdaterer oppføringen slik at den viser den nye URL-adressen. 
    - **Midlertidig omadressering (302)** – Velg dette alternativet for å omadressere trafikk uten å oppdatere søkemotorer. Denne fremgangsmåten brukes vanligvis hvis innholdet vil gå snart tilbake til den forrige URL-adressen.

1. Når du er klar til å implementere omadresseringen, må du lagre og publisere URL-adressen.

## <a name="additional-resources"></a>Tilleggsressurser

[Tilpasse områdenavigering](customize-site-navigation.md)

[Legg til en ny områdeside](add-new-page.md)

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Legge til språk på området](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
