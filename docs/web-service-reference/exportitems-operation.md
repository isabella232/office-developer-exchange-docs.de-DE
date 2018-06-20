---
title: ExportItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: e2846abb-0b16-4732-bbd8-038a674672f6
description: Der Vorgang ExportItems exportiert Elemente aus einem Postfach.
ms.openlocfilehash: 6f0760705c05de2a615544fe52ac50b398be6040
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758325"
---
# <a name="exportitems-operation"></a><span data-ttu-id="437a9-103">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="437a9-103">ExportItems operation</span></span>

<span data-ttu-id="437a9-104">Der Vorgang **ExportItems** exportiert Elemente aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="437a9-104">The **ExportItems** operation exports items out of a mailbox.</span></span> 
  
## <a name="exportitems-request-example"></a><span data-ttu-id="437a9-105">Anforderungsbeispiel ExportItems</span><span class="sxs-lookup"><span data-stu-id="437a9-105">ExportItems request example</span></span>

### <a name="description"></a><span data-ttu-id="437a9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="437a9-106">Description</span></span>

<span data-ttu-id="437a9-107">Im folgenden Beispiel wird einer Anforderung **ExportItems** bilden eine Anforderung zum Abrufen von drei Elemente, die aus einem Postfach exportiert veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="437a9-107">The following example of an **ExportItems** request shows how to form a request to get three items exported from a mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="437a9-108">Code</span><span class="sxs-lookup"><span data-stu-id="437a9-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="437a9-109">Comment</span><span class="sxs-lookup"><span data-stu-id="437a9-109">Comment</span></span>

<span data-ttu-id="437a9-110">Die Element-IDs im Beispiel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="437a9-110">The item identifiers in the example have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="437a9-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="437a9-111">Request elements</span></span>

<span data-ttu-id="437a9-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="437a9-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="437a9-113">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="437a9-113">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="437a9-114">ExportItems</span><span class="sxs-lookup"><span data-stu-id="437a9-114">ExportItems</span></span>](exportitems.md)
    
