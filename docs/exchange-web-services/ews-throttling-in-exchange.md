---
title: EWS-Einschränkung in Exchange
manager: sethgros
ms.date: 05/10/2019
ms.audience: Developer
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: Lernen Sie die Einschränkungsrichtlinien kennen, die sich bei Verwendung von Exchange auf EWS auswirken.
localization_priority: Priority
ms.openlocfilehash: 27db12c01180abbaf92b5b9a09a072212b6012ec
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012552"
---
# <a name="ews-throttling-in-exchange"></a>EWS-Einschränkung in Exchange

Lernen Sie die Einschränkungsrichtlinien kennen, die sich bei Verwendung von Exchange auf EWS auswirken.

**Bereitgestellt von:** Glen Scales; Michael Mainer, Microsoft Corporation

The article provides information about EWS throttling in Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange 2010. Throttling in Exchange helps to ensure server reliability and uptime by limiting the amount of server resources that a single user or application can consume. Throttling is a reactive response to overuse of system resources that may affect service reliability and functionality. Exchange constantly monitors the health of critical infrastructure resources, such as mailbox databases. When high load factors are detected that degrade the performance of these resources, EWS connections are throttled proportionally based on the amount that each caller has contributed to this high load condition. The result is that a user may be within their throttling limit and still experience slowdowns until the health of the resource is back to operational levels.

Each client access protocol in Exchange, including EWS, has a throttling policy. When you design applications that use EWS, it is important to account for throttling policies, to help ensure application reliability and the health of your Exchange server. This article identifies the different throttling policies and service limits for EWS, whether you are targeting Exchange Online or versions of Exchange on-premises starting with Exchange Server 2010. As applicable, this article also identifies differences in throttling policies in different versions of Exchange.

> [!IMPORTANT]
> Default throttling policy, access to throttling policy, and throttling policy configuration differs between Exchange Online and Exchange on-premises. Specific throttling setting values are only accurate for a specific version of Exchange. Because setting values vary across versions, and because Exchange administrators can change the default throttling policies for on-premises deployments, this article does not provide the default setting values. It is more important for you to be aware of the considerations for designing an application that functions within throttling limits and reacts appropriately to throttling scenarios.

Als Anwendungsentwickler müssen Sie in Ihrem Anwendungsentwurf Einschränkungen berücksichtigen. Unterschiedliche Exchange-Versionen haben unterschiedliche Standardwerte für die EWS-Einschränkungsparameter. Client- und Dienstanwendungen, die für den Zugriff auf verschiedene Exchange-Versionen konzipiert sind, müssen diese Einstellungen berücksichtigen, egal ob es sich um Standardwerte, von einem Exchange-Administrator festgelegte benutzerdefinierte Werte oder - wie im Fall von Exchange Online - standardmäßig festgelegte und nicht auffindbare Werte handelt. Da Werte für Einschränkungsparameter nicht programmgesteuert ermittelt werden können, sollten die Cliententwurfsspezifikationen einen Plan enthalten, wie sich die Anwendung an verschiedene mögliche Einschränkungsgrenzwerte anpasst. Wenn Sie Multithread-Anwendungen entwerfen, die auf eine große Anzahl von Postfächern zugreifen, oder wenn viele Clients auf dasselbe Postfach zugreifen, berücksichtigen Sie die Grenzwerte für die Parallelität, die die Standardrichtlinie auf Exchange angewendet wird.

## <a name="throttling-policies-that-affect-ews"></a>Einschränkungsrichtlinien mit Auswirkung auf EWS

Die Einschränkungsrichtlinien in Exchange wirken sich nicht nur auf EWS, sondern auch auf alle Clientverbindungen mit dem Exchange-Server aus, einschließlich der von Office Outlook, Outlook Web App und Exchange ActiveSync verwendeten Protokolle.

The **CPUStartPercent** throttling policy can affect EWS performance when you are running Exchange 2010. When the average CPU utilization of Exchange processes running on the Client Access server — including, but not limited to, the EWS process — exceeds the value specified by this policy, inbound requests will be delayed to reduce CPU utilization. You cannot change the value of this policy, but knowing about it can help you troubleshoot performance issues. The sampling logic the Client Access server performs for this value is an average over a 10 second rolling window. This allows the process to respond appropriately to quick spikes in CPU utilization. When this threshold is exceeded, inbound connections to EWS are delayed. This delay is capped at 500 milliseconds (msecs) at a theoretical 100% CPU usage per EWS request. If a batch EWS request to get 100 items is passed, the server will check the CPU usage 100 times (once per item) for a maximum delay of 50 seconds. The delay time is linearly proportional to CPU usage. At **CPUStartPercent**, the delay is 0 (a thread yield) and it increases linearly up to 500 msec at 100% CPU usage. Because throttling policies apply to all Exchange users, it's unlikely that CPU usage would exceed the **CPUStartPercent** limit on an Exchange Client Access server, because individual users or applications cannot gain enough CPU utilization to affect server operation.

