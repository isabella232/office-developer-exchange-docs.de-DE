---
title: EcpUrl-TmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: Das EcpUrl TmEditing-Element gibt eine partielle URL, die kombiniert werden kann, mit dem EcpUrl (POX) Elementwert generiert eine URL, die zum Bearbeiten eines vorhandenen Website-Postfachs verwendet werden kann.
ms.openlocfilehash: 29b27ffe9ef3c18a3b6471ca4a42956a43a5aaa6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758130"
---
# <a name="ecpurl-tmediting-pox"></a>EcpUrl-TmEditing (POX)

Das **EcpUrl TmEditing** -Element gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die zum Bearbeiten eines vorhandenen Website-Postfachs verwendet werden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-TmEditing (POX)](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die zum Bearbeiten eines vorhandenen Website-Postfachs verwendet werden kann. Der Wert des **EcpUrl TmEditing** -Elements enthält Parameter enthaltenen ' <' und ' >' Zeichen, die vom Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| 
  _ID_ <br/> |Die SMTP-e-Mail-Adresse oder die X500 distinguished Name des websitepostfachs.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **EcpUrl TmEditing** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

