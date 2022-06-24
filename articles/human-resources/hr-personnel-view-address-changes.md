---
title: Få vist og administrere adresseændringer
description: Denne artikel forklarer, hvordan du kan se og administrere adresseændringer i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 744ab532fcc663f25ce376817779924bbef15432
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899579"
---
# <a name="view-and-manage-address-changes"></a>Få vist og administrere adresseændringer


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel forklarer, hvordan du kan se og administrere adresseændringer på siden **Rediger personlige oplysninger** (åbnes i arbejdsområdet **Medarbejderselvbetjening**) eller detaljesiden for **Arbejder** i Dynamics 365 Human Resources.

Mange virksomheder ønsker, at medarbejderne kan administrere deres egne personlige oplysninger via en selvbetjeningsløsning. Du kan give brugerne mulighed for at opdatere deres adresse i arbejdsområdet **Medarbejderselvbetjening**. Du kan derefter overvåge disse ændringer i arbejdsområdet **Personalestyring**. Hvis du vil bruge denne funktion, skal du angive det antal dage, du vil have vist ændringer på siden **Parametre for personale**.

## <a name="configure-address-change-parameters"></a>Konfigurere parametre for adresseændring

Hvis du vil konfigurere det antal dage, du ønsker, at adresseændringer vises i arbejdsområdet **Personalestyring**, skal du udføre disse trin:

1. Vælg **Personalestyring** i navigationsruden.
2. Vælg **Links**.
3. Vælg **Parametre for personale**.
4. Angiv det antal dage, som adresseændringerne skal vises, i feltet **Antal dage** under **Adresseændring** i arbejdsområdet **Personalestyring**.
5. Luk siden.

## <a name="create-or-change-an-employee-address"></a>Oprette eller ændre en medarbejders adresse

Medarbejdere kan opdatere deres egen adresse i arbejdsområdet **Medarbejderselvbetjening**. Benyt denne fremgangsmåde for at oprette eller ændre en adresse:

1. Vælg feltet **Medarbejderselvbetjening** på **Startside**.
2. Vælg **Rediger personlige oplysninger**.
3. Vælg **Tilføj** for at tilføje en adresse. Hvis du vil opdatere en eksisterende adresse, skal du vælge adressen fra listen og derefter vælge **Rediger**.
4. Angiv **Navn eller beskrivelse**.
5. Vælg rullelisten **Formål**, og vælg derefter typen af adresse.
6. Angiv **Land/område**.
7. Angiv **Postnummer**.
8. Angiv **Gade**.
9. Angiv **By**, **Stat** og **Region**. Disse felter angives typisk automatisk ud fra feltet **Postnummer**.
10. Vælg eventuelt feltet **Primær** for at angive en primær adresse. Kun én adresse kan markeres som primær. Hvis en anden adresse allerede er markeret som den primære adresse, skal du bekræfte, at du vil bruge denne adresse som primær.
11. Vælg eventuelt feltet **Privat** for at angive, at adressen er privat. Kun brugere med udtrykkelig tilladelse til at få vist private adresseoplysninger kan få vist denne adresse.
12. Vælg **OK**.

## <a name="create-or-change-a-worker-address"></a>Oprette eller ændre en arbejderadresse

Du kan opdatere en adresse i arbejdsområdet **Personalestyring**. Benyt denne fremgangsmåde for at oprette eller ændre en adresse:

1. Vælg **Links** i arbejdsområdet **Personalestyring**, og vælg derefter **Arbejdere**.
2. Vælg medarbejderen, og vælg derefter **Adresser**.
3. Vælg **Tilføj** for at tilføje en adresse. Hvis du vil opdatere en eksisterende adresse, skal du vælge adressen fra listen og derefter vælge **Rediger**.
4. Angiv **Navn eller beskrivelse**.
5. Vælg rullelisten **Formål**, og vælg derefter typen af adresse.
6. Angiv **Land/område**.
7. Angiv **Postnummer**.
8. Angiv **Gade**.
9. Angiv **By**, **Stat** og **Region**. Disse felter angives typisk automatisk ud fra feltet **Postnummer**.
10. Vælg eventuelt feltet **Primær** for at angive en primær adresse. Kun én adresse kan markeres som primær. Hvis en anden adresse allerede er markeret som den primære adresse, skal du bekræfte, at du vil bruge denne adresse som primær.
11. Vælg eventuelt feltet **Privat** for at angive, at adressen er privat. Kun brugere med udtrykkelig tilladelse til at få vist private adresseoplysninger kan få vist denne adresse.
12. Vælg **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Oprette en fremtidig ændring af en adresse

I nogle tilfælde kan det være, at du vil opdatere en adresse, der skal ændres i fremtiden. Dette er f.eks. nyttigt, hvis en medarbejder skal flytte den 15. i den efterfølgende måned.

1. Åbn siden **Administrer adresser** ved at vælge **Flere indstillinger > Avanceret** fra et vilkårligt adressegitter.
2. Vælg **Ny** for at oprette en ny adresse.
3. Angiv oplysningerne om adressen.
4. Vælg oversigtspanelet **Generelt**.
5. Vælg den dato, hvorfra den nye adresse skal gælde, i feltet **Gælder fra**.
6. I feltet **Udløbsdato** kan du vælge den dato, hvor adressen ikke længere er gyldig.
7. Luk siderne.

## <a name="view-and-monitor-address-changes"></a>Få vist og overvåge adresseændringer

Human Resourcesmedarbejdere kan få vist og overvåge adresseændringer fra arbejdsområdet **Personalestyring**. Hvis du vil have vist adresseændringerne, skal du vælge feltet **Personalestyring** på **Startside**. Adresseændringerne vises i et felt i øverste højre hjørne. Antallet over **Adresse ændringer** viser, hvor mange adresseændringer der er foretaget inden for det antal dage, der er angivet på siden **Human Resources-parametre**. 

Når du markerer feltet **Adresseændringer**, vises oplysningerne om eventuelle adresseændringer på en ny side. Du kan evt. vælge **Medtag fremtidige adresseændringer** i øverste højre hjørne for at få vist adresseændringer med en fremtidig dato.

> [!NOTE]
> Hvis du vil modtage en påmindelse eller mail om disse adresseændringer, kan du oprette en ny påmindelsesregel på fanen **Indstillinger** i handlingsruden. Du kan finde flere oplysninger om påmindelsesregler under [Oprette påmindelsesregler](../fin-ops-core/fin-ops/get-started/create-alerts.md).
>
> Hvis du vil konfigurere en arbejdsgang for adresseændringerne, kan du vælge indstillingen **Send eksternt** på din påmindelsesregel og derefter bruge Power Automate til at udløse forretningshændelsen og konfigurere en arbejdsgang. Yderligere oplysninger finder du under [Påmindelser som forretningshændelser](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
