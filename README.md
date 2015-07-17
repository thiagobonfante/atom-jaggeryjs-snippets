# JaggeryJS-snippets
A collection of command snippets for optimizing JaggeryJS development productivity.

## Warning
You don't need this package if you already have the [language-jaggery](https://atom.io/packages/language-jaggery) package.

## Dependency
The JaggeryJS Snippets are made to JavaScript extension.
You can change extension pressing (`CTRL`) + (`SHIFT`) + (`L`) to every opened file or installing the [file-types](https://atom.io/packages/file-types) package to associate **.jag** files to JavaScript scope.

## Snippets
JaggeryJS Snippets aren't too short but it follow, in most of cases, the following pattern:

API class: **File**
API method: **open(r | r+ | w | w+ | a | a+)**
Snippet: **fiope** 2 first letters from API class and 3 from method.

Lets say that API class have more then one method open:
API method: **openWSDL(url)**
Snippet: **fiopew** 2 first letters from API class and 3 from method plus 1 for compose words.

### Basic

#### `jag⇥` syntax
```js
<%
${0}
%>
```

#### `out⇥` syntax out
```js
<%=${0}%>
```

#### `pr⇥` print()
```js
print(${1:value})${0}
```

#### `lo⇥` Log()
```js
var log = new Log();${0}
```

### HTTP request

#### `req⇥` request
```js
request.${0}
```

#### `getmet⇥` Method
```js
getMethod();
```

#### `getpro⇥` Protocol
```js
getProtocol();
```

#### `getques⇥` Query String
```js
getQueryString();
```

#### `getcon⇥` Content
```js
getContent();
```

#### `getcontt⇥` Content-Type
```js
getContentType();
```

#### `geturi⇥` Request URI
```js
getRequestURI();
```

#### `geturl⇥` Request URL
```js
getRequestURL();
```

#### `getpatt⇥` Path Translated
```js
getPathTranslated();
```

#### `getiss⇥` Is Secure
```js
isSecure();
```

#### `getrema⇥` Remote Addr
```js
getRemoteAddr();
```

#### `getconp⇥` Context Path
```js
getContextPath();
```

#### `getlocp⇥` Local Port
```js
getLocalPort();
```

#### `getuse⇥` User
```js
getUser();
```

#### `getinps⇥` Input Stream
```js
getInputStream();
```

#### `gethea⇥` Header
```js
getHeader("${1:name}");${0}
```

#### `getallh⇥` All Headers
```js
getAllHeaders();
```

#### `getpar⇥` Parameter
```js
getParameter("${1:paramName}");${0}
```

#### `getallp⇥` All Parameters
```js
getAllParameters();
```

#### `getlo⇥` Locale
```js
getLocale();
```

#### `getalll⇥` All Locales
```js
getAllLocales();
```

#### `getmapp⇥` Mapped Path
```js
getMappedPath();
```

#### `getfi⇥` File
```js
getFile("${1:fileName}");${0}
```

#### `sav⇥` Save As
```js
saveAs(${1:file}.getName());
```

#### `getallf⇥` All Files
```js
getAllFiles();
```

#### `getcoo⇥` Cookie
```js
getCookie(${1:name});${0}
```

#### `getallc⇥` All Cookies
```js
getAllCookies();
```

### HTTP response

#### `re⇥` response
```js
response.$0
```

#### `resta⇥` Status
```js
${1:response}.status${0}
```

#### `recont⇥` Content-Type
```js
${1:response}.contentType = '${1:type}';$0
```

#### `recha⇥` Character Enconding
```js
${1:response}.characterEncoding = '${1:type}';$0
```

#### `recon⇥` Content
```js
${1:response}.content = '${1:type}';$0
```

#### `readdh⇥` Add Header
```js
${1:response}.addHeader('${1:key}', '${2:value}');$0
```

#### `resenr⇥` Send Redirect
```js
${1:response}.sendRedirect(${1:url});$0
```

#### `resene⇥` Send Error
```js
${1:response}.sendError(${1:errCode});$0
```

#### `readdc⇥` Add Cookie
```js
${1:response}.addCookie(${1:cookie});$0
```

### Session

#### `ses⇥` HTTP session
```js
session.$0
```

#### `maxi⇥` Max Inactive
```js
maxInactive
```

#### `getcret⇥` Creation Time
```js
getCreationTime();
```

#### `getlasat⇥` Last Accessed Time
```js
getLastAccessedTime();
```

#### `pu⇥` PUT
```js
put(${1:key}, ${2:value});$0
```

#### `ge⇥` GET
```js
get(${1:key});$0
```

#### `getid⇥` Get ID
```js
getId();
```

#### `rem⇥` Remove
```js
remove(${1:key});
```

#### `inv⇥` Ivalidate Session
```js
invalidate();
```

#### `isn⇥` Is New?
```js
isNew();
```

### Application

#### `app⇥` Global App
```js
application.$0
```

#### `ser⇥` Serve
```js
serve(function(${1:request},${2:respond},${3:session}) {${0}});
```

### webSocket

#### `weont⇥` On Text
```js
${1:webSocket}.ontext = function (data) {
  ${0}
};
```

#### `weonb⇥` On Binary
```js
${1:webSocket}.onbinary = function (stream) {
  ${0}
};
```

#### `weono⇥` On Open
```js
${1:webSocket}.onopen = function (stream) {
  ${0}
};
```

#### `weonc⇥` On Close
```js
${1:webSocket}.onclose = function (stream) {
  ${0}
};
```

#### `wesen⇥` WS Send
```js
${1:webSocket}.send(${2:stream});$0
```

### HTTP Client (Wrap)

#### `wge⇥` HTTP/GET
```js
get(${1:url}${2:, [data]}${3:, [headers]}${4:, [type]}${5:, [success(data, xhr)]});$0
```

#### `wger⇥` HTTP/GET Response
```js
var ${1:response} = get(${2:url}${3:, [data]}${4:, [headers]}${5:, [type]});$0
```

#### `wpo⇥` HTTP/POST
```js
post(${1:url}${2:, [data]}${3:, [headers]}${4:, [type]}${5:, [success(data, xhr)]});$0
```

#### `wpor⇥` HTTP/POST Response
```js
var ${1:response} = post(${2:url}${3:, [data]}${4:, [headers]}${5:, [type]});$0
```

#### `wpu⇥` HTTP/PUT
```js
put(${1:url}${2:, [data]}${3:, [type]}${4:, [headers]}${5:, [success(data, xhr)]});$0
```

#### `wpur⇥` HTTP/PUT Response
```js
var ${1:response} = put(${2:url}${3:, [data]}${4:, [type]}${5:, [headers]});$0
```

#### `wde⇥` HTTP/DELETE
```js
del(${1:url}${2:, [data]}${3:, [type]}${4:, [headers]}${5:, [success(data, xhr)]});$0
```

### XMLHttpRequest

#### `XMLHttpRequest⇥` XMLHttpRequest
```js
var ${1:xhr} = new XMLHttpRequest();${0}
```

#### `xmonr⇥` On Ready State Change
```js
${1:xhr}.onreadystatechange = function() {
  if (${2:xhr}.readyState == 4 && ${3:xhr}.status == 200) {
${0}
  }
};
```

#### `xmsta⇥` Status
```js
${1:xhr}.status;${0}
```

#### `xmrea⇥` Ready State
```js
${1:xhr}.readyState;${0}
```

#### `xmstt⇥` Status Text
```js
${1:xhr}.statusText;${0}
```

#### `xmret⇥` Response Text
```js
${1:xhr}.responseText;${0}
```

#### `xmrex⇥` Response XML
```js
${1:xhr}.responseXML;${0}
```

#### `xmope⇥` Open
```js
${1:xhr}.open(${2:method},${3:url},${4:async});${0}
```

#### `xmsen⇥` Send
```js
${1:xhr}.send(${2:payload});${0}
```

#### `xmset⇥` Set Request Header
```js
${1:xhr}.setRequestHeader(${2:name}, ${3:value});${0}
```

#### `xmget⇥` Get Response Header
```js
${1:xhr}.getResponseHeader(${2:name});${0}
```

#### `xmabo⇥` Abort
```js
${1:xhr}.abort();${0}
```

### Utils

#### `ur⇥` URIMatcher
```js
var ${1:uriMatcher} = new URIMatcher(${2:uri});${0}
```

#### `urmat⇥` Match
```js
${1:uriMatcher}.match(${2:pattern});${0}
```

#### `urele⇥` Elements
```js
${1:uriMatcher}.elements();${0}
```

#### `inc⇥` Include
```js
include(${1:path});${0}
```

#### `incon⇥` Include Once
```js
include_once(${1:path});${0}
```

### Feed

#### `fee⇥` Feed
```js
var ${1:feed} = new Feed(${2:url});${0}
```

#### `feen⇥` Entries
```js
${1:feed}.entries${0}
```

#### `feaut⇥` Author
```js
${1:feed}.author${0}
```

#### `feauts⇥` Authors
```js
${1:feed}.authors${0}
```

#### `fecat⇥` Category
```js
${1:feed}.category${0}
```

#### `fecon⇥` Contributors
```js
${1:feed}.contributors${0}
```

#### `felog⇥` Logo
```js
${1:feed}.logo${0}
```

#### `feico⇥` Icon
```js
${1:feed}.icon${0}
```

#### `felin⇥` Links
```js
${1:feed}.links${0}
```

#### `fetit⇥` Title
```js
${1:feed}.title${0}
```

#### `ferig⇥` Rights
```js
${1:feed}.rights${0}
```

#### `feupd⇥` Updated
```js
${1:feed}.updated${0}
```

#### `fetox⇥` To XML
```js
${1:feed}.toXML();${0}
```

#### `fetos⇥` To String
```js
${1:feed}.toString();${0}
```

### Entry

#### `en⇥` Entry
```js
var ${1:entry} = new Entry();${0}
```

#### `enid⇥` Id
```js
${1:entry}.id${0}
```

#### `enaut⇥` Authors
```js
${1:entry}.authors${0}
```

#### `encat⇥` Categories
```js
${1:entry}.categories${0}
```

#### `encont⇥` Contributors
```js
${1:entry}.contributors${0}
```

#### `encon⇥` Content
```js
${1:entry}.content${0}
```

#### `enpub⇥` Published
```js
${1:entry}.published${0}
```

#### `enlin⇥` Links
```js
${1:entry}.links${0}
```

#### `entit⇥` Title
```js
${1:entry}.title${0}
```

#### `ensum⇥` Summary
```js
${1:entry}.summary${0}
```

#### `enrig⇥` Rights
```js
${1:entry}.rights${0}
```

#### `enupd⇥` Updated
```js
${1:entry}.updated${0}
```

#### `entox⇥` To XML
```js
${1:entry}.toXML();${0}
```

#### `entos⇥` To String
```js
${1:entry}.toString();${0}
```

### File

#### `fi⇥` File
```js
var ${1:file} = new File(${2:path});${0}
```

#### `fiope⇥` Open
```js
${1:file}.open("${2:r | r+ | w | w+ | a | a+}");${0}
```

#### `fiwri⇥` Write
```js
${1:file}.write(${2:object});${0}
```

#### `firea⇥` Read
```js
${1:file}.read(${2:num});${0}
```

#### `fistr⇥` Stream
```js
${1:file}.getStream();${0}
```

#### `fireaa⇥` Read All
```js
${1:file}.readAll();${0}
```

#### `ficlo⇥` Close
```js
${1:file}.close();${0}
```

#### `fimov⇥` Move
```js
${1:file}.move(${2:targetFileName});${0}
```

#### `fisav⇥` Save As
```js
${1:file}.saveAs(${2:targetLocation});${0}
```

#### `fidel⇥` Delete
```js
${1:file}.del();${0}
```

#### `filen⇥` Length
```js
${1:file}.getLength();${0}
```

#### `filas⇥` Last Modified
```js
${1:file}.getLastModified();${0}
```

#### `finam⇥` Name
```js
${1:file}.getName();${0}
```

#### `fiexi⇥` Exists?
```js
${1:file}.isExists();${0}
```

#### `fidir⇥` Is Directory?
```js
${1:file}.isDirectory();${0}
```

#### `fimkd⇥` Make Dir
```js
${1:file}.mkdir("${2:path}");${0}
```

#### `fipat⇥` Path
```js
${1:file}.getPath();${0}
```

### Database

#### `da⇥` Database
```js
var ${1:db} = new Database(${2:connectionUrl}, ${3:username}, ${4:password}${5:, [config]});${0}
```

#### `dacon⇥` Config DB
```js
var config = {
  defaultAutoCommit: ${1:boolean},
  defaultReadOnly: ${2:boolean},
  defaultTransactionIsolation: ${3:"String"},
  defaultCatalog: ${4:"String"},
  maxActive: ${5:number},
  maxIdle: ${6:number},
  minIdle: ${7:number},
  initialSize: ${8:number},
  maxWait: ${9:number},
  testOnBorrow: ${10:boolean},
  testOnReturn: ${11:boolean},
  testWhileIdle: ${12:boolean},
  validationQuery: ${13:"String"},
  accessToUnderlyingConnectionAllowed: ${14:boolean},
  logAbandoned: ${15:boolean},
  connectionProperties: ${16:"String"},
  initSQL: ${17:"String"},
  validationInterval: ${18:number},
  maxAge: ${19:number},
  suspectTimeout: ${20:number}
};${0}
```

#### `daque⇥` Query
```js
${1:db}.query(${2:query}, function(results) {
  ${0}
});
```

#### `daquer⇥` Query/Result
```js
var ${1:result} = ${2:db}.query(${3:query});${0}
```

#### `dacom⇥` Commit
```js
${1:db}.query(${2:query});${0}
```

#### `darol⇥` Rollback
```js
${1:db}.rollback();${0}
```

#### `daclo⇥` Close
```js
${1:db}.close();${0}
```

### MetadataStore

#### `me⇥` MetadataStore
```js
var ${1:dataStore} = new MetadataStore(${2:username}, ${3:password});${0}
```

#### `meres⇥` Resource Exists?
```js
${1:dataStore}.resourceExists(${2:path});${0}
```

#### `meget⇥` Get
```js
${1:dataStore}.get(${2:path}${3:, [start]}${4:, [pageSize]});${0}
```

#### `meput⇥` Put
```js
${1:dataStore}.put(${2:path}, ${3:resource});${0}
```

#### `merem⇥` Remove
```js
${1:dataStore}.remove(${2:path});${0}
```

#### `mecre⇥` Create Link
```js
${1:dataStore}.createLink(${2:path}, ${3:target});${0}
```

#### `menewr⇥` New Resource
```js
${1:dataStore}.newResource();${0}
```

#### `menewc⇥` New Collection
```js
${1:dataStore}.newCollection();${0}
```

### Collection

#### `coadd⇥` Add Property
```js
${1:collection}.addProperty("${2:name}", "${3:value}");${0}
```

#### `cogetp⇥` Get Property
```js
${1:collection}.getProperty(${2:name});${0}
```

#### `cogetpv⇥` Get Property Values
```js
${1:collection}.getPropertyValues(${2:name});${0}
```

#### `cogetps⇥` Get Properties
```js
${1:collection}.getProperties();${0}
```

#### `coedi⇥` Edit Property Value
```js
${1:collection}.editPropertyValue(${2:name}, ${3:value}, ${4:newValue});${0}
```

#### `coremv⇥` Remove Property Value
```js
${1:collection}.removePropertyValue(${2:name}, ${3:value});${0}
```

#### `corem⇥` Remove Property
```js
${1:collection}.removeProperty(${2:name});${0}
```

#### `coset⇥` Set Property
```js
${1:collection}.setProperty(${2:name}, ${3:value});${0}
```

#### `coaut⇥` author
```js
${1:collection}.author${0}
```

#### `colasu⇥` Last Updated User
```js
${1:collection}.lastUpdatedUser${0}
```

#### `colast⇥` Last Updated Time
```js
${1:collection}.lastUpdatedTime${0}
```

#### `cocre⇥` Created Time
```js
${1:collection}.createdTime${0}
```

#### `coid⇥` Id
```js
${1:collection}.id${0}
```

#### `copat⇥` Path
```js
${1:collection}.path${0}
```

#### `copar⇥` Parent Path
```js
${1:collection}.parentPath${0}
```

#### `coper⇥` Permanent Path
```js
${1:collection}.permanentPath${0}
```

#### `costa⇥` State
```js
${1:collection}.state${0}
```

#### `comed⇥` Media Type
```js
${1:collection}.mediaType${0}
```

#### `cocon⇥` Content
```js
${1:collection}.content${0}
```

#### `codes⇥` Description
```js
${1:collection}.description${0}
```

#### `cochi⇥` Get Children
```js
${1:collection}.getChildren${0}
```

### Data Resource

#### `dradd⇥` Add Property
```js
${1:resource}.addProperty("${2:name}", "${3:value}");${0}
```

#### `drgetp⇥` Get Property
```js
${1:resource}.getProperty(${2:name});${0}
```

#### `drgetpv⇥` Get Property Values
```js
${1:resource}.getPropertyValues(${2:name});${0}
```

#### `drgetps⇥` Get Properties
```js
${1:resource}.getProperties();${0}
```

#### `dredi⇥` Edit Property Value
```js
${1:resource}.editPropertyValue(${2:name}, ${3:value}, ${4:newValue});${0}
```

#### `drremv⇥` Remove Property Value
```js
${1:resource}.removePropertyValue(${2:name}, ${3:value});${0}
```

#### `drrem⇥` Remove Property
```js
${1:resource}.removeProperty(${2:name});${0}
```

#### `drset⇥` Set Property
```js
${1:resource}.setProperty(${2:name}, ${3:value});${0}
```

#### `draut⇥` author
```js
${1:resource}.author${0}
```

#### `drlasu⇥` Last Updated User
```js
${1:resource}.lastUpdatedUser${0}
```

#### `drlast⇥` Last Updated Time
```js
${1:resource}.lastUpdatedTime${0}
```

#### `drcre⇥` Created Time
```js
${1:resource}.createdTime${0}
```

#### `drid⇥` Id
```js
${1:resource}.id${0}
```

#### `drpat⇥` Path
```js
${1:resource}.path${0}
```

#### `drpar⇥` Parent Path
```js
${1:resource}.parentPath${0}
```

#### `drper⇥` Permanent Path
```js
${1:resource}.permanentPath${0}
```

#### `drsta⇥` State
```js
${1:resource}.state${0}
```

#### `drmed⇥` Media Type
```js
${1:resource}.mediaType${0}
```

#### `drcon⇥` Content
```js
${1:resource}.content${0}
```

#### `drdes⇥` Description
```js
${1:resource}.description${0}
```

### Dataformats

#### `pa⇥` Parse
```js
parse(${1:jsonString})${0}
```

#### `str⇥` Stringify
```js
stringify(${1:jsonObject})${0}
```

#### `xml⇥` XML
```js
var ${1:xml} = new XML(${2:xmlString});${0}
```

### Email

#### `em⇥` Email
```js
var ${1:email} = require('email');
var ${2:sender} = new email.Sender("${3:smtp}", "${4:port}", "${5:username}", "${6:password}"${7:, "tls"});${0}
```

#### `emfro⇥` From
```js
${1:sender}.from = ${0}
```

#### `emto⇥` To
```js
${1:sender}.to = ${0}
```

#### `emcc⇥` Cc
```js
${1:sender}.cc = ${0}
```

#### `embcc⇥` Bcc
```js
${1:sender}.bcc = ${0}
```

#### `emsub⇥` Subject
```js
${1:sender}.subject = ${0}
```

#### `emtex⇥` Text
```js
${1:sender}.text = ${0}
```

#### `emhtm⇥` Html
```js
${1:sender}.html = ${0}
```

#### `emadd⇥` Add Attachment
```js
${1:sender}.addAttachment(${2:file});${0}
```

#### `emsen⇥` Send
```js
${1:sender}.send();${0}
```

### WSRequest

#### `ws⇥` WSRequest
```js
var ${1:ws} = require('ws');

var ${2:wsRequest} = new ${1:ws}.WSRequest();
var ${3:options} = new Array();

${3:options}.useSOAP = 1.2;
${3:options}.useWSA = 1.0;
${3:options}.action = "urn:getreq";
var ${4:payload} = ${5:null};
var ${6:endpoint} = "${7:url}";
var ${8:result};

try {
  ${2:wsRequest}.open(${3:options}, ${6:endpoint}, ${9:false});
  ${2:wsRequest}.send(${4:payload});
  ${8:result} = ${2:wsRequest}.responseE4X;
} catch (e) {
  e.toString();
}${0}
```

#### `wsrex⇥` Response XML
```js
${1:wsRequest}.responseXML;${0}
```

#### `wsret⇥` Response Text
```js
${1:wsRequest}.responseText;${0}
```

#### `wsree⇥` Response E4X
```js
${1:wsRequest}.responseE4X;${0}
```

#### `wsrea⇥` Ready State
```js
${1:wsRequest}.readyState;${0}
```

#### `wserr⇥` Error
```js
${1:wsRequest}.error;${0}
```

#### `wsrex⇥` Response XML
```js
IGUAL: wsrex
${1:wsRequest}.responseXML;${0}
```

#### `wsonr⇥` On Ready State Change
```js
${1:wsRequest}.onreadystatechange = function() {
  if (${2:request}.readyState == 4) {
${0}
  }
};
```

#### `wsope⇥` Open
```js
${1:wsRequest}.open(${0});
```

#### `wsopenw⇥` Open WSDL
```js
${1:wsRequest}.openWSDL(${0});
```

#### `wssen⇥` Send
```js
${1:wsRequest}.send(${2:payload});${0}
```

### wsRequest

#### `st⇥` WSStub
```js
var ${1:ws} = require('ws');
var ${2:stub} = new ws.WSStub('${3:url}');${0}
```

#### `stser⇥` Services
```js
${1:stub}.services['${2:name}'];${0}
```

#### `stope⇥` Operations
```js
${1:stub}.services['${2:name}'].operations['${3:operation}'];${0}
```

#### `streq⇥` Request
```js
${1:stub}.request();${0}
```

### OAuthProvider

#### `oa⇥` OAuthProvider
```js
var ${1:oauth} = require('oauth');
var ${2:config} = {
  "oauth_version" : "${3:version}",
  "authorization_url" : "${4:url}",
  "access_token_url" : "${5:url}",
  "request_token_url" : "${6:url}",
  "api_key" : "${7:key}",
  "api_secret" : "${8:secret}"
}
var ${9:provider} = new oauth.OAuthProvider(${2:config});${0}
```

#### `oagetau⇥` Auth Url
```js
${1:provider}.getAuthorizationUrl();${0}
```

#### `oagetac⇥` Access Token
```js
${1:provider}.getAccessToken(${2:authCode});${0}
```

#### `oasen⇥` Send OAuth Request
```js
${1:provider}.sendOAuthRequest(${2:accessToken}, ${3:verb}${4:, [parameters]});${0}
```

#### `oagetb⇥` Body
```js
${1:provider}.getBody();${0}
```

### Process

#### `pro⇥` Process
```js
var ${1:process} = require('process');${0}
```

#### `prgete⇥` Environment Var
```js
${1:process}.getEnv("${2:name}");${0}
```

#### `prgetes⇥` All Environment Vars
```js
${1:process}.getEnvs();${0}
```

#### `prset⇥` Set Property
```js
${1:process}.setProperty(${2:key}, ${3:value});${0}
```

#### `prget⇥` Get Property
```js
${1:process}.getProperty(${2:key});${0}
```

#### `prgetp⇥` Get Properties
```js
${1:process}.getProperties();${0}
```

### i18n

#### `i1⇥` i18n
```js
var ${1:i18n} = require('i18n');
${1:i18n}.init(${2:request});${0}
```

#### `i1ini⇥` Init
```js
${1:i18n}.init(${2:request});${0}
```

#### `i1pat⇥` Set Path
```js
${1:i18n}.localeResourcesBasePath = ${0}
```

#### `i1loc⇥` Localize
```js
${1:i18n}.localize(${2:key}, ${3:fallback});${0}
```

### Carbon

#### `car⇥` Carbon
```js
var ${1:carbon} = require('carbon');${0}
```

### UserManager

#### `um⇥` User Manager
```js
var ${1:userManager} = new carbon.user.UserManager(${2:server}, ${3:tenantId});${0}
```

#### `umadd⇥` Add User
```js
${1:userManager}.addUser(${2:userName}, ${3:password}, ${4:roles}, ${5:claims}, ${6:profile});${0}
```

#### `umgetu⇥` Get User
```js
${1:userManager}.getUser(${2:userName});${0}
```

#### `umexi⇥` User Exists
```js
${1:userManager}.userExists(${2:userName});${0}
```

#### `umrem⇥` Remove User
```js
${1:userManager}.removeUser(${2:userName});${0}
```

#### `umlis⇥` List Users
```js
${1:userManager}.listUsers(${2:filter});${0}
```

#### `umsetcs⇥` Set Claims
```js
${1:userManager}.setClaims(${2:userName}, ${3:claims}, ${4:profile});${0}
```

#### `umgetcs⇥` Get Claims
```js
${1:userManager}.getClaims(${2:userName}, ${3:profile});${0}
```

#### `umgetc4⇥` Get Claims For Set
```js
${1:userManager}.getClaimsForSet(${2:userName}, ${3:claims}, ${4:profile});${0}
```

#### `umgetc⇥` Get Claim
```js
${1:userManager}.getClaim(${2:userName}, ${3:claim}, ${4:profile});${0}
```

#### `umaddr⇥` Add Role
```js
${1:userManager}.addRole(${2:role}, ${3:users}, ${4:permissions});${0}
```

#### `umall⇥` All Roles
```js
${1:userManager}.allRoles();${0}
```

#### `umrol⇥` Role Exists?
```js
${1:userManager}.roleExists(${2:role});${0}
```

#### `umupd⇥` Update Role
```js
${1:userManager}.updateRole(${2:previousRoleName}, ${3:newRoleName});${0}
```

#### `umaut⇥` Authorize Role
```js
${1:userManager}.authorizeRole(${2:role}, ${3:permission}, ${4:action});${0}
```

#### `umisa⇥` Is Authorized?
```js
${1:userManager}.isAuthorized(${2:role}, ${3:permission}, ${4:action});${0}
```

#### `umden⇥` Deny Role
```js
${1:userManager}.denyRole(${2:role}, ${3:permission}, ${4:action});${0}
```

#### `umupdr⇥` Upd Role List Of User
```js
${1:userManager}.updateRoleListOfUser(${2:username}, ${3:deletedRoles}, ${4:newRoles});${0}
```

#### `umupdu⇥` Upd User List Of Role
```js
${1:userManager}.updateUserListOfRole(${2:rolename}, ${3:deletedUsers}, ${4:newUsers});${0}
```

### User

#### `us⇥` User
```js
var ${1:user} = new carbon.user.User(${2:userManager}, ${3:userName});${0}
```

#### `ussetcs⇥` Set Claims
```js
${1:user}.setClaims(${2:claims}, ${3:profile});${0}
```

#### `usgetcs⇥` Get Claims
```js
${1:user}.getClaims(${2:profile});${0}
```

#### `usgetc4⇥` Get Claims For Set
```js
${1:user}.getClaimsForSet(${2:claims}, ${3:profile});${0}
```

#### `usaddr⇥` Add Roles
```js
${1:user}.addRoles(${2:roles});${0}
```

#### `usrem⇥` Remove Roles
```js
${1:user}.removeRoles(${2:roles});${0}
```

#### `usgetr⇥` Get Roles
```js
${1:user}.getRoles();${0}
```

#### `ushas⇥` Has Roles?
```js
${1:user}.hasRoles(${2:roles});${0}
```

#### `usupd⇥` Update Roles
```js
${1:user}.updateRoles(${2:remove}, ${3:add});${0}
```

#### `usisa⇥` Is Authorized?
```js
${1:user}.isAuthorized(${2:permission}, ${3:action});${0}
```

### Registry

#### `reg⇥` Registry
```js
var ${1:registry} = new carbon.registry.Registry(${2:server}, ${3:options});${0}
```

#### `reopt⇥` Options
```js
var ${1:options} = {
  username : '${2:username}',
  domain : '${3:domain}',
  tenantId : ${$:tenant}
};${0}
```

#### `reput⇥` Put
```js
${1:registry}.put(${2:path}, ${3:resource});${0}
```

#### `reres⇥` Resource
```js
var ${1:resource} = {
  content : '${2:content}',
  mediaType : '${3:text/plain}',
  description : '${4:description}',
  uuid : '${5:uuid}',
  properties : {${0}}
};
```

#### `reget⇥` Get
```js
${1:registry}.get(${2:path});${0}
```

#### `remov⇥` Remove
```js
${1:registry}.move(${2:src}, ${3:dest});${0}
```

#### `recop⇥` Copy
```js
${1:registry}.copy(${2:src}, ${3:dest});${0}
```

#### `renam⇥` Rename
```js
${1:registry}.rename(${2:path}, ${3:newName});${0}
```

#### `rerem⇥` Remove
```js
${1:registry}.remove(${2:path});${0}
```

#### `reexi⇥` Exists?
```js
${1:registry}.exists(${2:path});${0}
```

#### `retag⇥` Tag
```js
${1:registry}.tag(${2:path}, ${3:tags});${0}
```

#### `retags⇥` Tags
```js
${1:registry}.tags(${2:path});${0}
```

#### `reunt⇥` Untag
```js
${1:registry}.untag(${2:path}, ${3:tags});${0}
```

#### `rerat⇥` Rate
```js
${1:registry}.rate(${2:path}, ${3:rate});${0}
```

#### `readdp⇥` Add Property
```js
${1:registry}.addProperty(${2:path}, ${3:propName}, ${4:value});${0}
```

#### `repro⇥` Properties
```js
${1:registry}.properties(${2:path});${0}
```

#### `rerati⇥` Rating
```js
${1:registry}.rating(${2:path}, ${3:user});${0}
```

#### `reunr⇥` Unrate
```js
${1:registry}.unrate(${2:path);${0}
```

#### `recom⇥` Comment
```js
${1:registry}.comment(${2:path}, ${3:comment});${0}
```

#### `recoms⇥` Comments
```js
${1:registry}.comments(${2:path});${0}
```

#### `recomc⇥` Comment Count
```js
${1:registry}.commentCount(${2:path});${0}
```

#### `reunc⇥` Uncomment
```js
${1:registry}.uncomment(${2:path});${0}
```

#### `rever⇥` Version
```js
${1:registry}.version(${2:path});${0}
```

#### `revers⇥` Versions
```js
${1:registry}.versions(${2:path});${0}
```

#### `rerest⇥` Restore
```js
${1:registry}.restore(${2:path});${0}
```

#### `reunv⇥` Unversion
```js
${1:registry}.unversion(${2:path}, ${3:versionId});${0}
```

#### `relin⇥` link
```js
${1:registry}.link(${2:path}, ${3:target});${0}
```

#### `reque⇥` query
```js
${1:registry}.query(${2:path});${0}
```

### Server

#### `se⇥` Server
```js
var ${1:server} = new carbon.server.Server(${2:url});${0}
```

#### `seadd⇥` Address
```js
${1:carbon}.server.address('${2:http|https}');${0}
```

#### `seten⇥` Tenant Domain
```js
${1:carbon}.server.tenantDomain();${0}
```

#### `seteni⇥` Tenant Id
```js
${1:carbon}.server.tenantId();${0}
```

#### `setenu⇥` Tenant User
```js
${1:carbon}.server.tenantUser('${2:userName}');${0}
```

#### `sesan⇥` Sandbox
```js
${1:carbon}.server.sandbox(${2:options}, ${3:fn});${0}
```

#### `seaut⇥` Authenticate
```js
${1:server}.authenticate(${2:username}, ${3:password});${0}
```

### jaggery.conf

#### `cfdis⇥` displayName
```js
"displayName" : "${1:displayName}"${0}
```

#### `cfwel⇥` welcomeFiles
```js
"welcomeFiles" : ["${1:files}"]${0}
```

#### `cflog⇥` logLevel
```js
"logLevel" : "${1:info|debug|error|warn|fatal}"${0}
```

#### `cferr⇥` errorPages
```js
"errorPages" : [
  {
    "errorCode" : "${1:errorCode}",
    "location" : "${2:location}"
  }
]${0}
```

#### `cfsecc⇥` securityConstraints
```js
    },
  }
}]$0
```

#### `cflogi⇥` loginConfig
```js
"loginConfig" : { "authMethod" : "${1: BASIC | CLIENT-CERT | FORM}" }${0}
```

#### `cfsecr⇥` securityRoles
```js
"securityRoles" : ["${1:roles}"]${0}
```

#### `cfurl⇥` urlMappings
```js
"urlMappings" : [
  {
    "url" : "${1:url}",
    "path" : "${2:path}"
  }
]${0}
```

#### `cfdist⇥` distributable
```js
"distributable" : ${1:true}${0}
```

#### `cfini⇥` initScripts
```js
"initScripts" : ["${1:scripts}"]${0}
```

#### `cfdes⇥` destroyScripts
```js
"destroyScripts" : ["${1:scripts}"]${0}
```

# License

The MIT License (MIT)

Copyright (c) 2015, Thiago Bonfante

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
