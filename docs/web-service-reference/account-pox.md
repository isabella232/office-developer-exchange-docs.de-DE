---
title: Konto (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Das Konto-Element gibt Konten-Einstellungen für den Benutzer oder Fehlerantworten enthält.
ms.openlocfilehash: 6cd87e678b3a524a69f6dca4d6999a3cff22fa57
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353343"
---
# <a name="account-pox"></a>Konto (POX)

Das **Konto** -Element gibt Konten-Einstellungen für den Benutzer oder Fehlerantworten enthält. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
- [Response (POX)](response-pox.md)
- [Konto (POX)](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Stellt die Kontenart an.  <br/> |
|[Aktion (POX)](action-pox.md) <br/> |Enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Enthält einen Wert, der angibt, ob das Postfach des Benutzers im Exchange Online gehostet wird oder Exchange Online als Teil von Office 365.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Enthält die URL des Computers, der Exchange-Server ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Gibt die e-Mail-Adresse, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.  <br/> |
|[Bild (POX)](image-pox.md) <br/> |Enthält den Pfad eines Bilds, das verwendet wird, um die Konfiguration Erfahrung mit Branding versehen.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Enthält die URL der Startseite des Internet-Dienstanbieters (ISP).  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Enthält Informationen, mit denen Clients eine Anforderung der AutoErmittlung zum Ermitteln von Öffentliche Ordner-Informationen für den Benutzer zu senden.  <br/> |
|[Fehler (POX)](error-pox.md) <br/> |Enthält eine Fehlerantwort AutoErmittlung an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Enthält die Antwort vom AutoErmittlungsdienst.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

