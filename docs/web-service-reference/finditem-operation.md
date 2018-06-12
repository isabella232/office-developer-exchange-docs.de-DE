---
title: FindItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Informationen zum FindItem-EWS-Vorgang.
ms.openlocfilehash: b033ac2930981819a20f1336d40058a5f7c03b89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758463"
---
# <a name="finditem-operation"></a><span data-ttu-id="b1228-103">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b1228-103">FindItem operation</span></span>

<span data-ttu-id="b1228-104">Informationen zum **FindItem**-EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b1228-104">Find information about the **FindItem** EWS operation.</span></span> 
  
<span data-ttu-id="b1228-p101">Der **FindItem**-Vorgang durchsucht Elemente im Benutzerpostfach. Dieser Vorgang bietet viele Möglichkeiten zum Filtern und Formatieren der im Aufrufer zurückgegebenen Suchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b1228-p101">The **FindItem** operation searches for items that are located in a user's mailbox. This operation provides many ways to filter and format how search results are returned to the caller.</span></span> 
  
## <a name="using-the-finditem-operation"></a><span data-ttu-id="b1228-107">Verwenden des FindItem-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="b1228-107">Using the FindItem operation</span></span>

<span data-ttu-id="b1228-p102">Der **FindItem**-Vorgangsanforderung bietet zahlreiche Möglichkeiten zum Durchsuchen eines Postfachs und zum Formatieren der in einer Antwort zurückgegebenen Suchergebnisse. Sie können folgende Parameter in einer **FindItem**-Anforderung festlegen:</span><span class="sxs-lookup"><span data-stu-id="b1228-p102">The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response. You can specify the following in a **FindItem** request:</span></span> 
  
- <span data-ttu-id="b1228-p103">Ob die Suche mit flachen Einschränkungen durchgeführt und ob die Ergebnisse vorläufig gelöscht werden sollen. Erforderlich. Beachten Sie, dass eine Suche mit vorläufig zu löschenden Ergebnissen und einer Sucheinschränkung keine Elemente zurückgibt, wenn Elemente vorhanden sind, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b1228-p103">Whether the search is a shallow or soft-deleted traversal. Specifying this is required. Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.</span></span>
    
- <span data-ttu-id="b1228-p104">Das Antwortshape von Elementen. Identifiziert die Eigenschaften, die in der Antwort zurückgegeben werden. Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1228-p104">The response shape of items. This identifies the properties that are returned in the response. Specifying this is required.</span></span>
    
- <span data-ttu-id="b1228-p105">Die Ordner, für die die Suche durchgeführt werden soll. Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1228-p105">The folders from which to perform the search. Specifying this is required.</span></span>
    
- <span data-ttu-id="b1228-p106">Seitennummerierungsmechanismus und Ansichtstypen für das Zurückgeben von Daten auf Seiten. Optional.</span><span class="sxs-lookup"><span data-stu-id="b1228-p106">The paging mechanism and view types for returning view data in pages. Specifying this is optional.</span></span>
    
- <span data-ttu-id="b1228-p107">Optionen zum Gruppieren und Sortieren der Elemente, die zurückgegeben werden. Optional.</span><span class="sxs-lookup"><span data-stu-id="b1228-p107">Options for grouping and sorting the items that are returned. Specifying this is optional.</span></span>
    
- <span data-ttu-id="b1228-p108">Sucheinschränkungen oder AQS-Zeichenfolgen zum Filtern der Elemente, die zurückgegeben werden. Weitere Informationen zur Verwendung von AQS für Inhaltsindexsuchen finden Sie unter [QueryString (Zeichenfolge)](querystring-string.md). Optional.</span><span class="sxs-lookup"><span data-stu-id="b1228-p108">Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned. For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md). Specifying this is optional.</span></span>
    
- <span data-ttu-id="b1228-p109">Die Sortierreihenfolge für die in einer Antwort zurückgegebenen Elemente. Optional.</span><span class="sxs-lookup"><span data-stu-id="b1228-p109">The sort order for items returned in the response. Specifying this is optional.</span></span>
    
