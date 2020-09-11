---
title: Få vist og administrere adresseændringer
description: Dette emne forklarer, hvordan du kan få vist og administrere adresseændringer i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 288df4fe766536e51ca9b5306c5bb948b7772ac5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2020
ms.locfileid: "3688315"
---
# <a name="view-and-manage-address-changes"></a>Få vist og administrere adresseændringer

I dette emne forklares det, hvordan du kan få vist og administrere adresseændringer på siden **Rediger personlige oplysninger** i Medarbejderselvbetjening eller detaljesiden for **Medarbejder** i Dynamics 365 Human Resources.

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

1. Vælg feltet **Medarbejderselvbetjening** på startsiden.

2. Vælg **Rediger personlige oplysninger**.

3. Vælg **Tilføj** for at tilføje en adresse. Hvis du vil opdatere en eksisterende adresse, skal du vælge adressen fra listen og derefter vælge **Rediger**.

4. Angiv **Navn eller beskrivelse**.

5. Vælg rullelisten **Formål**, og vælg derefter typen af adresse.

6. Angiv **Land/område**.

7. Angiv **Postnummer**.

8. Angiv **Gade**.

9. Angiv **By**, **Stat**og **Region**. Disse felter angives typisk automatisk ud fra feltet **Postnummer**.

10. Vælg eventuelt feltet **Primær** for at angive en primær adresse. Kun én adresse kan markeres som primær. Hvis en anden adresse allerede er markeret som den primære adresse, skal du bekræfte, at du vil bruge denne adresse som primær.

11. Vælg eventuelt feltet **Privat** for at angive, at adressen er privat. Kun brugere med udtrykkelig tilladelse til at få vist private adresseoplysninger kan få vist denne adresse.

12. Vælg **OK**.

## <a name="create-or-change-a-worker-address"></a>Oprette eller ændre en arbejderadresse

Du kan opdatere en adresse i arbejdsområdet **Personalestyring**. Benyt denne fremgangsmåde for at oprette eller ændre en adresse:

1. Vælg **Links** i arbejdsområdet **Personalestyring**, og vælg derefter **Arbejdere**.

3. Vælg medarbejderen, og vælg derefter **Adresser**.

3. Vælg **Tilføj** for at tilføje en adresse. Hvis du vil opdatere en eksisterende adresse, skal du vælge adressen fra listen og derefter vælge **Rediger**.

4. Angiv **Navn eller beskrivelse**.

5. Vælg rullelisten **Formål**, og vælg derefter typen af adresse.

6. Angiv **Land/område**.

7. Angiv **Postnummer**.

8. Angiv **Gade**.

9. Angiv **By**, **Stat**og **Region**. Disse felter angives typisk automatisk ud fra feltet **Postnummer**.

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

Personalemedarbejdere kan få vist og overvåge adresseændringer fra arbejdsområdet **Personalestyring**. Hvis du vil have vist adresseændringerne, skal du åbne vinduet **Personalestyring** fra siden **Start**. Adresseændringerne vises i et felt i øverste højre hjørne. Antallet over **Adresse ændringer** viser, hvor mange adresseændringer der er foretaget inden for det antal dage, der er angivet på siden **Parametre for personale**. 

Når du markerer feltet **Adresseændringer**, vises oplysningerne om eventuelle adresseændringer på en ny side. Du kan evt. vælge **Medtag fremtidige adresseændringer** i øverste højre hjørne for at få vist adresseændringer med en fremtidig dato.

> [!NOTE]
> Hvis du vil modtage en påmindelse eller mail om disse adresseændringer, kan du oprette en ny påmindelsesregel på fanen **Indstillinger** i handlingsruden. Du kan finde flere oplysninger om påmindelsesregler under [Oprette påmindelsesregler](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).<br><br>

> Hvis du vil konfigurere en arbejdsgang for adresseændringerne, kan du vælge indstillingen **Send eksternt** på din påmindelsesregel og derefter bruge Power Automate til at udløse forretningshændelsen og konfigurere en arbejdsgang. Yderligere oplysninger finder du under [Påmindelser som forretningshændelser](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).
