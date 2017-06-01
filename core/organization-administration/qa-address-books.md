---
title: "Adressebøker"
description: 
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 568000b37fa067dfd34b4ee0642e4ba6cbe3aa54
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="address-books"></a>Adressebøker

[!include[banner](../includes/banner.md)]




<a name="how-do-i-check-for-duplicate-records"></a>Hvordan kontrollerer jeg duplikate poster?
-------------------------------------

Du kan se etter like poster direkte fra **Global adressebok**-listesiden. I handlingsruten, i fanen **Part** i gruppen **Vedlikehold** klikker du **Kontroller om det finnes duplikater**. Velg deretter verdiene som skal tas med i duplikatkontrollen.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Kan jeg legge til eller slette partsposter samlet fra en adressebok?
Ja, du kan legge til flere partsposter i en adressebok og også fjerne flere partsposter.

-   For å legge til flere partsposter i en adressebok velger du partene i listen på listesiden **Global adressebok**. I handlingsruten i fanen **Part** i gruppen **Vedlikehold**klikker du **Tilordne parter**. Velg adressebøkene der du vil legge til de valgte partspostene, og klikk deretter **OK**. Alle de valgte partspostene legges til i adressebøkene du valgte.
-   For å fjerne flere partsposter fra en adressebok velger du partene i listen på listesiden **Global adressebok**. I handlingsruten i fanen **Part** i gruppen **Vedlikehold**klikker du **Fjern parter**. Velg adressebøkene du vil fjerne partene fra, og klikk deretter **OK**. Alle de valgte partspostene fjernes adressebøkene du valgte.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Kan jeg endre partstypen for en post, eller må jeg slette den gamle posten og opprette en ny?
Noen ganger må du kanskje endre partstypen for en post fra person til organisasjon eller fra organisasjon til person. Nora er eksempelvis medlem av salgsteamet for Fabrikam Storbritannia. På en varemesse i London møter hun seks nye kundeemner. Nora lager en kundeemnepost for parten for hvert kundeemne. Når Nora lagrer postene, opprettes også hver post i den globale adresseboken. Fabrikam har satt standard partstype til organisasjon, men to av de nye kundeemnene bør ha posttypen person. Derfor, når Nora kommer tilbake fra varemessen, må hun endre partstypen for de to kundeemnepostene. Hvis du vil endre en partspost fra én partstype til en annen, må du først opprette en ny partspost av riktig type i den globale adresseboken. Deretter knytter du den gamle partposten til denne nye posten. Når du har gjort den nye partstilknytningen, sletter du den opprinnelige partposten med feil posttype.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Hvordan kan jeg endre navnet eller adressen til en partspost?
Du kan oppdatere navnet på en partspost, og adressene som er knyttet til posten, når som helst.

-   Hvis du vil oppdatere navnet på en partspost, åpner du partsposten, og deretter i handlingsruten klikker du **Rediger**. På **Generelt**-hurtigfanen skriver du inn det nye navnet på parten, og deretter lagrer du posten.
-   For å oppdatere en adresse for en partspost åpner du partsposten og velger adressen som skal oppdateres, på hurtigfanen **Adresser**. Klikk **Rediger**, og gjør deretter de nødvendige endringene i adressen eller adresseparametrene på siden **Rediger adresse**.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Kan jeg slå sammen to eller flere partsposter til én post?
Noen ganger kan det hende at du vil slå sammen to eller flere partsposter til én enkelt post. Dette kan skje hvis du oppretter én eller flere dupliserte partiposter, enten med hensikt eller ved et uhell. Når du fletter partsposter, velger du én oppføring som skal beholdes. Informasjonen fra de andre postene flettes deretter inn i denne posten. Du oppdager for eksempel at informasjon om Fabrikam er lagret i tre partsposter: A, B og C. Du vil beholde partspost A. Derfor vil informasjonen som er lagret i partsposter B og C, slås sammen med partspost A. Det finnes situasjoner der du ikke kan flette partsposter:

-   Du kan ikke flette partsposter som er knyttet til den samme partsrollen, for eksempel kunde eller leverandør, i den samme juridiske enheten. For eksempel er part A knyttet til en kunde i den juridiske enheten 123 og part B er knyttet til en annen kunde i den juridiske enheten 123. Disse partsoppføringene kan ikke slås sammen fordi hvis de ble slått sammen, vil sammenslåtte partsposter være knyttet til flere kunder i samme juridiske enhet, og dette er ikke tillatt. Postene kan imidlertid flettes hvis part B knyttes til en leverandør i den juridiske enheten 123 eller til en kunde i en annen juridisk enhet.
-   Du kan ikke flette interne partiorganisasjonsposter i den samme juridiske enheten, teamet eller driftsenheten.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Bør jeg opprette en partspost i den globale adresseboken eller et annet sted, for eksempel på kunde- eller leverandørsiden?
Du kan angi partsposter i den globale adresseboken eller på den rette enhetssiden. Når du legger til en post på én lokasjon, legges den samme posten alltid til på den andre lokasjonen. Hvis du for eksempel legger til en partspost for en kunde i den globale adresseboken, legges posten også til på **Kunde**-siden. På samme måte legges posten også til i den globale adresseboken hvis du legger til en partspost for en kunde på **Kunde**-siden. Bruk retningslinjene nedenfor for å avgjøre hvor du bør skrive inn nye partsposter:

-   **Opprette en partspost når du ikke vet enhetstypen** – Hvis du må opprette en partspost, men ikke kjenner enhetstypen (for eksempel hvis du ikke vet om enheten er en kunde eller en salgsmulighet), oppretter du posten i den globale adresseboken. Du kan velge enhetstypen senere.
-   **Opprette en partpost når du vet enhetstypen** – Hvis du kjenner enhetstypen for parten, kan du opprette en post på den gjeldende siden for denne typen. Opprett for eksempel en post for en kunde på **Kunde**-siden. Når du oppretter og lagrer en post ved hjelp av riktig enhetsside, opprettes posten automatisk i den globale adresseboken.

## <a name="can-i-translate-address-information-for-party-records"></a>Kan jeg oversette adresseinformasjon for partsposter?
Du kan definere oversettelser av adresseinformasjon slik at informasjonen vises på ditt brukerspråk (systemspråk) i Microsoft Dynamics 365 for Operations, men på et annet språk på dokumenter som salgsordrer. Du kan angi oversettelser for land-/områdenavn, adresseformål og navnerekkefølger. Systemspråket ditt er eksempelvis dansk, og du oppretter en salgsordre for en kunde i Frankrike. I så fall kan du vise kundeposten på dansk i programmet, men vise adresseinformasjonen på fransk på den utskrevne salgsordren. Når du definerer oversettelser, bør du angi en oversettelse for hvert element i listen. Alle elementer som du ikke angir en oversettelse for, vises på systemspråket. Systemspråket ditt er eksempelvis dansk, og du sender et dokument til en kunde i Spania. Hvis du ikke har angitt spanske (ESP) oversettelser for adresseinformasjonen, vil denne informasjonen vises på dansk både i programmet og på det utskrevne dokumentet.




