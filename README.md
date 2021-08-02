


<img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/hugo-logo-wide.svg?sanitize=true" alt="Hugo" width="200"/>  | + |  <img src="https://upload.wikimedia.org/wikipedia/commons/a/a8/Microsoft_Azure_Logo.svg" alt="Azure" width="200"/>

**Use this stack** to spin up a Static blogging website in seconds. 

## **Why** should you use this stack?

This stack offers to create a static website using Hugo and deploy it to an Azure Static Web site. Static website do not have a data store associated to it. But there are some core functional pieces it needs, which the stack offers. 
This stack leverages Github workflows to setup an end to end Build/Deploy CI/CD setup for you. It does so by creating a default action workflow and even runs it at the time of setting the stack. Just like any other stack, It is a guided experience and you dont have to write a single line of code to get started. 

## **What** does it contain?

### Hugo

Hugo is a static HTML and CSS website generator written in [Go][].
It is optimized for speed, ease of use, and configurability.
Hugo takes a directory with content and templates and renders them into a full HTML website.

[Website](https://gohugo.io)

### Azure 

This stack uses [Static website hosting in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website) to host the deployed website. 

### Search

This stack builds a Search App and the Search Index, which is a [Blazor WebAssembly application](https://docs.microsoft.com/en-gb/aspnet/core/blazor/?view=aspnetcore-3.0)  and console application.

### Updating Azure CDN

With this stack, latest website updates are uploaded to a Azure CDN. With this your website renders even faster !!

## **How** is this stack built?

Here are the logical steps when the stack is run.
1. Build a Hugo binary using minification
2. Publish the website output and Blog Jsons
3. Build and publish search app
4. Build and publish search index
5. Download all the artifacts and deploy to Azure static website
6. Update web assembly
7. Update Azure CDN

