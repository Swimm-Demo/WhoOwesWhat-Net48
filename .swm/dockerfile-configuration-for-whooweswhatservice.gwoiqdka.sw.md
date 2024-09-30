---
title: Dockerfile Configuration for WhoOwesWhat.Service
---
# Intro

This document explains how Docker is used in the WhoOwesWhat.Service project. It will go through the <SwmPath>[WhoOwesWhat.Service/Dockerfile](WhoOwesWhat.Service/Dockerfile)</SwmPath> configuration step by step.

<SwmSnippet path="/WhoOwesWhat.Service/Dockerfile" line="1">

---

# <SwmPath>[WhoOwesWhat.Service/Dockerfile](WhoOwesWhat.Service/Dockerfile)</SwmPath> configuration

The <SwmPath>[WhoOwesWhat.Service/Dockerfile](WhoOwesWhat.Service/Dockerfile)</SwmPath> begins with comments explaining that the base image may need to be changed depending on the host machine's operating system. This is crucial for ensuring compatibility across different environments.

```
#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Service/Dockerfile" line="4">

---

The base image used is <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="4:2:20" line-data="FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019">`mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019`</SwmToken>

which is a Microsoft-provided image for [ASP.NET](http://ASP.NET) applications running on .NET Framework <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="4:14:16" line-data="FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019">`4.8`</SwmToken>.

```
FROM mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Service/Dockerfile" line="5">

---

An <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="5:0:0" line-data="ARG source">`ARG`</SwmToken> instruction is used to define a variable named <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="5:2:2" line-data="ARG source">`source`</SwmToken>. This variable can be passed at build time to specify the source directory for the application files.

```
ARG source
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Service/Dockerfile" line="6">

---

The <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="6:0:0" line-data="WORKDIR /inetpub/wwwroot">`WORKDIR`</SwmToken> instruction sets the working directory inside the container to <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="6:2:5" line-data="WORKDIR /inetpub/wwwroot">`/inetpub/wwwroot`</SwmToken>, which is the default directory for IIS web applications.

```
WORKDIR /inetpub/wwwroot
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Service/Dockerfile" line="7">

---

The <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="7:0:0" line-data="COPY ${source:-obj/Docker/publish} .">`COPY`</SwmToken> instruction copies the application files from the source directory (defaulting to <SwmToken path="WhoOwesWhat.Service/Dockerfile" pos="7:6:10" line-data="COPY ${source:-obj/Docker/publish} .">`obj/Docker/publish`</SwmToken>) to the working directory inside the container.

```
COPY ${source:-obj/Docker/publish} .
```

---

</SwmSnippet>

&nbsp;

*This is an auto-generated document by Swimm AI 🌊 and has not yet been verified by a human*

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48"><sup>Powered by [Swimm](https://app.swimm.io/)</sup></SwmMeta>
