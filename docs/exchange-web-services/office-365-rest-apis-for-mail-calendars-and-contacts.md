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
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="cfe2d-103">Microsoft Graph-REST-APIs für E-Mail, Kalender und Kontakte</span><span class="sxs-lookup"><span data-stu-id="cfe2d-103">Microsoft Graph REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="cfe2d-104">Hier finden Sie Informationen zu den Microsoft Graph-APIs, die Sie für den Zugriff auf e-Mails, Kalender und Kontakte in Office 365, Exchange Online oder Exchange Server in hybridbereitstellungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-104">Find information about the Microsoft Graph APIs that you can use to access mail, calendars, and contacts in Office 365, Exchange Online, or Exchange Server in hybrid deployments.</span></span>

<span data-ttu-id="cfe2d-105">Office 365, Exchange Online und Exchange Server in hybridbereitstellungen stellen eine neue Möglichkeit zum Arbeiten mit e-Mails, Kalendern und Kontakten dar.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-105">Office 365, Exchange Online, and Exchange Server in hybrid deployments provide a new way to work with email, calendars, and contacts.</span></span> <span data-ttu-id="cfe2d-106">Die REST-APIs für Microsoft Graph-E-Mails, Kalender und Kontakte ermöglichen eine effiziente und einfache Möglichkeit zum Zugreifen auf und zum Bearbeiten von Exchange-Daten.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-106">The Microsoft Graph Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data.</span></span> <span data-ttu-id="cfe2d-107">Diese APIs basieren auf offenen Standards: OAuth 2.0 Version für Authentifizierung und OData-Version 4.0 und JSON für Datenabstraktion.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-107">These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction.</span></span> <span data-ttu-id="cfe2d-108">Diese bieten die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="cfe2d-108">This provides the following advantages:</span></span>

- <span data-ttu-id="cfe2d-109">Da die APIs OAuth für die Authentifizierung benötigen, muss Ihre Anwendung keine Benutzeranmeldeinformationen verarbeiten oder speichern.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>

- <span data-ttu-id="cfe2d-p102">OAuth ermöglicht die Anforderung von Berechtigungen mit bereichsbezogenem Gültigkeitsbereich für Benutzerdaten. Sie möchten ggf. eine Anwendung zum Anfordern von Berechtigungen und schreibgeschütztem Zugriff auf den Kalender eines Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-p102">OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.</span></span>

## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="cfe2d-112">Arbeiten mit E-Mails und E-Mail-Ordnern</span><span class="sxs-lookup"><span data-stu-id="cfe2d-112">Work with email and mail folders</span></span>

<span data-ttu-id="cfe2d-p103">Mit der [E-Mail-API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) können Sie E-Mails abrufen, erstellen, aktualisieren, löschen, verschieben, kopieren und senden. Sie können auch E-Mail-Ordner abrufen, erstellen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-p103">You can use the [Mail API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="cfe2d-115">Abreiten mit Ereignissen, Kalendern und Kalendergruppen</span><span class="sxs-lookup"><span data-stu-id="cfe2d-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="cfe2d-p104">Mit der [Kalender-API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) können Sie Ereignisse abrufen, erstellen, aktualisieren und löschen. Sie können auch Kalendergruppen und Kalender abrufen, erstellen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-p104">You can use the [Calendar API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="cfe2d-118">Arbeiten mit Kontakten und Kontakteordnern</span><span class="sxs-lookup"><span data-stu-id="cfe2d-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="cfe2d-p105">Mit der [Kontakte-API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) können Sie Kontakte im Postfach eines Benutzers abrufen, erstellen, aktualisieren und löschen. Sie können auch Kontakteordner abrufen.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-p105">You can use the [Contacts API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="cfe2d-121">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="cfe2d-121">Next steps</span></span>

<span data-ttu-id="cfe2d-122">Auf der Seite [Microsoft Graph-Dokumentation](https://developer.microsoft.com/graph/docs/concepts/overview) erhalten Sie weitere Informationen zu den E-Mail-, Kalender- und Kontakte-APIs, einschließlich Anleitungen zum Einrichten Ihrer Umgebung und Erste Schritte mit APIs .</span><span class="sxs-lookup"><span data-stu-id="cfe2d-122">Head over to the [Microsoft Graph documentation](https://developer.microsoft.com/graph/docs/concepts/overview) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.</span></span> 

<span data-ttu-id="cfe2d-123">Schauen Sie sich auch die [Schnellstarts](https://developer.microsoft.com/graph/quick-start) und [Codebeispiele](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) an, die veranschaulichen, wie diese APIs arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cfe2d-123">Also be sure to check out the [quick starts](https://developer.microsoft.com/graph/quick-start) and [code samples](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfe2d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfe2d-124">See also</span></span>

- [<span data-ttu-id="cfe2d-125">Microsoft Graph-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="cfe2d-125">Microsoft Graph documentation</span></span>](https://developer.microsoft.com/graph/docs/concepts/overview)   
- [<span data-ttu-id="cfe2d-126">Lokale Anforderungen für die Rest-API</span><span class="sxs-lookup"><span data-stu-id="cfe2d-126">On-premises requirements for the REST API</span></span>](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api)   

