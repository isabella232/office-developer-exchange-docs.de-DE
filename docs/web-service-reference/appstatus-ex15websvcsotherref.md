---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: Der Wert der AppStatus-Element gibt den Status der Mail-app.
ms.openlocfilehash: cf213fc3d7be02c411e9c2e83a4ff153dbefe098
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757369"
---
# <a name="appstatus"></a>AppStatus

Der Wert der **AppStatus** -Element gibt den Status der Mail-app. 
  
```XML
<AppStatus/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Metadaten](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **AppStatus** -Element gibt den Status der Mail-app. Wenn der Benutzer ein Problem im Zusammenhang mit den Status der Mail-app beheben kann, enthält das [ActionUrl](actionurl.md) -Element die URL, um das Update ausführen. 
  
**In Tabelle 1. AppStatus Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NULL oder 0  <br/> |Die Mail-app hat einen fehlerfreien Status.  <br/> |
|1,0  <br/> |Die Mail-app konnte nicht aktualisiert werden. Die Mail-app muss aus dem Office Store neu installiert werden.  <br/> |
|1.1  <br/> |Die Mail-app konnte nicht aktualisiert werden. Die Mail-app erhöhte Berechtigungen benötigt, und dies erfordert die Überprüfung und Bestätigung zum Installieren.  <br/> |
|1.2  <br/> |Die Mail-app konnte nicht automatisch aktualisiert werden. Die aktuelle Lizenz ist abgelaufen oder ist ungültig. Aktualisieren Sie die Mail-app aus dem Office Store.  <br/> |
|2.0  <br/> |Die Mail-app-Lizenz konnte nicht aktualisiert werden. Die Lizenz für die Mail-app muss aus dem Office Store wiederhergestellt werden.  <br/> |
|2.1  <br/> |Die Mail-app-Lizenz konnte nicht aktualisiert werden. Die aktuelle Lizenz ist abgelaufen. Eine neue Lizenz für diese app muss aus dem Office Store installiert werden.  <br/> |
|3.0  <br/> |Der Office Store Status für die Mail-app wurde geändert. Dies kann bedeuten, dass ein mit der Mail-app Problem. Wechseln Sie auf der Seite e-Mail-app im Office Store für Weitere Informationen.  <br/> |
|3.1  <br/> |Die Mail-app wurde aus dem Office Store entfernt.  <br/> |
|3.2  <br/> |Ein Problem mit der Mail-app ermittelt wurden und wurde aus dem Office Store vorübergehend wurde zurückgezogen.  <br/> |
|3.3  <br/> |Innerhalb von 30 Tagen werden die Mail-app aus dem Office Store entfernt.  <br/> |
|4.0  <br/> |Die Mail-app wurde automatisch durch Ihren e-Mail-Client deaktiviert.  <br/> |
|4.1  <br/> |Die Mail-app wurde von Outlook aus Leistungsgründen deaktiviert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> | http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Nicht zutreffend  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Metadaten](metadata-ex15websvcsotherref.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

