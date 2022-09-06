---
title: Datadeling til gavekort på tværs af virksomhed
description: Denne artikel beskriver, hvordan du konfigurerer funktionen Microsoft Dynamics 365 Commerce til deling af Dynamics 365 Finance-data på tværs af dataområder til synkronisering af gavekortdata.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387063"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Datadeling til gavekort på tværs af virksomhed

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel beskriver, hvordan du konfigurerer funktionen Microsoft Dynamics 365 Commerce så det bruger Dynamics 365 Finance-data på tværs af dataområder til synkronisering af gavekortdata. Funktionen til deling af datapost kan derefter bruges til deling af data på tværs af virksomheder mellem to dataområder. På denne måde kan den interne Commerce-gavetabel dele data mellem to firmaenheder. Yderligere oplysninger om Dynamics 365 Finance-deling af data på tværs af virksomheder finder du i [datadeling på tværs af virksomheder](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Virksomhed | Den juridiske enhed i Dynamics 365 Finance-miljøet. |
| Gavekort | Det interne Dynamics 365 Commerce-gavekortprodukt. |

## <a name="prerequisites"></a>Forudsætninger

Brugerne skal konfigurere deres miljø til deling af data på tværs af virksomheder som beskrevet i [deling af data på tværs af virksomheder](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

Feltet **DataSharingType** skal være angivet til **Dupliker** i **RetailGiftCardTable** for at aktivere deling af dubletter af poster (US) for tabellen Gavekort. Du kan finde flere oplysninger under [Dele data på tværs af virksomheder for udviklere](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigurere datadeling til gavekort på tværs af virksomhed

Konfigurere datadeling til gavekort på tværs af virksomhed ved at følge disse trin.

1. I Commerce Headquarters gå til **Systemadministration \> Opsætning \> Konfigurer datadeling på tværs af firma**.
1. Vælg **Ny** i handlingsruden for at tilføje en datadelingspost.
1. I feltet **Navn** skal du angive et navn på posten til deling af data (f.eks. **gavekort**).
1. Vælg **Tilføj** i sektionen **tabeller og felter, der skal deles**.
1. I feltet **Tabelnavn** i dialogboksen **Del ny tabel** skal du angive **RETAILGIFTCARDTABLE** (tabellen til detailgavekort). Feltet **Tabellabel** skal automatisk angives til **Gavekorttabel**.
1. Kontroller, at afkrydsningsfelterne **Gem data pr. regnskab**, **Har entydigt indeks** og **Endnu ikke delt** er markeret. Markering af disse afkrydsningsfelter udløser valideringer, der er knyttet til funktionen til deling af data.
1. Vælg **Tilføj tabel**. Posten **Gavekorttabel (RetailGiftCardTable)** skal nu vises under **tabeller og felter, der skal deles**. Vælg caret-symbolet (^) for at få vist alle de tabelfelter, der automatisk er knyttet til tabellen til deling.
1. I afsnittet **Firmaer, der deler posterne i disse tabeller**, skal du vælge **Tilføj** for at tilføje et regnskab, du vil dele data med.
1. Vælg et regnskab på rullelisten i rækken under **Regnskab**.
1. I feltet **Navn** skal du skrive firmanavn.
1. Gentag trin 8 til 10 for at tilføje flere firmarækker.
1. Når du er færdig med at tilføje firmarækker, skal du vælge **Aktivér** i handlingsruden.
1. Du modtager en advarsel, der viser "Det anbefales, at du kun udfører denne handling uden for arbejdstiden. Eventuelle samtidige transaktionshandlinger mislykkes for tabeller i politikken. Vil du fortsætte?" Vælg **Ja** for at bekræfte.
1. Du modtager en advarsel, der angiver, "Vil du kopiere alle eksisterende data på tværs af alle delte firmaer nu?" Vælg **Ja** for at bekræfte.

Når du accepterer begge meddelelser, begynder tabeller at kopiere data på tværs af de konfigurerede regnskaber. Saldi, der opstår i forhold til et firmagavekort, vil derefter være synlige for det andet firma.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](payments-retail.md)

[Betalingsmodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
