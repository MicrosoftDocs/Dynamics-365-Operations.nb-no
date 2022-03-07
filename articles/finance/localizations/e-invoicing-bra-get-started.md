---
title: Komme i gang med Elektronisk fakturering for Brasil
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Brasil i Finance and Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 82bbf806d207af0b15406e4bec516420db7f2c06
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984859"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Komme i gang med Elektronisk fakturering for Brasil 

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Brasil. Emnet veileder deg gjennom konfigurasjonstrinnene som er landavhengige i RCS (Regulatory Configuration Services), og utfyller trinnene som beskrives i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering for brasiliansk NF-e (BR)

Noen av parameterne fra funksjonen **Elektronisk fakturering for brasiliansk NF-e (BR)** publiseres med standardverdier. Gå gjennom og oppdater om nødvendig verdiene slik at bedre gjenspeiler forretningsoperasjonen din, før du distribuerer funksjonen for elektronisk fakturering til servicemiljøet.

Denne delen utfyller delen **Landspesifikk konfigurasjon for funksjon for elektronisk fakturering** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NF-e (BR)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. Velg **Send** i fanen **Oppsett** i rutenettet, og velg deretter **Rediger.**
5. Velg handlingen **(Forhåndsversjon) Signer XML-dokument** i feltgruppen **Handlinger** i fanen **Handlinger**.
6. Velg **Sertifikatnavn** i feltgruppen **Parametere**, og angir navnet på sertifikatet som er knyttet til Key Vault-parameteren, i feltet **Verdi**.
7. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
8. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
9. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av SEFAZ-dokumentasjonen for din stat, og deretter velger du **Lagre.**
10. I feltgruppen **Oppsett av relevansregler** i fanen **Relevansregler** går du gjennom og oppdaterer kriteriene for feltet **Tilstand** som obligatoriske for den samme tilstanden som URL-adressen for webtjenestene refererer til.
11. Velg **Lagre** og lukk siden.
12. Hvis du vil distribuere funksjonen for elektronisk fakturering til servicemiljøet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsett for funksjon for elektronisk fakturering for brasiliansk NF-e (BR)

Fullfør disse trinnene før du distribuerer programoppsettet til det tilkoblede programmet i Finans eller Supply Chain Management.

Denne delen utfyller delen **Landspesifikk konfigurasjon for programoppsett** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NF-e (BR)** er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. I fanen **Oppsett** velger du **Programopsett**, og i feltet **Tilkoblet program** velger du programmet der du vil distribuere.
5. I feltet **Tabellnavn** kontrollerer du at **Regnskapsdokumenthode** er valgt.
6. Velg **Svartyper**, og velg deretter **Ny**.
7. I feltet **Svartype** angir du "Svar" som en fast verdi, og i feltet **Beskrivelse** skriver du inn "Beskrivelse".
8. I feltet for **innsendingsstatus** velger du **Venter**.
9. I feltet **Modelltilordning** velger du **Modelltilordning fra svarmelding** med **(Forhåndsversjon) Format for import av svarmelding**, og deretter velger du **Lagre**.
10. Velg **Ny**, i feltet **Svartype** angir du "Svardata" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
11. I feltet for **innsendingsstatus** velger du **Venter**.
12. I feltet **Modelltilordning** velger du **Import av svardata** med **(Forhåndsversjon) Format for import av NF-e-svardata (BR)**, og deretter velger du **Lagre**.
13. Hvis du vil distribuere programoppsettet til det tilkoblede programmet i Finans eller Finance or Supply , kan du se [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR)

Noen av parameterne fra funksjonen **Elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR)** publiseres med standardverdier. Gå gjennom og oppdater om nødvendig verdiene slik at de passer bedre til forretningsoperasjonsbehovene, før du distribuerer funksjonen for elektronisk fakturering til servicemiljøet.

