---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: Der Wert des AppStatus-Elements gibt den Status der Mail-APP an.
ms.openlocfilehash: d833947fd62d500418f257829d241a2e0b3bca9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464777"
---
# <a name="appstatus"></a>AppStatus

Der Wert des **AppStatus** -Elements gibt den Status der Mail-APP an. 
  
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

Der Textwert des **AppStatus** -Elements gibt den Status der Mail-APP an. Wenn der Benutzer ein Problem im Zusammenhang mit dem Status der Mail-App beheben kann, stellt das [ActionUrl](actionurl.md) -Element die URL zum Durchführen des Updates bereit. 
  
**Tabelle 1. AppStatus-Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NULL oder 0  <br/> |Die Mail-APP hat einen fehlerfreien Status.  <br/> |
|1.0  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die Mail-app muss aus dem Office Store erneut installiert werden.  <br/> |
|1.1  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die Mail-App erfordert erhöhte Berechtigungen, und dies erfordert eine Überprüfung und Bestätigung für die Installation.  <br/> |
|1.2  <br/> |Die Mail-App konnte nicht automatisch aktualisiert werden. Die aktuelle Lizenz ist abgelaufen oder ist ungültig. Aktualisieren Sie die Mail-App aus dem Office Store.  <br/> |
|2.0  <br/> |Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden. Die Lizenz für die Mail-app muss aus dem Office Store wiederhergestellt werden.  <br/> |
|2.1  <br/> |Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden. Die aktuelle Lizenz ist abgelaufen. Eine neue Lizenz für diese APP muss aus dem Office Store installiert werden.  <br/> |
|3,0  <br/> |Der Office Store Status für die Mail-App wurde geändert. Dies deutet möglicherweise darauf hin, dass ein Problem mit der Mail-App vorliegt. Wechseln Sie zur Seite Mail-App im Office Store, um weitere Informationen zu erhalten.  <br/> |
|3.1  <br/> |Die Mail-App wurde aus dem Office Store entfernt.  <br/> |
|3.2  <br/> |Es wurde ein Problem mit der Mail-App entdeckt, und es wurde vorübergehend aus dem Office Store zurückgezogen.  <br/> |
|3.3  <br/> |Die Mail-APP wird innerhalb von 30 Tagen aus dem Office Store entfernt.  <br/> |
|4,0  <br/> |Die Mail-App wurde von Ihrem e-Mail-Client automatisch deaktiviert.  <br/> |
|4.1  <br/> |Die Mail-App wurde aus Leistungsgründen von Outlook deaktiviert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

