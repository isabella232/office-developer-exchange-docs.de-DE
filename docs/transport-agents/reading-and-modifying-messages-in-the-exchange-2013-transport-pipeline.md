---
title: Lesen und Ändern von Nachrichten in der Transportpipeline Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b53ed47a-3d01-4c4e-ad32-fb0532872aad
description: Lernen Sie .NET Framework-Klassen, mit denen Sie in Ihrer Exchange-können 2013 Transport-Agents zum Lesen, schreiben und Ändern von Nachrichten.
ms.openlocfilehash: c2a5d764140b86ddec49d51ec969aab63eb34f19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757206"
---
# <a name="reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline"></a>Lesen und Ändern von Nachrichten in der Transportpipeline Exchange 2013

Lernen Sie .NET Framework-Klassen, mit denen Sie in Ihrer Exchange-können 2013 Transport-Agents zum Lesen, schreiben und Ändern von Nachrichten.
  
**Gilt für:** Exchange Server 2013
  
- Klassen, die zum Lesen, schreiben oder Ändern von Nachrichten
- Encoder-namespace
- iCalendar-namespace
- MIME-namespace
- TextConverters-namespace
- TNEF-namespace
- vCard-namespace
  
Wie Nachrichten über die Transportpipeline übergeben, kann der Transport-Agent lesen, schreiben und Nachrichteninhalt zwischen verschiedenen Datenformaten zu konvertieren. Beispielsweise können Sie lesen und Schreiben von MIME-Daten, identifizieren Sie eingehende Nachrichten im UUENCODE oder Quoted-printable (qp) Format, und konvertieren Sie anschließend diese mit einem Standard Ihrer Organisation verwendeten oder lesen, und klicken Sie dann speichern Kalender-oder Kontakt zugeordnet ist eingehende Nachrichten. 
  
Auch kann Inhalte, die ein Sicherheitsrisiko birgt identifizieren und verschieben oder Löschen der Inhalt oder die Nachrichten, die sie enthalten; beispielsweise durch Entfernen von Hyperlinks in einer HTML-Nachricht.
  
Dieser Artikel enthält Informationen zu den .NET Framework-Klassen, die Sie zum Lesen, schreiben und Ändern von Nachrichten verwenden können.
  
> [!CAUTION]
> Viele der Eigenschaften und Parameter in der inhaltskonvertierung APIs können die Werte groß genug, um Leistungsprobleme, einschließlich Denial-of-Service. Bei Verwendung der inhaltskonvertierung APIs in einen Transport-Agent sollten Sie Grenzwerte auf die Eigenschaft und Parameter Wert Größen implementieren, die Sie beim Lesen oder schreiben, um beschränken Ressourcenverbrauch durch den Agent unterstützt. 

<a name="Namespaces"> </a>

## <a name="classes-used-to-read-write-or-modify-messages"></a>Klassen, die zum Lesen, schreiben oder Ändern von Nachrichten

Die folgende Tabelle enthält die .NET Framework-Klassen, die Sie zum Lesen, schreiben und Ändern von e-Mail-Nachrichten verwenden können.
  
**.NET Framework-Nachricht Verarbeitung namespaces**

