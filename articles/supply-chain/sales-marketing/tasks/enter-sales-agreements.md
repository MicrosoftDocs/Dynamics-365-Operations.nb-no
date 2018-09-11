--- 
title: Angi salgsavtaler
description: "Denne prosedyren viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a>Angi salgsavtaler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et

avtalt beløp over tid, i bytte mot spesialrabatter. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-sales-agreement-header"></a>Definere topptekst i salgsavtale
1. Gå til Salg og markedsføring > Salgsavtaler > Salgsavtaler.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk rullegardinknappen i feltet Salgsavtaleklassifisering for å åpne oppslaget.
7. Klikk koblingen i den valgte raden i listen.
8. Utvid delen Generelt.
9. Velg Produktverdiforpliktelse i feltet Standardforpliktelse.
    * En forpliktelsestype er et obligatorisk vilkår som du må tilordne til avtalen for å definere hvordan avtalekontrakten skal oppfylles. De fire forhåndsdefinerte typene lar deg definere kundens forpliktelsesmål, uttrykt som et antall eller en verdi. Forpliktelsestypen for antall kan bare brukes for et bestemt produkt, men de verdibaserte typene gjelder for salg av både spesifikke og ikke-spesifikke produkter.  
10. I Utløpsdato-feltet kan du sette datoen til en fremtidig dato som du vil at avtalen skal utløpe på.
11. Klikk OK.

## <a name="set-up-product-value-commitment-lines"></a>Definere produktverdiforpliktelseslinjer
1. Klikk Legg til linje.
2. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
    * Typen forpliktelse som du har valgt for avtalen, påvirker hva slags informasjon du kan angi for avtalelinjene. For en verdibasert avtale må du for eksempel angi det totale nettobeløpet (i valutaen som er avtalt) som kunden har forpliktet seg til ved kjøpet av varer fra deg. I dette eksemplet vil feltene Antall og Enhet på linjen være utilgjengelige fordi du oppretter en avtale for kunden om å kjøpe en bestemt verdi av et produkt.   
5. Angi pengebeløpet som kunden har forpliktet seg til å kjøpe, i Nettobeløp-feltet.
6. Angi en prosentverdi som skal gjelde for kundens salgsordrelinjer som er knyttet til denne avtalen, i Rabattprosent-feltet.
7. Vis seksjonen Linjedetaljer.
8. Velg Ja i Maks. håndheves-feltet.
    * Hvis du velger Maks. håndheves, betyr det at totalbeløpet for alle salgsordrelinjene som bruker forpliktelsens spesialpriser, rabatter og/eller betalingsbetingelser, ikke må overskride beløpet som er angitt i forpliktelsen.  
    * Minimums- og maksimumsfrigivelsesbeløpene angir et verdiområde som må selges på hver salgsordre som bruker den valgte avtalen.   
9. Vis delen Topptekst i salgsavtale.
    * Med mindre statusen for avtalen er satt til Gjeldende, kan ikke salgsordrer knyttes til avtalen, og derfor ikke bidra til oppfyllelse av avtalen. Du kan endre statusen manuelt på dette stadiet. Statusen vil imidlertid vanligvis endres når du bekrefter avtalen for kunden.  
10. Klikk Salgsavtale i handlingsruten.
11. Klikk Bekreftelse.
    * Kontroller at alternativet Merk avtale som gyldig er satt til Ja.  
12. Velg Ja i feltet Skriv ut rapport.
13. Klikk OK.
14. Lukk siden.
    * Avtalen er nå gyldig, og du kan begynne å koble kundens ordrer til avtalen for å motregne mot forpliktelsesmålet.  


