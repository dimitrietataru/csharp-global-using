# C# Global Using templates

## About Global Using directives
* [Microsoft docs - What's new](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#global-using-directives)
* [Microsoft docs - Specifications](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/globalusingdirective)
* [C# Corner](https://www.c-sharpcorner.com/article/global-using-directive-in-c-sharp-102)
* [Exploring C# 10: Global Using declarations - Dave Brock](https://www.daveabrock.com/2021/10/21/csharp-10-global-usings)
* [Every feature added in C# 10 - Nick Chapsas](https://youtu.be/Vft4QDUpyWY?t=15)

## Implicit Usings

#### Configuration
``` xml
<PropertyGroup>
  <ImplicitUsings>enable</ImplicitUsings>
</PropertyGroup>
```

#### Auto-generated code at _/obj/Debug/net6.0/GlobalUsings.g.cs_
``` csharp
global using global::Microsoft.AspNetCore.Builder;
global using global::Microsoft.AspNetCore.Hosting;
global using global::Microsoft.AspNetCore.Http;
global using global::Microsoft.AspNetCore.Routing;
global using global::Microsoft.Extensions.Configuration;
global using global::Microsoft.Extensions.DependencyInjection;
global using global::Microsoft.Extensions.Hosting;
global using global::Microsoft.Extensions.Logging;
global using global::System;
global using global::System.Collections.Generic;
global using global::System.IO;
global using global::System.Linq;
global using global::System.Net.Http;
global using global::System.Net.Http.Json;
global using global::System.Threading;
global using global::System.Threading.Tasks;
```

---

#### Configuration
``` xml
<PropertyGroup>
  <ImplicitUsings>disable</ImplicitUsings>
</PropertyGroup>

<ItemGroup>
  <Using Include="System"/>
</ItemGroup>
```

#### Auto-generated code at _/obj/Debug/net6.0/GlobalUsings.g.cs_
``` csharp
global using global::System;
```

## Templates

``` csharp
#pragma warning disable IDE0005 // Using directive is unnecessary
```

#### Common _System.*_ namespaces
``` csharp
global using System;
global using System.Collections;
global using System.Collections.Concurrent;
global using System.Collections.Generic;
global using System.Collections.Immutable;
global using System.ComponentModel.DataAnnotations;
global using System.ComponentModel.DataAnnotations.Schema;
global using System.Diagnostics;
global using System.Globalization;
global using System.IO;
global using System.Linq;
global using System.Net;
global using System.Net.Http;
global using System.Net.Http.Json;
global using System.Net.Security;
global using System.Reflection;
global using System.Security;
global using System.Security.Authentication;
global using System.Security.Cryptography;
global using System.Security.Cryptography.X509Certificates;
global using System.Text;
global using System.Text.Encodings.Web;
global using System.Text.Json;
global using System.Text.Json.Serialization;
global using System.Text.RegularExpressions;
global using System.Threading;
global using System.Threading.Tasks;
global using System.Timers;
global using System.Web;
```

<details>
  <summary> All System namespaces </summary>

``` csharp
global using System;

global using System.Buffers;
global using System.Buffers.Binary;
global using System.Buffers.Text;

global using System.CodeDom;
global using System.CodeDom.Compiler;

global using System.Collections;
global using System.Collections.Concurrent;
global using System.Collections.Generic;
global using System.Collections.Immutable;
global using System.Collections.ObjectModel;
global using System.Collections.Specialized;

global using System.ComponentModel;
global using System.ComponentModel.DataAnnotations;
global using System.ComponentModel.DataAnnotations.Schema;
global using System.ComponentModel.Design;
global using System.ComponentModel.Design.Serialization;

global using System.Configuration;
global using System.Configuration.Assemblies;

global using System.Data;
global using System.Data.Common;
global using System.Data.SqlTypes;

global using System.Diagnostics;
global using System.Diagnostics.CodeAnalysis;
global using System.Diagnostics.Contracts;
global using System.Diagnostics.Eventing;
global using System.Diagnostics.Metrics;
global using System.Diagnostics.SymbolStore;
global using System.Diagnostics.Tracing;

global using System.Drawing;

global using System.Dynamic;

global using System.Formats;
global using System.Formats.Asn1;

global using System.Globalization;

global using System.IO;

global using System.Linq;
global using System.Linq.Expressions;

global using System.Net;
global using System.Net.Cache;
global using System.Net.Http;
global using System.Net.Http.Headers;
global using System.Net.Http.Json;
global using System.Net.Mail;
global using System.Net.Mime;
global using System.Net.NetworkInformation;
global using System.Net.Security;
global using System.Net.Sockets;
global using System.Net.WebSockets;

global using System.Numerics;

global using System.Reflection;
global using System.Reflection.Emit;
global using System.Reflection.Metadata;
global using System.Reflection.Metadata.Ecma335;
global using System.Reflection.PortableExecutable;

global using System.Resources;

global using System.Runtime;
global using System.Runtime.CompilerServices;
global using System.Runtime.ConstrainedExecution;
global using System.Runtime.ExceptionServices;
global using System.Runtime.InteropServices;
global using System.Runtime.InteropServices.ComTypes;
global using System.Runtime.InteropServices.ObjectiveC;
global using System.Runtime.Intrinsics;
global using System.Runtime.Intrinsics.Arm;
global using System.Runtime.Intrinsics.X86;
global using System.Runtime.Loader;
global using System.Runtime.Remoting;
global using System.Runtime.Serialization;
global using System.Runtime.Serialization.Formatters;
global using System.Runtime.Serialization.Formatters.Binary;
global using System.Runtime.Serialization.Json;
global using System.Runtime.Versioning;

global using System.Security;
global using System.Security.AccessControl;
global using System.Security.Authentication;
global using System.Security.Authentication.ExtendedProtection;
global using System.Security.Claims;
global using System.Security.Cryptography;
global using System.Security.Cryptography.X509Certificates;
global using System.Security.Cryptography.Xml;
global using System.Security.Permissions;
global using System.Security.Policy;
global using System.Security.Principal;

global using System.Security;
global using System.Security.AccessControl;
global using System.Security.Authentication;
global using System.Security.Authentication.ExtendedProtection;
global using System.Security.Claims;
global using System.Security.Cryptography;
global using System.Security.Cryptography.X509Certificates;
global using System.Security.Cryptography.Xml;
global using System.Security.Permissions;
global using System.Security.Policy;
global using System.Security.Principal;

global using System.Text;
global using System.Text.Encodings;
global using System.Text.Encodings.Web;
global using System.Text.Json;
global using System.Text.Json.Nodes;
global using System.Text.Json.Serialization;
global using System.Text.Json.Serialization.Metadata;
global using System.Text.RegularExpressions;
global using System.Text.Unicode;

global using System.Threading;
global using System.Threading.Channels;
global using System.Threading.Tasks;
global using System.Threading.Tasks.Dataflow;
global using System.Threading.Tasks.Sources;

global using System.Timers;

global using System.Transactions;

global using System.Web;

global using System.Windows;
global using System.Windows.Input;
global using System.Windows.Markup;

global using System.Xml;
global using System.Xml.Linq;
global using System.Xml.Resolvers;
global using System.Xml.Schema;
global using System.Xml.Serialization;
global using System.Xml.XPath;
global using System.Xml.Xsl;
```

</details>

---

#### Common _Microsoft.AspNetCore.*_ namespaces
``` csharp
global using Microsoft.AspNetCore;
global using Microsoft.AspNetCore.Authentication;
global using Microsoft.AspNetCore.Authorization;
global using Microsoft.AspNetCore.Builder;
global using Microsoft.AspNetCore.Cors.Infrastructure;
global using Microsoft.AspNetCore.Diagnostics.HealthChecks;
global using Microsoft.AspNetCore.Hosting;
global using Microsoft.AspNetCore.Http;
global using Microsoft.AspNetCore.Identity;
global using Microsoft.AspNetCore.Localization;
global using Microsoft.AspNetCore.Mvc;
global using Microsoft.AspNetCore.Rewrite;
global using Microsoft.AspNetCore.Routing;
global using Microsoft.AspNetCore.SignalR;
```

<details>
  <summary> All Microsoft.AspNetCore namespaces </summary>

``` csharp
global using Microsoft.AspNetCore;

global using Microsoft.AspNetCore.Antiforgery;

global using Microsoft.AspNetCore.Authentication;
global using Microsoft.AspNetCore.Authentication.Cookies;
global using Microsoft.AspNetCore.Authentication.OAuth;
global using Microsoft.AspNetCore.Authentication.OAuth.Claims;

global using Microsoft.AspNetCore.Authorization;
global using Microsoft.AspNetCore.Authorization.Infrastructure;
global using Microsoft.AspNetCore.Authorization.Policy;

global using Microsoft.AspNetCore.Builder;
global using Microsoft.AspNetCore.Builder.Extensions;

global using Microsoft.AspNetCore.Components;
global using Microsoft.AspNetCore.Components.Authorization;
global using Microsoft.AspNetCore.Components.CompilerServices;
global using Microsoft.AspNetCore.Components.Forms;
global using Microsoft.AspNetCore.Components.Infrastructure;
global using Microsoft.AspNetCore.Components.Rendering;
global using Microsoft.AspNetCore.Components.RenderTree;
global using Microsoft.AspNetCore.Components.Routing;
global using Microsoft.AspNetCore.Components.Server;
global using Microsoft.AspNetCore.Components.Server.Circuits;
global using Microsoft.AspNetCore.Components.Server.ProtectedBrowserStorage;
global using Microsoft.AspNetCore.Components.Web;
global using Microsoft.AspNetCore.Components.Web.Infrastructure;
global using Microsoft.AspNetCore.Components.Web.Virtualization;

global using Microsoft.AspNetCore.Connections;
global using Microsoft.AspNetCore.Connections.Features;

global using Microsoft.AspNetCore.CookiePolicy;

global using Microsoft.AspNetCore.Cors;
global using Microsoft.AspNetCore.Cors.Infrastructure;

global using Microsoft.AspNetCore.Cryptography;
global using Microsoft.AspNetCore.Cryptography.KeyDerivation;

global using Microsoft.AspNetCore.DataProtection;
global using Microsoft.AspNetCore.DataProtection.AuthenticatedEncryption;
global using Microsoft.AspNetCore.DataProtection.AuthenticatedEncryption.ConfigurationModel;
global using Microsoft.AspNetCore.DataProtection.Infrastructure;
global using Microsoft.AspNetCore.DataProtection.Internal;
global using Microsoft.AspNetCore.DataProtection.KeyManagement;
global using Microsoft.AspNetCore.DataProtection.KeyManagement.Internal;
global using Microsoft.AspNetCore.DataProtection.Repositories;
global using Microsoft.AspNetCore.DataProtection.XmlEncryption;

global using Microsoft.AspNetCore.Diagnostics;
global using Microsoft.AspNetCore.Diagnostics.HealthChecks;

global using Microsoft.AspNetCore.HostFiltering;

global using Microsoft.AspNetCore.Hosting;
global using Microsoft.AspNetCore.Hosting.Builder;
global using Microsoft.AspNetCore.Hosting.Infrastructure;
global using Microsoft.AspNetCore.Hosting.Server;
global using Microsoft.AspNetCore.Hosting.Server.Abstractions;
global using Microsoft.AspNetCore.Hosting.Server.Features;
global using Microsoft.AspNetCore.Hosting.StaticWebAssets;

global using Microsoft.AspNetCore.Html;

global using Microsoft.AspNetCore.Http;

global using Microsoft.AspNetCore.HttpLogging;

global using Microsoft.AspNetCore.HttpOverrides;

global using Microsoft.AspNetCore.HttpsPolicy;

global using Microsoft.AspNetCore.Identity;

global using Microsoft.AspNetCore.Localization;
global using Microsoft.AspNetCore.Localization.Routing;

global using Microsoft.AspNetCore.Mvc;
global using Microsoft.AspNetCore.Mvc.Abstractions;
global using Microsoft.AspNetCore.Mvc.ActionConstraints;
global using Microsoft.AspNetCore.Mvc.ApiExplorer;
global using Microsoft.AspNetCore.Mvc.ApplicationModels;
global using Microsoft.AspNetCore.Mvc.ApplicationParts;
global using Microsoft.AspNetCore.Mvc.Authorization;
global using Microsoft.AspNetCore.Mvc.Controllers;
global using Microsoft.AspNetCore.Mvc.Core;
global using Microsoft.AspNetCore.Mvc.Core.Infrastructure;
global using Microsoft.AspNetCore.Mvc.Localization;
global using Microsoft.AspNetCore.Mvc.ModelBinding;
global using Microsoft.AspNetCore.Mvc.ModelBinding.Binders;
global using Microsoft.AspNetCore.Mvc.ModelBinding.Metadata;
global using Microsoft.AspNetCore.Mvc.ModelBinding.Validation;
global using Microsoft.AspNetCore.Mvc.Razor;
global using Microsoft.AspNetCore.Mvc.Razor.Compilation;
global using Microsoft.AspNetCore.Mvc.Razor.Infrastructure;
global using Microsoft.AspNetCore.Mvc.Razor.Internal;
global using Microsoft.AspNetCore.Mvc.Razor.TagHelpers;
global using Microsoft.AspNetCore.Mvc.RazorPages;
global using Microsoft.AspNetCore.Mvc.RazorPages.Infrastructure;
global using Microsoft.AspNetCore.Mvc.Rendering;
global using Microsoft.AspNetCore.Mvc.Routing;
global using Microsoft.AspNetCore.Mvc.TagHelpers;
global using Microsoft.AspNetCore.Mvc.TagHelpers.Cache;
global using Microsoft.AspNetCore.Mvc.ViewComponents;
global using Microsoft.AspNetCore.Mvc.ViewEngines;
global using Microsoft.AspNetCore.Mvc.ViewFeatures;
global using Microsoft.AspNetCore.Mvc.ViewFeatures.Buffers;
global using Microsoft.AspNetCore.Mvc.ViewFeatures.Infrastructure;

global using Microsoft.AspNetCore.Razor;
global using Microsoft.AspNetCore.Razor.Hosting;
global using Microsoft.AspNetCore.Razor.Runtime;
global using Microsoft.AspNetCore.Razor.Runtime.TagHelpers;
global using Microsoft.AspNetCore.Razor.TagHelpers;

global using Microsoft.AspNetCore.ResponseCaching;

global using Microsoft.AspNetCore.ResponseCompression;

global using Microsoft.AspNetCore.Rewrite;

global using Microsoft.AspNetCore.Routing;
global using Microsoft.AspNetCore.Routing.Constraints;
global using Microsoft.AspNetCore.Routing.Internal;
global using Microsoft.AspNetCore.Routing.Matching;
global using Microsoft.AspNetCore.Routing.Patterns;
global using Microsoft.AspNetCore.Routing.Template;
global using Microsoft.AspNetCore.Routing.Tree;

global using Microsoft.AspNetCore.Server;
global using Microsoft.AspNetCore.Server.HttpSys;
global using Microsoft.AspNetCore.Server.IIS;
global using Microsoft.AspNetCore.Server.IIS.Core;
global using Microsoft.AspNetCore.Server.IISIntegration;
global using Microsoft.AspNetCore.Server.Kestrel;
global using Microsoft.AspNetCore.Server.Kestrel.Core;
global using Microsoft.AspNetCore.Server.Kestrel.Core.Features;
global using Microsoft.AspNetCore.Server.Kestrel.Core.Internal;
global using Microsoft.AspNetCore.Server.Kestrel.Core.Internal.Http;
global using Microsoft.AspNetCore.Server.Kestrel.Https;
global using Microsoft.AspNetCore.Server.Kestrel.Transport;
global using Microsoft.AspNetCore.Server.Kestrel.Transport.Quic;
global using Microsoft.AspNetCore.Server.Kestrel.Transport.Sockets;

global using Microsoft.AspNetCore.Session;

global using Microsoft.AspNetCore.SignalR;
global using Microsoft.AspNetCore.SignalR.Protocol;

global using Microsoft.AspNetCore.StaticFiles;
global using Microsoft.AspNetCore.StaticFiles.Infrastructure;

global using Microsoft.AspNetCore.WebSockets;

global using Microsoft.AspNetCore.WebUtilities;
```

</details>

---

#### Common _Microsoft.Extensions.*_ namespaces
``` csharp
global using Microsoft.Extensions;
global using Microsoft.Extensions.Caching.Memory;
global using Microsoft.Extensions.Configuration;
global using Microsoft.Extensions.DependencyInjection;
global using Microsoft.Extensions.DependencyInjection.Extensions;
global using Microsoft.Extensions.Diagnostics.HealthChecks;
global using Microsoft.Extensions.Hosting;
global using Microsoft.Extensions.Http;
global using Microsoft.Extensions.Localization;
global using Microsoft.Extensions.Logging;
global using Microsoft.Extensions.Options;
global using Microsoft.Extensions.Primitives;
```

<details>
  <summary> All Microsoft.Extensions namespaces </summary>

``` csharp
global using Microsoft.Extensions;

global using Microsoft.Extensions.Caching;
global using Microsoft.Extensions.Caching.Distributed;
global using Microsoft.Extensions.Caching.Memory;

global using Microsoft.Extensions.Configuration;
global using Microsoft.Extensions.Configuration.CommandLine;
global using Microsoft.Extensions.Configuration.EnvironmentVariables;
global using Microsoft.Extensions.Configuration.Ini;
global using Microsoft.Extensions.Configuration.Json;
global using Microsoft.Extensions.Configuration.KeyPerFile;
global using Microsoft.Extensions.Configuration.Memory;
global using Microsoft.Extensions.Configuration.UserSecrets;
global using Microsoft.Extensions.Configuration.Xml;

global using Microsoft.Extensions.DependencyInjection;
global using Microsoft.Extensions.DependencyInjection.Extensions;

global using Microsoft.Extensions.Diagnostics;
global using Microsoft.Extensions.Diagnostics.HealthChecks;

global using Microsoft.Extensions.FileProviders;
global using Microsoft.Extensions.FileProviders.Composite;
global using Microsoft.Extensions.FileProviders.Embedded;
global using Microsoft.Extensions.FileProviders.Internal;
global using Microsoft.Extensions.FileProviders.Physical;

global using Microsoft.Extensions.FileSystemGlobbing;
global using Microsoft.Extensions.FileSystemGlobbing.Abstractions;
global using Microsoft.Extensions.FileSystemGlobbing.Internal;
global using Microsoft.Extensions.FileSystemGlobbing.Internal.PathSegments;
global using Microsoft.Extensions.FileSystemGlobbing.Internal.PatternContexts;
global using Microsoft.Extensions.FileSystemGlobbing.Internal.Patterns;

global using Microsoft.Extensions.Hosting;
global using Microsoft.Extensions.Hosting.Internal;

global using Microsoft.Extensions.Http;
global using Microsoft.Extensions.Http.Logging;

global using Microsoft.Extensions.Internal;

global using Microsoft.Extensions.Localization;

global using Microsoft.Extensions.Logging;
global using Microsoft.Extensions.Logging.Abstractions;
global using Microsoft.Extensions.Logging.Configuration;
global using Microsoft.Extensions.Logging.Console;
global using Microsoft.Extensions.Logging.Debug;
global using Microsoft.Extensions.Logging.EventLog;
global using Microsoft.Extensions.Logging.EventSource;
global using Microsoft.Extensions.Logging.TraceSource;

global using Microsoft.Extensions.ObjectPool;

global using Microsoft.Extensions.Options;

global using Microsoft.Extensions.Primitives;

global using Microsoft.Extensions.WebEncoders;
global using Microsoft.Extensions.WebEncoders.Testing;
```

</details>