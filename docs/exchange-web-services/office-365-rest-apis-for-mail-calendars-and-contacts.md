---
title: Microsoft Graph-Outlook-API für E-Mail, Kalender und Kontakte
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: Hier finden Sie Informationen zu der Microsoft Graph-API, mit denen Sie auf E-Mails, Kalender und Kontakte in Office 365 oder Exchange Online zugreifen können.
localization_priority: Priority
ms.openlocfilehash: 7ca77596afb59ffab76001abd495de7328d2dd29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463867"
---
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a>Microsoft Graph-REST-APIs für E-Mail, Kalender und Kontakte

Hier finden Sie Informationen zu den Microsoft Graph-APIs, die Sie für den Zugriff auf e-Mails, Kalender und Kontakte in Office 365, Exchange Online oder Exchange Server in hybridbereitstellungen verwenden können.

Office 365, Exchange Online und Exchange Server in hybridbereitstellungen stellen eine neue Möglichkeit zum Arbeiten mit e-Mails, Kalendern und Kontakten dar. Die REST-APIs für Microsoft Graph-E-Mails, Kalender und Kontakte ermöglichen eine effiziente und einfache Möglichkeit zum Zugreifen auf und zum Bearbeiten von Exchange-Daten. Diese APIs basieren auf offenen Standards: OAuth 2.0 Version für Authentifizierung und OData-Version 4.0 und JSON für Datenabstraktion. Diese bieten die folgenden Vorteile:

- Da die APIs OAuth für die Authentifizierung benötigen, muss Ihre Anwendung keine Benutzeranmeldeinformationen verarbeiten oder speichern.

- OAuth ermöglicht die Anforderung von Berechtigungen mit bereichsbezogenem Gültigkeitsbereich für Benutzerdaten. Sie möchten ggf. eine Anwendung zum Anfordern von Berechtigungen und schreibgeschütztem Zugriff auf den Kalender eines Benutzers erstellen.

## <a name="work-with-email-and-mail-folders"></a>Arbeiten mit E-Mails und E-Mail-Ordnern

Mit der [E-Mail-API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) können Sie E-Mails abrufen, erstellen, aktualisieren, löschen, verschieben, kopieren und senden. Sie können auch E-Mail-Ordner abrufen, erstellen, aktualisieren und löschen. 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>Abreiten mit Ereignissen, Kalendern und Kalendergruppen

Mit der [Kalender-API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) können Sie Ereignisse abrufen, erstellen, aktualisieren und löschen. Sie können auch Kalendergruppen und Kalender abrufen, erstellen, aktualisieren und löschen. 
  
## <a name="work-with-contacts-and-contact-folders"></a>Arbeiten mit Kontakten und Kontakteordnern

Mit der [Kontakte-API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) können Sie Kontakte im Postfach eines Benutzers abrufen, erstellen, aktualisieren und löschen. Sie können auch Kontakteordner abrufen. 
  
## <a name="next-steps"></a>Nächste Schritte

Auf der Seite [Microsoft Graph-Dokumentation](https://developer.microsoft.com/graph/docs/concepts/overview) erhalten Sie weitere Informationen zu den E-Mail-, Kalender- und Kontakte-APIs, einschließlich Anleitungen zum Einrichten Ihrer Umgebung und Erste Schritte mit APIs . 

Schauen Sie sich auch die [Schnellstarts](https://developer.microsoft.com/graph/quick-start) und [Codebeispiele](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) an, die veranschaulichen, wie diese APIs arbeiten. 
  
## <a name="see-also"></a>Siehe auch

- [Microsoft Graph-Dokumentation](https://developer.microsoft.com/graph/docs/concepts/overview)   
- [Lokale Anforderungen für die Rest-API](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api)   