<span data-ttu-id="b1228-p110">Der **FindItem**-Vorgang gibt nur die ersten 512 Byte einer beliebigen streamfähigen Eigenschaft zurück. Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet. Es werden keine Nachrichtentextformate oder Empfängerlisten zurückgegeben. **FindItem** gibt eine Empfängerübersicht zurück. Sie können den [GetItem Operation](getitem-operation.md) zum Abrufen von Details eines Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1228-p110">The **FindItem** operation returns only the first 512 bytes of any streamable property. For Unicode, it returns the first 255 characters by using a null-terminated Unicode string. It does not return any of the message body formats or the recipient lists. **FindItem** will return a recipient summary. You can use the [GetItem operation](getitem-operation.md) to get the details of an item.</span></span> 
  
 <span data-ttu-id="b1228-132">**FindItem** gibt nur das [Name (EmailAddressType)](name-emailaddresstype.md)-Element zurück und gibt kein [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element im [Postfach](mailbox.md)-Element für die folgenden Felder zurück:</span><span class="sxs-lookup"><span data-stu-id="b1228-132">**FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields:</span></span> 
  
- <span data-ttu-id="b1228-133">Das Feld [Von](from.md) für Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b1228-133">The [From](from.md) field for messages</span></span> 
    
- <span data-ttu-id="b1228-134">Das Feld [Absender](sender.md) für Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b1228-134">The [Sender](sender.md) field for messages</span></span> 
    
- <span data-ttu-id="b1228-135">Das Feld [Organisator](organizer.md) für die Elemente im Kalender</span><span class="sxs-lookup"><span data-stu-id="b1228-135">The [Organizer](organizer.md) field for calendar items</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b1228-p111">[!HINWEIS] Der **FindItem**-Vorgang kann Ergebnisse in einem [CalendarView](calendarview.md)-Element zurückgeben. Das **CalendarView**-Element gibt einzelne Kalenderelemente und alle Vorkommen wiederkehrender Besprechungen zurück. Wenn ein **CalendarView**-Element nicht verwendet wird, werden einzelne Kalenderelemente und wiederkehrende Masterterminserien zurückgegeben. Die Vorkommen müssen von der Masterterminserie aus erweitert werden, wenn ein **CalendarView**-Element nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1228-p111">The **FindItem** operation can return results in a [CalendarView](calendarview.md) element. The **CalendarView** element returns single calendar items and all occurrences of recurring meetings. If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned. The occurrences must be expanded from the recurring master if a **CalendarView** element is not used.</span></span> 
  
<span data-ttu-id="b1228-140">Der **FindItem**-Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b1228-140">The **FindItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="b1228-141">**Tabelle 1. SOAP-Header im FindItem-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="b1228-141">**Table 1. FindItem operation SOAP headers**</span></span>

|<span data-ttu-id="b1228-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="b1228-142">**Header**</span></span>|<span data-ttu-id="b1228-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1228-143">**Element**</span></span>|<span data-ttu-id="b1228-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1228-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1228-145">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="b1228-145">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="b1228-146">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="b1228-146">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="b1228-p112">Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1228-p112">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b1228-149">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="b1228-149">**Impersonation**</span></span> <br/> |[<span data-ttu-id="b1228-150">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="b1228-150">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="b1228-p113">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1228-p113">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b1228-153">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="b1228-153">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="b1228-154">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b1228-154">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="b1228-p114">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1228-p114">Identifies the RFC3066 culture to be used to access the mailbox. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b1228-157">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="b1228-157">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="b1228-158">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b1228-158">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="b1228-p115">Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1228-p115">Identifies the schema version for the operation request. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b1228-161">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="b1228-161">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="b1228-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b1228-162">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="b1228-p116">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="b1228-p116">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="b1228-165">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="b1228-165">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="b1228-166">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="b1228-166">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="b1228-p117">Gibt die Zeitzone für alle Antworten vom Server an. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1228-p117">Identifies the time zone to be used for all responses from the server. This is applicable to a request.</span></span>  <br/> |
   
## <a name="finditem-operation-request-example"></a><span data-ttu-id="b1228-169">Beispiel für eine FindItem-Vorgangsanforderung</span><span class="sxs-lookup"><span data-stu-id="b1228-169">FindItem operation request example</span></span>

<span data-ttu-id="b1228-170">Im folgenden Beispiel einer **FindItem**-Anforderung wird das Abrufen des Elementbezeichners erläutert, der in der **IdOnly** -Enumeration des [BaseShape](baseshape.md)-Elements für Elemente im Ordner „Gelöschte Elemente" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1228-170">The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b1228-171">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="b1228-171">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="b1228-172">FindItem</span><span class="sxs-lookup"><span data-stu-id="b1228-172">FindItem</span></span>](finditem.md)
    
- [<span data-ttu-id="b1228-173">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b1228-173">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="b1228-174">BaseShape</span><span class="sxs-lookup"><span data-stu-id="b1228-174">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="b1228-175">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="b1228-175">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="b1228-176">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b1228-176">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="b1228-p118">Weitere Optionen für eine **FindItem**-Anforderungsnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItem](finditem.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="b1228-p118">For more options for a **FindItem** request message, explore the schema hierarchy. Start at the [FindItem](finditem.md) element.</span></span> 
  
## <a name="successful-finditem-operation-response"></a><span data-ttu-id="b1228-179">Antwort bei einem erfolgreichen FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b1228-179">Successful FindItem operation response</span></span>

<span data-ttu-id="b1228-180">Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine **FindItem**-Anforderung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b1228-180">The following example shows a successful response to the **FindItem** request.</span></span> 
  
<span data-ttu-id="b1228-p119">[Message](message-ex15websvcsotherref.md) -Elemente stellen E-Mails und alle anderen Elemente dar, die durch das EWS-Schema nicht stark typisiert werden. Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben. Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück.</span><span class="sxs-lookup"><span data-stu-id="b1228-p119">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema. Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements. Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b1228-184">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="b1228-184">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b1228-185">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b1228-185">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b1228-186">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="b1228-186">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="b1228-187">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b1228-187">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b1228-188">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b1228-188">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="b1228-189">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b1228-189">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b1228-190">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="b1228-190">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="b1228-191">Elemente</span><span class="sxs-lookup"><span data-stu-id="b1228-191">Items</span></span>](items.md)
    
- [<span data-ttu-id="b1228-192">Message</span><span class="sxs-lookup"><span data-stu-id="b1228-192">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b1228-193">ItemId</span><span class="sxs-lookup"><span data-stu-id="b1228-193">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="b1228-p120">Weitere Optionen für eine **FindItem**-Antwortnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItemResponse](finditemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="b1228-p120">For more options for a **FindItem** response message, explore the schema hierarchy. Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="finditem-operation-error-response"></a><span data-ttu-id="b1228-196">Fehlerantwort bei einem FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b1228-196">FindItem operation error response</span></span>

<span data-ttu-id="b1228-197">Im folgenden Beispiel wird eine Fehlerantwort bei einer **FindItem**-Anforderung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b1228-197">The following example shows an error response to a **FindItem** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b1228-198">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="b1228-198">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="b1228-199">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b1228-199">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b1228-200">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="b1228-200">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="b1228-201">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b1228-201">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b1228-202">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b1228-202">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="b1228-203">MessageText</span><span class="sxs-lookup"><span data-stu-id="b1228-203">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b1228-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b1228-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b1228-205">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b1228-205">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="b1228-p121">Weitere Optionen für eine **FindItem**-Fehlerantwortnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItemResponse](finditemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="b1228-p121">For more options for a **FindItem** error response message, explore the schema hierarchy. Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="version-differences"></a><span data-ttu-id="b1228-208">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="b1228-208">Version differences</span></span>

<span data-ttu-id="b1228-209">Exchange-Versionen ab Hauptversion 15, die mit Build 15.0.898.11 enden, geben einen ErrorInvalidOperation-Wert im [ResponseCode](responsecode.md)-Element zurück, wenn der **FindItem**-Vorgang zum Durchsuchen mehrerer Ordner in einem Archivpostfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1228-209">Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1228-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1228-210">See also</span></span>

- [<span data-ttu-id="b1228-211">Finding Items</span><span class="sxs-lookup"><span data-stu-id="b1228-211">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [<span data-ttu-id="b1228-212">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b1228-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
    
- <span data-ttu-id="b1228-213">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="b1228-213">**FindItemType**</span></span>
    

