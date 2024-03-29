---
title: Opprette elektroniske signaturer
description: Bruk denne prosedyren for å definere elektroniske signaturer.
author: maertenm
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4075e47013bb6a3f42cb07f88df121cef8688463cab25c4a734c5363106ace4c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749538"
---
# <a name="set-up-electronic-signatures"></a>Opprette elektroniske signaturer

[!include [banner](../../includes/banner.md)]

Bruk denne prosedyren for å definere elektroniske signaturer. En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess. Demonstrasjonsdatafirmaet DAT brukes til å opprette denne fremgangsmåten.


## <a name="enable-the-electronic-signature-configuration-key"></a>Aktivere konfigurasjonsnøkkelen for elektronisk signatur
1. Gå til Systemadministrasjon > Oppsett > Lisenskonfigurasjon.
2. Utvid Administrasjon i treet.
    * Verifiser at det er merket av for Elektronisk signatur.  
    * Hvis det ikke er merket av for Elektronisk signatur, må du aktivere vedlikeholdsmodus. Vedlikeholdsmodus kan aktiveres i dette miljøet ved å kjøre en vedlikeholdsjobb fra Lifecycle Services, eller ved hjelp av verktøyet Deployment.Setup lokalt.  
3. Lukk siden.

## <a name="set-up-electronic-signature-parameters"></a>Definere parametere for elektronisk signatur
1. Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Parametere for elektronisk signatur.
2. Klikk på Rediger.
3. Skriv inn en verdi i feltet Varsel.
    * Angi varselet som signatarer vil motta når det bes om en signatur. Du kan skrive inn hvilken som helst tekst. Vanligvis forteller denne teksten brukeren hva det betyr å signere et dokument elektronisk.  
    * Hvis du vil angi varselteksten på flere språk, klikker du knappen Oversettelser.  
4. Klikk på Lagre.
5. Lukk siden.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Definere årsakskoder for elektroniske signaturer
1. Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Årsakskoder for elektronisk signatur.
2. Klikk på Ny.
    * Du må definere årsakskoder før bruk av elektroniske signaturer. Det kreves en gyldig årsakskode ved signering av et dokument.     En signatar velger en årsakskode for å angi formålet med en elektronisk signatur. En årsakskode kan for eksempel brukes til å angi juridisk godkjenning.  
3. Skriv inn en verdi i feltet Årsakskode.
4. Skriv inn en verdi i feltet Beskrivelse.
    * Angi flere årsakskoder, om nødvendig.  
5. Klikk på Lagre.
6. Lukk siden.

## <a name="require-electronic-signatures-for-existing-processes"></a>Kreve elektroniske signaturer for eksisterende prosesser
1. Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Krav til elektronisk signatur.
2. Finn og velg ønsket post i listen.
    * Velg en prosess som krever elektroniske signaturer.  
3. Merk av eller fjern merket i avmerkingsboksen Signatur nødvendig.
    * Gjenta disse trinnene for hver prosess som krever elektroniske signaturer.  
4. Klikk på Lagre.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Opprette et egendefinert krav til elektroniske signaturer
1. Klikk på Ny.
2. Merk av eller fjern merket i avmerkingsboksen Signatur nødvendig.
3. I Navn-feltet angir du et navn på prosessen som krever elektroniske signaturer.
4. Klikk på rullegardinknappen i feltet Tabellnavn for å åpne oppslaget.
5. Finn og velg tabellen der dataene må signeres og lagres, i listen.
6. Klikk på koblingen i den valgte raden i listen.
7. Klikk på rullegardinknappen i feltet Feltnavn for å åpne oppslaget.
8. Finn og velg feltet i tabellen som du vil overvåke, i listen.
9. Klikk på koblingen i den valgte raden i listen.
    * Angi når det kreves en signatur.     Velg Alltid hvis det kreves en signatur når dataene i feltet endres.     Velg Bare hvis det bare kreves en signatur under bestemte vilkår. Hvis du velger Bare, må du også velge ett av følgende alternativer: Når en post settes inn, Når en post oppdateres eller Når en post slettes.  
10. Klikk på Lagre.
11. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]