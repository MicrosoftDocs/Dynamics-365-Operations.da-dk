---
title: Få vist versionshistorikken for at tilbageføre sider og fragmenter
description: Denne artikel beskriver, hvordan du kan få vist versionshistorikken for en side eller et fragment og vende tilbage til en ældre version i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c4d78103a3c08ee4052290fccf6750aba7eecf4a
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474093"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Få vist versionshistorikken for at tilbageføre sider og fragmenter

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan få vist versionshistorikken for en side eller et fragment og vende tilbage til en ældre version i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Commerce-webstedsgenerator giver dig mulighed for at få vist versionshistorikken for en side eller et fragment og gå tilbage til en bestemt tidligere version af dokumentet, hvis det er nødvendigt. Når et dokument er åbent, kan du vælge **Vis historik** på kommandolinjen for at åbne en dialogboks til **versionshistorik**, hvor fanen **Version** viser historikken for alle versioner og gemmer aktiviteter for siden eller delen. Du kan derefter vælge en tidligere version af dokumentet på listen, få vist det som eksempel og gendanne det som den aktuelle version. Fanen **Aktivitet** i dialogboksen viser hele dokumentets aktivitetshistorik, herunder alle hændelser, der skal gemmes, publicere og ikke-udgives.

> [!NOTE]
> Der oprettes en ny version af et dokument, hver gang en webstedets forfatter foretager ændringer, og vælger derefter **Færdigredigering** for dokumentet. 

Hvis du vil have vist versionshistorikken for en side eller et fragment og vende tilbage til en tidligere version, skal du følge disse trin.

1. Åbn den side eller det fragment, du vil have vist versionshistorik for, i Site Builder.
1. Vælg **Vis historik** på kommandolinjen.

    ![Vis historik-knap](./media/version-history-1.png)

1. Vælg en tidligere version af dokumentet under fanen **Version** i dialogboksen **Versionshistorik**. I egenskabsruden til højre vises en forhåndsvisning af den valgte version samt oplysninger om, hvem der har ændret den og hvornår.

    ![Listevisning af versionshistorik.](./media/version-history-2.png)

1. Hvis du vil have vist en fuldstændigt gengivet forhåndsversion af den valgte version af dokumentet, skal du vælge **Forhåndsversion**. Vælg **Afslut forhåndsversion** for at lukke forhåndsversionen og returnere til dialogboksen **Versionshistorik**.
1. Hvis du vil gendanne en tidligere version af et dokument, skal du markere det på listen under fanen **Version** og derefter vælge **Gendan**. Der vises en meddelelsesboks **Gendan version \<version number\>**, som beder dig om at bekræfte gendannelseshandlingen. 

    ![Gendan knap og bekræftelsesmeddelelsesboksen.](./media/version-history-3.png)

1. Vælg Gendan for at fortsætte med **Gendan**. Site builder opdateres og viser den gendannede version af siden eller fragmenter.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere den gendannede version.
