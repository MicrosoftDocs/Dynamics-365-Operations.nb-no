---
title: Utvide Talent med Power Apps og Power Automate
description: Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36b8145764338b91bfedf96c43a7137a89831742
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410110"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Utvide med Power Apps og Power Automate

Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø. Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.

> [!IMPORTANT]
> Hvis du vil bruke malene og appene som er beskrevet i dette emnet, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.

## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.
- Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.

## <a name="integration-with-office-365-power-automate"></a>Integrering med Office 365, Power Automate

**Integrering med Office 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft Office 365. Den refererer til arbeidere i Human Resources for å trekke ut identifikasjonstyper for ansatte. Ledere kan kontrollere utløpsdatoer for ansatt-ID-typer. De kan også sende en e-postpåminnelse hvis ansatt-ID-typen utløper. Power Automate integreres med Power Apps for å sende denne påminnelsen. Bekreftelse vil bli sendt tilbake til Power Apps fra Power Automate når påminnelsen sendes. Identifikasjonstyper omfatter førerkort, pass og andre godkjente former for ID.

Du kan utvide denne appen til andre scenarier. Du kan for eksempel bruke den til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.

Du kan laste ned appen for **integrering med Office 365, Power Automate** ved å gå til [Integrering med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) i Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-tilkobling og kjøring

Malen **Power Automate – SQL-tilkobling og kjøring** kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.

Selv om denne malen leser og oppdaterer SQL-tabeller, kan du utvide den og bruke den i andre scenarioer. Du kan for eksempel bruke den til å fylle ut en oppsamlingstabell i Common Data Service med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.

Avansert spørring integreres med flyt for å muliggjøre datatransformering og trinnvis push.

For å laste ned malen **Power Automate – SQL-tilkobling og kjøring** kan du gå til [Power Automate – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.

## <a name="additional-resources"></a>Tilleggsressurser

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>