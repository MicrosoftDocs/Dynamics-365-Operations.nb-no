---
title: Administrere forretningspartnere på B2B-e-handelsnettsteder ved hjelp av Dynamics 365 Sales
description: Denne artikkelen beskriver hvordan du bruker Microsoft Dynamics 365 Sales til å administrere forretningspartnergodkjenninger for bedrift-til-bedrift-e-handelsnettsteder (B2B) for Dynamics 365 Commerce.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ac4aa15f2c6e7f557105254c2c8ce743a9466985
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878627"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Administrere forretningspartnere på B2B-e-handelsnettsteder ved hjelp av Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker Microsoft Dynamics 365 Sales til å administrere forretningspartnergodkjenninger for bedrift-til-bedrift-e-handelsnettsteder (B2B) for Dynamics 365 Commerce. Organisasjoner som allerede har investert i løsningen Dynamics 365 Sales, kan bruke konseptene kundeemne og salgsmulighet for prosessen for godkjenning av forretningspartner i B2B-e-handel.

Hvis du vil ha bakgrunnsinformasjon om prosessen for godkjenning av forretningspartnere i B2B, kan du se [Administrere forretningspartnerbrukere på B2B-e-handelsnettsteder](manage-b2b-users.md).

Potensielle forretningspartnere kan starte innføringsprosessen på et B2B-e-handelsnettsted ved å sende en innføringsforespørsel via en kobling på B2B-nettstedet. Når forespørselen er sendt og de relevante jobbene (for eksempel **P-0001** og **Synkroniser ordrer og kanalforespørsler**) kjøres i Commerce Headquarters, lagres innføringsforespørselen på siden **Alle kundeemner** i Commerce Headquarters. Godkjenningsprosessen for forretningspartnerkundeemner kan deretter fullføres i Sales.

Etter at integreringen mellom Sales og Commerce er aktivert, fører opprettelsen av et forretningspartnerkundeemne i Commerce til at det opprettes et *kundeemne* i Sales.

Illustrasjonen nedenfor viser et eksempel på en side for opprettelse av kundeemner for et forretningspartnerkundeemne i Sales.

![Side for opprettelse av kundeemne i Dynamics 365 Sales.](../media/LeadInSales.png)

I illustrasjonen viser **Kontakt**-delen personen som sendte inn innføringsforespørselen, og **Firma**-delen viser organisasjonen. En merknad i **Tidslinje**-delen angir at kundeemnet ble generert av infrastrukturen for dobbel skriving. Siden det ble opprettet av infrastrukturen for dobbel skriving, vises ikke dette kundeemnet i rullegardinlisten **Mine åpne kundeemner**. Det vises i stedet under en ny visning kalt **Alle B2B-kundeemner for handel**.

Når en bruker «kvalifiserer» kundeemnet, opprettes en *salgsmulighet*-post, en *kontakt*-post og en *konto*-post per standard prosess for kvalifisering av kundeemner i Sales. Infrastrukturen for dobbel skriving brukes til å skrive kontakt- og kontopostene til Commerce. Kontakten opprettes som en kunde av typen *person*, og firmaet opprettes som en kunde av typen *organisasjon*. Hvis en bruker velger **Lukk som vunnet** for salgsmuligheten, godkjennes kundeemnet i Commerce. Godkjenning av et kundeemne gjør at det opprettes et kundehierarki.

Alle gjenværende forretningsprosesser forekommer i Commerce. Disse prosessene omfatter sending av e-post til forretningspartneren, definisjon av kredittgrensebehandling for brukerne og tilføying av flere brukere på B2B-området. Hvis en bruker diskvalifiserer kundeemnet eller merker salgsmuligheten som tapt i stedet for å kvalifisere kundeemnet, merkes kundeemnet i Commerce som avvist, og anmoderen får tilsendt en e-postmelding om at innføringen er avvist.

## <a name="enable-integration-between-sales-and-commerce"></a>Aktivere integrering mellom Sales og Commerce

Integrering mellom Sales og Commerce er avhengig av infrastrukturen for dobbel skriving. Dobbel skriving må derfor aktiveres og fungere, slik at kunder som er opprettet i ett system, skrives til det andre systemet. Hvis du vil ha mer informasjon om infrastrukturen for dobbel skriving, kan du se [Oversikt over dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Etter at konfigurasjonen av dobbel skriving er fullført, kan implementeringspartneren gå til [Microsoft AppSource](https://appsource.microsoft.com/) og søke etter løsningen kalt [Commerce-løsninger for dobbel skriving](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Installer pakken ved hjelp av standard installasjonsveiviser, og test den deretter ved å opprette et kundeemne på et B2B-område. Etter at kundeemnet er opprettet, kontrollerer du at forespørselen vises i **Alle kundeemner** i Commerce, og deretter kontrollerer du at kundeemnet vises som et kundeemne i Sales.

## <a name="additional-resources"></a>Tilleggsressurser

[Administrere forretningspartnerbrukere på B2B-e-handelssider](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
