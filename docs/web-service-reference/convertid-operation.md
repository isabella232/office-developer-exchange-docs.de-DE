---
title: ConvertId-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Hier finden Sie Informationen über die ConvertId EWS Vorgang.
ms.openlocfilehash: 5f1bcd8a9f0adc25b7c598ef10cc6bb139dfe02d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757710"
---
# <a name="convertid-operation"></a><span data-ttu-id="adebf-103">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="adebf-103">ConvertId operation</span></span>

<span data-ttu-id="adebf-104">Hier finden Sie Informationen zum **ConvertId** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="adebf-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="adebf-105">Der Vorgang des **ConvertId** Exchange-Webdienste (EWS) konvertiert Element- und Bezeichner zwischen Formate, die von Exchange Online, Exchange Online als Teil von Office 365, akzeptiert werden und lokale Versionen von Exchange, beginnend mit Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="adebf-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="adebf-106">Verwenden des ConvertId-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="adebf-106">Using the ConvertId operation</span></span>
<span data-ttu-id="adebf-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-107"></span></span>

<span data-ttu-id="adebf-108">Sie können die folgenden Bezeichner mithilfe des Vorgangs **ConvertId** konvertieren:</span><span class="sxs-lookup"><span data-stu-id="adebf-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="adebf-109">Das Format Bezeichner für EWS in der ursprünglich freigegebenen Version von Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="adebf-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="adebf-110">Wird dies durch die `EwsLegacyId` -Enumerationswert in der [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="adebf-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="adebf-111">Das Format der Bezeichner für EWS in Exchange 2007 SP1 oder Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="adebf-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="adebf-112">Wird dies durch die `EwsId` in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab.</span><span class="sxs-lookup"><span data-stu-id="adebf-112">This is represented by the  `EwsId` enumeration value in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="adebf-113">Der MAPI-Bezeichner, wie in der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="adebf-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="adebf-114">Wird dies durch die `EntryId` -Enumerationswert in der [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="adebf-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="adebf-115">Der Bezeichner der Verfügbarkeit Kalender-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="adebf-115">The availability calendar event identifier.</span></span> <span data-ttu-id="adebf-116">Dies ist eine Hexadezimalzahl-codierte Darstellung der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="adebf-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="adebf-117">Wird dies durch die `HexEntryId` in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab.</span><span class="sxs-lookup"><span data-stu-id="adebf-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="adebf-118">Der Bezeichner für den Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="adebf-118">The Exchange store identifier.</span></span> <span data-ttu-id="adebf-119">Wird dies durch die `StoreId` in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)-Enumerationswert ab.</span><span class="sxs-lookup"><span data-stu-id="adebf-119">This is represented by the  `StoreId` enumeration value in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="adebf-120">Der Vorgang **ConvertId** konvertiert nicht öffentliche Ordner-IDs aus der EWS-ID auf den Store-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="adebf-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="adebf-121">Der Outlook Web App-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="adebf-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="adebf-122">Wird dies durch die `OwaId` -Enumerationswert in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adebf-122">This is represented by the  `OwaId` enumeration value in [IdFormat](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="adebf-123">Die Übergabe von URLs, die von dieser Bezeichner auf Outlook Web App erstellt werden, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adebf-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="adebf-124">Die Outlook Web App-ID gilt für Exchange 2007 und Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="adebf-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="adebf-125">Outlook Web App für Exchange Online und Versionen von Exchange beginnend mit Exchange Server 2013 verwendet EWS-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="adebf-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="adebf-126">Der Vorgang **ConvertId** funktioniert nicht wie erwartet beim Konvertieren von Öffentliche Ordner-IDs aus der EWS-ID in der Store-ID in Exchange Online und Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="adebf-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="adebf-127">Sie können die ID, die zur Umgehung dieses Problems zurückgegeben wird, manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="adebf-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="adebf-128">Den Bezeichner manuell zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="adebf-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="adebf-129">Bestimmen Sie in Ihrem Anwendungscode, ob der Zielordner/Element in einem öffentlichen Ordner.</span><span class="sxs-lookup"><span data-stu-id="adebf-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="adebf-130">Decodiert die Base64-codierte Bezeichnerzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="adebf-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="adebf-131">Überprüfen Sie, ob der Typ Byte (21. Byte) hat den Wert 7.</span><span class="sxs-lookup"><span data-stu-id="adebf-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="adebf-132">Der Wert 7 gibt an, dass der Bezeichner in der falschen Format ist.</span><span class="sxs-lookup"><span data-stu-id="adebf-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="adebf-133">Überspringen Sie die ersten vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="adebf-133">Skip the first four bytes.</span></span> <span data-ttu-id="adebf-134">Sie müssen auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adebf-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="adebf-135">Aktualisieren Sie die folgenden 16-Byte mit der folgenden GUID: 1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="adebf-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="adebf-136">Aktualisieren Sie das nächste Byte (Typ Byte) mit einem Wert von 9.</span><span class="sxs-lookup"><span data-stu-id="adebf-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="adebf-137">Ändern Sie den Bezeichner in eine Base64-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="adebf-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="adebf-138">Der Vorgang **ConvertId** überprüft, dass eine angegebene SMTP-Adresse ein gültiges Format hat.</span><span class="sxs-lookup"><span data-stu-id="adebf-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="adebf-139">Der Vorgang ermittelt nicht, ob eine SMTP-Adresse ein gültiges Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="adebf-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="adebf-140">Der Vorgang **ConvertId** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="adebf-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="adebf-141">**In Tabelle 1. ConvertId Vorgang SOAP-Header**</span><span class="sxs-lookup"><span data-stu-id="adebf-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="adebf-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="adebf-142">**Header**</span></span>|<span data-ttu-id="adebf-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="adebf-143">**Element**</span></span>|<span data-ttu-id="adebf-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="adebf-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="adebf-145">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="adebf-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="adebf-146">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="adebf-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="adebf-p112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="adebf-p112">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="adebf-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="adebf-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="adebf-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="adebf-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="adebf-151">Identifiziert die Schemaversion für die Anforderung Vorgang, dass sich dies auf eine Anforderung anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="adebf-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="adebf-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="adebf-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="adebf-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="adebf-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="adebf-p113">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="adebf-p113">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="adebf-156">ConvertId Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="adebf-156">ConvertId operation request example</span></span>
<span data-ttu-id="adebf-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-157"></span></span>

