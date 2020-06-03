---
title: EWS-Anwendungstypen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: Informieren Sie sich über die am häufigsten verwendeten Arten von Anwendungen, die Sie mithilfe von EWS in Exchange erstellen können.
localization_priority: Priority
ms.openlocfilehash: 02bbe039adaec1054ab33f642f3bf14a7ba22b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455429"
---
# <a name="ews-application-types"></a>EWS-Anwendungstypen

Informieren Sie sich über die am häufigsten verwendeten Arten von Anwendungen, die Sie mithilfe von EWS in Exchange erstellen können.
  
Die [EWS-und Exchange-Architektur](ews-applications-and-the-exchange-architecture.md) stellt ein einheitliches Entwicklungsmodell bereit, mit dem Sie die gängigsten Typen von Anwendungen einheitlich erstellen können, einschließlich der folgenden: 
  
- [Client Anwendungen](#bk_clientapps) – eigenständige Anwendungen, die EWS für den Zugriff auf Exchange-Daten verwenden. Outlook und Outlook Web App sind Beispiele für Clientanwendungen. 
    
- [Portal Anwendungen](#bk_portalapps) – Anwendungen, die eine vorhandene Webseite erweitern, indem Sie aus Exchange abgerufene Informationen einschließen, beispielsweise frei/gebucht-oder Kontaktinformationen. Ein SharePoint-Webpart, in dem Exchange-Daten abgerufen werden, ist ein Beispiel für eine Portalanwendung. 
    
- [Dienstanwendungen](#bk_serviceapps) – Hintergrundaufträge, die zum integrieren oder Synchronisieren von Daten aus Exchange in ein vorhandenes System verwendet werden. Beispielsweise eine Anwendung, mit der Kontaktinformationen aus Exchange in einer CRM-Anwendung synchronisiert werden. 
    
Jedes dieser Anwendungsmodelle kann eine gemeinsame Codebasis zum Abrufen von Informationen aus Exchange verwenden, sodass Sie den EWS-Code nicht ändern müssen, der zum Abrufen von Elementinformationen zwischen einem Client, einem Portal oder einer Dienstanwendung verwendet wird. Was sich möglicherweise von einer Anwendung zur nächsten ändert, ist der Postfachzugriffs-und Authentifizierungsmechanismus. Clientanwendungen verwenden beispielsweise häufig den direkten Benutzer Zugriff und die Standard-oder NTLM-Authentifizierung, wohingegen eine Dienstanwendung wahrscheinlich den Identitätswechsel für den Postfachzugriff und die OAuth-Authentifizierung verwendet.
  
## <a name="client-applications"></a>Clientanwendungen
<a name="bk_clientapps"> </a>

Bei einer EWS-Clientanwendung handelt es sich um eine eigenständige Anwendung, die EWS zum Abrufen von Informationen aus dem Exchange-Informationsspeicher verwendet. EWS-Clientanwendungen verwenden direkten Clientzugriff oder Stellvertretungszugriff, um Daten aus dem Postfachspeicher abzurufen. Im folgenden finden Sie einige Beispiele für Clientanwendungen, die EWS verwenden:
  
- Outlook in Features wie e-Mail-Infos, Verfügbarkeit und Abwesenheitsstatus des Benutzers
    
- OWA für Geräte
    
- Outlook für Mac 2011
    
- Lync für Verfügbarkeitsinformationen
    
Client Anwendungen verwenden häufig den direkten Zugriff und die Standard-oder NTLM-Authentifizierung, sodass Benutzer auf Informationen in Ihrem eigenen Postfach mit ihren eigenen Anmeldeinformationen zugreifen können. Client Anwendungen sollten auch Stellvertretungszugriff für Benutzer unterstützen, denen die Berechtigung für den Zugriff auf das Postfach eines anderen Benutzers erteilt wurde.
  
## <a name="portal-applications"></a>Portal Anwendungen
<a name="bk_portalapps"> </a>

Eine Portalanwendung erweitert eine vorhandene Webseite oder ein Portal, um Exchange-Postfachinformationen als personalisierte Komponente der Seite einzubeziehen. SharePoint-Webparts sind die am häufigsten verwendeten Portalanwendungen und bieten Benutzern eine personalisierte Umgebung, indem Sie Ansichten in Exchange-Postfachdaten wie ungelesene Nachrichten, die neuesten Nachrichten und Kalenderereignisse neben der Allgemein angezeigten SharePoint-Portalseite bereitstellen. EWS-Portalanwendungen können direkten Clientzugriff, Stellvertretungszugriff oder Identitätswechsel verwenden, um Daten aus dem Postfachspeicher abzurufen. Da Exchange 2013 und SharePoint 2013 beide das OAuth-Autorisierungs Protokoll für die Server-zu-Server-Authentifizierung unterstützen, bietet OAuth die nahtlosste und sichere Authentifizierungsmethode.
  
## <a name="service-applications"></a>Dienstanwendungen
<a name="bk_serviceapps"> </a>

Eine Dienstanwendung ist normalerweise ein Hintergrund Auftrag, der in eine vorhandene Anwendung integriert ist, die sich auf Exchange ausdehnt, um Daten zwischen dem System und dem Exchange-Informationsspeicher zu korrelieren. Dienstanwendungen verfügen normalerweise nicht über eine Benutzeroberfläche und verwenden Identitätswechsel oder OAuth für Authentifizierung und Zugriff. Das Erstellen eines Dienstkontos für die Identitätswechsel von Benutzern ist in EWS-Dienst-apps üblich, da Sie einem einzelnen Konto die Berechtigung erteilen können, eine Gruppe von Benutzern zu imitieren und postfachvorgänge für diese Konten auszuführen. Beispielsweise kann eine EWS-Dienstanwendung Daten zwischen Marketinglisten in einer CRM-Lösung und Exchange-Verteilergruppen mithilfe eines Dienstkontos und eines Identitätswechsels synchronisieren.
  
## <a name="see-also"></a>Siehe auch


- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS-Anwendungen und die Exchange-Architektur](ews-applications-and-the-exchange-architecture.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

