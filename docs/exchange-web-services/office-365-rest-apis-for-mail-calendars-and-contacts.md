---
title: Office 365-REST-APIs für E-Mail, Kalender und Kontakte
manager: sethgros
ms.date: 4/29/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: Hier finden Sie Informationen zu Office 365-APIs, mit denen Sie auf E-Mails, Kalender und Kontakte in Office 365 oder Exchange Online zugreifen können.
ms.openlocfilehash: d42d3ff0b68dfbf23d5a4eebb826a6d39a4ac116
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757117"
---
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a>Office 365-REST-APIs für E-Mail, Kalender und Kontakte

Hier finden Sie Informationen zu Office 365-APIs, mit denen Sie auf E-Mails, Kalender und Kontakte in Office 365 oder Exchange Online zugreifen können.
  
Office 365 und Exchange Online bieten eine neue Arbeitsweise mit E-Mails, Kalendern und Kontakten. Die REST-APIs für E-Mails, Kalender und Kontakte ermöglichen einen leistungsstarke und einfache Art des Zugriffs auf und der Bearbeitung von Exchange-Daten. Diese APIs basieren auf offenen Standards: OAuth-Version 2.0 für Authentifizierung und OData-Version 4.0 und JSON für Datenabstraktion. Diese bieten die folgenden Vorteile:
  
- Da die APIs OAuth für die Authentifizierung benötigen, muss Ihre Anwendung keine Benutzeranmeldeinformationen verarbeiten oder speichern.
    
- OAuth ermöglicht die Anforderung von Berechtigungen mit bereichsbezogenem Gültigkeitsbereich für Benutzerdaten. Sie möchten ggf. eine Anwendung zum Anfordern von Berechtigungen und schreibgeschütztem Zugriff auf den Kalender eines Benutzers erstellen.
    
## <a name="work-with-email-and-mail-folders"></a>Arbeiten mit E-Mails und E-Mail-Ordnern

Mit der [E-Mail-API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) können Sie E-Mails abrufen, erstellen, aktualisieren, löschen, verschieben, kopieren und senden. Sie können auch E-Mail-Ordner abrufen, erstellen, aktualisieren und löschen. 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>Abreiten mit Ereignissen, Kalendern und Kalendergruppen

Mit der [Kalender-API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) können Sie Ereignisse abrufen, erstellen, aktualisieren und löschen. Sie können auch Kalendergruppen und Kalender abrufen, erstellen, aktualisieren und löschen. 
  
## <a name="work-with-contacts-and-contact-folders"></a>Arbeiten mit Kontakten und Kontakteordnern

Mit der [Kontakte-API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) können Sie Kontakte im Postfach eines Benutzers abrufen, erstellen, aktualisieren und löschen. Sie können auch Kontakteordner abrufen. 
  
## <a name="work-with-file-providers"></a>Arbeiten mit Dateianbietern

Mit der [Dateianbieter-REST-API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) können Sie Informationen zu unterstützten Dateianbietern wie Mailbox, Dropbox usw. abrufen, erstellen, aktualisieren und löschen. 
  
## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu E-Mail-, Kalender- und Kontakte-APIs, einschließlich Anleitungen zum Einrichten Ihrer Umgebung und Erste Schritte mit APIs finden Sie auf der Seite [Entwickeln auf der Office 365-Plattform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx). Schauen Sie sich auch die [Startprojekte und Codebeispiele](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) an, die veranschaulichen, wie diese APIs arbeiten. 
  
## <a name="see-also"></a>Siehe auch


- [Entwickeln auf der Office 365-Plattform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [Erstellen einer Office 365 ASP.NET-MVC-App](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [E-Mail-REST-Vorgänge](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [Kalender-REST-Vorgänge](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [Kontakte-REST-Vorgänge](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [Office 365-APIs-Startprojekte und -Codebeispiele](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