<span data-ttu-id="adebf-158">Im folgenden Beispiel wird eine Anforderung **ConvertId** veranschaulicht, wie ein EWS-Bezeichner in einer Outlook Web App-Bezeichner konvertiert.</span><span class="sxs-lookup"><span data-stu-id="adebf-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="adebf-159">Das [RequestServerVersion](requestserverversion.md) -Element im SOAP-Header muss Exchange2007_SP1 oder höher für diesen Vorgang funktioniert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adebf-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="adebf-160">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adebf-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="adebf-161">ConvertId Vorgang antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="adebf-161">ConvertId operation response example</span></span>
<span data-ttu-id="adebf-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-162"></span></span>

<span data-ttu-id="adebf-163">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ConvertId** .</span><span class="sxs-lookup"><span data-stu-id="adebf-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="adebf-164">In diesem antwortbeispiel enthält einen Outlook Web App-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="adebf-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="adebf-165">Die Outlook Web App-ID wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adebf-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="adebf-166">ConvertId Vorgang Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="adebf-166">ConvertId operation error response example</span></span>
<span data-ttu-id="adebf-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-167"></span></span>

<span data-ttu-id="adebf-168">Das folgende Beispiel zeigt die Antwort auf eine Anforderung, die den falschen Typ des Formats Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="adebf-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="adebf-169">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="adebf-169">Version differences</span></span>
<span data-ttu-id="adebf-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-170"></span></span>

<span data-ttu-id="adebf-171">Das Format von EWS zwischen der ursprünglich freigegebenen Version von Exchange 2007 und Exchange 2007 Service Pack 1 (SP1) geändert.</span><span class="sxs-lookup"><span data-stu-id="adebf-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="adebf-172">Exchange Online als Teil von Office 365, Exchange Online und lokale Versionen von Exchange, beginnend mit Exchange 2010 verwenden das gleiche Bezeichner-Format, das Exchange 2007 SP1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="adebf-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="adebf-173">Der Vorgang **ConvertId** konvertiert für Öffentliche Ordner-IDs aus der EWS-ID in der Store-ID in Exchange 2007 und Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="adebf-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adebf-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adebf-174">See also</span></span>
<span data-ttu-id="adebf-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="adebf-175"></span></span>

- [<span data-ttu-id="adebf-176">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="adebf-176">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="adebf-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="adebf-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="adebf-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="adebf-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