In der folgenden Tabelle sind die Einschränkungsrichtlinienparameter aufgeführt, die sich auf Anwendungen mit EWS-Nutzung auswirken.

**Tabelle 1: Einschränkungsrichtlinienparameter mit Auswirkung auf EWS**

|**Name des Einschränkungsrichtlinienparameters**|**Gilt für**|**Beschreibung**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl der gleichzeitigen Discoverysuchverbindungen an, die ein Benutzer zur gleichen Zeit geöffnet haben kann.  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Schlüsselwörtern an, die ein Benutzer in eine Discoverysuche einschließen kann.  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl an Schlüsselwörtern an, für die Statistiken angezeigt werden sollen.  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Quellpostfächern an, die ein Benutzer in eine Discoverysuche einschließen kann.  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Postfächern an, die Sie in einer In-Situ-eDiscovery-Suche durchsuchen können, ohne die Statistik anzeigen zu können.  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl an Nachrichten an, die in der Vorschauantwort einer eDiscovery-Suche zurückgegeben werden.  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Grenzwerte für die Ressourcennutzung für EWS-Benutzer, bevor der Benutzer vollständig an der Ausführung von Vorgängen für eine bestimmte Komponente gehindert wird.  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Defines the amount of time that an EWS user can consume an elevated amount of resources before being throttled. This is measured in milliseconds. This value is set separately for each component.  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Rate, mit der das Budget eines EWS-Benutzers während der Budgetzeit aufgeladen wird (um die das Budget wächst).  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Defines the maximum number of active push, pull, and streaming notification subscriptions that a user can have on a specific Client Access server at one time. This is budgeted differently for different Exchange versions.  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |Definiert die Zeitspanne in Sekunden, die mit der Exchange-Suche in EWS durchgeführte schnelle Suchläufe fortgesetzt werden, bevor ein Timeout eintritt. Schnelle Suchläufe sind Suchvorgänge, die mithilfe einer AQS-Abfragezeichenfolge (Advanced Query Syntax, erweiterte Abfragesyntax) in einem [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) ausgeführt werden.      <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Defines the maximum number of items from a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) or [FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) that can exist in memory on the Client Access server at one time for one user. The default value for this property is 1000. The [fallback value](https://technet.microsoft.com/library/dd297964%28v=exchg.141%29.aspx#fallback)for this value is 1000.  <br/> In Exchange Online and on-premises versions of Exchange starting with Exchange 2013, this throttling policy cannot be queried or configured by a cmdlet. In Exchange Online and on-premises versions of Exchange starting with Exchange 2013, the EWSFindCountLimit for [AQS search](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) and any Exchange search with a restriction is 250 results. An Exchange search without a restriction will return up to 1000 results.  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Active Directory-Anforderungen ausführen kann.  <br/> |
|**EWSPercentTimeInCAS** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Clientzugriffsserver-Code ausführen kann.  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Postfach-RPC-Anforderungen ausführen kann.  <br/> |
|**EWSMaxConcurrency** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Defines the number of concurrent open connections that a specific user can have against an Exchange server that is using EWS at one time. The default value for Exchange 2010 is 10. The default value for Exchange 2013 and Exchange Online is 27.  <br/> This policy applies to all operations except for streaming notifications. Streaming notifications use the **HangingConnectionLimit** to indicate the number of open streaming event connections that are available. For more information, see [What throttling values do I need to take into consideration?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Anzahl an Nachrichten pro Minute, die gesendet werden können.  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert den Grenzwert für die Anzahl an Empfängern, die ein Benutzer in einem Zeitraum von 24 Stunden adressieren kann.  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert den Grenzwert für die Anzahl an Empfängern für Weiterleitungs-/Umleitungsaktionen im Posteingang in einem Zeitraum von 24 Stunden.  <br/> |
|**ConcurrentSyncCalls** <br/> |Exchange 2019  <br/> Exchange 2016  <br/> Exchange Online  <br/> |Definiert den Grenzwert für die Anzahl gleichzeitiger Synchronisierungs Aufrufe (SyncFolderHierarchy, SyncFolderItems) für einen Benutzer. <br/> |

> [!CAUTION]
> Do not set throttling polices to **null**. This will set the policy to equal unlimited, which indicates that a throttling policy isn't set.

## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>Anzeigen der für Exchange-Postfächer geltenden Richtlinien

Exchange on-premises provides Exchange Management Shell cmdlets that you can use to set and get throttling policy. Exchange Online does not provide access to the throttling policy cmdlets.

Sie können die folgenden Cmdlets verwenden, um Einschränkungsrichtlinien für eine lokale Bereitstellung von Exchange Server anzuzeigen:

- **Get-ThrottlingPolicy** - Ruft die Clienteinschränkungseinstellungen für eine oder mehrere Einschränkungsrichtlinien ab. Weitere Informationen finden Sie unter [Get-ThrottlingPolicy](https://technet.microsoft.com/library/dd351264.aspx) auf TechNet.

- **Get-ThrottlingPolicyAssociation** — Enables you to view the relationship between an object and its associated throttling policies. The object can be a user with a mailbox, a user without a mailbox, or a contact. For more information, see [Get-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459241.aspx) on TechNet.

Verwenden Sie den folgenden Befehl, um die standardmäßige Einschränkungsrichtlinie für Exchange 2010 anzuzeigen.

**Get-ThrottlingPolicy | Where-Object {$_.IsDefault -eq "True"} | format-list**

Verwenden Sie den folgenden Befehl, um die globale Einschränkungsrichtlinie in Exchange 2013 anzuzeigen (die der standardmäßigen Einschränkungsrichtlinie in Exchange 2010 entspricht).

**Get-ThrottlingPolicy | Where-Object {$_.ThrottlingPolicyScope -eq "Global"} | format-list**

Use the following command to show the throttling policy associated with a user in Exchange 2010 or Exchange 2013. Replace the user name john@contoso.com with the user name of the target user for whom you want to get throttling policy information.

**Get-ThrottlingPolicyAssociation john@contoso.com | format-list**

Bei Ausführung dieses Befehls in der Exchange-Verwaltungsshell wird eine Ausgabe ähnlich der folgenden generiert.

```powershell
PS C:\>Get-ThrottlingPolicyAssociation john@contoso.com
RunspaceId               : 72153d6-9dce-2fae-8dbd-5ca5f760g2df
ObjectId                 : john
ThrottlingPolicyId       :
Name                     : john
Identity                 : FHXB-28178dom.contoso.com/Users/john
IsValid                  : True
NeedsToSuppressPii       : False
ExchangeVersion          : 0.10 (15.0.0.0)
DistinguishedName        : CN=john,CN=Users,DC=FHXB-28178dom,DC=contoso,DC=com
Guid                     : 2c10dab6-de28-1937-ad8g-535832613a08
```

> [!NOTE]
> [!HINWEIS] Wenn die **ThrottlingPolicyId** -Eigenschaft leer ist, wird die Standardrichtlinie auf das Postfach angewendet.

Sie können Einschränkungsrichtlinien auf einem Exchange-Server mithilfe der Cmdlets [Set-ThrottlingPolicy](https://technet.microsoft.com/library/dd298094.aspx) und [Set-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459231.aspx) festlegen. Sie können nicht standardmäßige Einschränkungsrichtlinien mithilfe der Cmdlets [New-ThrottlingPolicy](https://technet.microsoft.com/library/dd351045.aspx) und [Remove-ThrottlingPolicy](https://technet.microsoft.com/library/dd351178.aspx) erstellen und entfernen.

> [!TIP]
> We recommend that you design your applications to adhere to the default throttling policy. Only make changes to default throttling policies if your client application design cannot accommodate the default policy. Be aware that less restrictive throttling policies can negatively affect service reliability.

## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>Überlegungen zu Einschränkungen für Anwendungen, die den EWS-Identitätswechsel verwenden

[Impersonation](impersonation-and-ews-in-exchange.md) is an authorization method that enables a single account to access many accounts. When a service account impersonates users, it acts as the users and therefore assumes the rights that are assigned to those users. Log files record the access as the impersonated user. Administrators use role-based access control (RBAC) to configure impersonation via the Exchange Management Shell.

Wenn Identitätswechsel verwendet wird, gelten die Budgets für alle Einschränkungsschwellenwerte je nach Exchange-Version unterschiedlich. Das Budget wird entweder für das Konto, dessen Identität angenommen wird, oder für das Dienstkonto verrechnet. Wenn Ihre Anwendung Multithreaded ist und gleichzeitige Anforderungen an mehrere Postfächer stellt, sollten Sie berücksichtigen, wie sich der einschränkungsschwellenwert auf die Leistung Ihrer Anwendung auswirkt. Im Allgemeinen sollten Sie die folgenden Grenzwerte für Dienstkonten berücksichtigen, wenn Sie eine dienstbasierte Anwendung erstellen, die Identitätswechsel für den Zugriff auf alle Postfächer verwendet:

- Bei Verwendung von Identitätswechsel hat das Dienstkonto ein getrenntes Budget für die folgenden Richtlinienparameter:

  - **EWSMaxConcurrency**

  - **EWSPercentTimeInAD**

  - **EWSPercentTimeInCAS**

  - **EWSPercentTimeInMailboxRPC**

  - **EWSMaxSubscriptions**

  - **EWSFastSearchTimeoutInSeconds**

  - **EWSFindCountLimit**

- The **EWSMaxConcurrency** budget is shared for the service account and the account being impersonated for all connections to versions of Exchange earlier than Exchange 2010 Service Pack 2 (SP2) Update Rollup 4 (RU4). Starting with Exchange 2010 SP2 RU4, and including Exchange Online, the service account access uses a separate budget from the user **EWSMaxConcurrency** budget. For more information about the update to the Exchange concurrent connection throttling policy for EWS, see [Description of Update Rollup 4 for Exchange Server 2010 Service Pack 2](https://support.microsoft.com/kb/2706690).

    EWS streaming notifications in versions of Exchange starting with Exchange 2010, and including Exchange Online, have an additional cloned **EWSMaxConcurrency** budget from all other EWS client connections. Streaming notification connections are counted against a separate budget than all other EWS operations. The streaming notification maximum concurrency budget is actually two different budgets: one budget is for all service accounts, and one budget is for the account being impersonated. Streaming notifications in Exchange Online and versions of Exchange starting with Exchange 2013 use the [HangingConnectionLimit](#throttling-considerations-for-ews-notification-applications) to limit the number of connections.

    For example, let's assume that **EWSMaxConcurrency** is equal to five. A user can have five open pull notification connections, while an service account can have five concurrent pull notification connections against the user's mailbox at the same time as the user.

- Die folgende Tabelle zeigt, wie **EWSMaxSubscriptions** -Einschränkungsbudgets für das Dienstkonto und das Konto, dessen Identität angenommen werden soll, verrechnet werden.

   **Tabelle 2: EWSMaxSubscriptions-Budgetberechnung**

   |**Exchange-Version**|**EWSMaxSubscriptions-Einschränkungsbudgetberechnung**|
   |:-----|:-----|
   |Exchange Online  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2013  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2010 SP3  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2010 SP2  <br/> |Charged against the calling account. Starting with Exchange 2010 SP2 RU4, the budget is charged against the target mailbox.  <br/> |
   |Exchange 2010 SP1  <br/> |Mit aufrufendem Konto verrechnet  <br/> |
   |Exchange 2010  <br/> |Mit aufrufendem Konto verrechnet  <br/> |

- Da das **EWSMaxSubscriptions** -Einschränkungsbudget mit dem Konto verrechnet wird, dessen Identität angenommen wird, ist die Anzahl der Postfächer, die ein Dienstkonto abonnieren und für die es Streamingbenachrichtigungen erhalten kann, unbegrenzt, solange der Identitätswechsel verwendet wird. Das Konto, dessen Identität angenommen wird, kann maximal  _n_ gleichzeitige Anforderungen pro Zielpostfach ausführen, wobei  _n_ der **EWSMaxSubscriptions** -Wert ist. Wenn kein Identitätswechsel verwendet wird, sind für das gleiche Dienstkonto insgesamt maximal  _n_ gleichzeitige Anforderungen zulässig. Die Schlussfolgerung ist daher, dass sich mithilfe eines Identitätswechsels auf einem Dienstkonto die Anzahl von Postfächern, die Sie bedienen können, exponentiell erhöht. Weitere Informationen finden Sie unter [Verwalten von Affinität zwischen einer Gruppe von Abonnements und Postfachserver in Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).

- The **EWSPercentTimeInMailboxRPC**, **EWSPercentTimeInCAS**, and **EWSPercentTimeInAD** policy parameters refer to actions performed by a single thread. When an application performs multiple concurrent operations, you should account for the cumulative effect of these operations on the user resource budget.

## <a name="throttling-implications-for-ews-batch-requests"></a>Auswirkungen von Einschränkungen für EWS-Batchanforderungen

EWS enables you to batch multiple item requests into a single request that is executed by the Client Access server. This allows for greater efficiency and performance. When an Exchange server executes a batched request, it checks the user's budget after the execution of each item within the batch. If the application is over budget, the processing of the next item in the batch is delayed until the budget for that user has recharged. To ensure that applications that use batch operations run successfully, limit the number of item requests that can be included in a single batch, and divide large batches across multiple smaller batches to increase the reliability of the results. The effect that a batch operation has on particular throttling thresholds depends on the type of the request, the size of the items to be processed (for example in **UploadItems** or **ExportItems** operations) and the mailbox content. Throttling policies affect batch operations by causing the request to take longer to process. The caller will therefore have to wait longer for the response, and, because EWS limits the execution time of a batch request to one minute, the call could time out.

Um die optimale Batchgröße für eine Anwendung zu bestimmen, führen Sie Komponententests mit verschiedenen Eingabesätzen durch, um sicherzustellen, dass in einer Produktionsumgebung keine Fehler in der Anwendung auftreten.

## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>Einschränkungsrichtlinienparameter mit Auswirkung auf EWS-Suchvorgänge

[Search operations in EWS](search-and-ews-in-exchange.md) can require large amounts of time and resources, depending on how the search is run and what information is requested. To control resource usage during searches, two policy parameters take effect: **EWSFastSearchTimeoutInSeconds** and **EWSFindCountLimit**.

Der **EWSFastSearchTimeoutInSeconds** -Richtlinienparameter gibt die Zeitspanne in Sekunden an, die schnelle EWS-Suchläufe (auch als Inhaltsindizierungssuche bezeichnet) ausgeführt werden, bevor ein Timeout eintritt. Schnelle Suchläufe sind Suchvorgänge, die mithilfe einer AQS-Abfragezeichenfolge (Advanced Query Syntax, erweiterte Abfragesyntax) in einem [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) ausgeführt werden.

Sie können einen Exchange-Postfachordner auf zwei Arten durchsuchen:

- Mithilfe einer Exchange-Informationsspeichersuche, die einen sequenziellen Scan aller Nachrichten im Zielsuchbereich durchführt

- Mithilfe des Exchange-Suchdiensts (Inhaltsindizierung)

Both of these types of searches can result in timeouts. When possible, use the Exchange Search service because these searches are often targeted against mailbox indexes and use AQS queries. The following example shows how to perform an AQS search of the Inbox by using EWS and the Exchange Search service.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

If you can't use an AQS search, avoid using overly complex search filters. Also try to avoid creating search filters based on computed values if the query involves extended MAPI properties. AQS search was introduced in Exchange 2010.

> [!NOTE]
> The first time you run a complex Exchange store search query, it runs very slowly and may time out. After that, the query will respond more quickly. For more information about the backend Exchange server processes that occur during Exchange store search queries, see [Understanding the Performance Impact of High Item Counts and Restricted Views](https://technet.microsoft.com/library/cc535025%28EXCHG.80%29.aspx) on TechNet. Using a **SearchFilter** creates a dynamic restriction that helps similar queries in the future, but because these restrictions are dynamic in nature, they are not permanent or reliable, and are deleted after a maximum of three days.

The **EWSFindCountLimit** policy parameter specifies the maximum number of items from the results of a **FindItem** or **FindFolder** operation that can exist in memory on a Client Access server at the same time for one user. Every item or folder that EWS processes in a **FindItem** or **FindFolder** request is counted against the budget specified in the **EWSFindCountLimit** element. When the response is sent back to the requester, the find count charge for the current call is released. The response the server returns to a requester when the budget is exceeded is based on the **RequestServerVersion** element value and whether the requester specified paging. When the value of the **RequestServerVersion** element indicates Exchange 2010 or an earlier version of Exchange, the server sends a failure response with error code **ErrorServerBusy**. If the value of the **RequestServerVersion** element indicates a version of Exchange starting with Exchange 2010 SP1 or Exchange Online, and the client is using paging, EWS may return a partial result set instead of an error. Your application should expect that EWS might not return all items. If the value of the **IncludesLastItemInRange** element is false, the application should make another **FindItem** or **FindFolder** request with the new offset and continue until the **IncludesLastItemInRange** element returns true.

When you use a **FindItem** or **FindFolder** operation, it is important to use paging. The EWS Managed API enforces the use of paging, but if you are using other methods, such as EWS proxy objects or raw SOAP, you need to explicitly set paging. The following example shows how to use paging in the EWS Managed API.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> The default policy in Exchange limits the page size to 1000 items. Setting the page size to a value that is greater than this number has no practical effect.

Applications should also account for the fact that the  _EWSFindCountLimit_ throttling parameter value may result in a partial result set being returned for applications that make concurrent requests. The following example shows how to use the **MoreAvailable** property in the EWS Managed API to ensure that all results are included in a query.

```cs
ItemView iv = new ItemView(1000);
service.TraceEnabled = false;
FindItemsResults<Item> fiResults = null;
Do
{
    fiResults = service.FindItems(WellKnownFolderName.Inbox, iv);
    PropertySet itItemPropSet = new PropertySet(BasePropertySet.IdOnly) { EmailMessageSchema.Body };
    //Process Items in Result Set
    iv.Offset += fiResults.Items.Count;
}
while (fiResults.MoreAvailable == true);
```

## <a name="throttling-policies-and-concurrency"></a>Einschränkungsrichtlinien und Parallelität

Concurrency refers to the number of connections from a specific user. A connection is held from the moment a request is received until a response is sent to the requester. If users try to make more concurrent requests than their policy allows, the new connection attempt fails. However, the existing connections remain valid. Throttling policies can affect concurrency in a number of different ways.

The **EWSMaxConcurrency** throttling policy parameter sets the number of concurrent connections that a specific user can have against an Exchange server at one time. To determine the maximum number of concurrent connections to allow, consider the connections that Outlook clients will use. Outlook 2007 and Outlook 2010 use EWS to access availability and Out of Office (OOF) information. Mac Outlook 2011 uses EWS for all client access functionality. Depending on the number of Outlook clients that are actively connecting to a user's mailbox, the number of concurrent connections available for a user might be limited. Also, if your application has to connect to multiple mailboxes simultaneously while using a single security context, it is important to take the value of the **EWSMaxConcurrency** policy into account. For more information about using a single security context with concurrent connections, see [Throttling considerations for applications that use EWS impersonation](#throttling-considerations-for-applications-that-use-ews-impersonation) earlier in this article.

Applications that concurrently connect to multiple mailboxes have to be able to track resource usage on the client side. Because EWS operations are request/response-based, you can ensure that your applications function well within the **EWSMaxConcurrency** threshold by tracking the number of connections that occur between the start of a request and when the response is received and ensuring that no more than ten open requests occur concurrently.

The **EWSFindCountLimit** policy parameter specifies the maximum result size a **FindItem** or **FindFolder** operation can use on a Client Access server at the same time for one user. If an application (or potentially multiple applications) makes two concurrent EWS **FindItem** requests that return 100 items each for a specific user, the **EWSFindCountLimit** charge against that specific user's budget will be 200. When the first request returns, the budget drops to 100, and when the second request returns, the budget drops to zero. If the same application were to make two simultaneous requests for 1000 items, the budget value would be 2000 items, which exceeds the **EWSFindCountLimit** value. If the user's budget for items drops below zero, the next request results in an error until the user's budget recharges to one or more.

## <a name="throttling-considerations-for-ews-notification-applications"></a>Überlegungen zu Einschränkungen für EWS-Benachrichtigungsanwendungen

Wenn Sie EWS-Benachrichtigungsanwendungen erstellen, die Push-, Pull- oder Streamingbenachrichtigungen verwenden, müssen Sie die Auswirkungen der Einschränkungsrichtlinien **EWSMaxSubscriptions** und **EWSMaxConcurrency** sowie des **HangingConnectionLimit** berücksichtigen.

The **EWSMaxSubscriptions** policy parameter specifies the maximum number of active push, pull, and streaming subscriptions that a user can have on a specific Client Access server at the same time. Different versions of Exchange have different default values for this parameter. A user can subscribe to all folders in a mailbox by using the **SubscribeToAllFolders** property - this uses a single subscription against the **EWSMaxSubscriptions** budget. Users can subscribe to individual folders, with each folder subscription counting towards the **EWSMaxSubscriptions** budget, up to the limit set by the value of the **EWSMaxSubscriptions** parameter (for example, users can subscribe to 20 calendar folders in different mailboxes if **EWSMaxSubscriptions** is set to 20).

Informationen zum Identitätswechsel und zum **EWSMaxSubscriptions** -Parameter finden Sie unter [Einschränkungsüberlegungen für Anwendungen, die EWS-Identitätswechsel verwenden](#throttling-considerations-for-applications-that-use-ews-impersonation) weiter vorne in diesem Artikel.

Auch der **EWSMaxConcurrency** -Richtlinienparameter kann ein Problem für EWS-Benachrichtigungen darstellen. Beispiel:

- Wenn EWS die Anzahl der Verbindungen für den Besitzer des Abonnements erhöht, während ein Pushabonnement eine Benachrichtigung generiert.

- Wenn eine Anwendung dafür entwickelt wurde, mehrere Benutzerpostfächer zu überwachen, und Benutzer gleichzeitige Benachrichtigungen für eine Instanz einer Nachricht erhalten, die an eine Verteilerliste gesendet wird.

Wenn die Benachrichtigungsanwendung Multithreaded ist und gleichzeitige Verbindungsanforderungen enthält, um weitere Informationen zu einer bestimmten Nachricht abzurufen, die von einem Benutzerkonto empfangen wurde, kann die **EWSMaxConcurrency** -Richtlinien Grenze überschritten werden. Um dies zu berücksichtigen, können Sie die gleichzeitigen Verbindungen in Ihrer Anwendung überwachen, einschließlich derjenigen, die möglicherweise vom Server verwendet werden, und Sie können Anforderungswarteschlangen auf dem Client implementieren.

Der **HangingConnectionLimit** gilt nur für Streamingbenachrichtigungen. Dieser Grenzwert wird in der web.config Datei festgelegt, was bedeutet, dass ein Exchange-Administrator diesen Wert auf einem lokalen Exchange-Server festlegen kann, aber Exchange Online Postfächer den Standardwert für diesen Grenzwert verwenden müssen, also 10 für Exchange Online, Exchange 2019, Exchange 2016 und 3 für Exchange 2013. Weitere Informationen finden Sie unter [Welche Einschränkungswerte muss ich berücksichtigen?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)

## <a name="throttling-policy-and-application-performance"></a>Einschränkungsrichtlinie und Anwendungsleistung

Die folgenden drei Parameter der **PercentTimeIn** -Einschränkungsrichtlinie wirken sich auf die Zeitspanne aus, die eine ESW-Anwendung auf einem Clientzugriffsserver nutzen kann:

- **EWSPercentTimeInAD**

- **EWSPercentTimeInCAS**

- **EWSPercentTimeInMailboxRPC**

The values specified in the **PercentTimeIn** policy parameters indicate the amount of time that one thread making one request is allocated. For example, assuming a **EWSPercentTimeInCAS** value of 90, if a process makes two concurrent requests that spend 54 seconds each running code on the Client Access server, the process uses 108 seconds in a 60 second window. This represents an **EWSPercentTimeInCAS** parameter value of 180 percent.

> [!NOTE]
> The **EWSPercentTimeInCAS** parameter value is an overlapping superset of the **EWSPercentTimeInAD** and **EWSPercentTimeInMailboxRPC** parameter values. This means that the expenditure in Client Access server processing time will always be larger than the expenditures in **EWSPercentTimeInAD** and **EWSPercentTimeInMailboxRPC**. This is because for the Exchange component to make an Active Directory or RPC call, it must already be running Client Access server code. In addition, the expenditure in processing time for **EWSPercentTimeInCAS** doesn't stop while LDAP or RPC calls are being made. Although the request might be synchronously waiting for a response from Active Directory Domain Services (AD DS) or the Exchange store, the process is still consuming a thread on the server, and therefore the thread should continue to be charged for that usage.

Die von einer Anwendung innerhalb eines 60-Sekunden-Zeitraums genutzte CPU-Zeit überschreitet diese Einschränkungsgrenzwerte möglicherweise; daher ist es wichtig, den Umfang und die Art der gestellten Anforderungen zu berücksichtigen. Beispielsweise kann ein großer Batch gleichzeitig ausgeführter **ResolveNames** -Vorgänge den Wert des **EWSPercentTimeInAD** -Richtlinienparameters überschreiten. Die Richtlinienwerte, die in der Standardeinschränkungsrichtlinie enthalten sind, sind so konzipiert, dass die meisten EWS-Anwendungen ohne Probleme funktionieren. Wenn Multithreaded-Anwendungen mit hohem Volumen eine große Menge von Anforderungen auf einem bestimmten Client Zugriffsserver platzieren, kann dies jedoch zu Problemen führen. Um dies zu vermeiden, können Sie die Größe der auf dem Server ausgeführten Batches beschränken.

## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>Einschränkungsrichtlinien und Anwendungen mit hohem E-Mail-Versandvolumen

Die standardmäßigen Einschränkungsrichtlinien enthalten drei Richtlinienparameter zur Ratenbegrenzung, die Auswirkungen auf Anwendungen haben können, die EWS zum Senden einer großen Anzahl von Nachrichten oder zum Senden von Nachrichten in großen Batches innerhalb kurzer Zeit nutzen.

> [!NOTE]
> In general, we recommend that you do not use EWS to send bulk email. Use an SMTP host that specializes in bulk mail services to submit frequent large bulk email messages.

The **MessageRateLimit** policy parameter specifies the number of messages per minute that can be submitted by any Exchange client, including EWS. By default, this policy is set to 30 messages per minute. For ordinary users, this is generally sufficient. However, applications that send large batches of email messages, for example as part of an invoicing program, can run into problems. When this policy limit is exceeded, message delivery for the mailbox is delayed. Specifically, messages will appear in the Outbox or Drafts folder for longer periods of time when a user or application submits a larger number of messages than the value specified by the **MessageRateLimit** parameter. Be sure to consider this when you are developing a delivery tracking system, especially if your application uses a mailbox that users connect to via Outlook. When deferred items are stored in the Outbox or drafts folder, users might interpret that as an error.

The **RecipientRateLimit** policy parameter specifies the limit on the number of recipients that a user can address in a 24-hour period. For example, if this value is set to 500, it means that a single Exchange mailbox account can send messages to no more than 500 recipients each day. This limit applies to messages to recipients that are inside and outside the organization. This default limit might cause problems for some line-of-business applications that do end-of-month invoice runs and need to send messages to more than this number of recipients. You can use external services that enable batch processing of messages or separate on-premises outbound relay solutions to work around this limitation.

The **ForwardeeLimit** policy parameter specifies the maximum number of recipients that messages can be forwarded or redirected to by means of Inbox rules. This parameter doesn't limit the number of messages that can be forwarded or redirected to the recipients.

## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>Bei Überschreitung von Einschränkungsgrenzwerten generierte Fehler

Wenn Einschränkungsrichtlinien überschritten werden, generiert EWS einen der in der folgenden Tabelle aufgeführten Fehler.

**Tabelle 3: Fehler bei Überschreitung von Einschränkungsgrenzwerten**

|**Fehler**|**Einschränkungsrichtlinienparameter**|**Beschreibung**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**EWSMaxConcurrency** <br/> |Gibt an, dass mehr gleichzeitige Anforderungen an den Server gestellt werden, als die Richtlinie des Benutzers zulässt.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |Gibt an, dass die maximale Abonnementanzahl für Richtlinieneinschränkungen eines Benutzers überschritten wurde.  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |Gibt an, dass ein Suchvorgangsaufruf die Gesamtzahl der Elemente überschritten hat, die zurückgegeben werden können.  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC**         **EWSPercentTimeInCAS**         **EWSPercentTimeInAD** <br/> |Occurs when the server is busy. The BackOffMilliseconds value returned with ErrorServerBusy errors indicates to the client the amount of time it should wait until it should resubmit the request that caused the response that returned this error code.  <br/> |

Die folgende Tabelle enthält die HTTP-Statuscodes, die von Einschränkungsfehlern zurückgegeben werden.

**Tabelle 4: Von Einschränkungsfehlern zurückgegebene HTTP-Statuscodes**

|**HTTP-Statuscode**|**Beschreibung**|
|:-----|:-----|
|HTTP 503  <br/> |Indicates that EWS requests are queuing with IIS. The client should delay sending additional requests until a later time.  <br/> |
|HTTP 500  <br/> |Indicates an internal server error with the ErrorServerBusy error code. This indicates that the client should delay sending additional requests until a later time. The response may contain a back off hint called BackOffMilliseconds. If present, the value of BackOffMilliseconds should be used as the duration until the client resubmits a request.  <br/> |
|HTTP 200  <br/> |Contains an EWS schema-based error response with an ErrorInternalServerError error code. An inner ErrorServerBusy error code may be present. This indicates that the client should delay sending additional requests until a later time.  <br/> |

## <a name="see-also"></a>Siehe auch

- [Verwaltung von Exchange-Arbeitsauslastungen](https://technet.microsoft.com/library/jj150503.aspx)
- [New-ThrottlingPolicy-Cmdlet](https://technet.microsoft.com/library/dd351045.aspx)
- [Grundlegendes zu Clienteinschränkungsrichtlinien](https://technet.microsoft.com/library/dd297964.aspx)
- [ThrottlingPolicy-Klasse](https://msdn.microsoft.com/library/ff342496%28v=EXCHG.140%29.aspx)
- [Einschränkungsrichtlinie und EWSFindCountLimit](https://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [Budgetmomentaufnahmen in den IIS-Protokollen](https://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)

- [Auswirkung der Einschränkung Ihrer Bereitstellung in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Einschränkungsrichtlinienzuordnungen in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [Einschränkungsrichtlinien und CPUStartPercent](https://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
