---
title: Opret vedligeholdelsesanmodninger
description: Denne artikel forklarer, hvordan du opretter en vedligeholdelsesanmodning i Styring af aktiver.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 92f3a2bc3d2a4d5d1c3be0c6dda2674dc3e7d0bb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016820"
---
# <a name="create-maintenance-requests"></a>Oprette vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

 

Vedligeholdelsesanmodninger kan bruges, hvis vedligeholdelsesarbejdere eller produktionsmedarbejdere opdager, at udstyr kræver reparation, men reparationsjobbet ikke kan udføres med det samme.

**Eksempel:** Mens en vedligeholdelsesarbejder foretager en reparation, opdager vedkommende, at et andet aktiv på samme sted skal serviceres. Vedligeholdelsesarbejderen har dog ikke tid eller de nødvendige reservedele til at udføre reparationsjobbet. Derfor opretter arbejderen en vedligeholdelsesanmodning på aktivet og indtaster en kort beskrivelse af problemet.

Afsnittet **Aktive vedligeholdelsesanmodninger** i ruden **Relaterede oplysninger** i højre side af siden **Alle aktiver** eller **Aktive aktiver** (**Styring af aktiver** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**) viser de aktive vedligeholdelsesanmodninger, der er knyttet til det valgte aktiv.

1. Vælg **Styring af aktiver** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.
2. Vælg **Ny**.
3. Vælg typen af vedligeholdelsesanmodning i feltet **Vedligeholdelsesanmodningstype** i dialogboksen **Opret anmodning**. Der foreslås en standardtype.
4. I feltet **Beskrivelse** skal du angive et navn eller en titel, der kort beskriver vedligeholdelsesanmodningen.
5. I felterne **Arbejdssted** og **Aktiv** skal du vælge et arbejdssted eller et aktiv eller en kombination af et arbejdssted og et aktiv, som du har brug for. Du kan oprette en vedligeholdelsesanmodning uden at vælge et aktiv, og aktivet kan føjes til vedligeholdelsesanmodningen senere. Hvis den vedligeholdelsesarbejder, der er logget på, er relateret til en ressource, der er relateret til et aktiv, er feltet **Aktiv** automatisk angivet.

    Hvis der allerede er knyttet en vedligeholdelsesanmodning til det valgte aktiv, vises der en meddelelseslinje øverst i dialogboksen **Opret anmodning** for at give dig besked om id'et for den eksisterende vedligeholdelsesanmodning. En meddelelseslinje giver dig også besked, hvis aktivet er dækket af en garantiaftale.

6. I feltet **Serviceniveau** skal du vælge et serviceniveau, der angiver anmodningens prioritetsniveau.
7. Hvis du har valgt et aktiv i trin 5, kan du bruge felterne **Fejlsymptom**, **Fejlområde** og **Fejltype** til at oprette en fejlregistrering.
8. Hvis vedligeholdelsesanmodningen har medført vedligeholdelsesnedetid, skal du angive startdato og -tidspunkt for nedetiden.

    Feltet **Startet af** indstilles automatisk til dit navn.

10. Feltet **Faktisk start** angives automatisk til den aktuelle dato og tid. Du kan dog ændre værdien efter behov.
11. Udfyld eventuelt feltet **Noter** med yderligere bemærkninger.
12. Vælg **OK**.

![Opret vedligeholdelsesanmodning.](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Efterfølgende behandling af vedligeholdelsesanmodninger

Når der er oprettet en vedligeholdelsesanmodning, men før den konverteres til en arbejdsordre, skal der opdateres forskellige oplysninger på den. En planlægger eller en anden administrativ medarbejder fuldfører typisk denne opgave.

- På siden **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** skal du vælge den anmodning, du vil arbejde med, og derefter vælge **Rediger**.

I detaljevisningen kan du opdatere forskellige oplysninger. Her er nogle eksempler:

- Vælg og bekræft aktivet. Hvis du senere skal vælge et andet aktiv, kan du angive indstillingen **Aktiv verificeret** til **Nej**.
- Vælg en ansvarlig vedligeholdelsesarbejdergruppe og/eller en ansvarlig vedligeholdelsesarbejder. Du finder flere oplysninger om den påkrævede opsætning under [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md).
- Vælg en vedligeholdelsesjobtype og, hvis disse oplysninger er relevante, en relateret vedligeholdelsesjobvariant og en jobhandel.
- Angiv geografiske koordinater i felterne **Breddegrad** og **Længdegrad**. Alle koordinater, der føjes til en vedligeholdelsesanmodning, overføres automatisk til en relateret arbejdsordre. 

![Opdatere vedligeholdelsesanmodning.](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Hvis du vælger et aktiv, når du opretter en vedligeholdelsesanmodning, kan du føje én fejl til aktivet. Når vedligeholdelsesanmodningen er blevet oprettet, kan du tilføje flere fejl efter behov. Hvis du vil tilføje fejl, skal du vælge **Aktivfejl** på siden **Alle vedligeholdelsesanmodninger**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]