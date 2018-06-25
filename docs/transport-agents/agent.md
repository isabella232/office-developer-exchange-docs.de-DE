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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 3895095ed4e469cdb9fec489ba6b6e228779a9c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757170"
---
# <a name="agent"></a>Agent
  
**Gilt für:** Exchange Server 2013
  
Das **Agent** -Element enthält Konfigurationsinformationen zu installierten Agenten. 
  
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

**AgentType (ComplexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name, der angegeben wurde, wenn der Agent installiert wurde. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der maximal 64 Zeichen enthält.  <br/> |
|**baseType** <br/> |Der vollständige Name, einschließlich des Namespace, der Klasse, von der der Agent abgeleitet wird. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.  <br/> |
|**classFactory** <br/> |Der vollständige Name, einschließlich des Namespace, der Klasse, die die Agentfactory implementiert wird, die Instanzen des Agents erstellt. Dieses Attribut muss den vollqualifizierten Namen der Klasse enthalten, die die Agentfactory implementiert, die Instanzen des Agents erstellt. Diese Klasse muss von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) oder [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse abgeleitet werden.  <br/> |
|**assemblyPath** <br/> |Der vollständig qualifizierte Pfad, einschließlich Dateiname der Assembly, die den Code für den Agent enthält. Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.  <br/> |
|**aktiviert** <br/> |Ein boolescher Wert, der angibt, ob der Agent aktiviert ist. Der Wert ist **true** , wenn der Agent aktiviert ist. Andernfalls ist der Wert **false**. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Ein **Agent** -Element enthält für jeden installierten Agent.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei ist nicht auf einen Namespace definieren.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |Falsch.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

