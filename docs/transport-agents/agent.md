---
title: Agent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 8bcfdd9bffd4c7a15af40528fd431a99c7868637
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520968"
---
# <a name="agent"></a>Agent
  
**Gilt für:** Exchange Server 2013
  
Das **Agent-Element** enthält Konfigurationsinformationen zu einem installierten Agent. 
  
- [Konfiguration](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [Agent](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

**agentType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name, der bei der Installation des Agents angegeben wurde. Dieses Attribut erfordert einen wert für eine leere Zeichenfolge, die maximal 64 Zeichen enthält.  <br/> |
|**Basetype** <br/> |Der vollständige Name einschließlich des Namespaces der Klasse, von der der Agent abgeleitet wird. Dieses Attribut erfordert einen wert für eine leere Zeichenfolge, die mindestens ein Zeichen enthält.  <br/> |
|**classFactory** <br/> |Der vollständige Name einschließlich des Namespaces der Klasse, die die Agentfactory implementiert, die Instanzen des Agents erstellt. Dieses Attribut muss den vollqualifizierten Namen der Klasse enthalten, die die Agentfactory implementiert, die Instanzen des Agents erstellt. Diese Klasse muss entweder von der [SmtpReceiveAgentFactory-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) oder [RoutingAgentFactory-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) abgeleitet werden.  <br/> |
|**Assemblypath** <br/> |Der vollqualifizierte Pfad einschließlich des Dateinamens der Assembly, die den Code für den Agent enthält. Dieses Attribut erfordert einen wert für eine leere Zeichenfolge, die mindestens ein Zeichen enthält.  <br/> |
|**enabled** <br/> |Ein boolescher Wert, der angibt, ob der Agent aktiviert ist. Der Wert ist **"true",** wenn der Agent aktiviert ist. andernfalls ist der Wert **false**. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Enthält ein **Agent-Element** für jeden installierten Agent.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei definiert keinen Namespace.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents-Konfigurationsdateielemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

