---
title: Overfør kundeemne til kontantdata fra dataintegrator til dobbel skriving
description: Denne artikkelen beskriver hvordan du overfører data for Kundeemne til kontanter fra Dataintegrator til dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: bbf5a7c2f409003816e2becf1a58ee7d7d5aafb2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289088"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Overfør kundeemne til kontantdata fra dataintegrator til dobbel skriving

[!include [banner](../../includes/banner.md)]

Løsningen Kundeemne til kontanter som er tilgjengelig for dataintegratoren, er ikke kompatibel med dobbel skriving. Årsaken til dette er msdynce_AccountNumber-indeksen i kontotabellen som kom som en del av løsningen Kundeemne til kontanter. Hvis denne indeksen finnes, kan du ikke opprette det samme kundekontonummeret i to forskjellige juridiske enheter. Du kan enten velge å starte på nytt med dobbel skriving ved å migrere Kundeemne til kontanter-dataene fra dataintegratoren til dobbel skriving, eller du kan installere den siste "dorman"-versjonen av løsningen Kundeemne til kontanter. Begge disse tilnærmingene dekkes i denne artikkelen.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Installer siste "dorman"-versjon av løsningen Kundeemne til kontanter for dataintegratoren

**P2C versjon 15.0.0.2** regnes som siste "dorman"-versjon av løsningen Kundeemne til kontanter for dataintegratoren. Du kan laste den ned fra [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Du må installere den manuelt. Etter installasjonen forblir alt nøyaktig likt, bortsett fra at msdynce_AccountNumber er fjernet.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Trinn for å overføre Kundeemne til kontant-data fra dataintegratoren til dobbel skriving

Følg fremgangsmåten nedenfor for å overføre dataene for Kundeemne til kontanter fra Dataintegrator til dobbel skriving.

1. Kjør Dataintegrator-jobbene for Kundeemne til kontanter for å utføre én siste, fullstendig synkronisering. Dermed sikrer du at begge systemene (økonomi- og driftsapper og kundeengasjementsapper) har alle dataene.
2. Du kan bidra til å unngå potensielt tap av data ved å eksportere dataene for Kundeemne til kontanter fra Microsoft Dynamics 365 Sales til en Excel-fil eller en fil med kommadelte verdier (CSV-fil). Eksporter data fra følgende enheter:

    - [Konto](#account-table)
    - [Kontakt](#contact-table)
    - [Faktura](#invoice-table)
    - Fakturaprodukter
    - [Bestilling](#order-table)
    - [Bestill produkter](#order-products-table)
    - [Produkter](#products-table)
    - [Tilbud](#quote-and-quote-product-tables)
    - [Tilbudsprodukter](#quote-and-quote-product-tables)

3. Avinstaller løsningen Kundeemne til kontanter fra Sales-miljøet. Dette trinnet fjerner kolonnene og tilsvarende data som løsningen Kundeemne til kontanter innførte.
4. Installer løsningen for dobbel skriving.
5. Opprett en tilkobling med dobbel skriving mellom økonomi- og driftsappen og kundeengasjementsappen for én eller flere juridiske enheter.
6. Aktiver dobbel skriving-tabelltilordninger, og kjør den innledende synkroniseringen for de nødvendige referansedataene. (Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).) Eksempler på nødvendige data omfatter kundegrupper, betalingsbetingelser og betalingsplaner. Ikke aktiver dobbel skriving-tilordninger for tabeller som krever initialisering, for eksempel tabeller for konto, tilbud, tilbudslinje, ordre og ordrelinje.
7. I kundeengasjementsappen går du til **Avanserte innstillinger \> Systeminnstillinger \> Databehandling \> Duplikatregistreringsregler** og deaktiverer alle reglene.
8. Initialiser tabellene som vises i trinn 2. Hvis du vil ha instruksjoner, kan du se de gjenstående delene i denne artikkelen.
9. Åpne økonomi- og driftsappen og aktiver tabelltilordningene, for eksempel tabelltilordningene for konto, tilbud, tilbudslinje, ordre og ordrelinje. Kjør deretter den innledende synkroniseringen. (Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).) Denne prosessen synkroniserer tilleggsinformasjon fra økonomi- og driftsappen, for eksempel behandlingsstatus, forsendelses- og faktureringsadresser, områder og lagre.

## <a name="account-table"></a>Kontotabell

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. I **Relasjonstype**-kolonnen angir du **Kunde** som en statisk verdi. Du ønsker kanskje ikke å klassifisere hver eneste kontooppføring som en kunde i forretningslogikken.
3. Angi kundegruppenummeret fra økonomi- og driftsappen i kolonnen **Kundegruppe-ID**. Standardverdien fra løsningen Kundeemne til kontanter er **10**.
4. Hvis du bruker løsningen Kundeemne til kontanter uten å tilpasse **Kontonummer**, angir du en **Kontonummer**-verdi i **Partsnummer**-kolonnen. Hvis det finnes tilpassinger og du ikke vet partsnummeret, henter du denne informasjonen fra økonomi- og driftsappen.

## <a name="contact-table"></a>Kontakttabell

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. Angi følgende kolonner, basert på verdien for **IsActiveCustomer** i CSV-filen:

    - Hvis **IsActiveCustomer** er satt til **Ja** i CSV-filen, angir du **Ja** i kolonnen **Kan selges**. Angi kundegruppenummeret fra økonomi- og driftsappen i kolonnen **Kundegruppe-ID**. Standardverdien fra løsningen Kundeemne til kontanter er **10**.
    - Hvis **IsActiveCustomer** er satt til **Nei** i CSV-filen, angir du **Nei** i kolonnen **Kan selges** og angir **Kunde** i kolonnen **Kontakt for**.

3. Hvis du bruker løsningen Kundeemne til kontanter uten tilpassing av **Kontaktnummer**, angir du følgende kolonner:

    - Overfør kontaktnummeret fra CSV-filen (**msdynce\_contactnumber**) til kontaktnummeret i **Kontakt**-tabellen (**msdyn\_contactnumber**).
    - Bruk verdier fra **Kontaktnummer**-tabellen i **Partsnummer**-kolonnen.
    - Bruk verdier fra **Kontaktnummer**-tabellen i kolonnen **Kontonummer/Kontaktperson-ID**.

## <a name="invoice-table"></a>Faktura-tabellen

Siden data fra **Faktura**-tabellen er utformet for å flyte én vei, fra økonomi- og driftsappen til kundeengasjementsappen, kreves ingen initialisering. Kjør den innledende synkroniseringen for å overføre alle de nødvendige dataene fra økonomi- og driftsappen til kundeengasjementsappen. Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).

## <a name="order-table"></a>Ordre-tabellen

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. Kopier verdien i **Ordre-ID**-kolonnen i CSV-filen til kolonnen **Salgsordrenummer**.
3. Kopier verdien i **Kunde**-kolonnen i CSV-filen til kolonnen **Kundefakturanummer**.
4. Kopier verdien i kolonnen **Leveringsland/-område** i CSV-filen til kolonnen **Leveringsland/-område**. Eksemple på denne verdien er **US** og **United States**.
5. Angi kolonnen **Ønsket mottaksdato**. Hvis du ikke bruker en mottaksdato, bruker du kolonnene **Ønsket leveringsdato**, **Fullføringsdato** og **Sendt dato** i CSV-filen. Et eksempel på denne verdien er **2020-03-27T00:00:00Z**.
6. Angi **Språk**-kolonnen. Et eksempel på denne verdien er **nb-no**.
7. Angi **Ordretype**-kolonnen ved å bruke **Varebasert**-kolonnen.

## <a name="order-products-table"></a>Bestill produkter-tabellen

- I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.

## <a name="products-table"></a>Produkter-tabellen

Siden data fra **Produkter**-tabellen er utformet for å flyte én vei, fra økonomi- og driftsappen til kundeengasjementsappen, kreves ingen initialisering. Kjør den innledende synkroniseringen for å overføre alle de nødvendige dataene fra økonomi- og driftsappen til kundeengasjementsappen. Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tabellene Tilbud og Tilbudsprodukt

Når det gjelder **Tilbud**-tabellen, følger du instruksjonene i [Ordre-tabellen](#order-table) tidligere i denne artikkelen. Når det gjelder **Tilbudsprodukt**-tabellen, følger du instruksjonene i [Bestill produkter-tabellen](#order-products-table) tidligere i dette emnet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

