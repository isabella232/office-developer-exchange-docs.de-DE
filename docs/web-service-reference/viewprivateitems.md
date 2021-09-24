---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: Das ViewPrivateItems-Element gibt an, ob ein Delegatbenutzer oder eine Clientanwendung über die Berechtigung zum Anzeigen privater Elemente im Postfach des Prinzipals verfügt.
ms.openlocfilehash: fcc63534603ea4cc6e5a7f91569a14c742b10a98
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509315"
---
# <a name="viewprivateitems"></a>ViewPrivateItems

Das **ViewPrivateItems-Element** gibt an, ob ein Delegatbenutzer oder eine Clientanwendung über die Berechtigung zum Anzeigen privater Elemente im Postfach des Prinzipals verfügt. 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert **"true"** gibt an, dass der Delegat oder Client private Elemente im Postfach des Prinzipals anzeigen kann. Der Wert **"false"** gibt an, dass private Elemente für einen Delegaten oder Client nicht sichtbar sind. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

