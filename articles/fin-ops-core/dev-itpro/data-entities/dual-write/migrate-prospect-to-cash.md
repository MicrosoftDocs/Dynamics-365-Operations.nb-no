---
title: Overføre data for Kundeemne til kontanter fra Dataintegrator til dobbel skriving
description: Dette emnet beskriver hvordan du overfører data for Kundeemne til kontanter fra Dataintegrator til dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959852"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Overføre data for Kundeemne til kontanter fra Dataintegrator til dobbel skriving

[!include [banner](../../includes/banner.md)]

Følg fremgangsmåten nedenfor for å overføre dataene for Kundeemne til kontanter fra Dataintegrator til dobbel skriving.

1. Kjør Dataintegrator-jobbene for Kundeemne til kontanter for å utføre én siste, fullstendig synkronisering. Dermed sikrer du at begge systemene (Finance and Operations-apper og kundeengasjementsapper) har alle dataene.
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
5. Opprett en tilkobling med dobbel skriving mellom Finance and Operations-appen og kundeengasjementsappen for én eller flere juridiske enheter.
6. Aktiver dobbel skriving-tabelltilordninger, og kjør den innledende synkroniseringen for de nødvendige referansedataene. (Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).) Eksempler på nødvendige data omfatter kundegrupper, betalingsbetingelser og betalingsplaner. Ikke aktiver dobbel skriving-tilordninger for tabeller som krever initialisering, for eksempel tabeller for konto, tilbud, tilbudslinje, ordre og ordrelinje.
7. I kundeengasjementsappen går du til **Avanserte innstillinger \> Systeminnstillinger \> Databehandling \> Duplikatregistreringsregler** og deaktiverer alle reglene.
8. Initialiser tabellene som vises i trinn 2. Hvis du vil ha instruksjoner, kan du se de gjenstående delene i dette emnet.
9. Åpne Finance and Operations-appen og aktiver tabelltilordningene, for eksempel tabelltilordningene for konto, tilbud, tilbudslinje, ordre og ordrelinje. Kjør deretter den innledende synkroniseringen. (Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).) Denne prosessen synkroniserer tilleggsinformasjon fra Finance and Operations-appen, for eksempel behandlingsstatus, forsendelses- og faktureringsadresser, områder og lagre.

## <a name="account-table"></a>Kontotabell

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. I **Relasjonstype**-kolonnen angir du **Kunde** som en statisk verdi. Du ønsker kanskje ikke å klassifisere hver eneste kontooppføring som en kunde i forretningslogikken.
3. Angi kundegruppenummeret fra Finance and Operations-appen i kolonnen **Kundegruppe-ID**. Standardverdien fra løsningen Kundeemne til kontanter er **10**.
4. Hvis du bruker løsningen Kundeemne til kontanter uten å tilpasse **Kontonummer**, angir du en **Kontonummer**-verdi i **Partsnummer**-kolonnen. Hvis det finnes tilpassinger og du ikke vet partsnummeret, henter du denne informasjonen fra Finance and Operations-appen.

## <a name="contact-table"></a>Kontakttabell

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. Angi følgende kolonner, basert på verdien for **IsActiveCustomer** i CSV-filen:

    - Hvis **IsActiveCustomer** er satt til **Ja** i CSV-filen, angir du **Ja** i kolonnen **Kan selges**. Angi kundegruppenummeret fra Finance and Operations-appen i kolonnen **Kundegruppe-ID**. Standardverdien fra løsningen Kundeemne til kontanter er **10**.
    - Hvis **IsActiveCustomer** er satt til **Nei** i CSV-filen, angir du **Nei** i kolonnen **Kan selges** og angir **Kunde** i kolonnen **Kontakt for**.

3. Hvis du bruker løsningen Kundeemne til kontanter uten tilpassing av **Kontaktnummer**, angir du følgende kolonner:

    - Overfør kontaktnummeret fra CSV-filen (**msdynce\_contactnumber**) til kontaktnummeret i **Kontakt**-tabellen (**msdyn\_contactnumber**).
    - Bruk verdier fra **Kontaktnummer**-tabellen i **Partsnummer**-kolonnen.
    - Bruk verdier fra **Kontaktnummer**-tabellen i kolonnen **Kontonummer/Kontaktperson-ID**.

## <a name="invoice-table"></a>Faktura-tabellen

Siden data fra **Faktura**-tabellen er utformet for å flyte én vei, fra Finance and Operations-appen til kundeengasjementsappen, kreves ingen initialisering. Kjør den innledende synkroniseringen for å overføre alle de nødvendige dataene fra Finance and Operations-appen til kundeengasjementsappen. Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).

## <a name="order-table"></a>Ordre-tabellen

1. I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.
2. Kopier verdien i **Ordre-ID**-kolonnen i CSV-filen til kolonnen **Salgsordrenummer**.
3. Kopier verdien i **Kunde**-kolonnen i CSV-filen til kolonnen **Kundefakturanummer**.
4. Kopier verdien i kolonnen **Leveringsland/-område** i CSV-filen til kolonnen **Leveringsland/-område**. Et eksempel på denne verdien er **USA**.
5. Angi kolonnen **Ønsket mottaksdato**. Hvis du ikke bruker en mottaksdato, bruker du kolonnene **Ønsket leveringsdato**, **Fullføringsdato** og **Sendt dato** i CSV-filen. Et eksempel på denne verdien er **2020-03-27T00:00:00Z**.
6. Angi **Språk**-kolonnen. Et eksempel på denne verdien er **nb-no**.
7. Angi **Ordretype**-kolonnen ved å bruke **Varebasert**-kolonnen.

## <a name="order-products-table"></a>Bestill produkter-tabellen

- I **Firma**-kolonnen angir du firmanavnet, for eksempel **USMF**.

## <a name="products-table"></a>Produkter-tabellen

Siden data fra **Produkter**-tabellen er utformet for å flyte én vei, fra Finance and Operations-appen til kundeengasjementsappen, kreves ingen initialisering. Kjør den innledende synkroniseringen for å overføre alle de nødvendige dataene fra Finance and Operations-appen til kundeengasjementsappen. Hvis du vil ha mer informasjon, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tabellene Tilbud og Tilbudsprodukt

Når det gjelder **Tilbud**-tabellen, følger du instruksjonene i [Ordre-tabellen](#order-table) tidligere i dette emnet. Når det gjelder **Tilbudsprodukt**-tabellen, følger du instruksjonene i [Bestill produkter-tabellen](#order-products-table) tidligere i dette emnet.
