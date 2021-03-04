---
title: Oppfylle salgsavtaler
description: Denne fremgangsmåten viser hvordan du kan oppfylle en salgsavtale ved å knytte salgsordrer til den.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3a35c7140b886f931df48e583b1582201b6547
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434210"
---
# <a name="fulfill-sales-agreements"></a>Oppfylle salgsavtaler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du kan oppfylle en salgsavtale ved å knytte salgsordrer til den. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Før du starter denne veiledningen kontroller at du har en gyldig salgsavtale av typen "Produktverdiforpliktelse". Du kan også kjøre oppgaveveiledningen kalt "Opprette salgsavtaler".  




## <a name="release-a-sales-order-from-the-agreement"></a>Frigi en salgsordre fra avtalen
1. Gå til Salg og markedsføring > Salgsavtaler > Salgsavtaler.
2. Åpne avtalen som du vil frigi ordren mot, i listen.
3. Klikk Salgsavtale i handlingsruten.
4. Klikk Frigivelsesordre.
    * Som teksten øverst på siden Opprett frigivelsesordre påpeker vil detaljene som kreves for salgsordrelinjene variere avhengig av om avtalen er antalls- eller verdibasert.  
    * Avtalen i denne veiledningen er av typen "Produktverdiforpliktelse". Det er derfor seksjonen Linjer på denne siden er tom. Hvis forpliktelsen var basert på antallet, ville linjeinformasjonen bli kopiert fra avtalen.  
5. Klikk Opprett.
    * Meldingen forteller deg at en salgsordre er blitt opprettet. Ettersom bestillingen ikke inneholder noen linjer, må du legge til ordrelinjedetaljer for å fullføre frigivelsesprosessen.   
6. Lukk siden.
7. Lukk siden.
8. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
9. Finn og åpne ordren som ble opprettet som et resultat av ordrefrigivelsen i den forrige oppgaven, i listen.
10. Klikk Legg til linje.
11. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
12. I Varenummer-feltet skriver du inn eller velger varen som er angitt på den tilknyttede salgsavtalen.
13. Angi et tall i feltet Antall.
    * Pass på at du angir et antall som bringer nettobeløpet under verdien for den tilknyttede salgsavtalen.  
    * Legg merke til at fordi salgsordren er knyttet til avtalen, brukes den avtalte rabattprosenten på ordrelinjen.  
14. Klikk Oppdater linje.
15. Klikk Vedlagt.
    * Siden Tilknyttet avtale viser ID-en og betingelsene i avtalen som linjen er frigitt fra.  
16. Lukk siden.
17. Klikk Generelt i handlingsruten.
18. Klikk Tilknyttet salgsavtalelinje.
19. Vis seksjonen Linjedetaljer.
20. Klikk kategorien Oppfyllelse.
    * Kategorien Oppfyllelse viser et sammendrag av alle salgsordrelinjer som er knyttet til denne forpliktelsen, og oppfyllelsestilstanden, i tillegg til beløpet eller antallet som ennå ikke er frigitt.   
21. Lukk siden.
22. Lukk siden.
23. Lukk siden.

## <a name="apply-sales-agreement-in-the-order-process"></a>Bruke salgsavtale i ordreprosessen
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg kunden som er angitt i salgsavtalen, i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Utvid delen Generelt.
7. Klikk rullegardinknappen i feltet Salgsavtale-ID for å åpne oppslaget.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk Ja.
10. Klikk OK.
11. Merk den valgte raden i listen.
12. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
13. I Varenummer-feltet skriver du inn eller velger varen som er angitt på den tilknyttede salgsavtalen.
14. Klikk koblingen i den valgte raden i listen.
15. Klikk Lagre.
16. Klikk Plukk og pakk i handlingsruten.
17. Klikk Poster følgeseddel.
18. Utvid seksjonen Parametere.
19. Velg Ja i feltet Postering.
20. Klikk OK.
21. Klikk OK.
22. Klikk Generelt i handlingsruten.
23. Klikk Tilknyttet salgsavtalelinje.
24. Klikk kategorien Oppfyllelse.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]