---
title: Identitätswechsel und EWS in Exchange
manager: sethgros
ms.date: 08/24/2020
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Erfahren Sie mehr über den Identitätswechsel und wann er in Ihren Exchange-Dienstanwendungen eingesetzt werden kann.
localization_priority: Priority
ms.openlocfilehash: da35fb04f316c21a1c85c71b789b7f1485653466
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254972"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="e921d-103">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e921d-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="e921d-104">Erfahren Sie mehr über den Identitätswechsel und wann er in Ihren Exchange-[Dienstanwendungen](ews-application-types.md) eingesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e921d-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="e921d-105">Benutzer können mithilfe der folgenden drei Möglichkeiten auf Postfächer anderer Benutzer zugreifen:</span><span class="sxs-lookup"><span data-stu-id="e921d-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="e921d-106">Durch das Hinzufügen von Stellvertretungen und dem Angeben von Berechtigungen für die einzelnen Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e921d-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="e921d-107">Durch direktes Ändern der Ordnerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="e921d-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="e921d-108">Durch Verwenden eines Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="e921d-108">By using impersonation.</span></span>
    
<span data-ttu-id="e921d-p101">Wann sollten eher der Identitätswechsel als Stellvertreter oder Ordnerberechtigungen eingesetzt werden? Die folgenden Richtlinien unterstützen Sie bei der Entscheidung:</span><span class="sxs-lookup"><span data-stu-id="e921d-p101">When should you choose impersonation over delegation or folder permissions? The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="e921d-111">Verwenden Sie Ordnerberechtigungen, wenn Sie einen Benutzerzugriff auf einen Ordner bereitstellen möchten, dem Benutzer jedoch keine „Senden im Auftrag von"-Berechtigungen geben möchten.</span><span class="sxs-lookup"><span data-stu-id="e921d-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="e921d-p102">Verwenden Sie den Stellvertreterzugriff , wenn Sie einem Benutzer die Berechtigung erteilen möchten, Arbeiten im Auftrag eines anderen Benutzers durchzuführen. In der Regel handelt es sich dabei um eine 1:1- oder 1:viele-Berechtigung - beispielsweise ein einzelner Verwaltungsassistent, der den Kalender für einen Administrator verwaltet, oder ein einzelner Raumbelegungsplaner, der die Kalender für eine Gruppe von Besprechungsräumen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e921d-p102">Use delegate access when you want to give one user permission to perform work on behalf of another user. Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="e921d-114">Verwenden Sie den Identitätswechsel, wenn Sie eine Dienstanwendung haben, die auf mehrere Postfächer zugreifen muss und als Postfachbesitzer agieren soll.</span><span class="sxs-lookup"><span data-stu-id="e921d-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="e921d-p103">Der Identitätswechsel ist die beste Wahl für den Umgang mit mehreren Postfächern, da Sie einfach einem Dienstkonto die Berechtigung erteilen können, auf alle Postfächer in einer Datenbank zuzugreifen. Die Stellvertretung und Ordnerberechtigungen sind die beste Wahl, wenn Sie nur einigen Benutzern den Zugriff gewähren, da Sie für jedes Postfach einzeln Berechtigungen hinzufügen müssen. Abbildung 1 veranschaulicht einige der Unterschiede zwischen den einzelnen Zugriffstypen.</span><span class="sxs-lookup"><span data-stu-id="e921d-p103">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database. Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox. Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="e921d-118">**Abbildung 1. Möglichkeiten für den Zugriff auf Postfächer anderer Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e921d-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![Diagramm, das Postfachzugriffstypen, die die Beziehung zwischen dem/den Postfacheigentümer(n) und dem Delegaten für jeden Typ und den Berechtigungstyp zeigt. Senden im Namen von Berechtigungen für Delegation und/oder Ordnerberechtigungen. Senden als Berechtigungen für Identitätswechsel.](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="e921d-p105">Der Identitätswechsel ist ideal für Anwendungen, die eine Verbindung zu Exchange Online, Exchange Online als Teil von Office 365 und lokalen Versionen von Exchange herstellen und Vorgänge ausführen, wie z. B. das Archivieren von E-Mails, das automatische Einstellen von Abwesenheitsnachrichten für abwesende Benutzer oder eine andere Aufgabe, für die die Anwendung als Besitzer eines Postfachs agieren muss. Wenn eine Anwendung den Identitätswechsel zum Senden einer Nachricht verwendet, wird die E-Mail so angezeigt, als hätte Sie der Postfachbesitzer gesendet. Es gibt für den Empfänger keine Möglichkeit, herauszufinden, dass die Nachricht vom Dienstkonto versendet wurde. Die Stellvertretung hingegen erteilt einem anderen Postfachkonto die Berechtigung, im Auftrag eines Postfachbesitzers zu agieren. Wenn eine Nachricht durch einen Stellvertreter gesendet wird, identifiziert der „von"-Wert den Postfachbesitzer und der „Absender"-Wert den Stellvertreter, der die E-Mail versendet hat.</span><span class="sxs-lookup"><span data-stu-id="e921d-p105">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox. When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner. There is no way for the recipient to know the mail was sent by the service account. Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner. When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="e921d-127">Sicherheitsaspekte für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="e921d-127">Security considerations for impersonation</span></span>

<span data-ttu-id="e921d-p106">Mit dem Identitätswechsel kann ein Aufrufer einen Identitätswechsel für ein angegebenes Benutzerkonto vornehmen. Dadurch kann der Aufrufer Vorgänge ausführen, indem er die Berechtigungen verwendet, die dem imitierten Konto zugeordnet sind, statt die Berechtigungen zu verwenden, die dem Konto des Aufrufers zugeordnet sind. Aus diesem Grund sollten Sie folgende Sicherheitsaspekte berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="e921d-p106">Impersonation enables a caller to impersonate a given user account. This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account. For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="e921d-131">Nur Konten, denen von einem Exchange-Serveradministrator die **ApplicationImpersonation**-Rolle gewährt wurde, können den Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="e921d-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="e921d-p107">Sie sollten einen Verwaltungsbereich erstellen, der den Identitätswechsel auf eine bestimmte Kontogruppe begrenzt. Wenn Sie keinen Verwaltungsbereich erstellen, wird die **ApplicationImpersonation**-Rolle allen Konten in einem Unternehmen gewährt.</span><span class="sxs-lookup"><span data-stu-id="e921d-p107">You should create a management scope that limits impersonation to a specified group of accounts. If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="e921d-p108">In der Regel wird die **ApplicationImpersonation**-Rolle einem Dienstkonto gewährt, das einer bestimmten Anwendung oder eine Gruppe von Anwendungen zugeordnet ist, statt einem Benutzerkonto. Sie können beliebig viele Dienstkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="e921d-p108">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account. You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="e921d-136">Sie können weitere Informationen über die [Konfiguration des Identitätswechsels](how-to-configure-impersonation.md) lesen, Sie sollten jedoch mit Ihrem Exchange-Administrator zusammenarbeiten, um zu gewährleisten, dass die erforderlichen Dienstkonten mit den [Berechtigungen und dem Zugriff](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) erstellt werden, der die Sicherheitsanforderungen Ihres Unternehmens erfüllt.</span><span class="sxs-lookup"><span data-stu-id="e921d-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e921d-137">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e921d-137">In this section</span></span>

- [<span data-ttu-id="e921d-138">Konfigurieren eines Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="e921d-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="e921d-139">Identifizieren des Kontos für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="e921d-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="e921d-140">Hinzufügen von Terminen mit Exchange-Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="e921d-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)

## <a name="performance-considerations-for-ews-impersonation"></a><span data-ttu-id="e921d-141">Überlegungen zur Leistung für EWS-Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="e921d-141">Performance considerations for EWS impersonation</span></span>

<span data-ttu-id="e921d-142">Wenn ein EWS-Identitätswechsel verwendet wird, sollte X-AnchorMailbox immer ordnungsgemäß festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e921d-142">When EWS Impersonation is used, the X-AnchorMailbox should always be correctly set.</span></span>  <span data-ttu-id="e921d-143">Andernfalls erhalten Sie möglicherweise die Fehlermeldungen 500 oder 503.</span><span class="sxs-lookup"><span data-stu-id="e921d-143">Otherwise, you may get error messages 500 or 503 at times.</span></span> <span data-ttu-id="e921d-144">Dies ist wichtig für die Leistung sowie für Benachrichtigungen mit Exchange Online/Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e921d-144">It is critical for performance and also for notifications with Exchange Online/Exchange 2013.</span></span>  <span data-ttu-id="e921d-145">Wenn Sie die Einstellung nicht festlegen, kann Sie die für die Ausführung des Aufrufs benötigte Zeit verdoppeln oder vervielfachen.</span><span class="sxs-lookup"><span data-stu-id="e921d-145">Not setting it can double or more the time it takes to complete the call.</span></span> <span data-ttu-id="e921d-146">In einigen Fällen können auch Timeouts auftreten.</span><span class="sxs-lookup"><span data-stu-id="e921d-146">In some cases, you can also get timeouts.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e921d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e921d-147">See also</span></span>


- [<span data-ttu-id="e921d-148">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="e921d-148">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="e921d-149">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e921d-149">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="e921d-150">Exchange 2013-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e921d-150">Exchange 2013 Permissions</span></span>](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

