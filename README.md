<img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/hugo-logo-wide.svg?sanitize=true" alt="Hugo" width="200"/>  | + |  <img src="https://upload.wikimedia.org/wikipedia/commons/a/a8/Microsoft_Azure_Logo.svg" alt="Azure" width="200"/>

**Use this stack** to spin up a Static blogging website in seconds. 

## **Why** should you use this stack?

This stack creates a static website using Hugo and deploy it to Azure Static Web site. Static website do not have a data store associated to it. But there are some core functional pieces it needs, such as search, CDN updates etc. This stack offers them. 

This stack leverages Github workflows to setup an end to end Build/Deploy CI/CD setup for you. It does so by creating a default action workflow and even runs it at the time of setting the stack. Just like any other stack, It is a guided experience to use this stack and you dont have to write a single line of code to get started. 

## **What** does it use to build the website?

### Hugo

[Hugo](https://gohugo.io) is a static HTML and CSS website generator written in [Go](https://golang.org/).
It is optimized for speed, ease of use, and configurability.
Hugo takes a directory with content and templates and renders them into a full HTML website.

### Azure 

This stack uses [Static website hosting in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website) to host the deployed website. 

### Blazor Search

This stack builds a Search App and the Search Index, which is a [Blazor WebAssembly application](https://docs.microsoft.com/en-gb/aspnet/core/blazor/?view=aspnetcore-3.0)  and console application.

### Azure CDN

With this stack, latest website updates are uploaded to a Azure CDN. With this your website renders even faster !!

## How to use this stack?
Follow these steps
1. Click on `Use this stack`. A Wizard UI starts to collect some inputs from you.
2. Provide your repository name. 
3. Provide the variables required by your stack. Here is the list of variables
  * HUGO Version - Version of HUGO, This is optional. Defaults to the latest Hugo Version
  * About Yourself - Provide a good description about yourself. This detail will be setup in the Home page of your blog.
4. App will redirect you to install Azure AD App. Please follow the instructions specified in [Azure App](app) for installation steps.
5. Click on `Initialize` button and once all the steps are completed, the website is waiting for you !!. You can find the website URL in a file called `output.txt` in your repository

## Further Reading

Here are the logical steps when the stack is run.
1. Build a Hugo binary using minification
2. Publish the website output and Blog Jsons
3. Build and publish search app
4. Build and publish search index
5. Download all the artifacts and deploy to Azure static website
6. Update web assembly
7. Update Azure CDN

