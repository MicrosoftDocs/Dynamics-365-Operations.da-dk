---
title: Konfigurere klyngepluk
description: Denne artikel beskriver, hvordan du konfigurerer klyngepluk og anvender varebekræftelse sammen med klyngepluk.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014714"
---
# <a name="set-up-cluster-picking"></a>Konfigurere klyngepluk

[!include[banner](../includes/banner.md)]

Denne artikel beskriver, hvordan arbejderne skal kunne bruge deres mobilenheder til at gruppere plukkearbejde i klynger, så de kan plukke varer fra et enkelt sted til flere arbejdsordrer på samme tid. Dette kaldes *klyngepluk*.

## <a name="about-cluster-picking"></a>Om klyngepluk

Når arbejdsordrer er frigivet til lagerstedet, kan arbejderen bruge en mobilenhed til at tildele ordrer til en klynge. Klyngen organiserer plukkearbejdet for arbejderen. Når en arbejdsordre er tildelt til en klynge, skal arbejderen bruge klyngepluk til at udføre plukkearbejdet for ordren. Arbejderen kan ikke bruge andre plukkemetoder. Hvis en arbejdsordre er tildelt til en klynge ved en fejl, skal arbejderen bryde klyngen op og derefter oprette den igen.

Hvis det er nødvendigt, kan en arbejder sende en klynge til en anden arbejder. Dette ændrer statussen på klyngen til Bestået. Når arbejderen bruger en mobilenhed til at angive, at plukning og læg på lager-arbejde er fuldført, skal forsendelsen eller lasten bekræftes i klienten.

## <a name="enable-cluster-picking"></a>Aktivere klyngepluk

Hvis du vil aktivere klyngepluk, skal du angive følgende:

- **Klyngeprofiler** – Angiv, om der automatisk skal oprettes klynge-id'er, antallet af positioner, der skal bruges, hvornår klynger skal brydes, og hvordan rækkefølgen af plukarbejdet skal angives og bekræftes.

- **Arbejdsskabeloner** – Definer, hvordan du opretter plukarbejde til klyngepluk.

- **Lokationsvejledninger** – Angiv, hvor du kan plukke varer fra, og hvor du kan placere dem.

- **Menupunkter i mobilenhed** – Konfigurer et menupunkt på en mobilenhed til at bruge eksisterende arbejde, der er pålagt ved hjælp af klyngepluk. Du skal tilføje menupunktet til en mobilenhedmenu, så den vises på mobilenheder.

- **Parametre til lokationsstyring** – Angiv den nummerserie, der skal bruges, hvis du vil generere id'er til klynger.

## <a name="set-up-a-cluster-profile"></a>Konfigurere en klyngeprofil

Du kan konfigurere en klyngeprofil på følgende måde:

1. Klik på **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \>  **Klyngeprofiler**.

1. Klik på **Ny** for at oprette en ny profil.

1. Klik på **Opret klynge** og under **Klyngesortering**, skal du klikke på **Ny** for at konfigurere sorteringskriterier for klyngen. Sorteringskriteriet styrer den rækkefølge, som arbejderen skal udføre plukkearbejdet i. Du kan tilføje lige så mange kriterier, der er behov for.

1. I feltet **Løbenummer** skal du angive et nummer for at definere den rækkefølge, som sorteringskriterierne behandles i.

1. Vælg det felt, der skal bestemme sorteringen, i feltet **Feltnavn**. Hvis du f.eks. vælger **WMSLocationId**, sorteres arbejdet efter den lokation.

1. Vælg en af følgende indstillinger i feltet **Sortering**.

| **Indstilling**     | **Beskrivelse**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Stigende**  | Plukarbejdet sorteres i stigende rækkefølge ud fra sorteringskriterierne. Hvis du f.eks. bruger feltet **WMSLocationId** som sorteringskriterier og dit lokations-id er 1, 2, 3 og 4, plukker du først fra lokation 4. |
| **Faldende** | Plukarbejdet sorteres i faldende rækkefølge ud fra sorteringskriterierne. Hvis du f.eks. bruger feltet **WMSLocationId** som sorteringskriterier og dit lokations-id er 1, 2, 3 og 4, plukker du først fra lokation 1. |

## <a name="item-confirmation"></a>Varebekræftelse

Når der anvendes en klyngepluk, er varebekræftelse afgørende for kontrol af de varer, der føjes til klynger. Du kan kontrollere varer i klyngepluk under klyngeplukprocessen. Opsætningen er baseret på opsætningen af produktets stregkode.

### <a name="set-up-item-verification-with-cluster-picking"></a>Konfigurer varekontrol med klyngepluk

1. Gå til **Lagerstedsstyring** > **Opsætning** > **Mobilenhed** > **Menupunkter i mobilenhed**.
1. Vælg det menupunkt, du vil konfigurere, i listeruden.
1. Vælg **Konfiguration af arbejdsbekræftelse** i handlingsruden.
1. Udfør en af følgende handlinger:
    - Hvis der allerede findes en linje for den **Arbejdstype**, du vil konfigurere, skal du markere den og derefter vælge **Rediger** i handlingsruden.
    - Hvis der ikke findes en relevant linje, skal du vælge **Ny** i handlingsruden og derefter angive **Arbejdstype** til den relevante type.
1. Markér afkrydsningsfeltet **Bekræftelse af produkt** for den nye eller valgte linje. Så kan arbejderne kontrollere hver enkelt vare på lageret fra mobilenheden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]