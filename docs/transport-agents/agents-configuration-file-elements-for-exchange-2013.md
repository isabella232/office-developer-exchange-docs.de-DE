---
title: Agents Datei Konfigurationselemente für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Hier finden Sie Informationen über die XML-Elemente in der Konfigurationsdatei "Agents.config" und fetagents.config in Exchange 2013.
ms.openlocfilehash: dd58c4bc21a968db2ca5b13e0c53f7058b29f233
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757178"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Agents Datei Konfigurationselemente für Exchange 2013

Hier finden Sie Informationen über die XML-Elemente in der Konfigurationsdatei "Agents.config" und fetagents.config in Exchange 2013.
  
**Gilt für:** Exchange Server 2013
  
Wenn Sie die Access-Client oder die Postfachserverrolle auf einem Exchange-Server installieren, erstellt der Installer eine XML-Datei, die Konfigurationsinformationen zu Agents enthält, die auf dem Server installiert sind. Sie können nicht direkt in diese Datei geschrieben werden. 
  
Der Front-End-Transport-Dienst auf Clientzugriffsservern ausgeführt, und schreibt in eine Datei namens fetagents.config. Der Transport-Dienst und den postfachtransportdienst auf Postfachservern führen, und Schreiben in eine Datei namens "Agents.config". Ein Computer, auf dem die Clientzugriffs-Serverrolle und die Postfachserverrolle hat müssen eine fetagents.config und eine Datei "Agents.config". 
  
Mithilfe von Transport-Agent-Cmdlets in der Exchange-Verwaltungsshell ist die einzige unterstützte Möglichkeit zum Schreiben in diese Dateien. Informationen zu den Transport-Agent-Cmdlets finden Sie unter [Mail Flow-Cmdlets](http://technet.microsoft.com/en-us/library/aa998553%28v=exchg.150%29.aspx) auf TechNet. 
  
> [!NOTE]
> Zur Unterscheidung zwischen Agents, die den Front-End-Transport-Dienst auf dem Client Access Server erweitern und den Transportdienst auf dem Postfachserver verfügen Transport-Agent-Cmdlets den Parameter _TransportService_ mit dem Wert "Hub" für den Transport Dienst- und "FrontEnd" für den Front-End-Transport-Dienst. 
  
Sie können die "Agents.config" oder die fetagents.config-Datei, um das Vorhandensein zu ermitteln und die Konfigurationsinformationen für einen oder mehrere Agents auf dem Server gelesen. Diese Dokumentation enthält einen Verweis, mit denen Sie die Informationen in der Datei "Agents.config" oder die fetagents.config lesen. Das Format für beide Dateien ist identisch. In dieser Dokumentation bietet keine Informationen dazu, wie Sie in den Dateien zu schreiben.
  
> [!CAUTION]
> Nicht unterstützte Methoden zum Schreiben in die Datei "Agents.config" oder fetagents.config kann unerwartete Ergebnisse, einschließlich Fehler bei der Transportdienst oder Transport-Agents führen. Nicht direkt in eine dieser beiden Dateien schreiben. Die einzige unterstützte Methode zum Schreiben in diese Dateien wird mithilfe der Exchange-Verwaltungsshell-Transport-Agent-Cmdlets. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Speicherort der Dateien Transport-Agent-Konfiguration
<a name="bk_ConfigLoc"> </a>

Bei der Installation von Exchange 2013 das Installationsprogramm erstellt eine XML-Datei mit dem Namen agents.config.template oder fetagents.config.template, abhängig von der Serverrolle installiert ist, in der \<ExchangeInstallFolder\>\TransportRoles\Agents Ordner (wobei \<ExchangeInstallFolder\> der Ordner, in dem Sie Exchange 2013 installiert, ist). Wenn Sie die Clientzugriffs-Serverrolle installieren, kopiert Exchange 2013 die Datei fetagents.config.template in fetagents.config. Wenn Sie die Postfachserverrolle installieren, kopiert Exchange 2013 die agents.config.template-Datei in "Agents.config". Exchange 2013 liest und schreibt diese Datei aus, wenn Sie die Konfiguration des Transport-Agents auf dem Server ändern.
  
## <a name="verifying-a-transport-agent-installation"></a>Überprüfen der Installation einen Transport-agent
<a name="bk_verifyinstall"> </a>

Sie können die XML-Funktionen, die .NET Framework zum Lesen und überprüfen die "Agents.config" oder der fetagents.config XML-Datei enthält. Um die Installation und Konfiguration eines Transport-Agents zu überprüfen, lesen Sie die XML-Konfigurationsdatei, und suchen Sie nach der [Agent](agent.md) -Element, das der Transport-Agent entspricht. Wenn ein **Agent** -Element für den bestimmten Transport-Agent nicht vorhanden ist, ist der Transport-Agent nicht installiert. Wenn der Transport-Agent installiert ist, können Sie die Attribute des Elements **Agent** die Konfiguration lesen. 
  
## <a name="configuration-file-element-hierarchy"></a>Hierarchie der Konfigurationsdatei-element
<a name="bk_elementref"> </a>

Der folgende Code zeigt die Elementhierarchie in der XML-Konfigurationsdatei.
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_elementreflist"> </a>

- [Agent](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [Konfiguration](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [Überwachung](monitoring.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)
- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Transport-Agent-Namespaces in Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets für den Nachrichtenfluss](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)
    

