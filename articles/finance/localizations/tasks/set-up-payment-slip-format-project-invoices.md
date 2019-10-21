---
title: Definere format for betalingsbilag for prosjektfakturaer
description: Bedrifter knytter vanligvis utskrevne betalingsbilag til fakturaer som skal hjelpe kunder og gi en betalingsreferanse for postering og utligning.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4671e1df3bc86361736b5882d67e6b160b4c5644
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174983"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Definere format for betalingsbilag for prosjektfakturaer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bedrifter knytter vanligvis utskrevne betalingsbilag til fakturaer som skal hjelpe kunder og gi en betalingsreferanse for postering og utligning. Betalingsbilaget kan brukes til prosjekt- eller tjenestefakturaer, purringer, rentenotaer og kontoutdrag, i tillegg til salgsfakturaer og fritekstfakturaer. Hvis du vil bruke betalingsbilag, må du først definere vedleggsformatene for kreditorens identifikasjonsnummer og betalingsbilag.

Denne fremgangsmåten bruker demonstrasjonsfirmaet DEMF. 

Denne funksjonen er tilgjengelig for juridiske enheter med primæradresse i Danmark.


## <a name="set-up-a-creditor-id-number"></a>Definere et ID-nummer for kreditor
1. Gå til Organisasjonsstyring > Organisasjoner > Juridiske enheter.
2. Vis eller skjul delen Bankkontoinformasjon.
3. Klikk Rediger.
4. Skriv inn en verdi i feltet ID for FI-kreditor.
5. Klikk Lagre.
6. Lukk siden.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Definere et betalingsbilagsformat for fakturaer, notater, brev og utdrag
1. Gå til Kunder > Oppsett > Skjemaer > Skjemaoppsett.
2. Klikk kategorien Faktura.
3. Velg et alternativ i feltet Tilknyttet betalingsvedlegg på kundefaktura.
    * Ingen – Ikke skriv ut et betalingsbilag. Velg dette alternativet hvis betalingsbeløpet er i en annen valuta enn norske kroner (NOK).   FIK 751 – Skriv ut et FIK 751-betalingsbilag hvis du har tenkt å skrive betalingsbeløpet og forfallsdatoen manuelt på betalingsbilaget.   FIK 752 – Skriv ut et FIK 752-betalingsbilag hvis du har tenkt å bruke et datamaskingenerert betalingsbilag med forhåndsutskrevet betalingsbeløp og forfallsdato.  
4. Klikk Lagre.
5. Klikk kategorien Fritekstfaktura.
6. Velg et alternativ i feltet Tilknyttet betalingsvedlegg på fritekstfaktura.
    * Ingen – Ikke skriv ut et betalingsbilag. Velg dette alternativet hvis betalingsbeløpet er i en annen valuta enn norske kroner (NOK).   FIK 751 – Skriv ut et FIK 751-betalingsbilag hvis du har tenkt å skrive betalingsbeløpet og forfallsdatoen manuelt på betalingsbilaget.   FIK 752 – Skriv ut et FIK 752-betalingsbilag hvis du har tenkt å bruke et datamaskingenerert betalingsbilag med forhåndsutskrevet betalingsbeløp og forfallsdato.  
7. Klikk Lagre.
8. Klikk kategorien Fritekstfaktura.
9. Velg et alternativ i feltet Tilknyttet betalingsvedlegg på rentenota.
    * Ingen – Ikke skriv ut et betalingsbilag. Velg dette alternativet hvis betalingsbeløpet er i en annen valuta enn norske kroner (NOK).   FIK 751 – Skriv ut et FIK 751-betalingsbilag hvis du har tenkt å skrive betalingsbeløpet og forfallsdatoen manuelt på betalingsbilaget.   FIK 752 – Skriv ut et FIK 752-betalingsbilag hvis du har tenkt å bruke et datamaskingenerert betalingsbilag med forhåndsutskrevet betalingsbeløp og forfallsdato.  
10. Klikk Lagre.
11. Klikk kategorien Purring.
12. Velg et alternativ i feltet Tilknyttet betalingsvedlegg på purring.
    * Ingen – Ikke skriv ut et betalingsbilag. Velg dette alternativet hvis betalingsbeløpet er i en annen valuta enn norske kroner (NOK).   FIK 751 – Skriv ut et FIK 751-betalingsbilag hvis du har tenkt å skrive betalingsbeløpet og forfallsdatoen manuelt på betalingsbilaget.   FIK 752 – Skriv ut et FIK 752-betalingsbilag hvis du har tenkt å bruke et datamaskingenerert betalingsbilag med forhåndsutskrevet betalingsbeløp og forfallsdato.  
13. Klikk Lagre.
14. Klikk kategorien Kontoutdrag.
15. Velg et alternativ i feltet Tilknyttet betalingsvedlegg på kontoutdrag.
    * Ingen – Ikke skriv ut et betalingsbilag. Velg dette alternativet hvis betalingsbeløpet er i en annen valuta enn norske kroner (NOK).   FIK 751 – Skriv ut et FIK 751-betalingsbilag hvis du har tenkt å skrive betalingsbeløpet og forfallsdatoen manuelt på betalingsbilaget.   FIK 752 – Skriv ut et FIK 752-betalingsbilag hvis du har tenkt å bruke et datamaskingenerert betalingsbilag med forhåndsutskrevet betalingsbeløp og forfallsdato.  
16. Klikk Lagre.
17. Lukk siden.
