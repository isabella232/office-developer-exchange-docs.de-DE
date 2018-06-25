---
title: EWS-Anwendungstypen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: Informieren Sie sich über die am häufigsten verwendeten Arten von Anwendungen, die Sie mithilfe von EWS in Exchange erstellen können.
ms.openlocfilehash: 1ce739f453ba1bc6f1b5d38edae3776daa562ffb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756827"
---
# <a name="ews-application-types"></a>EWS-Anwendungstypen

Informieren Sie sich über die am häufigsten verwendeten Arten von Anwendungen, die Sie mithilfe von EWS in Exchange erstellen können.
  
Die [EWS und Exchange-Architektur](ews-applications-and-the-exchange-architecture.md) bietet eine einheitliche Entwicklungsmodell, die Sie verwenden können, die am häufigsten verwendeten Anwendungstypen einheitlich, einschließlich der folgenden erstellen: 
  
- [Clientanwendungen](#bk_clientapps) – eigenständige Anwendungen, die Exchange-Webdienste verwenden, um die Exchange-Daten zugreifen. Outlook und Outlook Web App sind Beispiele für Clientanwendungen. 
    
- [Portal Applikationen](#bk_portalapps) – Anwendungen, die eine vorhandene Webseite zu erweitern, indem Sie einschließlich Informationen, die von Exchange, wie etwa Frei/Gebucht-Informationen und persönlichen Informationen abgerufen. Ein SharePoint-Webpart, der Exchange-Daten abruft ist ein Beispiel einer Portal-Anwendung. 
    
- [Dienstanwendungen](#bk_serviceapps) – Hintergrundaufträge zum integrieren oder Synchronisieren von Daten aus Exchange in einem vorhandenen System verwendet. Beispielsweise eine Anwendung, die Kontaktinformationen aus den Exchange in eine CRM-Anwendung synchronisiert wird. 
    
Jedes dieser Anwendungsmodelle können eine gemeinsame Codebasis zum Abrufen von Informationen aus Exchange -, sodass Sie nicht den EWS-Code zum Abrufen von Informationen zwischen einem Client, Portal oder -Anwendung ändern müssen. Was möglicherweise von einer Anwendung zur nächsten ändert ist der Postfach-Zugriffs und der Authentifizierung Mechanismus. Beispielsweise verwenden Clientanwendungen häufig vor direktem Benutzerzugriff und Basic oder NTLM-Authentifizierung, während eine-Anwendung wahrscheinlich Identitätswechsel für den Postfachzugriff und OAuth-Authentifizierung verwendet.
  
## <a name="client-applications"></a>Clientanwendungen
<a name="bk_clientapps"> </a>

Eine EWS-Client-Anwendung ist eigenständige Anwendung, die die EWS zum Abrufen von Informationen aus dem Exchange-Speicher verwendet. EWS-Clientanwendungen mithilfe von direct-ClientAccess oder Stellvertretungszugriff zum Abrufen von Daten aus dem Postfachspeicher. Es folgen einige Beispiele für Clientanwendungen, die Exchange-Webdienste verwenden:
  
- Outlook in Features wie beispielsweise e-Mail-Infos, Verfügbarkeit und Benutzer Abwesenheitsstatus
    
- OWA für Geräte
    
- Outlook für Mac 2011
    
- Lync, Informationen zur Verfügbarkeit
    
Clientanwendungen verwenden häufig direkten Zugriff und Basic oder NTLM-Authentifizierung, damit Benutzer auf den Zugriff auf Informationen in ihr eigenes Postfach mit ihren eigenen Anmeldeinformationen beschränkt sind. Clientanwendungen sollten auch unterstützen Delegieren des Zugriffs für Benutzer, die Berechtigung zum Postfach eines anderen Benutzers zugreifen auf erteilt wurden.
  
## <a name="portal-applications"></a>Portal Applikationen
<a name="bk_portalapps"> </a>

Eine Webportal Anwendung erweitert eine vorhandene Webseiten oder Portal mit Exchange-Postfachinformationen als personalisierte Komponente der Seite aktualisiert. SharePoint-Webparts sind die am häufigsten verwendeten Anwendungen Portal und bieten den Benutzern eine personalisierte Erfahrung durch Bereitstellen von Ansichten in der Exchange-Postfachdaten, wie ungelesene Nachrichten, neuesten Nachrichten und Kalenderereignisse zusammen mit ihren häufigsten angezeigten SharePoint Portal-Seite. Portal EWS-Anwendungen können direkte Clientzugriff, Stellvertretungszugriff oder Identitätswechsel zum Abrufen von Daten aus dem Postfachspeicher verwenden. Da Exchange 2013 und SharePoint 2013 das OAuth-Autorisierung-Protokoll für die Server-zu-Server-Authentifizierung unterstützen, bietet OAuth die am häufigsten nahtlose und sichere Authentifizierungsmethode.
  
## <a name="service-applications"></a>Dienstanwendungen
<a name="bk_serviceapps"> </a>

Eine dienstanwendung ist in der Regel einen Hintergrundauftrag in eine vorhandene Anwendung, die erweitert zu Exchange zum Korrelieren von Daten zwischen dem System und Exchange-Speicher integriert. Dienstanwendungen werden in der Regel nicht über eine Benutzeroberfläche verfügen und Identitätswechsel oder OAuth-Authentifizierung und Zugriff verwenden. Erstellen eines Dienstkontos, um Benutzer zu imitieren ist häufig in EWS-Dienst-apps, da Sie eine Konto die Berechtigung zum Identitätswechsel für eine Gruppe von Benutzern und Postfachverschiebevorgänge für diese Konten ausführen gewähren können. Beispielsweise kann eine EWS-Anwendung Daten zwischen Marketinglisten in einer CRM-Lösung und Exchange-Verteilergruppen mithilfe eines Dienstkontos und Identitätswechsel synchronisieren.
  
## <a name="see-also"></a>Siehe auch


- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS-Anwendungen und der Exchange-Architektur](ews-applications-and-the-exchange-architecture.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

