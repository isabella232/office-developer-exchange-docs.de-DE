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
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="ed800-103">Office 365-REST-APIs für E-Mail, Kalender und Kontakte</span><span class="sxs-lookup"><span data-stu-id="ed800-103">Office 365 REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="ed800-104">Hier finden Sie Informationen zu Office 365-APIs, mit denen Sie auf E-Mails, Kalender und Kontakte in Office 365 oder Exchange Online zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ed800-104">Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.</span></span>
  
<span data-ttu-id="ed800-p101">Office 365 und Exchange Online bieten eine neue Arbeitsweise mit E-Mails, Kalendern und Kontakten. Die REST-APIs für E-Mails, Kalender und Kontakte ermöglichen einen leistungsstarke und einfache Art des Zugriffs auf und der Bearbeitung von Exchange-Daten. Diese APIs basieren auf offenen Standards: OAuth-Version 2.0 für Authentifizierung und OData-Version 4.0 und JSON für Datenabstraktion. Diese bieten die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="ed800-p101">Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts. The Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data. These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction. This provides the following advantages:</span></span>
  
- <span data-ttu-id="ed800-109">Da die APIs OAuth für die Authentifizierung benötigen, muss Ihre Anwendung keine Benutzeranmeldeinformationen verarbeiten oder speichern.</span><span class="sxs-lookup"><span data-stu-id="ed800-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>
    
- <span data-ttu-id="ed800-p102">OAuth ermöglicht die Anforderung von Berechtigungen mit bereichsbezogenem Gültigkeitsbereich für Benutzerdaten. Sie möchten ggf. eine Anwendung zum Anfordern von Berechtigungen und schreibgeschütztem Zugriff auf den Kalender eines Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed800-p102">OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.</span></span>
    
## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="ed800-112">Arbeiten mit E-Mails und E-Mail-Ordnern</span><span class="sxs-lookup"><span data-stu-id="ed800-112">Work with email and mail folders</span></span>

<span data-ttu-id="ed800-p103">Mit der [E-Mail-API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) können Sie E-Mails abrufen, erstellen, aktualisieren, löschen, verschieben, kopieren und senden. Sie können auch E-Mail-Ordner abrufen, erstellen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="ed800-p103">You can use the [Mail API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="ed800-115">Abreiten mit Ereignissen, Kalendern und Kalendergruppen</span><span class="sxs-lookup"><span data-stu-id="ed800-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="ed800-p104">Mit der [Kalender-API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) können Sie Ereignisse abrufen, erstellen, aktualisieren und löschen. Sie können auch Kalendergruppen und Kalender abrufen, erstellen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="ed800-p104">You can use the [Calendar API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="ed800-118">Arbeiten mit Kontakten und Kontakteordnern</span><span class="sxs-lookup"><span data-stu-id="ed800-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="ed800-p105">Mit der [Kontakte-API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) können Sie Kontakte im Postfach eines Benutzers abrufen, erstellen, aktualisieren und löschen. Sie können auch Kontakteordner abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed800-p105">You can use the [Contacts API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders.</span></span> 
  
## <a name="work-with-file-providers"></a><span data-ttu-id="ed800-121">Arbeiten mit Dateianbietern</span><span class="sxs-lookup"><span data-stu-id="ed800-121">Work with file providers</span></span>

<span data-ttu-id="ed800-122">Mit der [Dateianbieter-REST-API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) können Sie Informationen zu unterstützten Dateianbietern wie Mailbox, Dropbox usw. abrufen, erstellen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="ed800-122">You can use the [File Providers REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) to get, create, update, and delete information about supported file providers, such as mailbox, Dropbox, and so on.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="ed800-123">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ed800-123">Next steps</span></span>

<span data-ttu-id="ed800-p106">Weitere Informationen zu E-Mail-, Kalender- und Kontakte-APIs, einschließlich Anleitungen zum Einrichten Ihrer Umgebung und Erste Schritte mit APIs finden Sie auf der Seite [Entwickeln auf der Office 365-Plattform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx). Schauen Sie sich auch die [Startprojekte und Codebeispiele](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) an, die veranschaulichen, wie diese APIs arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ed800-p106">Head over to the [Developing on the Office 365 platform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs. Also be sure to check out the [starter projects and code samples](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed800-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed800-126">See also</span></span>


- [<span data-ttu-id="ed800-127">Entwickeln auf der Office 365-Plattform</span><span class="sxs-lookup"><span data-stu-id="ed800-127">Developing on the Office 365 platform</span></span>](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [<span data-ttu-id="ed800-128">Erstellen einer Office 365 ASP.NET-MVC-App</span><span class="sxs-lookup"><span data-stu-id="ed800-128">Building an Office 365 ASP.NET MVC app</span></span>](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [<span data-ttu-id="ed800-129">E-Mail-REST-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ed800-129">Mail REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="ed800-130">Kalender-REST-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ed800-130">Calendar REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="ed800-131">Kontakte-REST-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ed800-131">Contacts REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="ed800-132">Office 365-APIs-Startprojekte und -Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="ed800-132">Office 365 APIs starter projects and code samples</span></span>](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

