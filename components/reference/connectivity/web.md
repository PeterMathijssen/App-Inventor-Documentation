# Web

Non-visible component that provides functions for HTTP GET, POST, PUT, and DELETE requests.

---

### Properties

#### AllowCookies

Whether the cookies from a response should be saved and used in subsequent requests. Cookies are only supported on Android version 2.3 or greater.

#### RequestHeaders

The request headers, as a list of two-element sublists. The first element of each sublist represents the request header field name. The second element of each sublist represents the request header field values, either a single value or a list containing multiple values.

#### ResponseFileName

The name of the file where the response should be saved. If SaveResponse is true and ResponseFileName is empty, then a new file name will be generated.

#### SaveResponse

Whether the response should be saved in a file.

#### Url

The URL for the web request.

---

### Events

#### GotFile(text url, number responseCode, text responseType, text fileName)

Event indicating that a request has finished.

#### GotText(text url, number responseCode, text responseType, text responseContent)

Event indicating that a request has finished.

---

### Methods

#### BuildRequestData(list list)

Converts a list of two-element sublists, representing name and value pairs, to a string formatted as application/x-www-form-urlencoded media type, suitable to pass to PostText.

#### ClearCookies()

Clears all cookies for this Web component.

#### Delete()

Performs an HTTP DELETE request using the Url property and retrieves the response.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### Get()

Performs an HTTP GET request using the Url property and retrieves the response.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### HtmlTextDecode(text htmlText)

Decodes the given HTML text value. HTML character entities such as &amp;, &lt;, &gt;, &apos;, and &quot; are changed to &, <, >, ', and ". Entities such as &#xhhhh, and &#nnnn are changed to the appropriate characters.
any JsonTextDecode(text jsonText)
Decodes the given JSON encoded value to produce a corresponding AppInventor value. A JSON list [x, y, z] decodes to a list (x y z), A JSON object with name A and value B, (denoted as A:B enclosed in curly braces) decodes to a list ((A B)), that is, a list containing the two-element list (A B).

#### PostFile(text path)

Performs an HTTP POST request using the Url property and data from the specified file.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### PostText(text text)

Performs an HTTP POST request using the Url property and the specified text.
The characters of the text are encoded using UTF-8 encoding.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The responseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### PostTextWithEncoding(text text, text encoding)

Performs an HTTP POST request using the Url property and the specified text.
The characters of the text are encoded using the given encoding.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### PutFile(text path)

Performs an HTTP PUT request using the Url property and data from the specified file.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### PutText(text text)

Performs an HTTP PUT request using the Url property and the specified text.
The characters of the text are encoded using UTF-8 encoding.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The responseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### PutTextWithEncoding(text text, text encoding)

Performs an HTTP PUT request using the Url property and the specified text.
The characters of the text are encoded using the given encoding.
If the SaveResponse property is true, the response will be saved in a file and the GotFile event will be triggered. The ResponseFileName property can be used to specify the name of the file.
If the SaveResponse property is false, the GotText event will be triggered.

#### UriEncode(text text)

Encodes the given text value so that it can be used in a URL.
any XMLTextDecode(text XmlText)
Decodes the given XML string to produce a list structure. 
