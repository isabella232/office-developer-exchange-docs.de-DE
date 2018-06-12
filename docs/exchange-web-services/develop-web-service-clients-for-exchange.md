---
title: Entwickeln von Webdienstclients für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 899ba15b-336d-4f9b-8563-318c61e43713
description: Hier finden Sie Informationen zum Entwickeln von EWS- und Webdienst-Clientanwendungen für Exchange.
ms.openlocfilehash: 2b8b032124e45dda7c83932d519ffb87bcdb5514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756817"
---
# <a name="develop-web-service-clients-for-exchange"></a><span data-ttu-id="f0447-103">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-103">Develop web service clients for Exchange</span></span>

<span data-ttu-id="f0447-104">Hier finden Sie Informationen zum Entwickeln von EWS- und Webdienst-Clientanwendungen für Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0447-104">Find information to help you develop EWS and web service client applications for Exchange.</span></span>
  
<span data-ttu-id="f0447-105">In den Artikeln dieses Abschnitts wird erläutert, wie EWS und Webdienste in Ihren Exchange-Clientanwendungen für Exchange Online, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Exchange 2013 verwendet werden. Außerdem werden Beispiele für die Durchführung bestimmter Aufgaben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f0447-105">The articles in this section explain how to use EWS and web services in your Exchange client applications for Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange 2013, and provide examples that show you how to perform specific tasks.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="f0447-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="f0447-106">In this section</span></span>

- [<span data-ttu-id="f0447-107">Archivierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-107">Archiving in EWS in Exchange</span></span>](archiving-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-108">Attachments and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-108">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-109">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-109">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-110">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-110">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-111">Verteilergruppen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-111">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-112">eDiscovery in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-112">eDiscovery in EWS in Exchange</span></span>](ediscovery-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-113">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-113">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-114">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-114">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-115">Bezeichner in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-115">Identifiers in Exchange</span></span>](ews-identifiers-in-exchange.md)
    
- [<span data-ttu-id="f0447-116">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-116">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-117">Posteingangsverwaltung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-117">Inbox management and EWS in Exchange</span></span>](inbox-management-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-118">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-118">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-119">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-119">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-120">Persistent Anwendungseinstellungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-120">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-121">Eigenschaften und erweiterte Eigenschaften in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-121">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-122">Eigenschaftensätze und Antwort shapes in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-122">Property sets and response shapes in EWS in Exchange</span></span>](property-sets-and-response-shapes-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-123">Zugriff auf Öffentliche Ordner mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-123">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-124">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-124">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-125">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-125">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-126">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-126">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f0447-127">Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-127">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    
- [<span data-ttu-id="f0447-128">Überprüfen der Ergebnisse eines EWS oder EWS verwalteten API-Aufrufs</span><span class="sxs-lookup"><span data-stu-id="f0447-128">Verifying the results of an EWS or EWS Managed API call</span></span>](verifying-the-results-of-an-ews-or-ews-managed-api-call.md)
    
## <a name="see-also"></a><span data-ttu-id="f0447-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0447-129">See also</span></span>

- [<span data-ttu-id="f0447-130">Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-130">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)     
- [<span data-ttu-id="f0447-131">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-131">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="f0447-132">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-132">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)  
- [<span data-ttu-id="f0447-133">Referenz für Webdienste für Exchange</span><span class="sxs-lookup"><span data-stu-id="f0447-133">Web services reference for Exchange</span></span>](../web-service-reference/web-services-reference-for-exchange.md)
    
