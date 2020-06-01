---
title: Elemente der Konfigurationsdatei der Agents für Exchange 2013
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
description: Hier finden Sie Informationen zu den XML-Elementen in der Konfigurationsdatei Agents. config und fetagents. config in Exchange 2013.
ms.openlocfilehash: f19fe8316a78cef668db881e630562d3be8be64a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461569"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Elemente der Konfigurationsdatei der Agents für Exchange 2013

Hier finden Sie Informationen zu den XML-Elementen in der Konfigurationsdatei Agents. config und fetagents. config in Exchange 2013.
  
**Gilt für:** Exchange Server 2013
  
Wenn Sie die Client Zugriffs-oder Postfachserverrolle auf einem Exchange-Server installieren, erstellt das Installationsprogramm eine XML-Datei mit Konfigurationsinformationen zu Agents, die auf dem Server installiert sind. Sie können nicht direkt in diese Datei schreiben. 
  
Der Front-End-Transport-Dienst wird auf Client Zugriffsservern ausgeführt und schreibt in eine Datei mit dem Namen "fetagents. config". Der Transportdienst und der postfachtransportdienst werden auf Postfachservern ausgeführt und in eine Datei mit dem Namen Agents. config geschrieben. Ein Computer, der über die Client Zugriffs-Serverrolle und die Postfachserverrolle verfügt, verfügt über eine Datei fetagents. config und eine Agents. config. 
  
Die einzige unterstützte Möglichkeit, in diese Dateien zu schreiben, ist die Verwendung der Transport-Agent-Cmdlets im Exchange-Verwaltungsshell. Informationen zu den Transport-Agent-Cmdlets finden Sie unter [Nachrichtenfluss-Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) auf TechNet. 
  
> [!NOTE]
> Um zwischen Agents zu unterscheiden, die den Front-End-Transport-Dienst auf dem Client Zugriffsserver und den Transportdienst auf dem Postfachserver erweitern, verfügen Transport-Agent-Cmdlets über einen _Transportservice_ -Parameter mit dem Wert "Hub" für den Transportdienst und "Frontend" für den Front-End-Transport-Dienst. 
  
Sie können die Datei Agents. config oder fetagents. config lesen, um das vorhanden sein von und Konfigurationsinformationen für einen oder mehrere Agents auf dem Server zu bestimmen. Diese Dokumentation enthält eine Referenz, die Sie verwenden können, um die Informationen in der Datei "Agents. config" oder in der fetagents. config zu lesen. Das Format für beide Dateien ist identisch. In dieser Dokumentation werden keine Informationen zum Schreiben in die Dateien bereitgestellt.
  
> [!CAUTION]
> Die Verwendung nicht unterstützter Methoden zum Schreiben in die Datei Agents. config oder fetagents. config kann zu unerwarteten Ergebnissen führen, einschließlich des Fehlers des Transportdiensts oder der Transport-Agents oder beider. Schreiben Sie nicht direkt in eine dieser Dateien. Die einzige unterstützte Methode zum Schreiben in diese Dateien ist die Verwendung der Cmdlets für den Exchange-Verwaltungsshell Transport-Agent. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Speicherort der Transport-Agent-Konfigurationsdateien
<a name="bk_ConfigLoc"> </a>

Wenn Sie Exchange 2013 installieren, erstellt das Installationsprogramm je nach installierter Serverrolle eine XML-Datei mit dem Namen "Agents. config. Template" oder "fetagents. config. Template" im \<ExchangeInstallFolder\> Ordner "\TransportRoles\Agents" (wobei \<ExchangeInstallFolder\> es sich um den Ordner handelt, in dem Sie Exchange 2013 installiert haben). Wenn Sie die Client Zugriffs-Serverrolle installieren, kopiert Exchange 2013 die Datei fetagents. config. Template in fetagents. config. Wenn Sie die Postfachserverrolle installieren, kopiert Exchange 2013 die Datei Agents. config. Template in Agents. config. Exchange 2013 liest und schreibt diese Datei, wenn Sie die Transport-Agent-Konfiguration auf dem Server ändern.
  
## <a name="verifying-a-transport-agent-installation"></a>Überprüfen der Installation eines Transport-Agents
<a name="bk_verifyinstall"> </a>

Sie können die XML-Funktionen verwenden, die der .NET Framework zum Lesen und Validieren der XML-Datei "Agents. config" oder "fetagents. config" bereitstellt. Zum Überprüfen der Installation und Konfiguration eines Transport-Agents lesen Sie den XML-Code in der Konfigurationsdatei, und suchen Sie nach dem [Agent](agent.md) -Element, das dem Transport-Agent entspricht. Wenn kein **Agent** -Element für den bestimmten Transport-Agent vorhanden ist, ist der Transport-Agent nicht installiert. Wenn der Transport-Agent installiert ist, können Sie die Attribute des **Agent** -Elements lesen, um die Konfiguration zu bestimmen. 
  
## <a name="configuration-file-element-hierarchy"></a>Hierarchie der Konfigurationsdateielemente
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
    
- [Agentliste](agentlist.md)
    
- [Konfiguration](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [Überwachung](monitoring.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)
- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Namespaces des Transport-Agents in Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets für den Nachrichtenfluss](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

