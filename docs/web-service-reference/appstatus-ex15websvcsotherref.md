---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: Der Wert des AppStatus-Elements gibt den Status der Mail-App an.
ms.openlocfilehash: 69f481b197db513761b97d4fbba38452bbb4a9a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525316"
---
# <a name="appstatus"></a>AppStatus

Der Wert des **AppStatus-Elements** gibt den Status der Mail-App an. 
  
```XML
<AppStatus/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Metadaten](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **AppStatus-Elements** gibt den Status der Mail-App an. Wenn der Benutzer ein Problem im Zusammenhang mit dem Status der Mail-App beheben kann, stellt das [ActionUrl-Element](actionurl.md) die URL zum Ausführen der Korrektur bereit. 
  
**Tabelle 1. AppStatus-Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Null oder 0  <br/> |Die Mail-App hat einen fehlerfreien Status.  <br/> |
|1.0  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die Mail-App muss vom Office Store neu installiert werden.  <br/> |
|1.1  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die Mail-App erfordert erhöhte Berechtigungen, und dies erfordert Ihre Überprüfung und Bestätigung, um installiert zu werden.  <br/> |
|1.2  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die aktuelle Lizenz ist abgelaufen oder ungültig. Aktualisieren Sie die Mail-App aus dem Office Store.  <br/> |
|2.0  <br/> |Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden. Die Lizenz für die Mail-App muss vom Office Store wiederhergestellt werden.  <br/> |
|2.1  <br/> |Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden. Die aktuelle Lizenz ist abgelaufen. Eine neue Lizenz für diese App muss über die Office Store installiert werden.  <br/> |
|3.0  <br/> |Der Office Store Status für die Mail-App wurde geändert. Dies kann darauf hindeuten, dass ein Problem mit der Mail-App vorliegt. Wechseln Sie zur Mail-App-Seite im Office Store, um weitere Informationen zu erfahren.  <br/> |
|3.1  <br/> |Die Mail-App wurde aus dem Office Store entfernt.  <br/> |
|3.2  <br/> |Ein Problem mit der Mail-App wurde entdeckt und vorübergehend aus dem Office Store entfernt.  <br/> |
|3.3  <br/> |Die Mail-App wird innerhalb von 30 Tagen aus dem Office Store entfernt.  <br/> |
|4.0  <br/> |Die Mail-App wurde von Ihrem Mailclient automatisch deaktiviert.  <br/> |
|4.1  <br/> |Die Mail-App wurde aus Leistungsgründen von Outlook deaktiviert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Nicht zutreffend  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Metadaten](metadata-ex15websvcsotherref.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

