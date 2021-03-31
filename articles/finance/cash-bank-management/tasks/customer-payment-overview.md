---
title: Oversikt over kundebetaling
description: Denne oppgaveveiledningen hjelper deg med forskjellige metoder som brukes til å angi kundebetalinger.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e93703815d899baa7045f2c5f1e0323944e91c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225423"
---
# <a name="customer-payment-overview"></a>Oversikt over kundebetaling

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen hjelper deg med forskjellige metoder som brukes til å angi kundebetalinger. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Moduler > Kunder > Betalinger > Betalingsjournal** i navigasjonsruten.
2. Klikk på **Ny**.
3. Velg betalingsjournalen som kundebetalingene skal lagres i.
4. Velg eller angi journalen manuelt.
5. Klikk på **Angi kundebetalinger** **handlingsruten**. Angi kundebetalinger som brukes til å registrere én kundebetaling om gangen. Du kan angi betalingsinformasjon øverst, og deretter kan du merke fakturaene som ble betalt med betalingen, alt fra samme side.  
6. Angi kunden som du har mottatt betalingen fra. Hvis du ikke kjenner til kunden, men kjenner en transaksjon som ble betalt, kan du bruke feltet Transaksjon til å angi betalingen. Angi eller velg fakturaen i feltet Transaksjon. Kunden angis som standard automatisk når du har valgt transaksjonen.
7. I feltet **Betalingsreferanse** angir du en betalingsreferanse. Betalingsreferansen kan være kundens sjekknummer eller en referanse fra kundens elektroniske betaling. Betalingsreferansen er bare nødvendig hvis du merker å inkludere betalingen på et betalingsbilag.  
8. I feltet **Betalingsbilag** velger du om betalingen skal tas med i et betalingsbilag. 
9. Angi beløpet for kundebetalingen i **Beløp**-feltet. Betalingsbeløpet angis ikke som standard. Det må angis manuelt. 
10. Merk fakturaene som ble betalt av kunden. Hvis betalingen er en forskuddsbetaling, trenger du ikke å merke alle fakturaer for utligning. Betalingen kan fremdeles lagres og posteres. Utligning mot en faktura kan skje på et senere tidspunkt.
11. Angi betalingsbeløpet som skal utlignes mot den merkede fakturaen. Dette feltet kan brukes når betalingen gjelder en delbetaling. Hvis du ikke angir et beløp, bestemmes beløpet som skal utlignes automatisk for deg.
12. Klikk på **Lagre i journal**. Før du lagrer betalingen i journalen, må du kontrollere at motkontoen er definert. Ved hjelp av **Lagre i journal** lagres betalingen og flyttes til journalen. Du kan deretter fortsette å angi den neste betalingen.
13. Lukk siden.
14. I **Handlingsrute** klikker du på Linjer. Når du åpner Linjer, vises eventuelle betalinger du registrert på siden **Angi kundebetalinger** og lagret i journalen. Du kan også bruke denne siden til å angi nye kundebetalinger, eller redigere eksisterende kundebetalinger før de posteres.
15. Klikk på **Ny** for å opprette en annen betaling. 
16. Velg kunden som du har mottatt betalingen fra. Hvis du ikke kjenner til kunden, men kjenner en faktura betalt av betalingen, kan du bruke feltet Faktura til å manuelt angi eller velge fakturaen. Kunden angis som standard når fakturaen er valgt.  
17. Klikk **Utlign transaksjoner** hvis du vil merke fakturaene som ble betalt. Du trenger ikke å utligne betalingen mot noen fakturaer. Hvis dette er en forskuddsbetaling, eller hvis du ikke vet hvilken faktura som er betalt, kan du angi og postere betalingen. Betalingen kan utlignes mot en faktura på et senere tidspunkt.  
18. Merk fakturaene som betalt av betalingen. 
19. I **Beløp**-feltet angir du betalingsbeløpet som skal utlignes mot fakturaen.
20. Klikk **OK**.
21. I feltet **Betalingsreferanse** angir du en betalingsreferanse. Betalingsreferansen er bare nødvendig hvis du merker å inkludere betalingen på et betalingsbilag.  
22. Klikk på **Poster** i **handlingsruten** for å postere kundebetalingene. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]