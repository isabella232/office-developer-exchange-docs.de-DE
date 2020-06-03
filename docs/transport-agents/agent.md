---
title: Agent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: a810bb229015054e0f244773760235114655a982
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455681"
---
# <a name="agent"></a>Agent
  
**Gilt für:** Exchange Server 2013
  
Das **Agent** -Element enthält Konfigurationsinformationen zu einem installierten Agent. 
  
- [Konfiguration](configuration.md) 
- [mexRuntime](mexruntime.md)
- [Agentliste](agentlist.md)
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

**AgentType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name, der beim Installieren des Agents angegeben wurde. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der maximal 64 Zeichen enthält.  <br/> |
|**BaseType** <br/> |Der vollständige Name, einschließlich des Namespaces, der Klasse, von der der Agent abgeleitet wird. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.  <br/> |
|**ClassFactory** <br/> |Der vollständige Name, einschließlich des Namespaces, der Klasse, die die Agent-Factory implementiert, die Instanzen des Agents erstellt. Dieses Attribut muss den vollqualifizierten Namen der Klasse enthalten, die die Agent-Factory implementiert, die Instanzen des Agents erstellt. Diese Klasse muss entweder von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -oder der [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse abgeleitet werden.  <br/> |
|**assemblyPath** <br/> |Der vollqualifizierte Pfad einschließlich des Datei namens der Assembly, die den Code für den Agent enthält. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.  <br/> |
|**enabled** <br/> |Ein boolescher Wert, der angibt, ob der Agent aktiviert ist. Der Wert ist **true** , wenn der Agent aktiviert ist; Andernfalls ist der Wert **false**. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Agentliste](agentlist.md) <br/> |Enthält ein **Agent** -Element für jeden installierten Agent.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