- [<span data-ttu-id="437a9-115">Artikelnummern ein (NonEmptyArrayOfItemIdsType).</span><span class="sxs-lookup"><span data-stu-id="437a9-115">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
    
- [<span data-ttu-id="437a9-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="437a9-116">ItemId</span></span>](itemid.md)
    
## <a name="successful-exportitems-response-example"></a><span data-ttu-id="437a9-117">Erfolgreiche ExportItems antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="437a9-117">Successful ExportItems response example</span></span>

### <a name="description"></a><span data-ttu-id="437a9-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="437a9-118">Description</span></span>

<span data-ttu-id="437a9-119">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ExportItems** .</span><span class="sxs-lookup"><span data-stu-id="437a9-119">The following example shows a successful response to an **ExportItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="437a9-120">Code</span><span class="sxs-lookup"><span data-stu-id="437a9-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <t:ServerVersionInfo MajorVersion="14"
    MinorVersion="1"
    MajorBuildNumber="139"
    MinorBuildNumber="0"
    Version="Exchange2010_SP1"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
    xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            QAAyAAAh9SpR08oBAwAEQAMAFkANABMOAwAAQAMAIQ4AAAAAsIQSN0oAAAAyAGEAYgAxADYA
            MQA2ADYALQBhAGUANQBkAC0ANAAyAGUAZgAtAGEANQA1ADkALQBjADgAOQAwADgANwBkADIA
            MwBkADgANAAAAAMACzf/////AwAgDmQEAAADAPcPAAAAAEAABzBPMXstUdPKAUAACDBPMXst
            UdPKAQMABTcFAAAAsIQONx4AAABtAGUAcwBzAGEAZwBlAC8AcgBmAGMAOAAyADIAAACwhAEw
            IgAAAE0AbwBzAHQAIABmAGEAcwBjAGkAbgBhAHQAaQBuAGcAAAACAfkPBAAAAAAAAAADAAFA
            FABKZ3QrAAAAZF2mAwAXAAEAAACwhBoAEgAAAEkAUABNAC4ATgBvAHQAZQAAAAMANgAAAAAA
            sIQ3ACIAAABNAG8AcwB0ACAAZgBhAHMAYwBpAG4AYQB0AGkAbgBnAAAAQAA5AACq+za80coB
            AgE7AGUAAABFWDovTz1GSVJTVCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RS
            QVRJVkUgR1JPVVAgKEZZRElCT0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05F
            ALCEPQACAAAAAAACAUEAfgAAAAAAAADcp0DIwEIQGrS5CAArL+GCAQAAAAAAAAAvTz1GSVJT
            VCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RSQVRJVkUgR1JPVVAgKEZZRElC
            T0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05FALCEQgAQAAAAVQB
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            BAAAAAYAAAABDouAAAACAAAAEiAAAOSECEBbAAAAL089RklSU1QgT1JHQU5JWkFUSU9OL09V
            PUVYQ0hBTkdFIEFETUlOSVNUUkFUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJF
            Q0lQSUVOVFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAAALACMAAAAL
            ACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUAcwB0AGkAbgBnACAALQAgAGYAcgBv
            AG0AIABFAFcAUwBNAEEAAABAADkAAHZeFxfRygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FO
            SVpBVElPTi9PVT1FWENIQU5HRSBBRE1JTklTVFJBVElWRSBHUk9VUCAoRllESUJPSEYyM1NQ
            RExUKS9DTj1SRUNJUElFTlRTL0NOPVVTRVJPTkUAsIQ9AAIAAAAAAAIBPwB+AAAAAAAAANyn
            QMjAQhAatLkIACsv4YIBAAAAAAAAAC9PPUZJUlNUIE9SR0FOSVpBVElPTi9PVT1FWENIQU5H
          </m:Data>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comment"></a><span data-ttu-id="437a9-121">Comment</span><span class="sxs-lookup"><span data-stu-id="437a9-121">Comment</span></span>

<span data-ttu-id="437a9-122">Die Element-IDs und Ändern von Schlüsseln im Beispiel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="437a9-122">The item identifiers and change keys in the example have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="437a9-123">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="437a9-123">Response elements</span></span>

<span data-ttu-id="437a9-124">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="437a9-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="437a9-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="437a9-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="437a9-126">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="437a9-126">ExportItemsResponse</span></span>](exportitemsresponse.md)
    
- [<span data-ttu-id="437a9-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="437a9-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="437a9-128">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="437a9-128">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
    
- [<span data-ttu-id="437a9-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="437a9-129">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="437a9-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="437a9-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="437a9-131">Daten (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="437a9-131">Data (base64Binary)</span></span>](data-base64binary.md)
    
## <a name="exportitems-error-response-example"></a><span data-ttu-id="437a9-132">Antwortbeispiel ExportItems-Fehler</span><span class="sxs-lookup"><span data-stu-id="437a9-132">ExportItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="437a9-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="437a9-133">Description</span></span>

<span data-ttu-id="437a9-134">Das folgende Beispiel zeigt eine Antwort auf die **ExportItems** -Anforderung, die zwei Fehler und ein erfolgreich exportiert Element enthält.</span><span class="sxs-lookup"><span data-stu-id="437a9-134">The following example shows a response to the **ExportItems** request that contains two errors and one successfully exported item.</span></span> <span data-ttu-id="437a9-135">Das erste Element im Beispiel wurde erfolgreich exportiert.</span><span class="sxs-lookup"><span data-stu-id="437a9-135">The first item in the example is successfully exported.</span></span> <span data-ttu-id="437a9-136">Das zweite Element enthält ein Key falsche ändern.</span><span class="sxs-lookup"><span data-stu-id="437a9-136">The second item contains an incorrect change key.</span></span> <span data-ttu-id="437a9-137">Das dritte Element stellt Versuch, ein Element aus dem falschen Postfach zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="437a9-137">The third item represents an attempt to export an item from the wrong mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="437a9-138">Code</span><span class="sxs-lookup"><span data-stu-id="437a9-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGU0oMf0GPIQeAAAAUC8iAABseAAAAUFZ7AAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>No mailbox with such guid.</m:MessageText>
          <m:ResponseCode>ErrorNonExistentMailbox</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:Value Name="MailboxGuid">f3f6f699-2254-40ce-9994-388d9d98419e</t:Value>
          </m:MessageXml>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="comments"></a><span data-ttu-id="437a9-139">Kommentare</span><span class="sxs-lookup"><span data-stu-id="437a9-139">Comments</span></span>

<span data-ttu-id="437a9-140">Der Elementbezeichner Tasten ändern, und Daten im Beispiel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="437a9-140">The item identifiers, change keys, and data in the example have been shortened to preserve readability.</span></span>
  
### <a name="error-response-elements"></a><span data-ttu-id="437a9-141">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="437a9-141">Error response elements</span></span>

<span data-ttu-id="437a9-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="437a9-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="437a9-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="437a9-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="437a9-144">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="437a9-144">ExportItemsResponse</span></span>](exportitemsresponse.md)
    
- [<span data-ttu-id="437a9-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="437a9-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="437a9-146">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="437a9-146">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
    
- [<span data-ttu-id="437a9-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="437a9-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="437a9-148">ItemId</span><span class="sxs-lookup"><span data-stu-id="437a9-148">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="437a9-149">Daten (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="437a9-149">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="437a9-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="437a9-150">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="437a9-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="437a9-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="437a9-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="437a9-152">MessageXml</span></span>](messagexml.md)
    
- <span data-ttu-id="437a9-153">**Wert**</span><span class="sxs-lookup"><span data-stu-id="437a9-153">**Value**</span></span>
    
> [!NOTE]
> <span data-ttu-id="437a9-154">Das **Value** -Element ist im Schema nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="437a9-154">The **Value** element does not exist in the schema.</span></span> <span data-ttu-id="437a9-155">Dieses Element ist gültig, da das [MessageXml](messagexml.md) -Element, in dem das **Value** -Instanzelement auftritt, wohlgeformtes XML enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="437a9-155">This element is valid because the [MessageXml](messagexml.md) element, in which the **Value** instance element occurs, can contain any well-formed XML.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="437a9-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="437a9-156">See also</span></span>



[<span data-ttu-id="437a9-157">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="437a9-157">UploadItems operation</span></span>](uploaditems-operation.md)


[<span data-ttu-id="437a9-158">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="437a9-158">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="437a9-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="437a9-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