Denne delen utfyller delen **Landspesifikk konfigurasjon for funksjon for elektronisk fakturering** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NFS-e ABRASF Curitiba (BR)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt, og i fanen **Oppsett** i rutenettet velger du **Send**.
4. Velg **Rediger**, og i feltgruppen **Handlinger** i fanen **Handlinger** velger du den første forekomsten av **(Forhåndsversjon) Signer XML-dokument**.
5. Velg **Sertifikatnavn** i feltgruppen **Parametere**.
6. I feltet **Verdi** angir du navnet på sertifikatet som er knyttet til Key Vault-parameteren.
7. I feltgruppen **Handlinger** velger du den andre forekomsten av **(Forhåndsvis) Signer XML-dokument**.
8. Velg **Sertifikatnavn** i feltgruppen **Parametere**.
9. I feltet **Verdi** angir du navnet på sertifikatet som er knyttet til Key Vault-parameteren.
10. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
11. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
12. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av skattemyndighetene i byen Curitiba, og deretter velger du **Lagre.**
13. Velg **Forespør** i fanen **Oppsett** i rutenettet, og velg deretter **Rediger.**
14. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
15. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
16. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av skattemyndighetene i byen Curitiba.
17. Velg **Lagre** og lukk deretter siden.
18. Hvis du vil distribuere funksjonen for elektronisk fakturering til servicemiljøet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsett for funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR)

Fullfør disse trinnene før du distribuerer programoppsettet til det tilkoblede programmet i Finans eller Supply Chain Management.

Denne delen utfyller delen **Landspesifikk konfigurasjon for programoppsett** i emnet [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS, i **Funksjoner**-delen i arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering**.
2. På siden **Funksjoner for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NFS-e ABRASF Curitiba (BR)**, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt, og i fanen **Oppsett** i rutenettet velger du **Programoppsett**.
4. Velg programmet du vil distribuere til, i feltet **Tilkoblet program**.
5. I feltet **Tabellnavn** kontrollerer du at regnskapsdokumenthodet er valgt.
6. Velg **Svartyper** og deretter **Ny**.
7. I feltet **Svartype** angir du "ABRASFCuritibaSendSvar" som en fast verdi, og i feltet **Beskrivelse** skriver du inn "Beskrivelse".
8. I feltet for **innsendingsstatus** velger du **Venter**.
9. I feltet **Modelltilordning** velger du **Import av svarmelding** med **(Forhåndsversjon) Import av svarmelding for NFS-e-ABRASF Curitiba (BR)**, og deretter velger du **Lagre**.
10. Velg **Ny**, i feltet **Svartype** angir du "ABRASFCuritibaSendSvardata" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
11. I feltet for **innsendingsstatus** velger du **Venter**.
12. I feltet **Modelltilordning** velger du **Import av svardata** med **(Forhåndsversjon) Format for import av svardata for NFS-e-ABRASF (BR)**, og deretter velger du **Lagre**.
13. Velg **Ny**, i feltet **Svartype** angir du "ABRASFCuritibaForespørSvar" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
14. I feltet for **innsendingsstatus** velger du **Venter**.
15. I feltet **Modelltilordning** velger du **Import av svarmelding** med **(Forhåndsversjon) Import av svarmelding for NFS-e-ABRASF Curitiba (BR).**
16. Velg **Lagre** og lukk siden.
17. Hvis du vil distribuere programoppsettet til det tilkoblede programmet i Finans eller Finance or Supply , kan du se [Komme i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Personvernerklæring
Aktivering av funksjonene **NF-e Føderal – Brasiliansk elektronisk fakura (BR)** og **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)** kan kreve at begrensede data sendes, inkludert skatteregistrerings-ID-en for organisasjonen. Disse dataene blir overført til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. Som administrator kan du aktivere eller slå av funksjonene **NF-e Føderal – Brasiliansk elektronisk faktura (BR)** og **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)**. Følgende fremgangsmåte viser hvordan du gjør dette: 

1. Gå til **Organisasjonsstyring** > **Oppsett** > **Parametere for elektronisk dokument**. 
2. I fanen **Funksjoner** velger du raden som inneholder funksjonen **NF-e Føderal – Brasiliansk elektronisk faktura (BR)** eller **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)** og velger funksjonen. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