|**.NET Framework-namespace**|**Kurse**|
|:-----|:-----|
|[Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Enthält Klassen für die in-Memory-Codierung und-Decodierung, eine Encoder Stream-Klasse, die eine der in eine zugeordnete-Enumeration enthaltenen Klassen Encoder oder Decoder akzeptiert und die Basisklasse [' ByteEncoder '](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) und [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) Exception-Klasse für die Encoder und Decoder.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Enthält Typen, mit denen Sie das Lesen und Schreiben von Datenströmen, die Kalenderinformationen enthalten. Enthält einen Kalender Reader und Writer, ein Exception-Objekt, ein Objekt Serie und Strukturen und Enumerationen, mit denen Sie Eigenschaftsinformationen für Kalenderelemente zurückzugeben.  <br/> |
|[Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Enthält Klassen, Strukturen, Enumerationen und Delegaten, die Sie zum Erstellen, lesen, schreiben, durchlaufen, codieren und Decodieren MIME-Daten verwenden können. Enthält einen datenstrombasierte Reader und Writer, die Sie Vorwärtscursor Lese- und Schreibzugriff auf MIME-Datenströmen sowie DOM-basierte Methoden ermöglicht und Klassen, mit denen, die Sie auf MIME-Dokumenten verwenden können.  <br/> |
|[Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Enthält Klassen, Strukturen, Enumerationen und Delegaten, mit denen Sie zum Lesen und Schreiben einen Datenstrom und Durchführen von Konvertierungen zwischen bestimmten Datentypen. beispielsweise HTML, Rich Text Format (RTF). Textkonverter können Sie das Format des Document-Datenstrom aus einem Formular zu einer anderen wechseln als auch entfernen Wählen Sie einzelne Elemente eines Dokuments, die ein Sicherheitsrisiko darstellen kann.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Enthält einen vorwärtsgerichteten Datenstrom Reader und Writer, ein Exception-Klasse und Strukturen und Enumerationen, die das Lesen und Schreiben von Daten Transport Neutral Encapsulation Format (TNEF) erleichtern.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Enthält einen vorwärtsgerichteten Datenstrom Reader und Writer, ein Exception-Klasse und Strukturen und Enumerationen, die zu erleichtern, lesen und Schreiben von Kontaktdaten vCard-Format.  <br/> |
   
## <a name="encoders-namespace"></a>Encoder-namespace
<a name="Encoders"> </a>

Der Encoder-Namespace enthält die Klassen für die in-Memory-Codierung und-Decodierung. Diese erben von der [' ByteEncoder '](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) -Basisklasse. Klassen codieren und Decodieren für Base64 BinHex, Quoted-printable (qp) und Unix-to-Unix (Uu). Die folgenden Klassen sind für in-Memory-Codierung und-Decodierung verwendet: 
  
- [Base64Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Encoder.aspx)
    
- [Base64Decoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Decoder.aspx)
    
- [BinHexEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [BinHexDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexDecoder.aspx)
    
- [QPEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPEncoder.aspx)
    
- [QPDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPDecoder.aspx)
    
- [UUEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUEncoder.aspx)
    
- [UUDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUDecoder.aspx)
    
Die Encoder und Decoder von [' ByteEncoder '](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) -Basisklasse erben, und verwenden Sie die [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) Ausnahme-Klasse für die Fehlerbehandlung. 
  
Der Namespace enthält darüber hinaus die [MacBinaryHeader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.MacBinaryHeader.aspx) -Klasse, die identifiziert codierte MacBinary-Dateien und ihre zugehörigen Dateiheader liest. 
  
Schließlich führt die [EncoderStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStream.aspx) -Klasse eine Konvertierung für einen Datenstrom anstelle einer in-Memory-Objekts. Diese Klasse nimmt eine der Encoder oder Decoder Klassen und entweder Lesevorgänge oder schreibt entsprechend die zugeordnete [EncoderStreamAccess](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStreamAccess.aspx) -Enumeration. 
  
## <a name="icalendar-namespace"></a>iCalendar-namespace
<a name="iCalendar"> </a>

Der iCalendar-Namespace stellt einen Vorwärtscursor Reader und Writer für iCalendar-Daten zusätzlich zu unterstützenden Strukturen und Klassen zum Erstellen, die Zugriff auf und Ändern von iCalendar-Streams.
  
Die Klassen [CalendarReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.aspx) und [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) dienen zum Lesen und Schreiben von iCalendar Streaming von Daten. 
  
Die CalendarReader nimmt einen lesbaren [Stream-Objekt](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument an den Konstruktoren. Die Methoden [ReadFirstChildComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadFirstChildComponent.aspx) , [ReadNextSiblingComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextSiblingComponent.aspx) und [ReadNextComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextComponent.aspx) können dann nacheinander die iCalendar-Komponenten in der Datenstrom zugreifen. Basierend auf dem Wert, den Sie für die [ComplianceMode](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceMode.aspx) -Eigenschaft festgelegt haben, Fehler im iCalendar-Stream eine Ausnahme ausgelöst oder bewirkt, dass die [ComplianceStatus](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceStatus.aspx) -Eigenschaft auf einen anderen Wert als [konform](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarComplianceStatus.Compliant.aspx) festgelegt werden. Sie können diese Eigenschaft zum Ermitteln von Problemen mit eingehenden iCalendar-Daten überprüfen. 
  
Die [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) -Klasse verwendet einen schreibbaren [Stream-Objekt](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument an den Konstruktoren. 
  
## <a name="mime-namespace"></a>MIME-namespace
<a name="MIME"> </a>

Der MIME-Namespace enthält Klassen, mit denen Sie erstellen, zugreifen und Bearbeiten von MIME-Dokumenten. Sie können mit MIME-Dokumenten mithilfe von entweder eine Methode datenstrombasierte oder DOM-basierten arbeiten.
  
### <a name="mimedocument-class-and-the-mime-dom"></a>MimeDocument-Klasse und dem MIME DOM

Die Klasse [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) ermöglicht den Zugriff zu einem Dokument MIME DOM. Verwenden von Objekten dieses Typs, wenn Sie den verfügbaren Speicher zum Laden einer gesamten DOM und Sie haben benötigen direkten Zugriff auf die Kopfzeilen und Inhalte der Nachricht. 
  
Sie Laden von Daten in ein [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) -Objekt mithilfe der Methods [GetLoadStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.GetLoadStream.aspx) oder [Laden](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.Load.aspx) . Sie können dann durchlaufen die DOM-Hierarchie und erstellen, ändern oder Entfernen von MIME-Daten. Nachdem Sie die MIME-Daten geändert haben, können Sie es in einem Stream-Objekt mithilfe der Methoden [WriteTo](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.WriteTo.aspx) schreiben. 
  
Die folgende Abbildung zeigt die Struktur der Daten in einem [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) -Objekt. 
  
**Abbildung 1. Struktur von MimeDocument-Objekten**

![MIME DOM-Architektur](media/MimeDomArchitecture.gif)
  
### <a name="mimereader-and-mimewriter-classes-and-stream-based-mime-parsing"></a>MimeReader und MimeWriter Klassen und datenstrombasierte MIME-Analyse

Die Klassen [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) und [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) aktivieren vorwärts-Zugriff in MIME-Streams. Verwenden Sie diese Klassen, wenn Sie nicht zum Ändern der MIME-Daten, die Daten erforderlich sind, die bereits gelesenen oder geschriebenen verfügen. Beispielsweise wenn Sie Nachrichten zu drucken, die ein vordefiniertes Format anpassen möchten, die [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) -Klasse ideal möglicherweise. 
  
Die [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) -Klasse kapselt DOM. Die Klassen [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) und [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) darstellen Zustand Computern. Wird aufgerufen, ihre basierend auf der Eingabe empfangen und die Methoden Zustände ändert. Zahlen von 2 bis 5 werden vereinfachte Zustand Übergang Diagramme, die für das Objekt [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) zeigen, welche Methoden zulässig sind, rufen Sie jeden Zustand und den Status mit der führt. 
  
Führen Sie die Pfeile für die von einem Zustand zum nächsten, ruft die Methode besagt oder Rückgabewerte, die dazu führen, den Zustand dass, ändern, um diese Diagramme zu verwenden. Angenommen Sie im ersten Diagramm, dass Sie am Anfang des Datenstroms sind, zu der die MimeReader gehört, die Sie erstellt haben. Wenn Sie auf den Status des Part-Kopfzeilen erhalten möchten, rufen Sie eine der [ReadNextPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadNextPart.aspx) oder [ReadFirstChildPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadFirstChildPart.aspx) , in dieser Reihenfolge aus. Wenn Header (d. h., wenn der MIME wohlgeformt ist) vorhanden sind, geben Sie in den Status des Part-Kopfzeilen ein. Andernfalls wird eine Ausnahme ausgelöst. 
  
**Abbildung 2. Vereinfachte Statusübergangsdiagramm für MimeReader-Objekte**

![MimeReader-Statusdiagramm](media/MimeReader_StateDiagram_01.gif)
  
> [!NOTE]
> Abbildung 3, 4 und 5 erweitern Sie dann auf Status in der vorherigen Diagramme angezeigt. 
  
**Abbildung 3. Erweiterung des Status von Abbildung 2 Part-Kopfzeilen**

![Erweiterung des Status "Part-Kopfzeilen"](media/MimeReader_StateDiagram_02.gif)
  
**Abbildung 4. Erweiterung des Status der Kopfzeilen aus Abbildung 3, wenn ein Parameter in einer Kopfzeile aufgetreten**

![Erweiterung des Status "Part-Kopfzeilen"](media/MimeReader_StateDiagram_03.gif)
  
> [!NOTE]
> Durch die in Abbildung 5 dargestellt werden rekursive, wenn Adressgruppe gefunden wird, können Sie die [GroupRecipientReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeAddressReader.GroupRecipientReader.aspx) -Eigenschaft verwenden, lesen Sie die Adressen in der Gruppe. 
  
**Abbildung 5. Erweiterung des Status der Kopfzeilen aus Abbildung 3, wenn eine Adresse oder die Gruppe "Adresse" aufgetreten ist**

![Erweiterung des Status "Kopfzeilen" für eine Adresse oder Gruppe](media/MimeReader_StateDiagram_04.gif)
  
Abbildung 6 und 7 anzeigen vereinfachte Zustand Übergang Diagramme für [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) -Objekt. 
  
> [!NOTE]
> Abbildung 7 wird auf dem in Abbildung 6 gezeigte Part-Kopfzeilen Zustand erweitert. 
  
**Abbildung 6. Vereinfachte Statusübergangsdiagramm für MimeWriter-Objekte**

![Statusübergang-Diagramm für MimeWriter](media/MimeWriter_TopLevel.gif)
  
**Abbildung 7. Erweiterung des Status von Abbildung 6 Part-Kopfzeilen**

![Statusübergang-Diagrammerweiterung für MimeWriter](media/MimeWriter_Diagram_Expansion.gif)
  
## <a name="textconverters-namespace"></a>TextConverters-namespace
<a name="TextConverters"> </a>

Der TextConverters-Namespace enthält Typen, die die Konvertierung des Inhalts der e-Mail-Nachrichten unterstützen. Diese Typen können Code Seite Konvertierung ausführen, entfernen HTML, die nicht sicher ist, und führen andere Transformationen auf e-Mail-Nachrichtentexte. Der [Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) -Namespace enthält die folgenden Klassen, die von der abstrakten [TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) -Klasse abgeleitet sind: 
  
- [EnrichedToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToHtml.aspx)
    
- [EnrichedToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToText.aspx)
    
- [HtmlToEnriched](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToEnriched.aspx)
    
- [HtmlToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToHtml.aspx)
    
- [HtmlToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToRtf.aspx)
    
- [HtmlToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToText.aspx)
    
- [RtfCompressedToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfCompressedToRtf.aspx)
    
- [RtfToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToHtml.aspx)
    
- [RtfToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtf.aspx)
    
- [RtfToRtfCompressed](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtfCompressed.aspx)
    
- [RtfToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToText.aspx)
    
- [TextToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToHtml.aspx)
    
- [TextToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToRtf.aspx)
    
- [TextToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToText.aspx)
    
Diese Textkonverter können Sie so ändern Sie das Format des Document-Datenstrom oder zum Entfernen von Elementen, die nicht sichere aus einem HTML-Dokument sind. Diese Klassen selbst Durchführung eine Umrechnung mit einem einzigen Aufruf einer der Convert-Methode in der Basisklasse [TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) verwendet werden können, oder können sie an den Konstruktor eines wird verwendet, um die konvertierten Lesevorgänge ausführen oder schreibt den Konverter übergeben werden. 
  
Die Funktionen, die von der Basisklasse geerbt eignet sich für die dokumentkonvertierung ausführen, wenn Sie über ausreichend Speicherplatz zum Speichern von dem Originaldokument und die konvertierten Ausgaben verfügen oder wenn Sie die Ergebnisse der Konvertierung speichern möchten. Die **Convert** -Methode akzeptiert Eingabe und Ausgabedatenströme, Text Leser oder Text Autoren und den Inhalt der Eingabe in die zugehörige Ausgabe konvertiert. 
  
Auch in den Namespace eingefügt werden, die folgenden Textleser, Autor und Stream-Klassen:
  
- [ConverterReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterReader.aspx) – **System.IO.TextReader**abgeleitet. 
    
- [ConverterWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx) – **System.IO.TextWriter**abgeleitet. 
    
- [ConverterStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx) – **System.IO.Stream**abgeleitet. 
    
Diese dienen zum Durchführen von Konvertierungen, wenn Sie keinen Platz zum Speichern des Originals oder ihre konvertierten Ausgabe, wenn Sie die Ausgabe in einem Stream senden oder die Eingabe von empfangen, oder Sie möchten die Ausgabe nur für die Indizierung oder Zwecke und daher nicht zum speichern möchten Das Ergebnis einer Umrechnung.
  
## <a name="tnef-namespace"></a>TNEF-namespace
<a name="TNEF"> </a>

Der Tnef-Namespace enthält die Klassen und Typen, die Vorwärtscursor datenstrombasierte lesen und Schreiben von TNEF-Daten zu ermöglichen. TNEF ist ein Datenformat, die zum Kapseln von MAPI-Eigenschaften für Clients, die MAPI interpretieren kann nicht verwendet wird.
  
Die [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) und [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) -Klassen bieten die Basisfunktionalität im [Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) -Namespace. 
  
Die [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) -Klasse verwendet einen lesbaren Stream als Argument an den Konstruktoren. Sie verwenden klicken Sie dann die [ReadNextAttribute](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadNextAttribute.aspx) -Methode, um die Attribute im Datenstrom TNEF sequenziell zu lesen. Nachdem Sie ein Attribut gelesen haben, können Sie Informationen über das Attribut mithilfe eines der der schreibgeschützte Eigenschaften für das Objekt [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) zusätzlich zum Abrufen einer [TnefPropertyReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefPropertyReader.aspx) zum Lesen von der aktuellen-Eigenschaft zugreifen. Sie können das aktuelle Attribut auch direkt mithilfe der Methode [ReadAttributeRawValue](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadAttributeRawValue.aspx) zugreifen. 
  
Die [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) -Klasse verwendet einen schreibbaren [Stream-Objekt](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument an den Konstruktoren. Die [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) -Klasse stellt mehrere Methoden zum Schreiben von Daten in diesen Stream. 
  
## <a name="vcard-namespace"></a>vCard-namespace
<a name="vCard"> </a>

Der vCard-Namespace enthält die Klassen, Strukturen und Enumerationen zum Lesen und Schreiben von Kontaktinformationen in einer e-Mail-Nachricht, die in das vCard-Datenformat ist enthalten sind. Der Namespace enthält einen Kontakt Reader und Writer, ein Exception-Klasse, eine Eigenschaft Leser, ein Parameter-Reader und Unterstützung von Enumerationen, mit die Sie eine e-Mail-Nachricht zugeordnete vCard-Daten lesen können.
  
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)  
- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [MIME-Medientypen](http://www.iana.org/assignments/media-types)
    

