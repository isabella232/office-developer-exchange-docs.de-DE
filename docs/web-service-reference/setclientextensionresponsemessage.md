---
title: SetClientExtensionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3365e58c-adb3-4d92-92cc-acc95ce36cca
description: Das SetClientExtensionResponseMessage-Element gibt die Antwortnachricht für eine SetClientExtension-Anforderung an.
ms.openlocfilehash: 3743d2f1643bece044ff7b7c8ccac95bbd7401ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468719"
---
# <a name="setclientextensionresponsemessage"></a>SetClientExtensionResponseMessage

Das **SetClientExtensionResponseMessage** -Element gibt die Antwortnachricht für eine **SetClientExtension** -Anforderung an. 
  
```XML
<SetClientExtensionResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</SetClientExtensionResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ResponseMessages](responsemessages.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

